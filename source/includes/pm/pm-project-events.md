## Events

### Event Object

```json 
{
    "id": 3633,
    "title": "Slide Presentation",
    "description": "Give a detail about upcoming projects",
    "start_dt": "2016-07-22T16:30:00Z",
    "end_dt": "2016-07-22T17:30:00Z",
    "start": "2016-07-22 16:30:00+00:00",
    "end": "2016-07-22 17:30:00+00:00",
    "all_day": false,
    "start_time": "04:30 PM",
    "end_time": "05:30 PM",
    "rule_txt": false,
    "rule_id": null,
    "end_type": "never",
    "occurrence_count": "2",
    "end_recurring_period": null,
    "is_private": false,
    "post_count": 0
}
```

Attribute | Description
----------| -----------
id (*integer*) | Identificatoin number of the Event,
title (*string*) | Title of the Event,
description (*string*) | Description given of the Event,
start_dt (*date*) | Start date of the Event,
end_dt (*date*) | End date the Event,
start (*datetime*) | Start date time of the Event,
end (*datetime*) | End date time of the Event,
all_day (*boolean*) | Status to check the event will occur all day or not,
start_timet (*datetime*) | Start time of the Event,
end_timet (*datetime*) | End time of the Event,
rule_txt (*string*) | Event repeat information,
rule_id (*string*) | Id of the repeat mode,
end_type (*string*) | end_type can be 'never','occurrence' or 'date',
occurrence_count (*integer*) | Occurrence count of the event,
end_recurring_period (*string*) |It can be null if end_type is 'never' or a paricular date if end_type is 'date,
is_private (*boolean*) | Status to check note is private or not,
post_count (*integer*) | Post count of the event

### Create Event

```http
POST api/projects/{project_id}/events HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

```json
{
 	"id":0,
 	"title":"Slide Presentation",
 	"occurrence_count":0,
 	"rule_id":0,
 	"end_type":"never",
 	"start":"2016-07-22",
 	"start_time":"10:00 PM",
 	"end_time":"11:00PM",
 	"end":"2016-07-22",
 	"all_day":false,
 	"end_recurring_period":"",
 	"repeat":false,
 	"send_email":true,
 	"description":"Give a detail about upcoming projects",
 	"emails":[1],
 	"is_repeating":false
 }
 ```

<aside>POST api/projects/{project_id}/events</aside>

### Update Event

```http
PATCH api/projects/{project_id}/events/{event_id} HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

```json
{
 	"id":13633,
 	"event":3633,
 	"all_day":true,
 	"order_no":1,
 	"title":"Slide Presentation Every day",
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
	"emails":[1],
	"is_repeating":false,
	"is_private":false,
	"start":"2016-07-22",
	"start_time":"10:00PM",
	"old_start":"2016-07-22",
	"old_start_time":"10:00 PM",
	"end":"2016-07-22",
	"end_time":"11:00 PM",
	"old_end":"2016-07-22",
	"old_end_time":"11:00 PM",
	"description":"Give a detail about upcoming projects",
	"rule_txt":false,
	"rule_id":0,
	"end_type":"never",
	"occurrence_count":0,
	"end_recurring_period":"",
	"durationEditable":false,
	"is_milestone":false,
	"post_count":0,
	"send_email":true,
	"_id":"13633",
	"_start":"2016-07-21T18:30:00.000Z",
	"_end":null,
	"allDay":true,
	"className":[],
	"repeat":false,
	"event_id":3633,
	"old_event_data":{
		"event_id":3633,
		"title":"SlidePresentation",
		"start":"2016-07-22",
		"end":"2016-07-22",
		"start_time":"10:00 PM",
		"end_time":"11:00 PM"
		}
}
```
<aside>PATCH api/projects/{project_id}/events/{event_id}</aside>

### Delete Event

```http
PATCH api/projects/{project_id}/events/{event_id} HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```


<aside>DELETE api/projects/{project_id}/events/{event_id}</aside>

