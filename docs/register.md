# Register API

Create a new user account.

## Endpoint

```http
POST /api/auth/register
```

## Request Body

```json
{
  "email": "user@example.com",
  "password": "123456"
}
```

## Success Response

```json
{
  "success": true,
  "message": "User registered successfully"
}
```