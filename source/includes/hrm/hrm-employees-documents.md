## Documents 

### Document Object

```json
{
    "id": 85,
    "title": "images_004.jpeg",
    "attachment": "https://mediatw.s3.amazonaws.com/hrm/1466509302976_images_004.jpeg?Signature=Fx1mcacqtpi%2B7YpbIY5LejDFLjc%3D&Expires=1469185988&AWSAccessKeyId=AKIAJ3L5LCTCJXCFVTYA",
    "is_drivebox": false,
    "is_trashed": false,
    "modified_by": {
        "id": 1,
        "label_txt": "s",
        "image": "https://twprofile.s3.amazonaws.com/users/user-61ddc395-8145-493c-a72f-df70ac205783-image.jpg",
        "full_name": "sathish",
        "email": "sathish@example_domain.com",
        "upcoming_birthday": "2017-03-15"
    },
    "size": "4612",
    "created_by": {
        "id": 1,
        "label_txt": "s",
        "image": "https://twprofile.s3.amazonaws.com/users/user-61ddc395-8145-493c-a72f-df70ac205783-image.jpg",
        "full_name": "sathish",
        "email": "sathish@example_domain.com",
        "upcoming_birthday": "2017-03-15"
    },
    "thumbnail": null,
    "directory": 59,
    "is_live": true,
    "ext": "jpeg",
    "download_url": "http://192.168.1.51:8000/hrm/files/download/85",
    "created_on": "2016-06-21",
    "tags": [],
    "is_shared": false
}
```

Attribute | Description 
----------| ------------
id (*integer*) | Identificatoin number of the file
title (*string*) | Title of the file
attachment (*string*) | URl of the file
is_drivebox (*boolean*) | Status to check file is from drivebox(google drive or drop box) or not
is_trashed (*boolean*) | Status to check Cfile is trashed or not
[modified_by](#user-object) (*object*) | user object who modified the file
size (*string*) | Size of the file
[created_by](#user-object) (*object*) | user who created the file
thumbnail (*string*) | URL of the file's thumbnail
directory (*integer*) | Identificatoin number of the files's directory
is_live (*boolean*) | Status to check file is live or not
ext (*string*) | Extension type of the file
download_url (*string*) | URL to download the file
created_on (*date*) | date on which the file is created
tags (*array*) | tags belongs to the file.
is_shared (*boolean*) | Status to check file is shared or not

### Create Document


```http
POST api/hrm/people/{people_id}/files HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

```json
{
 	"title":"images_007.jpeg",
 	"attachment":"hrm/1469182994232_images_007.jpeg",
 	"ext":"jpeg",
 	"directory":59,
 	"file_size":7218,
 	"is_shared":false,
 	"is_live":false
 }
 ```

<aside>POST  api/hrm/people/{people_id}/files</aside>

### Activate Document

```http
PATCH api/hrm/people/{people_id}/files/activate HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

```json
{
 	"file_ids":[234],
 	"is_shared":true
}
```

<aside>PATCH api/hrm/people/{people_id}/files/activate</aside>


### Delete Document

```http
DELETE api/hrm/people/{people_id}/files/{file_id} HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

<aside>DELETE api/hrm/people/{people_id}/files/{file_id}</aside>

