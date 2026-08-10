# Authentication

Our API uses JWT (JSON Web Token) for authentication.

## How Authentication Works

1. Register a new account.
2. Login using email and password.
3. The API returns a JWT token.
4. Send the token with protected API requests.

```text
Register
   ↓
Login
   ↓
JWT Token
   ↓
Protected API
```

## Login

```http
POST /api/auth/login
```

### Request

```json
{
  "email": "user@example.com",
  "password": "123456"
}
```

### Response

```json
{
  "success": true,
  "token": "YOUR_JWT_TOKEN"
}
```

## Using the Token

For protected endpoints, send the token in the `Authorization` header.

```http
Authorization: Bearer YOUR_JWT_TOKEN
```

### Example

```http
GET /api/orders

Authorization: Bearer YOUR_JWT_TOKEN
```

## Important

Do not share your JWT token with anyone.

Do not store real passwords or real tokens inside documentation examples.