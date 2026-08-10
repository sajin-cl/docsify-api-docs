# Orders API

This API is used to create and manage orders.

## Create Order

### Endpoint

```http
POST /api/orders
```

### Request Body

```json
{
  "productId": "123",
  "quantity": 2,
  "address": "Trivandrum"
}
```

### Success Response

```json
{
  "success": true,
  "message": "Order created successfully",
  "order": {
    "id": "ORD123",
    "status": "Pending"
  }
}
```

---

## Get Orders

### Endpoint

```http
GET /api/orders
```

### Success Response

```json
{
  "success": true,
  "orders": [
    {
      "id": "ORD123",
      "status": "Pending"
    }
  ]
}
```