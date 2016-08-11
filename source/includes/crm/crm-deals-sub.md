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


### Upload Files in Deal


```http
POST api/crm/deals/{deal_id}/files HTTP/1.1
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
   "title":"logo.png",
   "attachment":"deals/278/1470895170858_logo.png",
   "ext":"png",
   "file_size":1911
}
```

```
Sample Response
```

```json
{
   "id":277,
   "title":"logo.png",
   "attachment":"deals/278/1470895170858_logo.png",
   "is_drivebox":false,
   "is_trashed":false,
   "modified_by":null,
   "size":"1911",
   "created_by":{
      "url":"/users/1",
      "image":"https://twprofile.s3.amazonaws.com/users/image.jpg",
      "id":1,
      "full_name":"SathishVenkat",
      "email":"sathish@adhome.com",
      "label_txt":"SV"
   },
   "act_on":"2016-08-11T05:59:34.690463Z",
   "created_on":"2016-08-11T05:59:34.690463Z",
   "is_live":true,
   "thumbnail":null,
   "modified_on":"2016-08-11T05:59:34.690521Z",
   "ext":"png",
   "resource_url":"/crm/deals/278/files/277",
   "download_url":"https://app.adhome.com/api/crm/deals/278/files/download/277"
}
```

<aside>POST  api/crm/deals/{deal_id}/files</aside>

Attributes | Description
-----------| ------------
title (*string*) | file name
attachment (*string*) | file location
ext (*string*) | extension
file_size (*integer*)| file size in bytes
