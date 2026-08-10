# Products API

This API is used to manage products.

## Get All Products

### Endpoint

```http
GET /api/products
```

### Response

```json
{
  "success": true,
  "products": [
    {
      "id": "123",
      "name": "Laptop",
      "price": 50000
    }
  ]
}
```

---

## Get Single Product

### Endpoint

```http
GET /api/products/:id
```

### Example

```http
GET /api/products/123
```

### Response

```json
{
  "success": true,
  "product": {
    "id": "123",
    "name": "Laptop",
    "price": 50000
  }
}
```