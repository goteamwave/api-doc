## Projects

### Project Object

```
Sample Object 
```

```json
{
   "id":280,
   "name":"Explore teamwave",
   "description":"This template will give you to create sample project",
   "logo":"https://twprofile.s3.amazonaws.com/image.jpg",
   "owner":{
      "id":2,
      "name":"DoubleSpring",
      "domain":"doublespring",
      "logo":null,
      "email":"shuhaib@doublespring.com",
      "tenant_domain":"doublespring.com",
      "created_on":"2015-06-04",
      "default_currency":"USD",
      "default_currency_symbol":"$",
      "label_txt":null,
      "orgkey":"doublespring",
      "status":"paying",
      "trial_end_on":"2016-07-07"
   },
   "clients":[

   ],
   "users":[
      537,
      3300,
      3692,
      3858,
      3633,
      491,
      493,
      58,
      4,
      8
   ],
   "is_trashed":false,
   "start_date":null,
   "end_date":null,
   "budget":0.0,
   "privacy_enabled":false,
   "permissions":{
      "can_add_messages":true,
      "can_delete_messages":true,
      "can_add_tasks":true,
      "can_delete_tasks":true,
      "can_add_milestones":true,
      "can_delete_milestones":true,
      "can_add_timelogs":true,
      "can_delete_timelogs":true,
      "can_add_files":true,
      "can_delete_files":true,
      "can_add_notebooks":true,
      "can_delete_notebooks":true,
      "can_add_events":true,
      "can_delete_events":true,
      "project":280,
      "is_active":true,
      "calendar_enabled":true,
      "messages_enabled":true,
      "tasks_enabled":true,
      "notes_enabled":true,
      "milestones_enabled":true,
      "files_enabled":true,
      "time_enabled":true
   },
   "last_updated":"2016-07-22T09:36:11.442229Z",
   "tasks_enabled":true,
   "created_by":8,
   "milestones_enabled":true,
   "messages_enabled":true,
   "files_enabled":true,
   "time_enabled":true,
   "notes_enabled":true,
   "calendar_enabled":true,
   "label_color":null,
   "label_txt":"Ex",
   "created_on":"2015-10-15T07:49:41.957253Z",
   "modified_on":"2015-10-15T07:49:43.119392Z",
   "resource_url":"/projects/280",
   "drive_access":null,
   "drop_box_access":null,
   "is_active":true,
   "owner_name":"DoubleSpring",
   "is_template":false,
   "creating":false,
   "tags":null
}
```


### Create Project

```http
POST  api/projects HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

 ```json
{
	"name": "Explore teamwave",
	"description": "Unified Platform for Collaboration, Sales, 
	Marketing & Support",
	"logo": "https://twprofile.s3.amazonaws.com/image.jpg",
	"Invite_data": [11],
	"Invite_note": "I invite you to work with me on this project. 
	Please feel free to share ideas, participate in discussions and give feedback. ",
	"label_txt": "Ex",
	"new_invite_data": [ ],
	"share_data": null,
	"share_note": "We invite you to collaborate with us on TeamWave 
	for this project. We use TeamWave to manage tasks, share ideas and discuss issues.",
	"share_type": "c"
 }
```

<aside>POST  api/projects</aside>

Attribute | Description
----------| ------------
name (*string*)| Name of the project
description (*string*)| Description of the project
logo (*string*)| Logo url of the project
Invite_data (*string*)| List of user who already exists in the organization
Invite_note (*string*)| Invite message to be send to the invited user’s email 
label_txt (*string*)| Label text of the project
new_invite_data (*string*)| New email ids to be invited to the project
share_data (*string*)| client’s email id . eg.,john@casio.com
share_note (*string*)| shared message to be send to the client’s email 
share_type (*string*)| (*(*'C', 'Client'*), (*'V', 'Vendor'*), (*'O', 'Other'*)*)



### List all Projects

```http
GET  api/projects HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```


```json
[
   {
      "id":280,
      "name":"Explore teamwave",
      "description":"This template will give you to create sample project",
      "logo":"https://twprofile.s3.amazonaws.com/image.jpg",
      "label_color":null,
      "tags":null,
      "owner_id":2,
      "label_txt":"Ex",
      "resource_url":"/projects/280",
      "last_updated":"2016-07-22T09:36:11.442229Z",
      "is_active":true,
      "owner_name":"DoubleSpring",
      "creating":false
   },
   {
      "id":253,
      "name":"TeamWave",
      "description":"Unified Platform for Collaboration, Sales, Marketing & Support",
      "logo":"https://twprofile.s3.amazonaws.com/image.jpg",
      "label_color":"#9da2a6",
      "tags":{
         "28":{
            "color":"label-color-6",
            "tag":"TeamWave"
         }
      },
      "owner_id":2,
      "label_txt":"Te",
      "resource_url":"/projects/253",
      "last_updated":"2016-07-22T08:09:24.534065Z",
      "is_active":true,
      "owner_name":"DoubleSpring",
      "creating":false
   }
]
```

<aside>GET   api/projects</aside>

Attribute | Description
----------| -------------
Id (*integer*)| Identification number of the project
name (*string*)| Name of the project
description (*string*)| Description of the project
logo (*uel string*)| Logo of the project
label_txt (*string*)| Label text of the project
owner_id | owner of the project 
resource_url (*url string*)| project access url 
last_updated (*date string*)| Last updated time of the project 
owner_name (*string*)| Project’s organization Name
creating (*boolean*)| status whether the project is still creating by the celery or not. If it is still creating , the status is True else false
