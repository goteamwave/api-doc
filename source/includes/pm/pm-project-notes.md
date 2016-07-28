## Notes

### Note Object

```json
{
    "id": 518,
    "name": "Creating a Template from an Existing Project",
    "content": "<p>Create a template by copying the customizations of an existing project. <br/>You will be given option to either include or exclude the assigned tasks<br/> to the new template. The new template will have all the discussions, <br/>tasks, files, notes, milestones and team members of the existing <br/>project. The completed tasks will be reopened automatically in the new <br/>template.<br/></p>",
    "modified_by": null,
    "resource_url": "/projects/1190/notes/518",
    "is_trashed": false,
    "created_on": "2016-07-21T10:53:26.663830Z",
    "modified_on": "2016-07-21T10:53:26.663857Z",
    "comment_count": 0,
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
            "logo": "https://twprofile.s3.amazonaws.com/logos/image.jpeg",
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
        "image": "https://twprofile.s3.amazonaws.com/users/image.jpg",
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
    "versions": [
        {
            "id": 972,
            "name": "Creating a Template from an Existing Project",
            "created_on": "2016-07-21T10:53:26.773477Z",
            "version": 1,
            "is_current": true,
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
                    "logo": "https://twprofile.s3.amazonaws.com/logos/image.jpeg",
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
                "image": "https://twprofile.s3.amazonaws.com/users/image.jpg",
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
            "resource_url": "/projects/1190/notes/518/version/972"
        }
    ],
    "is_private": false
}
```

Attribute | Description
----------| ------------
id (*int*) | Identification number of the Note
name (*string*) | title given of the Note
content (*string*) | Description of the Note
[modified_by](#pm-user-object) (*object*) | user object who modified the Note
resource_url (*string*)  | Note's detail page access url
is_trashed (*boolean*) | Status to check note is trashed or not
created_on (*date*) | Note created date
modified_on (*date*) | Date on which the note is modified
comment_count (*int*) | No of comments for the note
[created_by](#pm-user-object) (*object*) | User object who created the note
[versions](#version-object) (*array of objects*) | Version of the note
is_private (*boolean*) | Status to check note is private or not

#### Version Object

Attribute | Description
----------| ------------
id (*int*) | Identification number of the version
name (*string*) | title given of the Note
created_on (*date*) | Note created date
version (*int*) | version number
is_current (*boolean*) | Status to identify this is the current version of the note  or not
created_by (*object*) | User object who created the note version
resource_url (*string*) | Note Version's detail page access url

### Create Note

```http
POST api/projects/{project_id}/notes/{note_id} HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

```json
{
	"project":"1190",
	"name":"Creating a Template from an Existing Project",
	"content":
    "<p>Create a template
        by copying the customizations of an existing project. <br/>You will be given option to either include
        or exclude the assigned tasks<br/> to the new template. The new template will have all the discussions
        , <br/>tasks, files, notes, milestones and team members of the existing <br/>project. The completed tasks
        will be reopened automatically in the new <br/>template.<br/>
    </p>"
}
```

<aside>POST  api/projects/{project_id}/notes/{note_id}</aside>


### Update Note

```http
PATCH api/projects/{project_id}/notes/{note_id} HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

```json
{
"id":520,
"name":"Creating a Template from an Existing Project",
"content":
    "<p><b>Create a template by
        copying the customizations</b> of an existing project. <br/>You will be given option to either include
        or exclude the assigned tasks<br/> to the new template. The new template will have all the discussions
        , <br/>tasks, files, notes, milestones and team members of the existing <br/>project. The completed tasks
        will be reopened automatically in the new <br/>template.<br/>
    </p>",
"modified_by":null,
"resource_url":"/projects/1190/notes/520",
"is_trashed":false,
"created_on":"2016-07-21T11:08:40.692271Z",
"modified_on":"2016-07-21T11:08:40.692310Z",
"comment_count":0,
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
        "logo": "https://twprofile.s3.amazonaws.com/image.jpeg",
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
    "image": "https://twprofile.s3.amazonaws.com/image.jpg",
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
"versions":[
    {
        "id": 972,
        "name": "Creating a Template from an Existing Project",
        "created_on": "2016-07-21T10:53:26.773477Z",
        "version": 1,
        "is_current": true,
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
                "logo": "https://twprofile.s3.amazonaws.com/image.jpeg",
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
            "image": "https://twprofile.s3.amazonaws.com/image.jpg",
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
        "resource_url": "/projects/1190/notes/518/version/972"
    }
],
"is_private":true,
}
```

<aside>PATCH api/projects/{project_id}/notes/{note_id}</aside>

#### Returns 

If the call succeeds, it will return the Note object.

### Delete Note

```http
PATCH api/projects/{project_id}/notes/{note_id}/trash HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

```json
{
    "trashed":"success"
}
```

<aside>PATCH api/projects/{project_id}/notes/{note_id}/trash</aside>


