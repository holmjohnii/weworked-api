
# Reports
The reports resource allows you to retrieve specific reports.

## Endpoints
* [Retrieve summary by person and task report](#retrieve-summary-by-person-and-task-report)
* [Retrieve detailed line items with comments report](#retrieve-detailed-line-items-with-comments-report)

## Retrieve summary by person and task report
Retrieves the summary by person and task report.

`GET /v1/reports/summary`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/reports/summary?fromdate=2020-01-01&todate=2020-01-31&projects=all&showzeros=1&taskstatus=all&timestatus=all&users=all"`

### Parameters
##### * = Required
* `* fromdate` - The date of the start of the reporting period. Format is yyyy-mm-dd.
* `* todate` - The date of the end of the reporting period. Format is yyyy-mm-dd.
* `* projects` - The projects to include in the report. Options: all, allactive, alldisabled, project id, or comma-delimited list of project ids.
* `* showzeros` - Flag indicating if results with zero hours should be returned. 1 = yes, 0 = no
* `* taskstatus` - The status of tasks to include in the report. Options: all, billable, or nonbillable.
* `* timestatus` - The status of the time entries to include in the report. Options: all, approved, or notapproved. 
* `* users` - The unique identifiers of the users to include in the report. A single user id or a comma-delimited list of user ids.

### Returns
Returns a summary of timesheet data by person and task.

-------------

## Retrieve detailed line items with comments report
Returns the detailed line item with comments report.

`GET /v1/reports/detailed`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/reports/detailed?fromdate=2020-01-01&todate=2020-01-31&projects=all&showzeros=1&taskstatus=all&timestatus=all&users=all"`

### Parameters
##### * = Required
* `* fromdate` - The date of the start of the reporting period. Format is yyyy-mm-dd.
* `* todate` - The date of the end of the reporting period. Format is yyyy-mm-dd.
* `* projects` - The projects to include in the report. Options: all, allactive, alldisabled, project id, or comma-delimited list of project ids.
* `* showzeros` - Flag indicating if results with zero hours should be returned. 1 = yes, 0 = no
* `* taskstatus` - The status of tasks to include in the report. Options: all, billable, or nonbillable.
* `* timestatus` - The status of the time entries to include in the report. Options: all, approved, or notapproved. 
* `* users` - The unique identifiers of the users to include in the report. A single user id or a comma-delimited list of user ids.

### Returns
Returns detailed line item timesheet data with comments.

-------------

##### Example JSON Response
```SAMPLE RESPONSE
WILL
GO HERE```

