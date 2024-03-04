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


Request Header :

- X-API_TOKEN : Token (Mandatory)

Request Body :


Response Body (Success) :


Response Body (Faile) :


## Get Address

Endpoint :


Request Header :

- X-API_TOKEN : Token (Mandatory)

Request Body :


Response Body (Success) :


Response Body (Faile) :


## Remove Address

Endpoint :


Request Header :

- X-API_TOKEN : Token (Mandatory)

Request Body :


Response Body (Success) :


Response Body (Faile) :


## List Address

Endpoint :


Request Header :

- X-API_TOKEN : Token (Mandatory)

Request Body :


Response Body (Success) :


Response Body (Faile) : 
