# Authentication

Authenticate your account when using the API by including your secret API key in the request. Your API keys carry many privileges, so be sure to keep them secret!

## Get API Key

You can get your API key from your TeamWave Account `Profile --> You --> API Key`. Copy the API key.

<aside class="warning">Do not share your secret API key in publicly accessible areas.</aside>

## Make an API Call

```
Sample Request

https://app.teamwave.com/api/crm/deals/{deal_id}?api_key=Your_API_Key&format=json
```

```http
GET /api/crm/deals/{deal_id} HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```


To make an API call, use this key as url parameter or header parameter with the url of the API (http://app.teamwave.com/api/)

<aside class="success">GET https://app.teamwave.com/api/crm?api_key={Your_API_Key}</aside>

Add `api_key=Your API Key` to your API url link for requests (POST, PATCH, GET, PUT).

<aside class="warning">All API requests must be made over HTTPS. Calls made over plain HTTP will fail. API requests without authentication(api_key) will also fail. </aside>


## Status Codes


Our REST API uses the following status codes:


Status Code | Meaning
---------- | -------
200 | Request OK
201 | Resource created
400 | Bad Request -- Your request is bad
401 | Unauthorized -- Your API key is wrong
402 | Failed request
403 | Forbidden -- requested is hidden for administrators only
404 | Not Found -- The specified item could not be found
50x | Internal Server Error
