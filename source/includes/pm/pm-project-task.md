## Task 

[Task Object](#task-object) 

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

