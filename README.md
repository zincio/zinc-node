# Zinc API TypeScript Library

[![fern shield](https://img.shields.io/badge/%F0%9F%8C%BF-Built%20with%20Fern-brightgreen)](https://buildwithfern.com?utm_source=github&utm_medium=github&utm_campaign=readme&utm_source=https%3A%2F%2Fgithub.com%2Fzincio%2Fzinc-node)
[![npm shield](https://img.shields.io/npm/v/zinc)](https://www.npmjs.com/package/zinc)

**`zinc`** is the official SDK for the [Zinc API](https://www.zinc.com/docs) —
search, buy, track, and return products from major online retailers
(Amazon, Walmart, and more) through a single, type-safe API.

Keywords: e-commerce API, place an order, buy products programmatically,
Amazon ordering API, checkout automation, order tracking, returns,
product search, AI agent commerce, autonomous purchasing, MPP / HTTP 402.

Every method is fully typed. Instantiate `ZincClient` once and call resource
methods on it — placing an order, searching for a product, and tracking a
shipment are each a single call. (Method names follow each language's
convention: `createOrder` in TypeScript, `create_order` in Python.)


## Table of Contents

- [Installation](#installation)
- [Reference](#reference)
- [Authentication](#authentication)
- [Test Mode](#test-mode)
- [Errors](#errors)
- [Faq](#faq)
- [Usage](#usage)
- [Environments](#environments)
- [Request and Response Types](#request-and-response-types)
- [Exception Handling](#exception-handling)
- [Advanced](#advanced)
  - [Subpackage Exports](#subpackage-exports)
  - [Additional Headers](#additional-headers)
  - [Additional Query String Parameters](#additional-query-string-parameters)
  - [Retries](#retries)
  - [Timeouts](#timeouts)
  - [Aborting Requests](#aborting-requests)
  - [Access Raw Response Data](#access-raw-response-data)
  - [Logging](#logging)
  - [Custom Fetch](#custom-fetch)
  - [Runtime Compatibility](#runtime-compatibility)
- [Contributing](#contributing)

## Installation

```shell
npm install zinc
```


## Reference

A full reference for this library is available [here](https://github.com/zincio/zinc-node/blob/HEAD/./reference.md).

## Authentication

Most endpoints require a Zinc API key (prefixed `zn_`), sent as the
`Authorization` header. Pass it verbatim, **including the `Bearer` prefix**:

```ts
import { ZincClient } from "zinc";

const zinc = new ZincClient({
  apiKey: `Bearer ${process.env.ZINC_API_KEY}`, // "zn_..."
  // baseUrl defaults to https://api.zinc.com
});
```

The `zinc.agent.*` endpoints need **no API key** — they are paid
per-call via MPP (HTTP 402), so an agent can order without an account.


## Test mode

Use a **test API key** (`zn_test_...`) to hit the sandbox — same
client, same base URL; the key prefix routes you to test data:

```ts
const zinc = new ZincClient({ apiKey: `Bearer ${process.env.ZINC_TEST_KEY}` });
```

`zinc.orders.listTestProducts()` returns product URLs that trigger
specific sandbox scenarios.


## Errors

Failed requests throw a typed `ZincError` exposing `.statusCode` and
`.body`. Notable subtypes: `PaymentRequiredError` (HTTP 402 — returned
by `zinc.agent.*` when payment is required) and `UnprocessableEntityError`
(validation).


## FAQ

**Which version should I use?** The package version mirrors the Zinc
API version (CalVer, e.g. `2026.7.17` = API `2026-07-17`). Pin an exact
version or take `latest`.

**Do I need an account to place orders as an agent?** No. `zinc.agent.createMppOrder`
settles payment via MPP (HTTP 402) — no API key required.

**How is `max_price` interpreted?** In cents. It's a ceiling; the order
is not finalized above it.

**Where are the full API docs?** https://www.zinc.com/docs


## Usage

Instantiate and use the client with the following:

```typescript
import { ZincClient } from "zinc";

const client = new ZincClient({ apiKey: "YOUR_API_KEY" });
await client.orders.createOrder({
    body: {
        products: [{
                url: "https://www.amazon.com/dp/B07JGBW826"
            }],
        shipping_address: {
            first_name: "first_name",
            last_name: "last_name",
            address_line1: "address_line1",
            city: "city",
            postal_code: "postal_code",
            phone_number: "phone_number"
        },
        max_price: 1
    }
});
```

## Environments

This SDK allows you to configure different environments for API requests.

```typescript
import { ZincClient, ZincEnvironment } from "zinc";

const client = new ZincClient({
    environment: ZincEnvironment.Production,
});
```

## Request and Response Types

The SDK exports all request and response types as TypeScript interfaces. Simply import them with the
following namespace:

```typescript
import { Zinc } from "zinc";

const request: Zinc.ValidateBulkUploadOrdersBulkValidatePostRequest = {
    ...
};
```

## Exception Handling

When the API returns a non-success status code (4xx or 5xx response), a subclass of the following error
will be thrown.

```typescript
import { ZincError } from "zinc";

try {
    await client.orders.createOrder(...);
} catch (err) {
    if (err instanceof ZincError) {
        console.log(err.statusCode);
        console.log(err.message);
        console.log(err.body);
        console.log(err.rawResponse);
    }
}
```

## Advanced

### Subpackage Exports

This SDK supports direct imports of subpackage clients, which allows JavaScript bundlers to tree-shake and include only the imported subpackage code. This results in much smaller bundle sizes.

```typescript
import { OrdersClient } from 'zinc/orders';

const client = new OrdersClient({...});
```

### Additional Headers

If you would like to send additional headers as part of the request, use the `headers` request option.

```typescript
import { ZincClient } from "zinc";

const client = new ZincClient({
    ...
    headers: {
        'X-Custom-Header': 'custom value'
    }
});

const response = await client.orders.createOrder(..., {
    headers: {
        'X-Custom-Header': 'custom value'
    }
});
```

### Additional Query String Parameters

If you would like to send additional query string parameters as part of the request, use the `queryParams` request option.

```typescript
const response = await client.orders.createOrder(..., {
    queryParams: {
        'customQueryParamKey': 'custom query param value'
    }
});
```

### Retries

The SDK is instrumented with automatic retries with exponential backoff. A request will be retried as long
as the request is deemed retryable and the number of retry attempts has not grown larger than the configured
retry limit (default: 2).

Which status codes are retried depends on the `retryStatusCodes` generator configuration:

**`legacy`** (current default): retries on
- [408](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/408) (Timeout)
- [429](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/429) (Too Many Requests)
- [5XX](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status#server_error_responses) (All server errors, including 500)

**`recommended`**: retries on
- [408](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/408) (Timeout)
- [429](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/429) (Too Many Requests)
- [502](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/502) (Bad Gateway)
- [503](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/503) (Service Unavailable)
- [504](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/504) (Gateway Timeout)

Use the `maxRetries` request option to configure this behavior.

```typescript
const response = await client.orders.createOrder(..., {
    maxRetries: 0 // override maxRetries at the request level
});
```

### Timeouts

The SDK defaults to a 60 second timeout. Use the `timeoutInSeconds` option to configure this behavior.

```typescript
const response = await client.orders.createOrder(..., {
    timeoutInSeconds: 30 // override timeout to 30s
});
```

### Aborting Requests

The SDK allows users to abort requests at any point by passing in an abort signal.

```typescript
const controller = new AbortController();
const response = await client.orders.createOrder(..., {
    abortSignal: controller.signal
});
controller.abort(); // aborts the request
```

### Access Raw Response Data

The SDK provides access to raw response data, including headers, through the `.withRawResponse()` method.
The `.withRawResponse()` method returns a promise that results to an object with a `data` and a `rawResponse` property.

```typescript
const { data, rawResponse } = await client.orders.createOrder(...).withRawResponse();

console.log(data);
console.log(rawResponse.headers['X-My-Header']);
```

### Logging

The SDK supports logging. You can configure the logger by passing in a `logging` object to the client options.

```typescript
import { ZincClient, logging } from "zinc";

const client = new ZincClient({
    ...
    logging: {
        level: logging.LogLevel.Debug, // defaults to logging.LogLevel.Info
        logger: new logging.ConsoleLogger(), // defaults to ConsoleLogger
        silent: false, // defaults to true, set to false to enable logging
    }
});
```
The `logging` object can have the following properties:
- `level`: The log level to use. Defaults to `logging.LogLevel.Info`.
- `logger`: The logger to use. Defaults to a `logging.ConsoleLogger`.
- `silent`: Whether to silence the logger. Defaults to `true`.

The `level` property can be one of the following values:
- `logging.LogLevel.Debug`
- `logging.LogLevel.Info`
- `logging.LogLevel.Warn`
- `logging.LogLevel.Error`

To provide a custom logger, you can pass in an object that implements the `logging.ILogger` interface.

<details>
<summary>Custom logger examples</summary>

Here's an example using the popular `winston` logging library.
```ts
import winston from 'winston';

const winstonLogger = winston.createLogger({...});

const logger: logging.ILogger = {
    debug: (msg, ...args) => winstonLogger.debug(msg, ...args),
    info: (msg, ...args) => winstonLogger.info(msg, ...args),
    warn: (msg, ...args) => winstonLogger.warn(msg, ...args),
    error: (msg, ...args) => winstonLogger.error(msg, ...args),
};
```

Here's an example using the popular `pino` logging library.

```ts
import pino from 'pino';

const pinoLogger = pino({...});

const logger: logging.ILogger = {
  debug: (msg, ...args) => pinoLogger.debug(args, msg),
  info: (msg, ...args) => pinoLogger.info(args, msg),
  warn: (msg, ...args) => pinoLogger.warn(args, msg),
  error: (msg, ...args) => pinoLogger.error(args, msg),
};
```
</details>


### Custom Fetch

The SDK provides a low-level `fetch` method for making custom HTTP requests while still
benefiting from SDK-level configuration like authentication, retries, timeouts, and logging.
This is useful for calling API endpoints not yet supported in the SDK.

```typescript
const response = await client.fetch("/v1/custom/endpoint", {
    method: "GET",
}, {
    timeoutInSeconds: 30,
    maxRetries: 3,
    headers: {
        "X-Custom-Header": "custom-value",
    },
});

const data = await response.json();
```

### Runtime Compatibility


The SDK works in the following runtimes:



- Node.js 18+
- Vercel
- Cloudflare Workers
- Deno v1.25+
- Bun 1.0+
- React Native


## Contributing

While we value open-source contributions to this SDK, this library is generated programmatically.
Additions made directly to this library would have to be moved over to our generation code,
otherwise they would be overwritten upon the next generated release. Feel free to open a PR as
a proof of concept, but know that we will not be able to merge it as-is. We suggest opening
an issue first to discuss with us!

On the other hand, contributions to the README are always very welcome!
