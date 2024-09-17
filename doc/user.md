# User API Spec

## Register User

Endpoint : POST /api/users

Request Body :

```json
{
  "username": "rendi",
  "password": "rendi",
  "mlId": 1,
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "username": "rendi",
    "mlId": 1,
    "groupId": "null"
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
  "username": "rendi",
  "password": "rahasia"
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "username": "rendi",
    "password": "rahasia",
    "mlId": 1,
    "groupId": "null",
    "token": "Bcrypt"
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
    "username": "rendi",
    "mlId": 1,
    "groupId": "null"
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
