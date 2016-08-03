# Authentication

Authenticate your account when using the API by including your secret API key in the request. You can manage your API keys in the `You` tab. Your API keys carry many privileges, so be sure to keep them secret! Do not share your secret API key in publicly accessible areas.

## Get API Key

You can get your API key from `Profile --> You --> API Key`. Copy the API key.

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


To make an API call, use this key as url parameter with the root url of the API (http://app.teamwave.com/api/)

Add `api_key=Your API Key` to your API url link for requests (POST, PATCH, GET, PUT).

All API requests must be made over HTTPS. Calls made over plain HTTP will fail. API requests without authentication(api_key) will also fail. 