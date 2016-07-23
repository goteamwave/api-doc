## Milestone

### Milestone Object

```json
{
    "id": 682,
    "title": "Customer issue completely fixed",
    "completed": false,
    "completed_on": null,
    "task_groups": [],
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
        "last_login": "2016-07-21T06:24:04.037715Z",
        "job_title": "Developer",
        "time_zone": "Asia/Kolkata",
        "uuid": "7452387e2f1d4eda952cb12ffbefb6b1",
        "country": null,
        "is_noticeboard_enabled": true,
        "is_user_directory_enabled": true
    },
    "post_count": 0,
    "resource_url": "/projects/1190/milestones/682",
    "modified_on": "2016-07-21T11:42:02.351870Z",
    "modified_by": null,
    "start": "2016-07-22",
    "created_on": "2016-07-21T11:42:02.199063Z",
    "assigned_to": {
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
        "last_login": "2016-07-21T06:24:04.037715Z",
        "job_title": "Developer",
        "time_zone": "Asia/Kolkata",
        "uuid": "7452387e2f1d4eda952cb12ffbefb6b1",
        "country": null,
        "is_noticeboard_enabled": true,
        "is_user_directory_enabled": true
    },
    "notify_when": "0",
    "notify_time": "06:00:00",
    "description": "fix all the issues",
    "is_trashed": false,
    "project": 1190,
    "is_private": false,
    "tmp_start": null,
    "project_name": "Pro_11"
}
```

Attribute | Description
----------| ------------
id (*integer*) | Identification number of the milestone,
title (*string*) | title given of the milestone,
completed (*boolean*) | Status to check milestone is completed or not,
completed_on (*date*) | completed date given of the milestone,
task_groups (*array*) | task groups which belongs to the milestone,
[created_by](#pm-user-object) (*object*) | User object who created the milestone,
post_count (*integer*) | post count of the milestone,
resource_url (*string*)  | Milestone's detail access url,
modified_on (*date*) | Date on which the milestone is modified,
[modified_by](#pm-user-object) (*object*) | user object who modified the milestone,
start (*date*) | Start date of the milestone,
created_on (*date*) | Date on which the milestone is created,
[assigned_to](#pm-user-object) (*object*) | User object who is assigned to the milestone to complete,
notify_when (*string*) | get a notification of the milestone on notify time,
notify_time (*time*) | notification time of the milestone,
description (*string*) | Description of the milestone,
is_trashed (*boolean*) | Status to check milestone is trashed or not,
project (*integer*) | Identification number of the project,
is_private (*boolean*) | Status to check milestone is private or not,
tmp_start (*date*) | Temporary start date of the milestone,
project_name (*string*) | name of the project,

### Create Milestone

```http
POST api/projects/{project_id}/milestones HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

```json
{
	"id":0,
	"title":"Customer issue completely fixed",
	"is_milestone":true,
	"notify_when":0,
	"notify_time":"06:00:00",
	"start":"2016-08-10",
	"assigned_to":
		{
			"id":1
		},
	"description":"fix all the issues",
	"object_id":"1190",
	"is_private":false
}
```

<aside>POST api/projects/{project_id}/milestones</aside>

### Update Milestone

```http
PATCH api/projects/{project_id}/milestones/{milestone_id} HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

```json
{
	"id":683,
	"title":"Customer issue completely fixed",
	"completed":false,
	"completed_on":null,
	"task_groups":[],
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
        "last_login": "2016-07-21T06:24:04.037715Z",
        "job_title": "Developer",
        "time_zone": "Asia/Kolkata",
        "uuid": "7452387e2f1d4eda952cb12ffbefb6b1",
        "country": null,
        "is_noticeboard_enabled": true,
        "is_user_directory_enabled": true
    },
	"post_count":0,
	"resource_url":"/projects/1190/milestones/683",
	"modified_on":"2016-07-21T11:59:54.589285Z",
	"modified_by":null,
	"start":"2016-08-11",
	"created_on":"2016-07-21T11:59:54.589259Z",
	"assigned_to": {
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
        "last_login": "2016-07-21T06:24:04.037715Z",
        "job_title": "Developer",
        "time_zone": "Asia/Kolkata",
        "uuid": "7452387e2f1d4eda952cb12ffbefb6b1",
        "country": null,
        "is_noticeboard_enabled": true,
        "is_user_directory_enabled": true
    },			
	"notify_when":"0",
	"notify_time":"06:00:00",
	"description":"fix all the issues",
	"is_trashed":false,
	"project":1190,
	"is_private":true,
	"tmp_start":null,
	"project_name":"Pro_11",
	"action_type":"added",
	"is_milestone":true,
	"_id":"683",
	"_start":"2016-08-09T18:30:00.000Z",
	"end":null,
	"_end":null,
	"allDay":true,
	"className":[]
}
```
<aside>PATCH api/projects/{project_id}/milestones/{milestone_id}</aside>


### Complete the Milestone

```http
PATCH api/projects/{project_id}/milestones/{milestone_id}/complete HTTP/1.1
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
    "completed":"success"
}
```

<aside>PATCH  api/projects/{project_id}/milestones/{milestone_id}/complete</aside>

### Delete Milestone

```http
PATCH api/projects/{project_id}/milestones/{milestone_id}/trash HTTP/1.1
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

<aside>PATCH  api/projects/{project_id}/milestones/{milestone_id}/trash</aside>


