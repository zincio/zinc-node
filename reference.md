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

<details><summary><code>client.orders.<a href="/src/api/resources/orders/client/Client.ts">downloadBulkResults</a>({ ...params }) -> unknown</code></summary>
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

<details><summary><code>client.products.<a href="/src/api/resources/products/client/Client.ts">getProductOffers</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get offers for a product from a retailer.
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

<details><summary><code>client.products.<a href="/src/api/resources/products/client/Client.ts">getProductDetails</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get details for a product from a retailer.
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

<details><summary><code>client.agent.<a href="/src/api/resources/agent/client/Client.ts">searchPost</a>({ ...params }) -> Zinc.SearchResponse</code></summary>
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
await client.agent.searchPost({
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

**request:** `Zinc.AgentSearchPostRequest` 
    
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

<details><summary><code>client.agent.<a href="/src/api/resources/agent/client/Client.ts">productSearchPost</a>({ ...params }) -> Zinc.ProductSearchResponse</code></summary>
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
await client.agent.productSearchPost({
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

**request:** `Zinc.AgentProductSearchPostRequest` 
    
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

<details><summary><code>client.agent.<a href="/src/api/resources/agent/client/Client.ts">productOffers</a>({ ...params }) -> unknown</code></summary>
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

<details><summary><code>client.agent.<a href="/src/api/resources/agent/client/Client.ts">productOffersPost</a>({ ...params }) -> unknown</code></summary>
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
await client.agent.productOffersPost({
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

**request:** `Zinc.AgentProductOffersPostRequest` 
    
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

<details><summary><code>client.agent.<a href="/src/api/resources/agent/client/Client.ts">productDetails</a>({ ...params }) -> unknown</code></summary>
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

<details><summary><code>client.agent.<a href="/src/api/resources/agent/client/Client.ts">productDetailsPost</a>({ ...params }) -> unknown</code></summary>
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
await client.agent.productDetailsPost({
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

**request:** `Zinc.AgentProductDetailsPostRequest` 
    
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

