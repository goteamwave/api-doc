## Reports

### Project Report Object

```json
{
   "overview":[
      {
         "com_per":80.3661,
         "od_tasks":18,
         "name":"TeamWave",
         "t_time":{
            "mns":0,
            "hrs":19
         },
         "od_per":2.995,
         "billable":{
            "mns":0,
            "hrs":2
         },
         "inp_per":16.6389,
         "inp_tasks":100,
         "non_billable":{
            "mns":0,
            "hrs":17
         },
         "owner__name":"example_domain",
         "c_tasks":483,
         "t_tasks":601,
         "id":253,
         "owner_id":2
      },
      {
         "com_per":70.5882,
         "od_tasks":0,
         "name":"Explore teamwave",
         "t_time":{
            "mns":0,
            "hrs":27
         },
         "od_per":0.0,
         "billable":{
            "mns":0,
            "hrs":10
         },
         "inp_per":29.4118,
         "inp_tasks":5,
         "non_billable":{
            "mns":0,
            "hrs":17
         },
         "owner__name":"example_domain",
         "c_tasks":12,
         "t_tasks":17,
         "id":280,
         "owner_id":2
      }
   ],
   "t_time":{
      "hours__sum":12,
      "mins__sum":0
   },
   "projects_with_unassigned_tasks":[
      {
         "tasks":29,
         "project_id":253,
         "project__name":"TeamWave"
      },
      {
         "tasks":4,
         "project_id":280,
         "project__name":"Explore teamwave"
      }
   ],
   "t_milestones":1,
   "pieChartData":{
      "od_tasks":2.91,
      "inp_tasks_count":105,
      "od_tasks_count":18,
      "inp_tasks":16.99,
      "c_tasks_count":495,
      "c_tasks":80.1
   }
}
```

Attribute | Description
----------| ------------
[overview](#overview-object) (*array of objects*) | List of all projects with its overview
[t_time](#total time object) | total time
[projects_with_unassigned_tasks](#projects_with_unassigned_tasks-object) | project list with unassigned tasks
t_milestones | total milestones
[pieChartData](#pie-chart-data-object) | pie chart data

#### Overview Object

Attribute | Description
----------| ------------
