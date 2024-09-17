# Grub API Spec

## Create Grub

Endpoint : POST /api/grub

Headers :

- Authorization: token

Request Body :

```json
{
  "name": "Join ml",
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": "UUD",
    "userId": 1,
    "name": "Join ml",
    "totalUsers": 10
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Unauthorized",
}
```

## Join Grub

Endpoint : POST /api/grub/join

Headers :

- Authorization: token

Request Body :

```json
{
  "grubId": 1
}
```

Response Body (Success) :

```json
{
  "data": {
    "userId": 1,
    "grubId": "random number",
    "name": "Join ml",
    "totalUsers": 10
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "GrubId not found",
}
```

## Update Group

Endpoint : PACTH /api/grub

Headers :

- Authorization: token

Request Body :

```json
{
  "name": "Mabar ml",
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "name": "Mabar ml",
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "No grub"
}
```

## Get Grub

Endpoint : GET /api/grub

Headers :

- Authorization: token

Response Body (Success) :

```json
{
  "data": [
    {
      "userId": 1,
      "username": "rendi"
    },
    {
      "userId": 2,
      "username": "hendra"
    }
  ]
}
```

Response Body (Failed) :

```json
{
  "errors": "Unauthorized"
}
```

## Logout Grub

Endpoint : DELETE /api/grub

Headers :

- Authorization: token

Response Body (Success) :

```json
{
  "data": true
}
```
