# HTTP Status Codes

Our API uses standard HTTP status codes to indicate whether a request was successful or failed.

## Success Codes

### 200 OK

The request was successful.

```http
GET /api/products
```

```json
{
  "success": true,
  "products": []
}
```

### 201 Created

A new resource was successfully created.

```http
POST /api/orders
```

```json
{
  "success": true,
  "message": "Order created successfully"
}
```

## Client Error Codes

### 400 Bad Request

The request contains invalid or missing data.

```json
{
  "success": false,
  "message": "Email is required"
}
```

### 401 Unauthorized

Authentication is required or the JWT token is invalid.

```json
{
  "success": false,
  "message": "Unauthorized"
}
```

### 404 Not Found

The requested resource does not exist.

```json
{
  "success": false,
  "message": "Product not found"
}
```

## Server Error

### 500 Internal Server Error

An unexpected error occurred on the server.

```json
{
  "success": false,
  "message": "Internal server error"
}
```