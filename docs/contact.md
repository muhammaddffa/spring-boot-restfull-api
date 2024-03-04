# Contact API User

## Create Contact

Endpoint : POST /api/contacts

Request Haader :

- X-API_TOKEN : Token (Mandatory)

Request body :

```json
{
  "firstnam": "Muhammad",
  "lastname": "Daffa",
  "email": "daffa@gmail.com",
  "phone": "098754323456"
}
```

Response body (Success):

````json
{
  "data": {
    "id": "Random-String",
    "firstname": "Daffa",
    "lastname": "Muhammad",
    "email": "daffa@gmail.com",
    "phone": "098754323456"
  }
}
````

Response body (Failed)

```json
{
  "errors": "Email format invalid, phone format invalid, ..."
}
```

## Update Contact

Endpoint : PUT /api/contacts/{idContact}

Request Haader :

- X-API_TOKEN : Token (Mandatory)

Request body :

```json
{
  "firstnam": "Muhammad",
  "lastname": "Daffa",
  "email": "daffa@gmail.com",
  "phone": "098754323456"
}
```

Response body (Success):

````json
{
  "data": {
    "id": "Random-String",
    "firstname": "Daffa",
    "lastname": "Muhammad",
    "email": "daffa@gmail.com",
    "phone": "098754323456"
  }
}
````

Response body (Failed):

```json
{
  "errors": "Email format invalid, phone format invalid, ..."
}
```

## Get Contact

Endpoint : GET /api/contacts/{idContacts}

Request Haader :

- X-API_TOKEN : Token (Mandatory)

Response body (Success):

````json
{
  "data": {
    "id": "Random-String",
    "firstname": "Daffa",
    "lastname": "Muhammad",
    "email": "daffa@gmail.com",
    "phone": "098754323456"
  }
}
````

Response body (Failed, 404):

```json
{
  "errors": "Contact not found"
}
```

## Search Contact

Endpoint : GET /api/contacts

Request Param:

- name : String, contact fistname of lastname, using like query, optional
- phone : String, contact phone , using like query, optional
- email : String, contact email, using like query, optional
- page : Integer, start from 0, default 0
- size : Integer, default 10

Request Haader :

- X-API_TOKEN : Token (Mandatory)

Response body (Success):

```json
{
  "data": [
    {
      "id": "Random-String",
      "firstname": "Daffa",
      "lastname": "Muhammad",
      "email": "daffa@gmail.com",
      "phone": "098754323456"
    }
  ],
  "pagging": {
    "curretPage": 0,
    "totalPage": 10,
    "size":10
  }
}
```

Response body (Failed):

## Remove Contact


Endpoint :

Request Haader : DELETE /api/contacts/{idContacts}

- X-API_TOKEN : Token (Mandatory)

Response body (Success):

```json
{
  "data": "OK"
}
```

Response body (Failed):

```json
{
  "errors": "Contact is not found"
}
```