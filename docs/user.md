# User API Spec

## Register User

Endpoint Body : POST /api/users

Request Body :

```json
{
  "username": "Daffa",
  "password": "rahasia",
  "name": "Muhammad Daffa"
}
```

Response body (Success) :

```json
{
  "data": "OK"
}
```
Response body (Failed) :

```json
{
  "erorrs": "Username must not blanks, ??"
}
```

## Login User

Endpoint Body : POST /api/auth/login

Request Body :

```json
{
  "username": "Daffa",
  "password": "rahasia"
}
```

Response body (Success) :

```json
{
  "data": {
    "token": "TOKEN",
    "expiredAt": 234567892736353 // milliseconds 
  }
}
```
Response body (Failed, 401) :

```json
{
  "erorrs": "Username or password wrong"
}
```

## Get User

Endpoint Body : GET /api/users/current

Request Haader :z

- X-API_TOKEN : Token (Mandatory)


Response body (Success) :

```json
{
  "data": {
    "username": "Daffa",
    "name": "Muhammad Daffa"
  }
}
```
Response body (Failed, 401) :

```json
{
  "erorrs": "Unauthorized"
}
```

## Update User

Endpoint Body : PATCH /api/users/current

Request Haader :

- X-API_TOKEN : Token (Mandatory)

Request body :

```json
{
  "name": "Daffa", // out if only want to update name
  "password": "new password" // put if only sent to update password
}
```

Response body (Success) :

```json
{
  "data": {
    "username": "Daffa",
    "name": "Muhammad Daffa"
  }
}
```
Response body (Failed, 401) :

```json
{
  "erorrs": "Unauthorized"
}
```

## Logout User

Endpoint Body : DELETE /api/auth/logout

Request Haader :

- X-API_TOKEN : Token (Mandatory)

Response body (Success) :

```json
{
  "data": "OK"
}
```