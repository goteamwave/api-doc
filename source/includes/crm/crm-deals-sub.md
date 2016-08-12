### Add Note in Deals


```http
POST api/crm/deals/{deal_id}/notes HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

```
Sample Request 
```

```json
{
"content": "<p>Test Note<br/></p>"
}
```

```
Sample Response
```

```json
{
   "id":202,
   "content":"<p>Test Note<br/></p>",
   "created_by":{
      "url":"/users/1",
      "image":"https://s3.amazonaws.com/image.jpg",
      "id":1,
      "full_name":"Jamie Jackson",
      "email":"jamie@adhome.com",
      "label_txt":"SV"
   },
   "act_on":"2016-08-11T05:47:22.470967Z",
   "is_pinned":false
}
```

<aside>POST  api/crm/deals/{deal_id}/notes</aside>
