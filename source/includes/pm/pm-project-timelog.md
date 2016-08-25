## Time log

### Time log Object

```json
{
    "id": 548,
    "description": "Issues fixed and updated.",
    "project": 1190,
    "task": 5403,
    "logdate": "2016-07-22",
    "logtime": "4:30",
    "is_billable": true,
    "task_object": {  
            "taskgroup_id":919,
            "id":3208,
            "name":"social"
         },
    "log_month": "July, 2016",
    "created_on": "2016-07-22T06:27:53.602712Z",
    "created_by": {
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
            "domain": "adhome",
            "logo": "https://twprofile.s3.amazonaws.com/logo.jpeg",
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
        "image": null,
        "email": "aravind@adhome.com",
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
    "resource_url": "/projects/1190/timelogs/548",
    "modified_on": "2016-07-22T06:27:53.602749Z",
    "billed": false,
    "modified_by": null
}
```

Attribute | Description
----------| -----------
id (*integer*) | Identification number of the time log
description (*string*) | Description for the time log
project (*integer*) | Identification number of the Project
task (*integer*) | Identification number of the task for the time log
logdate (*date*)  | log date of the time log
logtime (*time*) | Total time spend for the task
is_billable (*boolean*) | Status to check time log is billable or not
[task_object](#timelog-task-object) (*object*) | Particular task object for the time log
log_month (*string*) | Month and Year on which the time log is created
created_on (*date*) | Time log created date
[created_by](#pm-user-object) (*object*) | User object who created the timelog
resource_url (*string*)  | Timelog's detail page access url
modified_on (*date*) | Date on which the time log is modified
billed (*boolean*) | Status to check time log is billed or not
[modified_by](#pm-user-object) (*object*) | user object who modified the time log

#### Timelog Task Object

Attibute | Description
---------| ------------
taskgroup_id (*integer*)| ID of the taskgroup_id
id (*integer*) | ID of the task
name (*string*)| Name of the task 


### Retrieve Time log

```
Sample Request 
```

```
GET  api/projects/825/timelogs?dateRange=This Week&dateRangeEnd=20/05/2016&dateRangeStart=25/05/2016  HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```


<aside> GET  api/projects/{project_id}/timelog </aside>

#### URL Parameters for filtering time logs:

##### Based on dates: `dateRange` , `dateRangeEnd`, `dateRangeStart`


<aside class="success">dateRange</aside>

Value | Description
------| ------------
This Week | by week
Today | for today
Yesterday | for yesterday
Last Week | for last week 
Last Month | for last month
This Month | for this month
This Quarter | for this quarter
Last Quarter | for last quarter
From Beginning | from the beginning


<aside class="success">dateRangeEnd : end date for range</aside>


<aside class="success">dateRangeStart : start date for range</aside>

##### Based on User: `user`

<aside> GET  api/projects/{project_id}/timelogs?user={user_id}</aside> 



### Create Time log

```http
POST /api/projects/{project_id}/timelogs HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

```json
{
	"description":"Issues fixed and updated.",
	"logdate":"2016-07-22",
	"logtime":"4:18",
	"task":5403,
	"is_billable":true
	}
```

<aside>POST  api/projects/{project_id}/timelogs</aside>

### Update Time log

```http
PATCH /api/projects/{project_id}/timelogs/{timelog_id} HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

```json
{
    "description":"New dependencies are added for monitoring and updated on online.",
    "logdate":"2016-07-22",
    "logtime":"5:30",
    "task":5403,
    "is_billable":true
}
```
	

<aside>PATCH  api/projects/{project_id}/timelogs/{timelog_id}</aside>

### Delete Time log

```http
DELETE api/projects/{project_id}/timelogs/{timelog_id} HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

<aside>DELETE  api/projects/{project_id}/timelogs/{timelog_id}</aside>



