# User API Spec

## Register User

Endpoint : POST /api/users
Role: admin

Request Body :

```json
{
  "name": "rendi",
  "password": "rendi"
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "name": "rendi",
    "role": "admin"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Username already registered"
}
```

## Login User

Endpoint : POST /api/users/login

Request Body :

```json
{
  "name": "rendi",
  "password": "rahasia"
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "name": "rendi",
    "password": "rahasia",
    "token": "Bcrypt",
    "role": "admin"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Username or password is wrong"
}
```

## Get User

Endpoint : GET /api/users/current

Headers :

- Authorization: token

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "name": "rendi",
    "role": "admin"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Unauthorized"
}
```

## Logout User

Endpoint : DELETE /api/users/current

Headers :

- Authorization: token

Response Body (Success) :

```json
{
  "data": true
}
```
