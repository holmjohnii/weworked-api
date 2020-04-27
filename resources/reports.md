
# Reports
The reports resource allows you to retrieve specific reports.

## Endpoints
* [Retrieve summary by person and task report](#retrieve-summary-by-person-and-task-report)
* [Retrieve detailed line items with comments report](#retrieve-detailed-line-items-with-comments-report)

## Retrieve summary by person and task report
Retrieves the summary by person and task report.

`GET /v1/timesheets/reports/summary`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/reports/summary?fromdate=501&todate=501&projects=04/05/2020&showzeros=501&taskstatus=501&timestatus=501&users=501"`

### Parameters
* `fromdate` - The date of the start of the reporting period. Format is yyyy-mm-dd.
* `todate` - The date of the end of the reporting period. Format is yyyy-mm-dd.
* `projects` - The projects to include in the report. Options: all, allactive, alldisabled, project id, or comma-delimited list of project ids.
* `showzeros` - Flag indicating if results with zero hours should be returned. 1 = yes, 0 = no
* `taskstatus` - The status of tasks to include in the report. Options: all, billable, or nonbillable.
* `timestatus` - The status of the time entries to include in the report. Options: all, approved, or notapproved. 
* `users` - The unique identifiers of the users to include in the report. A single user id or a comma-delimited list of user ids.

### Returns
Returns a 

-------------

## Retrieve a weekly timesheet
Returns a full week (7 days) of timesheet data.

`GET /v1/timesheets/weekly`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/weekly?userid=501&date=04/03/2020"`

### Parameters
* `userid` - The unique identifier for the user.
* `date` - The date of the timesheet to return.

### Returns
Returns an array of timesheet objects for a specific week.

-------------

### The timesheet week object attributes:

| Attribute  | Description   |
| ---------- | ------------- |
| startDate   | The first day of the timesheet's week.  |
| endDate       | The last day of the timesheet's week.  |
| totalHours    | The total hours entered for the week on the timesheet. |
| status       | The overall status of the week's timesheet. |
| days      | An array of timesheet day objects.  |
| comments        | An array of the timesheet's weekly comments.  |

### The timesheet day object attributes:

| Attribute  | Description   |
| ---------- | ------------- |
| specificDate   | The date of a particular day on the timesheet.  |
| totalHours       | The total hours for a particular day on the timesheet.  |
| status       | The status of a particular day on the timesheet.  |
| tasks      | An array of timesheet task objects associated to a particular day on the timesheet.  |
| clockInOut        | An array of clock objects associated to a particular day on the timesheet.  |

## The timesheet task object attributes:
| Attribute  | Description   |
| ---------- | ------------- |
| hrsWorkedId    | The unique identifier of the timesheet entry.  |
| specificDate   | The date associated with the timesheet entry.  |
| projectName  | The name of the project associated with the timesheet entry.  |
| projectTaskId    | The unique identifier of the task associated with the timesheet entry. |
| longDesc    | The name of the task associated with the timesheet entry. |
| shortDesc    | The name of the task code associated with the timesheet entry. |
| hours    | The hours associated with the timesheet entry. |
| comment    | The comment associated with the timesheet entry. |
| isApproved    | Flag indicating if the timesheet entry was approved. 1 = approved, 0 = not approved |

## The timesheet clock object attributes:
| Attribute  | Description   |
| ---------- | ------------- |
| clockInOutId    | The unique identifier of the clock in and out activity. |
| specificDate   | The date of a particular day on the timesheet. |
| projectName  | The name of the project associated with the clock's activity. |
| longDesc    | The name of the task associated with the clock's activity. |
| shortDesc    | The name of the task code associated with the clock's activity. |
| projectTaskId    | The unique identifier of the task associated with the clock's activity. |
| clockIn    | The clock in time stamp for the clock's activity. |
| clockOut    | The clock out time stamp for the clock's activity. |
| clockInFormatted    | The clock in time stamp for the clock's activity formatted based on the user's preference. |
| clockOutFormatted    | The clock out time stamp for the clock's activity formatted based on the user's preference. |
| sumHours    | The total hours for the clock in and out period. |

-------------

##### Example JSON Response
```SAMPLE RESPONSE
WILL
GO HERE```

