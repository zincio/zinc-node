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

