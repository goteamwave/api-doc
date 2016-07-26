## Templates

A project is added to templates, if the boolean variable `is_template` becomes true. 

### Template Object

```json
{
   "id":929,
   "name":"cv",
   "description":null,
   "logo":null,
   "owner":{
      "id":1,
      "name":"Sam Johnson",
      "domain":"adhome",
      "logo":"https://twprofile.s3.amazonaws.com/image.jpg",
      "email":"sathish@adhome.com",
      "tenant_domain":"adhome.com",
      "created_on":"2015-03-07",
      "default_currency":"USD",
      "default_currency_symbol":"$",
      "label_txt":null,
      "orgkey":"adhomemediaindiapvtltd",
      "status":"paying",
      "trial_end_on":"2016-07-07"
   },
   "clients":[

   ],
   "users":[
      272,
      1
   ],
   "is_trashed":false,
   "start_date":null,
   "end_date":null,
   "budget":0.0,
   "privacy_enabled":false,
   "permissions":{

   },
   "last_updated":"2016-06-14T06:37:43.336521Z",
   "tasks_enabled":true,
   "created_by":1,
   "milestones_enabled":true,
   "messages_enabled":true,
   "files_enabled":true,
   "time_enabled":true,
   "notes_enabled":true,
   "calendar_enabled":true,
   "label_color":"#9da2a6",
   "label_txt":"cv",
   "created_on":"2016-06-14T06:37:42.617356Z",
   "modified_on":"2016-06-14T06:37:43.336495Z",
   "resource_url":"/projects/929",
   "drive_access":null,
   "drop_box_access":null,
   "is_active":true,
   "owner_name":"adhome",
   "is_template":true,
   "creating":false,
   "tags":null
}
```

This is the project object(refer [Project Object](#project-object)).

### Create Template

```http
POST  /api/projects HTTP/1.1
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
   "name":"Test template",
   "label_txt":"Te",
   "description":"this is a test template",
   "share_data":null,
   "invite_data":[
      273,
      67,
      262
   ],
   "new_invite_data":[

   ],
   "invite_note":"I invite you to work with me on this project. Please
    feel free to share ideas, participate in discussions and give feedback.",
   "share_note":"We invite you to collaborate with us on TeamWave for this 
   project. We use TeamWave to manage tasks, share ideas and
 discuss issues.",
   "share_type":"C",
   "is_template":true
}
```

```
Sample Response
```

```json
{
   "id":950,
   "name":"Test template",
   "description":"this is a test template",
   "logo":null,
   "owner":{
      "id":1,
      "name":"Doublespring Media India Pvt ltd",
      "domain":"doublespring",
      "logo":"https://twprofile.s3.amazonaws.com/image.jpg",
      "email":"sathish@doublespring.com",
      "tenant_domain":"doublespring.com",
      "created_on":"2015-03-07",
      "default_currency":"USD",
      "default_currency_symbol":"$",
      "label_txt":null,
      "orgkey":"doublespringmediaindiapvtltd",
      "status":"paying",
      "trial_end_on":"2016-07-07"
   },
   "clients":[

   ],
   "users":[
      1
   ],
   "is_trashed":false,
   "start_date":null,
   "end_date":null,
   "budget":0.0,
   "privacy_enabled":false,
   "permissions":{
      "all_permission":true
   },
   "last_updated":"2016-07-26T07:28:08.717738Z",
   "tasks_enabled":true,
   "created_by":1,
   "milestones_enabled":true,
   "messages_enabled":true,
   "files_enabled":true,
   "time_enabled":true,
   "notes_enabled":true,
   "calendar_enabled":true,
   "label_color":"#9da2a6",
   "label_txt":"Te",
   "created_on":"2016-07-26T07:28:07.872298Z",
   "modified_on":"2016-07-26T07:28:08.717710Z",
   "resource_url":"/projects
/950",
   "drive_access":null,
   "drop_box_access":null,
   "is_active":true,
   "owner_name":"Doublespring Media India
 Pvt ltd",
   "is_template":true,
   "creating":false,
   "tags":null
}
```

<aside>POST   api/projects</aside>

### Update Template

```http
PATCH  /api/projects/{project_id} HTTP/1.1
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
   "label_txt":"Te",
   "label_color":"#9da2a6",
   "description":"this is a test template and this the updated
 template",
   "name":"Test template Updated",
   "logo":null
}
```

```
Sample Response
```

```json
{
   "id":950,
   "name":"Test template Updated",
   "description":"this is a test template and this the updated
 template",
   "logo":null,
   "owner":{
      "id":1,
      "name":"Doublespring Media India Pvt ltd",
      "domain":"doublespring",
      "logo":"https://twprofile.s3.amazonaws.com/image.jpg",
      "email":"sathish@doublespring.com",
      "tenant_domain":"doublespring.com",
      "created_on":"2015-03-07",
      "default_currency":"USD",
      "default_currency_symbol":"$",
      "label_txt":null,
      "orgkey":"doublespringmediaindiapvtltd",
      "status":"paying",
      "trial_end_on":"2016-07-07"
   },
   "clients":[

   ],
   "users":[
      262,
      273,
      67,
      1
   ],
   "is_trashed":false,
   "start_date":null,
   "end_date":null,
   "budget":0.0,
   "privacy_enabled":false,
   "permissions":{
      "all_permission":true
   },
   "last_updated":"2016-07-26T07:32:33.177241Z",
   "tasks_enabled":true,
   "created_by":1,
   "milestones_enabled":true,
   "messages_enabled":true,
   "files_enabled":true,
   "time_enabled":true,
   "notes_enabled":true,
   "calendar_enabled":true,
   "label_color":"#9da2a6",
   "label_txt":"Te",
   "created_on":"2016-07-26T07:28:07.872298Z",
   "modified_on":"2016-07-26T07:32:33.177220Z",
   "resource_url":"/projects/950",
   "drive_access":null,
   "drop_box_access":null,
   "is_active":true,
   "owner_name":"Doublespring Media India Pvt ltd",
   "is_template":true,
   "creating":false,
   "tags":null
}
```
<aside>PATCH  /api/projects/{project_id}</aside>

### Delete Template

```http
PATCH  /api/projects/{project_id} HTTP/1.1
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
  "is_trashed":true
}
```

<aside>PATCH  /api/projects/{project_id}</aside>

