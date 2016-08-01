## Time Off Policy


### Time off Policy Object

```http
GET /api/hrm/organization/settings/timeoff-policy/{timeoff_policy_id} HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

```json
{
   "id":51,
   "name":"Sick leave policy",
   "policy_effective_date":"2016-03-01",
   "total_timeoff":21,
   "schedule":51,
   "timeoff_interval":1,
   "is_public":true,
   "timeoff_type":"D",
   "timeoff_disply_type":"D",
   "day_hours":8,
   "policy_renew_type":"YF",
   "total_employees":10,
   "modified_on":"2016-06-10T11:10:53.824171Z",
   "is_active":false,
   "is_default":false,
   "assigned_users":[
      {
         "id":19,
         "label_txt":"rt",
         "image":null,
         "full_name":"rajmohan",
         "email":"rajmohantestmail@gmail.com",
         "upcoming_birthday":null
      },
      {
         "id":74,
         "label_txt":"Ac",
         "image":null,
         "full_name":"Aravind cse",
         "email":"arvindcse2014@gmail.com",
         "upcoming_birthday":null
      },
      {
         "id":76,
         "label_txt":"GY",
         "image":null,
         "full_name":"Geo Yahoo",
         "email":"geojacobm6@yahoo.com",
         "upcoming_birthday":null
      },
      {
         "id":72,
         "label_txt":"ym",
         "image":null,
         "full_name":"yolanda messina",
         "email":"yolandamessina364@gmail.com",
         "upcoming_birthday":null
      },
      {
         "id":201,
         "label_txt":"GJ",
         "image":null,
         "full_name":"Geo Jacob",
         "email":"geo.jacob11@adhome.com",
         "upcoming_birthday":null
      },
      {
         "id":1,
         "label_txt":"SV",
         "image":"https://twprofile.s3.amazonaws.com/usersuser-8011f79c-007c-4943-a968-1d13dd13b1d9-image.jpg",
         "full_name":"Sathish Venkat",
         "email":"sathish@adhome.com",
         "upcoming_birthday":null
      }
   ]
}
```

<aside>GET /api/hrm/organization/settings/timeoff-policy/{timeoff_policy_id} </aside>

Attribute | Description 
--------- | ----------- 
id (*integer*)| ID of the policy
name (*string*)| name of the policy
policy_effective_date (*string*)|  policy effective-from date
total_timeoff (*integer*)| total number of timeoff
schedule (*integer*)| schedule ID
timeoff_interval (*integer*)| days after which new employee can apply for timeoff
timeoff_type (*string*)| timeoff displayed in days ('D') and displayed in hours ('H')
timeoff_display_type (*string*)| timeoff displayed in days ('D') and displayed in hours ('H')
day_hours (*integer*)| hours of work per day
policy_renew_type (*string*)| Policy renewal type- first of every year ('YF') or half year ('YH')
total_employees (*integer*)| total number of employees
modified_on (*string*)| date of modification
is_active (*boolean*)| is the policy active
is_default (*boolean*)| is the policy default for the organization
[assigned_users](#assigned-users-object) (*array of objects*)| assigned user details

#### Assigned Users Object

Attribute | Description
----------| -----------
id (*integer*)| ID for the user
label_txt (*string*)| label text for avatar
image (*string*)| image url for the profile picture
full_name (*string*)| full name of the user
email (*string*)| email ID
upcoming_birthday (*string*)| Next birthday of this user

<!-- 
Attribute | Description 
--------- | ----------- 
used_timeoff (*integer*) | Number of used timeoff days
available_timeoff (*integer*) | Number of available timeoff days
policy_status (*boolean*)| Policy active or not
[policy_details](#policy-details-object) (*object*) | Details about the policy
policy_emp_timeoff (*integer*) | total number of timeoff days
policy (*boolean*) | is policy is activated for the specific employee
pending_timeoff (*integer*)| Number of timeoff days left
approved_timeoff (*integer*)| Number of timeoff days approved
id | ID of the Timeoff policy


#### Policy Details Object

Attribute | Description 
--------- | ----------- 
[working_hours](#working-hours-object) (*object*)| details about the working hours
total_timeoff (*integer*)| total number of timeoff days
name (*string*) | name of the policy
policy_renew_type (*string*)| Policy renewal type- first of every year or half year
renew_date (*string*)| next renewal date
carry_over (*boolean*)| is timeoff balance can be carried over to next year
id (*integer*) | ID of the timeoff policy
timeoff_interval (*integer*) | 

#### Working Hours Object

Attribute | Description 
--------- | ----------- 
id (*integer*) | id of the object
created_on (*datefield*) | working hours creation date
modified_on | date on which modified the working hours
notes | description of the working hours
mon_start (*string*)| work start time on monday
mon_end (*string*)| work end time on monday
tue_start (*string*)| work start time on tuesday
tue_end (*string*)| work end time on tuesday 
wed_start (*string*)| work start time on wednesday
wed_end (*string*)| work end time on wednesday
thu_start (*string*)| work start time on thursday
thu_end (*string*)| work end time on thursday 
fri_start (*string*)| work start time on friday
fri_end (*string*)| work end time on friday
sat_start (*string*)| work start time on saturday
sat_end (*string*)| work end time on saturday
sun_start (*string*)| work start time on sunday
sun_end (*string*)| work end time on sunday
status (*string*)|
created_by (*integer*)| ID of user who created the working hours
modified_by (*integer*)| ID of user who modified the working hours
 -->
### Create Time off Policy

```http
POST /api/hrm/organization/settings/timeoff-policy HTTP/1.1
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
   "name":"Test Policy DS",
   "total_timeoff":15,
   "policy_effective_date":"2016-07-13",
   "policy_renew_type":"YF",
   "day_hours":9,
   "timeoff_interval":20
}
```

```
Sample Response
```

```json
{
   "id":76,
   "name":"Test Policy DS",
   "policy_effective_date":"2016-07-13",
   "total_timeoff":15,
   "schedule":76,
   "timeoff_interval":20,
   "is_public":true,
   "timeoff_type":"D",
   "timeoff_disply_type":"D",
   "day_hours":9,
   "policy_renew_type":"YF",
   "total_employees":0,
   "modified_on":"2016-07-12T07:58:46.687121Z",
   "is_active":true,
   "is_default":false,
   "assigned_users":[

   ]
}
```

<aside>POST /api/hrm/people/{id}/timeoff</aside>

Create new Time off Policy.

Attribute | Description 
--------- | ----------- 
name (*string*)| Name of the Time off policy
total_timeoff (*integer*)| total number of timeoff
policy_effective_date (*date string*)| policy effective from date
policy_renew_type (*string*)| time of renewal of policy
day_hours (*string*)| total work hours per day 
timeoff_interval (*integer*)| number of days after which new hire can apply for leave

#### Returns 

If the call succeeds, the [timeoff policy](#time-off-policy-object) object is returned with all the information about the timeoff policy.

### Update Time Off Policy

```http
PATCH /api/hrm/organization/settings/timeoff-policy/{timeoff_policy_id} HTTP/1.1
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
   "id":71,
   "name":"test",
   "policy_effective_date":"2016-05-31",
   "total_timeoff":30,
   "schedule":71,
   "timeoff_interval":15,
   "is_public":true,
   "timeoff_type":"D",
   "timeoff_disply_type":"D",
   "day_hours":9,
   "policy_renew_type":"YF",
   "total_employees":3,
   "modified_on":"2016-06-02T12:32:24.887566Z",
   "is_active":false,
   "is_default":false,
   "assigned_users":[
      {
         "id":202,
         "label_txt":"GT",
         "image":null,
         "full_name":"Geo Test 12",
         "email":"geo.jacob12@adhome.com",
         "upcoming_birthday":null
      },
      {
         "id":76,
         "label_txt":"GY",
         "image":null,
         "full_name":"Geo Yahoo",
         "email":"geojacobm6@yahoo.com",
         "upcoming_birthday":null
      },
      {
         "id":77,
         "label_txt":"Go",
         "image":null,
         "full_name":"Geo outlook",
         "email":"geojacobm6@outlook.com",
         "upcoming_birthday":null
      }
   ]
}
```

<aside>PATCH /api/hrm/organization/settings/timeoff-policy/{timeoff_policy_id}</aside>

``` 
Sample Response
```

```json
{
   "id":71,
   "name":"test",
   "policy_effective_date":"2016-05-31",
   "total_timeoff":30,
   "schedule":71,
   "timeoff_interval":15,
   "is_public":true,
   "timeoff_type":"D",
   "timeoff_disply_type":"D",
   "day_hours":9,
   "policy_renew_type":"YF",
   "total_employees":3,
   "modified_on":"2016-07-25T07:04:23.225067Z",
   "is_active":false,
   "is_default":false,
   "assigned_users":[
      {
         "id":202,
         "label_txt":"GT",
         "image":null,
         "full_name":"Geo Test 12",
         "email":"geo.jacob12@adhome.com",
         "upcoming_birthday":null
      },
      {
         "id":76,
         "label_txt":"GY",
         "image":null,
         "full_name":"Geo Yahoo",
         "email":"geojacobm6@yahoo.com",
         "upcoming_birthday":null
      },
      {
         "id":77,
         "label_txt":"Go",
         "image":null,
         "full_name":"Geo outlook",
         "email":"geojacobm6@outlook.com",
         "upcoming_birthday":null
      }
   ]
}
```

#### Returns 

If the call succeeds, the [timeoff policy](#time-off-policy-object) object is returned with all the information about the updated timeoff policy.

### Delete Time Off Policy

```http
DELETE /api/hrm/organization/settings/timeoff-policy/{timeoff_policy_id} HTTP/1.1
Accept: application/json
Authorization: Token "YOUR ACCESS TOKEN"

HTTP/1.1 200 OK
Content-Type: application/json
```

<aside>DELETE api/hrm/organization/settings/timeoff-policy/{timeoff_policy_id}</aside>


