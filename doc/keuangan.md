# Keuangan API Spec

## Get keuangan all

Endpoint : Get /api/keuangan

Headers :

- Authorization: token

Response Body (Success) :

```json
{
  "data": [
    {
      "id": 1,
      "name": "rendi",
      "saldo": 50000
    },
    {
      "id": 2,
      "name": "Hendra",
      "saldo": 100000
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

## Get keuangan by Id

Endpoint : Get /api/keuangan/:id

Headers :

- Authorization: token

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "name": "rendi",
    "saldo": 50000
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Id not found"
}
```

## Update Saldo

Endpoint : Patch /api/keuangan/:id
Role: admin

Headers :

- Authorization: token

Request Body :

```json
{
  "saldo": 50000
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "name": "rendi",
    "saldo": 50000
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Unauthorized/Forbidden"
}
```
