# Address API Spec

## Create Address

Endpoint : POST /api/contact/{idContact}/addresses


Request Header :

- X-API_TOKEN : Token (Mandatory)

Request Body :

```json
{
  "street" : "jalan apa",
  "city": "Kota",
  "province": "Provinsi",
  "country": "Negara",
  "postalCode": "12313"
}
```


Response Body (Success) :

```json
{
  "data": {
    "id": "random string",
    "street": "jalan apa",
    "city": "Kota",
    "province": "Provinsi",
    "country": "Negara",
    "postalCode": "12313"
  }
}
```


Response Body (Failed) :

```json
{
  "errorrs": "Contact is not found",
  
}
```

## Update Address

Endpoint :


Request Header : PUT /api/contacts/{idContacts}/addresses/{idAddress}

- X-API_TOKEN : Token (Mandatory)

Request Body :

```json
{
  "street": "Jalan apa",
  "city": "Kota",
  "province": "Provinsi",
  "country": "Negara",
  "postalCode": "123232"
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": "randomstring",
    "street": "Jalan apa",
    "city": "Kota",
    "province": "Provinsi",
    "country": "Negara",
    "postalCode": "123232"
  }
}
```


Response Body (Failed) :

```json
{
  "errorrs": "Contact is not found",
  
}
```

## Get Address

Endpoint : GET /api/contacts/{idContacts}/addresses/{idAddress}


Request Header :

- X-API_TOKEN : Token (Mandatory)

Response Body (Success) :

```json
{
  "data": {
    "id": "randomstring",
    "street": "Jalan apa",
    "city": "Kota",
    "province": "Provinsi",
    "country": "Negara",
    "postalCode": "123232"
  }
}
```

Response Body (Failed) :

```json
{
  "errorrs": "Address is not found",
  
}
```

## Remove Address

Endpoint : DELETE /api/contacts/{idContacts}/addresses/{idAddress}


Request Header :

- X-API_TOKEN : Token (Mandatory)

Response Body (Success) :

```json
{
  "data": "OK"
}
```

Response Body (Failed) :

```json
{
  "errorrs": "Address is not found",
  
}
```

## List Address

Endpoint : GET /api/contacts/{idContacts}/addresses

Request Header :

- X-API_TOKEN : Token (Mandatory)

Response Body (Success) :

```json
{
  "data": [
    {
      "id": "randomstring",
      "street": "Jalan apa",
      "city": "Kota",
      "province": "Provinsi",
      "country": "Negara",
      "postalCode": "123232"
    }
  ]
}
```

Response Body (Failed) : 

```json
{
  "errorrs": "Contact is not found",
  
}
```
```