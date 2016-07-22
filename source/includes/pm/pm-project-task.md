## Task 

### Task Object

```json
{
    "name": "Important - Monitoring Third-party Services",
    "index": 0,
    "id": 5403,
    "assigned_to": {
        "id": 11,
        "first_name": "aravind",
        "last_name": "dsSpring",
        "label_txt": "ad",
        "is_crm_enabled": false,
        "is_crm_admin": false,
        "is_pm_enabled": true,
        "is_hrm_admin": false,
        "corp_email": true,
        "organization": {
            "id": 1,
            "name": "Dsqqqqqqq ds 2123",
            "domain": "doublespring",
            "logo": "https://twprofile.s3.amazonaws.com/logos/organization-1ae4b5e4-457f-4b0a-aad6-370b542fe1ce-image.jpeg",
            "email": "geo.jacob@doublespring.com",
            "tenant_domain": "doublespring.com",
            "created_on": "2015-03-10",
            "default_currency": "USD",
            "default_currency_symbol": "$",
            "label_txt": null,
            "orgkey": "Dsq",
            "status": "paying",
            "trial_end_on": "2016-07-07"
        },
        "image": null,
        "email": "aravind@doublespring.com",
        "full_name": "aravind dsSpring",
        "is_owner": false,
        "is_admin": false,
        "is_active": true,
        "last_login": "2016-07-22T06:26:52.720693Z",
        "job_title": "Developer",
        "time_zone": "Asia/Kolkata",
        "uuid": "340aec4d05984fa880a915c6c72ea794",
        "country": null,
        "is_noticeboard_enabled": false,
        "is_user_directory_enabled": true
    },
    "due_date": "2016-07-27",
    "completed_by": null,
    "modified_by": null,
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
            "domain": "doublespring",
            "logo": "https://twprofile.s3.amazonaws.com/logos/organization-1ae4b5e4-457f-4b0a-aad6-370b542fe1ce-image.jpeg",
            "email": "geo.jacob@doublespring.com",
            "tenant_domain": "doublespring.com",
            "created_on": "2015-03-10",
            "default_currency": "USD",
            "default_currency_symbol": "$",
            "label_txt": null,
            "orgkey": "Dsq",
            "status": "paying",
            "trial_end_on": "2016-07-07"
        },
        "image": "https://twprofile.s3.amazonaws.com/users/user-61ddc395-8145-493c-a72f-df70ac205783-image.jpg",
        "email": "sathish@doublespring.com",
        "full_name": "sathish ",
        "is_owner": true,
        "is_admin": true,
        "is_active": true,
        "last_login": "2016-07-22T06:28:01.261390Z",
        "job_title": "Developer",
        "time_zone": "Asia/Kolkata",
        "uuid": "7452387e2f1d4eda952cb12ffbefb6b1",
        "country": null,
        "is_noticeboard_enabled": true,
        "is_user_directory_enabled": true
    },
    "estimate": 0,
    "completed_date": null,
    "is_completed": false,
    "timelog": "4:30",
    "created_on": "2016-07-22T06:24:35.156302Z",
    "modified_on": "2016-07-22T06:24:35.660229Z",
    "taskgroup_is_private": false,
    "project_name": "Pro_11",
    "project_id": 1190,
    "tags": null,
    "taskgroup_name": "Customer Issues",
    "taskgroup_id": 1569,
    "taskgroup_is_trashed": false,
    "is_trashed": false,
    "comment_count": 0,
    "resource_url": "/projects/1190/taskgroups/1569/tasks/5403",
    "tmp_due_date": null,
    "attachments": [],
    "attachments_detail": []
}
```

Attribute | Description 
----------| ------------
name (*string*) | Name of the Task
index (*integer*) | index no of the Task
id (*integer*) | Identification number of the Task
[assigned_to](#pm-user-object) (*object*)| assign a user for this task to complete
due_date (*data*) | duedate for the particular task
[completed_by](#pm-user-object) (*object*) | user who completed the task
[modified_by](#pm-user-object) (*object*) | user who modified the task
[created_by](#pm-user-object) (*object*) | user who created the task
estimate (*integer*) | estimate cost for the task
completed_date (*date*) | completed date of the task
is_completed (*boolean*) | Status to identify task is completed or not
timelog (*date*) | time log for the particular task
created_on (*date*) | task created date 
modified_on (*date*) | date on which the task is modified
taskgroup_is_private (*boolean*) | Status to check taskgroup is private or not
project_name (*string*) | Name of the project
project_id (*integer*) | Id of the project
tags (*array*) | Tags belongs to the task
taskgroup_name (*string*) | Name of the taskgroup
taskgroup_id (*integer*) | Id of the taskgroup
taskgroup_is_trashed (*boolean*) | Status to check taskgroup is trashed or not
is_trashed (*boolean*) | Status to check task is trashed or not
comment_count (*integer*) | No of comments for the task
resource_url (*string*)  | Task detail page access url
tmp_due_date (*date*) | Temporary due date for the task
attachments (*array*) | Attachments object id like fileimage belongs to the task
[attachments_detail](#attachments-detail) (*array of object*)| Details of the attachments belonging to the task

#### Attachments Detail

Attribute | Description 
----------| ------------
id (*integer*) | Identification number of the attachment
title (*string*) | Name of the attachment
attachment (*string*) | URL of the attachment
object_id (*integer*) | id of the task
is_drivebox (*boolean*) | Status to check attachment is from drivebox(google drive or drop box) or not
is_trashed (*boolean*) | Status to check attachment is trashed or not
[modified_by](#pm-user-object) (*object*) | user object who modified the attachment
project (*integer*) | Id of the project
size (*string*) | Size of the attachment
for_comment (*boolean*) | Status to check attachment is for comments or not
[content_object_detail](#content-object-detail) (*object*) | Detail of the content_object
[created_by](#pm-user-object) (*object*) | user who created the attachment
created_on (*date*) | date on which the attachment is created
is_live (*boolean*) | Status to check attachment is live or not
thumbnail (*string*) | URL of the attachment's thumbnail
comment_count(*inr*) | Comment count of the attachment's thumbnail
modified_on (*date*) | date on which the attachment is modified
is_shared (*boolean*) | Status to check attachment is shared or not
shared_note (*string*) |Shared note of the attachment
content_type (*string*) | Content type of the attachment. eg.task
ext (*string*) | Extension type of the attachment
resource_url (*string*)  | Attachments detail page access url
download_url  (*string*) | URL to download the attachment
is_private (*boolean*) | Status to check attachment is private or not
tags (*array*) | tags belongs to the attachment.

#### Content Object Detail

Attribute | Description 
----------| ------------
display_name (*string*) | Display name of the content object
url (*string*) | URL to access the task detail page
group_name (*string*) | Task group name
group_url (*string*) | Task group's URL
group_id (*integer*) | Id of the Task group
id"(*integer*) | Id of the task.


### Create Task

```http
POST   api/projects/{project_id}/taskgroups/{task_group_id}/tasks HTTP/1.1
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
	"name":"Important - Monitoring Third-party Services",
	"taskgroup_id":901,
	"due_date":"2016-07-29",
	"assigned_to":{"id":273},
	"attachment":[3781]
}
```
<aside>POST  api/projects/{project_id}/taskgroups/{task_group_id}/tasks</aside>

### Retrieve Task

```http
GET  api/projects/{project_id}/taskgroups/{task_group_id}/tasks/{task_id} HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

<aside>GET   api/projects/{project_id}/taskgroups/{task_group_id}/tasks/{task_id}</aside>

#### Returns 

If the call succeeds, the [task object](#task-object) will be returned.


### Update Task

```http
PATCH  api/projects/{project_id}/taskgroups/{task_group_id}/tasks/{task_id} HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```


```json
{
	"name":"Important - Monitoring Third-party Services",
	"assigned_to":
		{
			"id":273
		},
	"due_date":"2016-07-29",
	"attachment":[3781],
	"estimate":0
}
```
<aside>PATCH  api/projects/{project_id}/taskgroups/{task_group_id}/tasks/{task_id}</aside>

#### Returns

If call succeeds, the [task object](#task-object) will be returned.

### Delete Task

```http
DELETE  api/projects/{project_id}/taskgroups/{task_group_id}/tasks/{task_id} HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```
<aside>DELETE  api/projects/{project_id}/taskgroups/{task_group_id}/tasks/{task_id}</aside>

