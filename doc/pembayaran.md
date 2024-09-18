# Pembayaran API Spec

## Create Pembayaran

Endpoint : POST /api/pembayaran
Role: admin
Headers :

- Authorization: token

Request Body :

```json
{
  "nominal": 10000
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "name": "rendi",
    "nominal": 10000,
    "transaction_time": "2024-01-01T00:00:00"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Nominal Required"
}
```

## Update Pembayaran

Endpoint : Patch /api/pembayaran/:id
Role: admin
Headers :

- Authorization: token

Request Body :

```json
{
  "nominal": 5000
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "name": "rendi",
    "nominal": 5000,
    "transaction_time": "2024-01-01T00:00:00"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Nominal Required"
}
```

## Get Pembayaran by ID

Endpoint : Get /api/pembayaran/:id

Headers :

- Authorization: token

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "name": "rendi",
    "nominal": 10000,
    "transaction_time": "2024-01-01T00:00:00"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Id not found"
}
```

## Get Pembayaran by Current

Endpoint : Get /api/pembayaran/current

Headers :

- Authorization: token

Response Body (Success) :

```json
{
  "data": [
    {
      "id": 1,
      "name": "rendi",
      "nominal": 10000,
      "transaction_time": "2024-01-01T00:00:00"
    },
    {
      "id": 2,
      "name": "rendi",
      "nominal": 5000,
      "transaction_time": "2024-01-01T00:00:00"
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

## Get Pembayaran all

Endpoint : Get /api/pembayaran

Headers :

- Authorization: token

Response Body (Success) :

```json
{
  "data": [
    {
      "id": 1,
      "name": "rendi",
      "nominal": 10000,
      "transaction_time": "2024-01-01T00:00:00"
    },
    {
      "id": 2,
      "name": "rendi",
      "nominal": 5000,
      "transaction_time": "2024-01-01T00:00:00"
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
