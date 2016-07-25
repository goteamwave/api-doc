## Files


```json
{
    "id": 4412,
    "title": "images_006.jpeg",
    "attachment": "https://mediatw.s3.amazonaws.com/projects/1190/1469097342438_images_006.jpeg?Signature=ZiE9Qvf1LK%2BxA4gxNkLrx4%2Bzx8c%3D&Expires=1469100966&AWSAccessKeyId=AKIAJ3L5LCTCJXCFVTYA",
    "object_id": null,
    "is_drivebox": false,
    "is_trashed": false,
    "modified_by": null,
    "project": 1190,
    "size": "7114",
    "for_comment": false,
    "content_object_detail": {},
    "created_by": {
        "id": 1,
        "first_name": "sathish",
        "last_name": "",
        "label_txt": "s",
        "is_crm_enabled": true,
        "is_crm_admin": true,
        "is_pm_enabled": true,
        "is_hrm_admin": true,
        "corp_email": true,
        "organization": {
            "id": 1,
            "name": "Dsqqqqqqq ds 2123",
            "domain": "adhome",
            "logo": "https://twprofile.s3.amazonaws.com/logos/organization-1ae4b5e4-457f-4b0a-aad6-370b542fe1ce-image.jpeg",
            "email": "geo.jacob@adhome.com",
            "tenant_domain": "adhome.com",
            "created_on": "2015-03-10",
            "default_currency": "USD",
            "default_currency_symbol": "$",
            "label_txt": null,
            "orgkey": "Dsq",
            "status": "paying",
            "trial_end_on": "2016-07-07"
        },
        "image": "https://twprofile.s3.amazonaws.com/users/user-61ddc395-8145-493c-a72f-df70ac205783-image.jpg",
        "email": "sathish@adhome.com",
        "full_name": "sathish ",
        "is_owner": true,
        "is_admin": true,
        "is_active": true,
        "last_login": "2016-07-21T06:24:04.037715Z",
        "job_title": "Developer",
        "time_zone": "Asia/Kolkata",
        "uuid": "7452387e2f1d4eda952cb12ffbefb6b1",
        "country": null,
        "is_noticeboard_enabled": true,
        "is_user_directory_enabled": true
    },
    "created_on": "2016-07-21T10:35:48.556209Z",
    "is_live": true,
    "thumbnail": null,
    "comment_count": 0,
    "modified_on": "2016-07-21T10:35:48.556252Z",
    "is_shared": false,
    "shared_note": null,
    "content_type": null,
    "ext": "jpeg",
    "resource_url": "/projects/1190/files/4412",
    "download_url": "http://192.168.1.51:9002/projects/1190/files/download/4412",
    "is_private": false,
    "tgs": null
}		
```

Attribute | Description 
----------| ------------
id (*integer*) | Identification number of the attachment,
title (*string*) | Name of the attachment,
attachment (*string*) | URL of the attachment,
object_id (*integer*) | id of the task,
is_drivebox (*boolean*) | Status to check attachment is from drivebox(google drive or drop box) or not,
is_trashed (*boolean*) | Status to check attachment is trashed or not,
[modified_by](#pm-user-object) (*object*) | user object who modified the attachment,
project (*integer*) | Id of the project,
size (*string*) | Size of the attachment,
for_comment (*boolean*) | Status to check attachment is for comments or not,
[content_object_detail](#content-object-detail) (*object*) | Detail of the content_object,
[created_by](#pm-user-object) (*object*) | user who created the attachment,
created_on (*date*) | date on which the attachment is created,
is_live (*boolean*) | Status to check attachment is live or not,
thumbnail (*string*) | URL of the attachment's thumbnail,
comment_count(*inr*) | Comment count of the attachment's thumbnail,
modified_on (*date*) | date on which the attachment is modified,
is_shared (*boolean*) | Status to check attachment is shared or not,
shared_note (*string*) |Shared note of the attachment,
content_type (*string*) | Content type of the attachment. eg,.task,
ext (*string*) | Extension type of the attachment,
resource_url (*string*)  | Attachments detail page access url,
download_url  (*string*) | URL to download the attachment,
is_private (*boolean*) | Status to check attachment is private or not,
tags (*array*) | tags belongs to the attachment.


### Create File

```http
POST /api/projects/{project_id}/files HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

```json
{
	"status":"A",
	"title":"images_002.jpeg",
	"attachment":"http://amazons.com/projects/1190/1469097941615_images_002.jpeg",
	"ext":"jpeg",
	"project":"1190",
	"file_size":8773
}
```

<aside>POST  api/projects/{project_id}/files</aside>

### Activate File

```http
PATCH /api/projects/{project_id}/files/activate HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

```
Sample Response
```

```json
{
	"ids":[4413],
	"is_private":false
}
```

<aside>PATCH api/projects/{project_id}/files/activate</aside>

### Delete File

```http
PATCH /api/projects/{project_id}/files/{file_id}/trash HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

``` 
Sample Response
```

```json
{
	"trashed":"success"
}
```



<aside>PATCH api/projects/{project_id}/files/{file_id}/trash</aside>