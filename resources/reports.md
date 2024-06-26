
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
* `* users` - The unique identifiers of the users to include in the report. Options: all, a single user id, or a comma-delimited list of user ids.

### Returns
Returns a summary of timesheet data by person and task.

### Example JSON Response
```json
[
    {
        "firstName": "Daniel",
        "lastName": "Scott",
        "userId": "70240",
        "internalId": "",
        "Rows": [
            {
                "project": "Tech Builder Site",
                "task": "Programming",
                "taskCode": "PROG23",
                "billable": "1",
                "invoiceMethodId": "1",
                "invoiceMethodName": "Task Rate",
                "rate": "10.00",
                "hours": "20.00",
                "total": "200.00"
            },
            {
                "project": "Tech Builder Site",
                "task": "Design",
                "taskCode": "",
                "billable": "1",
                "invoiceMethodId": "1",
                "invoiceMethodName": "Task Rate",
                "rate": "25.00",
                "hours": "12.00",
                "total": "300.00"
            }
        ]
    },
    {
        "firstName": "Lisa",
        "lastName": "Reginald",
        "userId": "2815",
        "internalId": "",
        "Rows": [
            {
                "project": "Leave",
                "task": "Annual",
                "taskCode": "",
                "billable": "0",
                "invoiceMethodId": null,
                "invoiceMethodName": null,
                "rate": 0,
                "hours": "8.00",
                "total": 0
            },
            {
                "project": "Leave",
                "task": "Personal",
                "taskCode": "",
                "billable": "0",
                "invoiceMethodId": null,
                "invoiceMethodName": null,
                "rate": 0,
                "hours": "8.00",
                "total": 0
            }
        ]
    }
]
```

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
* `* users` - The unique identifiers of the users to include in the report. Options: all, a single user id, or a comma-delimited list of user ids.

### Returns
Returns detailed line item timesheet data with comments.

-------------

#### Example JSON Response
```json
[
    {
        "userId": "70240",
        "internalId": null,
        "firstName": "Taylor",
        "lastName": "Timber",
        "date": "2019-06-17",
        "project": "Cramer Index",
        "projectId": "2344",
        "taskId": "39404",
        "task": "IND",
        "taskCode": "",
        "billable": "1",
        "hours": "6.00",
        "comments": "Reviewed the filing for the last quarter."
    },
    {
        "userId": "70233",
        "internalId": "758",
        "firstName": "Kennedy",
        "lastName": "Rolands",
        "date": "2019-06-17",
        "project": "Novavax",
        "projectId": "3434",
        "taskId": "90992",
        "task": "Standard",
        "taskCode": "",
        "billable": "1",
        "hours": "8.00",
        "comments": null
    }
]
```

