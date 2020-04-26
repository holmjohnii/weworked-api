
# Reports
The reports resource allows you to retrieve  reports.

## Endpoints
* [Retrieve a report](#retrieve-a-report)

## Retrieve a report
Retrieves a report

`GET /v1/timesheets/reports/:reportname`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/timesheets/daily?userid=501&date=04/05/2020"`

### Parameters
* `fromdate` - The unique identifier for the user.
* `todate` - The date of the timesheet to return.
* `projects` - The date of the timesheet to return.
* `showzeros` - The date of the timesheet to return.
* `taskstatus` - The date of the timesheet to return.
* `timestatus` - The date of the timesheet to return.
* `users` - The date of the timesheet to return.

### Returns
Returns a timesheet object for a specific day.

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

