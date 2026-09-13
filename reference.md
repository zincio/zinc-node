# Reference
## Orders
<details><summary><code>client.orders.<a href="/src/api/resources/orders/client/Client.ts">validateBulkUpload</a>({ ...params }) -> Zinc.BulkValidateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Dry-run a CSV upload: validate every row and report estimated spend.

No orders are placed. Use this to show the confirmation preview before
calling POST /orders/bulk.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.orders.validateBulkUpload({
    body: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.ValidateBulkUploadOrdersBulkValidatePostRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.orders.<a href="/src/api/resources/orders/client/Client.ts">listBulkUploads</a>({ ...params }) -> Zinc.BulkBatchListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List the current user's bulk-upload batches, newest first.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.orders.listBulkUploads();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.ListBulkUploadsOrdersBulkGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.orders.<a href="/src/api/resources/orders/client/Client.ts">createBulkUpload</a>({ ...params }) -> Zinc.BulkBatchResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a bulk-upload batch and place its rows asynchronously.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.orders.createBulkUpload({
    body: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.CreateBulkUploadOrdersBulkPostRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.orders.<a href="/src/api/resources/orders/client/Client.ts">getBulkUpload</a>({ ...params }) -> Zinc.BulkBatchResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a batch with per-row results and live order statuses.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.orders.getBulkUpload({
    batch_id: "batch_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.GetBulkUploadOrdersBulkBatchIdGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.orders.<a href="/src/api/resources/orders/client/Client.ts">downloadBulkResults</a>({ ...params }) -> string</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Download the batch results as a CSV (status + echoed custom columns).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.orders.downloadBulkResults({
    batch_id: "batch_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.DownloadBulkResultsOrdersBulkBatchIdResultsCsvGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.orders.<a href="/src/api/resources/orders/client/Client.ts">listOrders</a>({ ...params }) -> Zinc.OrderListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a list of orders for the current user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.orders.listOrders();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.ListOrdersOrdersGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.orders.<a href="/src/api/resources/orders/client/Client.ts">createOrder</a>({ ...params }) -> Zinc.OrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Posts an order to a queue for processing
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
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
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.CreateOrderOrdersPostRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.orders.<a href="/src/api/resources/orders/client/Client.ts">exportOrdersCsv</a>({ ...params }) -> string</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Stream the current user's orders as a CSV file.

Takes the same filters as ``GET /orders`` (via the shared
``_visible_orders_filter``) so an export always contains exactly the rows
the caller was looking at — but no ``limit``/``offset``: the export covers
the whole filtered set, paged internally so memory stays flat.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.orders.exportOrdersCsv();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.ExportOrdersCsvOrdersExportGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.orders.<a href="/src/api/resources/orders/client/Client.ts">listTestProducts</a>() -> Record&lt;string, unknown&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get list of test products for sandbox testing.

Returns list of test product URLs that can be used with test API keys
to trigger different test scenarios.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.orders.listTestProducts();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.orders.<a href="/src/api/resources/orders/client/Client.ts">getOrder</a>({ ...params }) -> Zinc.OrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves an order by its ID
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.orders.getOrder({
    order_id: "order_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.GetOrderOrdersOrderIdGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.orders.<a href="/src/api/resources/orders/client/Client.ts">getOrderTimeline</a>({ ...params }) -> Zinc.OrderTimelineResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Customer-facing lifecycle timeline for an order.

Derived on read from existing data — no dedicated storage. Merges the
placement outcome (OrderLog) with carrier tracking state (TrackingNumber /
TrackingCheckpoint) into an ordered list of milestones. This is the order's
story to the customer, distinct from the admin-only job/automation log.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.orders.getOrderTimeline({
    order_id: "order_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.GetOrderTimelineOrdersOrderIdTimelineGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.orders.<a href="/src/api/resources/orders/client/Client.ts">cancelOrder</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cancel an order by its ID. Orders can only be cancelled if they are pending.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.orders.cancelOrder({
    order_id: "order_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.CancelOrderOrdersOrderIdCancelPostRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Products
<details><summary><code>client.products.<a href="/src/api/resources/products/client/Client.ts">searchProducts</a>({ ...params }) -> Zinc.ProductSearchResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Search for products on a retailer.

**Best Buy returns a partial page.** Best Buy server-renders only about 4 of
the ~24 products on a search page and loads the rest in the browser, so each
page yields roughly 4 results rather than a full page. Ranking, pricing and
availability are Best Buy's own; there are simply fewer items per page. Page
through with `next_page` to collect more — `next_page` reflects whether Best
Buy has further results, not how many came back in this response.

**Shopify stores are their own retailer**: pass the store's domain as
`retailer` (e.g. `retailer=yetch.studio`; any Shopify-powered storefront
works). Results are the store's own top matches (~10) and there is no
pagination, so `next_page` is always null and `page` must be omitted or 1.
`product_id` is the store-scoped product handle to pass to the details
endpoint with the same `retailer`.

**Etsy search covers US shops, priced in USD.** Etsy sellers price in their
own currency and a single page routinely mixes several, which makes `price`
incomparable across a result set — so search is narrowed to US-located
shops and any remaining non-USD listing is dropped. `currency_code` is set
on every result and is always `USD` here, and prices are never converted,
so the number is what the seller charges. Because the currency check runs
after Etsy paginates, **a page can come back short while more results still
exist** — page on with `next_page`. (Details is neither narrowed nor
filtered: it returns any listing, in its own currency.)

Etsy results carry no `stars`/`num_reviews` — Etsy publishes a rating for
the *shop*, not the listing, and reporting a seller's rating as the
product's would be misleading; `brand` carries the shop name, and the
details endpoint reports the shop's rating explicitly. `product_id` is the
numeric listing id.

**Billing.** This is a metered data call: $0.01 is drawn from your wallet per successful request, before any order is placed. An empty wallet gets `402` instead. Sandbox (`zn_test_`) calls are free and never touch the live wallet.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.products.searchProducts({
    query: "query",
    retailer: "retailer"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.SearchProductsProductsSearchGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.products.<a href="/src/api/resources/products/client/Client.ts">getProductOffers</a>({ ...params }) -> Zinc.GetProductOffersProductsProductIdOffersGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get offers for a product from a retailer.

Not available for Shopify stores: a storefront lists one seller (itself),
so per-variant price and availability live on the details endpoint instead.

**Billing.** This is a metered data call: $0.01 is drawn from your wallet per successful request, before any order is placed. An empty wallet gets `402` instead. Sandbox (`zn_test_`) calls are free and never touch the live wallet.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.products.getProductOffers({
    product_id: "product_id",
    retailer: "retailer"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.GetProductOffersProductsProductIdOffersGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.products.<a href="/src/api/resources/products/client/Client.ts">getProductDetails</a>({ ...params }) -> Zinc.GetProductDetailsProductsProductIdGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get details for a product from a retailer.

**Best Buy is addressed by `bsin`**, not by the numeric SKU — the bsin is the
trailing id in a Best Buy product URL (`/product/{slug}/{bsin}`). Search
results return the SKU as `product_id` and also carry the bsin, so pass the
bsin here. The response repeats the SKU as `sku` for cross-referencing.

Unlike `/search`, a Best Buy detail response is complete: detail pages are
fully server-rendered, so nothing is withheld for client-side loading.

**Shopify is addressed by (store, handle)**: pass the store's domain as
`retailer` (e.g. `retailer=yetch.studio`) and the product handle — the slug
in `/products/{handle}`, returned as `product_id` by search — as the path
parameter. The response includes per-variant price and availability.
`async` is not supported for Shopify stores.

**Etsy is addressed by the numeric listing id** (returned as `product_id` by
search). `price` is in minor units of `currency_code`, not converted to USD.

Etsy ratings are the **shop's**, reported as `shop_review_average` /
`shop_review_count`, and both cover only the **past year** — an established
shop with no recent sales reports 0, and an unrated shop reports a null
average rather than 0.0 stars. `stars` and `num_reviews` are deliberately
not set: they mean a product's rating everywhere else in this API, and a
seller's rating is a different claim.

`listing_type` is `physical`, `download` or `both` — a download has nothing
to ship. `available` accounts for the shop being on vacation as well as
stock, so it can be false on an in-stock active listing; `shop_is_vacation`
says which it was. `variants` is populated only when Etsy exposes a
listing's inventory matrix — check `has_variations` to tell "no variants"
from "variants not visible". `taxonomy_id` is Etsy's raw category id; there
is no category name yet. `async` is not supported for Etsy.

**Billing.** This is a metered data call: $0.01 is drawn from your wallet per successful request, before any order is placed. An empty wallet gets `402` instead. Sandbox (`zn_test_`) calls are free and never touch the live wallet.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.products.getProductDetails({
    product_id: "product_id",
    retailer: "retailer"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.GetProductDetailsProductsProductIdGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Search
<details><summary><code>client.search.<a href="/src/api/resources/search/client/Client.ts">search</a>({ ...params }) -> Zinc.SearchResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Search for products across retailers; returns orderable zn_sku_ listings.

**Billing.** This is a metered data call: $0.01 is drawn from your wallet per successful request, before any order is placed. An empty wallet gets `402` instead. Sandbox (`zn_test_`) calls are free and never touch the live wallet.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.search.search({
    q: "q"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.SearchSearchGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SearchClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## ManagedAccounts
<details><summary><code>client.managedAccounts.<a href="/src/api/resources/managedAccounts/client/Client.ts">listRetailerCredentials</a>({ ...params }) -> Zinc.RetailerCredentialsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all retailer credentials for the current user.
If is_global=True (admin only), list global credentials instead.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.managedAccounts.listRetailerCredentials();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.ListRetailerCredentialsManagedAccountsGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ManagedAccountsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.managedAccounts.<a href="/src/api/resources/managedAccounts/client/Client.ts">createRetailerCredentials</a>({ ...params }) -> Zinc.RetailerCredentialsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create new retailer credentials for the current user.
If is_global=True (admin only), creates global credentials owned by the system user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.managedAccounts.createRetailerCredentials({
    email: "email"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.RetailerCredentialsCreate` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ManagedAccountsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.managedAccounts.<a href="/src/api/resources/managedAccounts/client/Client.ts">updateRetailerCredentials</a>({ ...params }) -> Zinc.RetailerCredentialsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update retailer credentials for the current user.
Admins can also update global credentials.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.managedAccounts.updateRetailerCredentials({
    short_id: "short_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.RetailerCredentialsUpdate` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ManagedAccountsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.managedAccounts.<a href="/src/api/resources/managedAccounts/client/Client.ts">deleteRetailerCredentials</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete retailer credentials for the current user.
Admins can also delete global credentials.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.managedAccounts.deleteRetailerCredentials({
    short_id: "short_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.DeleteRetailerCredentialsManagedAccountsShortIdDeleteRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ManagedAccountsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Agent
<details><summary><code>client.agent.<a href="/src/api/resources/agent/client/Client.ts">createMppOrder</a>({ ...params }) -> Zinc.OrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Place an order via the Machine Payments Protocol (MPP).

No Zinc account required. Payment is made upfront via MPP.
Supports multiple payment methods (e.g. Tempo, Stripe).
If no valid payment credential is provided, returns HTTP 402
with payment challenges for all configured methods.

Payment is the gate, but only for a genuine discovery probe: a bodyless
POST (from a registry like mppscan) is parsed leniently and reaches the 402
challenge instead of a 422. A *present-but-invalid* body, by contrast —
including malformed JSON and non-object JSON — is a real order attempt
and is rejected with a 422 up front, before any payment
challenge is issued or honored. Otherwise an agent could settle an on-chain
payment against the challenge and then be rejected on the retry, with no way
to refund the settlement (the MPP layer cannot verify or reverse a payment
whose retry body no longer matches the challenge).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.agent.createMppOrder({
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
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.CreateMppOrderAgentOrdersPostRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AgentClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.agent.<a href="/src/api/resources/agent/client/Client.ts">search</a>({ ...params }) -> Zinc.SearchResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Beta** — response shape may change. Cross-retailer product search for agents. Returns orderable listings whose
`url` can be passed straight to POST /agent/orders.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.agent.search({
    q: "q"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.AgentSearchRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AgentClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.agent.<a href="/src/api/resources/agent/client/Client.ts">productSearch</a>({ ...params }) -> Zinc.ProductSearchResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Per-retailer product search for agents (amazon | walmart).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.agent.productSearch({
    query: "query",
    retailer: "amazon"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.AgentProductSearchRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AgentClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.agent.<a href="/src/api/resources/agent/client/Client.ts">productOffers</a>({ ...params }) -> Zinc.AgentProductOffersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Offers/pricing for a specific product on a retailer.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.agent.productOffers({
    product_id: "product_id",
    retailer: "amazon"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.AgentProductOffersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AgentClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.agent.<a href="/src/api/resources/agent/client/Client.ts">productDetails</a>({ ...params }) -> Zinc.AgentProductDetailsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Full product details for a specific product on a retailer.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.agent.productDetails({
    product_id: "product_id",
    retailer: "amazon"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.AgentProductDetailsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AgentClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Returns
<details><summary><code>client.returns.<a href="/src/api/resources/returns/client/Client.ts">listReturnRequests</a>({ ...params }) -> Zinc.ReturnRequestListResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.returns.listReturnRequests();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.ListReturnRequestsReturnsGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ReturnsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.returns.<a href="/src/api/resources/returns/client/Client.ts">createReturnRequest</a>({ ...params }) -> Zinc.ReturnRequestResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.returns.createReturnRequest({
    order_id: "order_id",
    items: [{
            order_item_id: "order_item_id",
            quantity: 1
        }],
    reason: "damaged"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.ReturnRequestCreate` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ReturnsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.returns.<a href="/src/api/resources/returns/client/Client.ts">getReturnRequest</a>({ ...params }) -> Zinc.ReturnRequestResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.returns.getReturnRequest({
    return_request_id: "return_request_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.GetReturnRequestReturnsReturnRequestIdGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ReturnsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Retailers
<details><summary><code>client.retailers.<a href="/src/api/resources/retailers/client/Client.ts">listRetailers</a>({ ...params }) -> Zinc.PublicRetailerListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List the retailers Zinc supports — the public "what do you support?" catalog.

No authentication required. One flat object per retailer brand: identifier,
domain, countries shipped to, and the free-shipping policy. International
marketplaces (e.g. amazon.com / amazon.de) are grouped under one brand with
the country listed in `supported_countries`. Optionally filter by name.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.retailers.listRetailers();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.ListRetailersRetailersGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RetailersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Usage
<details><summary><code>client.usage.<a href="/src/api/resources/usage/client/Client.ts">getMyUsage</a>({ ...params }) -> Zinc.UserUsageResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The caller's own data-API usage over a trailing window, per endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.usage.getMyUsage();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.GetMyUsageUsageGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UsageClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Wallet
<details><summary><code>client.wallet.<a href="/src/api/resources/wallet/client/Client.ts">getWallet</a>({ ...params }) -> Zinc.WalletResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get your wallet balance.

All amounts are integer cents. `balance` is the ledger balance;
`spendable_balance` is what `POST /orders` actually checks against (the two
differ only for Zinc Connect accounts with in-flight holds). An order needs
`max_price + order_fee_cents` spendable, so compare against that before
placing one instead of discovering a shortfall as a 402. Bulk-deal customers
(`billed_by_invoice: true`) are invoiced monthly and skip the balance check.

Under a `zn_test_` key (or `X-Test-Mode`) this reads the sandbox wallet,
which sandbox orders never draw down. Funds are added from the dashboard.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.wallet.getWallet();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.GetWalletWalletMeGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WalletClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Stats
<details><summary><code>client.stats.<a href="/src/api/resources/stats/client/Client.ts">getDeliveryMap</a>() -> Zinc.DeliveryMapResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Recent delivered orders as anonymized, city-level map points.

Public and unauthenticated — feeds the marketing site's globe. Points are
ZIP-centroid coordinates rounded to two decimals with a curated category
emoji; deduplicated and capped. Cached for about an hour.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.stats.getDeliveryMap();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `StatsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.stats.<a href="/src/api/resources/stats/client/Client.ts">getLifetimeStats</a>() -> Zinc.LifetimeStatsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Zinc's all-time successful-order count and GMV.

Public and unauthenticated. Top-level numbers are v2 (this service);
``v1`` is the worker-computed legacy snapshot (seed until the first
compute lands); ``combined`` sums both. Cached for about a day.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.stats.getLifetimeStats();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `StatsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Tracking
<details><summary><code>client.tracking.<a href="/src/api/resources/tracking/client/Client.ts">getPublicTracking</a>({ ...params }) -> Zinc.PublicTrackingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Public tracking view for a single order, keyed by its UUID.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tracking.getPublicTracking({
    order_id: "order_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.GetPublicTrackingTrackOrderIdGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TrackingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Sandbox
<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">createSandboxKey</a>({ ...params }) -> Zinc.SandboxKeyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Mint a provisional sandbox user + test API key. No account needed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.createSandboxKey({});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.SandboxKeyCreate | null` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SandboxClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">claimSandbox</a>({ ...params }) -> Zinc.SandboxClaimResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Fold a provisional sandbox into the authenticated account.

Always a merge: Stytch's callback creates a real user row on first login,
so a caller reaching this endpoint already has an account. The agent's key
is reassigned rather than revoked, so whatever it has hardcoded keeps
working — that is the point of claiming rather than starting over.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.claimSandbox({
    token: "token"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.SandboxClaimRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SandboxClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">getSandboxStatus</a>({ ...params }) -> Zinc.SandboxStatusResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Whether the sandbox this key belongs to has been claimed yet.

An agent hands its claim URL to a human and then has no way to learn what
happened — a device-code grant would tell it for free (issue #825). Until
we have one, polling this closes the loop.

Still provisional means nobody has claimed it. Past that, "not provisional"
alone would be a lie — every ordinary account would read as claimed — so
the answer comes from the claim event written on the account, which is
also the only durable evidence a claim happened once the provisional row
is deleted.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.getSandboxStatus();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.GetSandboxStatusSandboxStatusGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SandboxClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">getQuickstart</a>() -> string</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The agent quickstart, served as plain markdown.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.getQuickstart();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `SandboxClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Device
<details><summary><code>client.device.<a href="/src/api/resources/device/client/Client.ts">createDeviceCode</a>({ ...params }) -> Zinc.DeviceCodeResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Mint a device code. No account needed.

Send your `zn_test_` sandbox key as the bearer and the sandbox comes along:
when the owner approves, its orders and key move onto their account and
your sandbox key keeps working, alongside the live key you receive.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.device.createDeviceCode({
    body: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.CreateDeviceCodeDeviceCodePostRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DeviceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.device.<a href="/src/api/resources/device/client/Client.ts">describeDeviceCode</a>({ ...params }) -> Zinc.DeviceCodeInfo</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Public on purpose: it holds only what the agent said about itself, and
the approval page needs it before the human has signed in.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.device.describeDeviceCode({
    user_code: "user_code"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.DescribeDeviceCodeDeviceCodesUserCodeGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DeviceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.device.<a href="/src/api/resources/device/client/Client.ts">decideDeviceCode</a>({ ...params }) -> Zinc.DeviceApproveResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The human's decision. A machine credential must never make it: an API
key approving a device code would be a key minting a key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.device.decideDeviceCode({
    user_code: "user_code",
    granted: true
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.DeviceApproveRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DeviceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.device.<a href="/src/api/resources/device/client/Client.ts">redeemDeviceCode</a>({ ...params }) -> Zinc.ApiKeyExchangeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.device.redeemDeviceCode({
    device_code: "device_code"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.DeviceTokenRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DeviceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Webhooks
<details><summary><code>client.webhooks.<a href="/src/api/resources/webhooks/client/Client.ts">getWebhookEndpoint</a>({ ...params }) -> Zinc.WebhookEndpointResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The URL Zinc delivers this account's webhooks to, and the HMAC secret
that signs them. Both are null until ``PUT /webhooks/endpoint`` is called.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.webhooks.getWebhookEndpoint();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.GetWebhookEndpointWebhooksEndpointGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.<a href="/src/api/resources/webhooks/client/Client.ts">setWebhookEndpoint</a>({ ...params }) -> Zinc.WebhookEndpointResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Register (or replace) the webhook URL for this account.

Every order and return event Zinc emits for the account is POSTed to this
URL. A signing secret is generated on first registration and returned so
the caller can verify the ``X-Webhook-Signature`` header; replacing the URL
keeps the existing secret, so a URL move never invalidates verification.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.webhooks.setWebhookEndpoint({
    url: "https://example.com/zinc/webhook"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.WebhookEndpointUpdate` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.<a href="/src/api/resources/webhooks/client/Client.ts">clearWebhookEndpoint</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Stop webhook delivery for this account by clearing the URL.

The signing secret is kept, so re-registering a URL later resumes
deliveries signed with the same secret the caller already verifies against.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.webhooks.clearWebhookEndpoint();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Zinc.ClearWebhookEndpointWebhooksEndpointDeleteRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Health
<details><summary><code>client.health.<a href="/src/api/resources/health/client/Client.ts">getPublicHealth</a>() -> Zinc.PublicHealthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Customer-facing platform health.

No auth. Cached in-process for 4 minutes — at the marketing site's 5-min
cron cadence, the DB is touched at most ~once per tick.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.health.getPublicHealth();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `HealthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

