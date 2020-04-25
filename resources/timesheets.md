
# Timesheets
The timesheet resource allows you to retrieve a daily timesheet and a weekly timesheet for a user on your account.

## Endpoints
* [Retrieve a daily timesheet](#retrieve-a-daily-timesheet)
* [Retrieve a weekly timesheet](#retrieve-a-weekly-timesheet)

## Retrieve a daily timesheet
Retrieves a single days timesheet. 

`GET /v1/timesheets/daily`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/timesheets/daily?userid=501&date=04/05/2020"`

### Parameters
* userid - The unique identifier for the user.
* date - The date of the timesheet to return.

### Returns
Returns a timesheet object for a specific day.

-------------

## Retrieve a weekly timesheet
Returns a full week (7 days) of timesheet data.

`GET /v1/timesheets/weekly`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/weekly?userid=501&date=04/03/2020"`

### Parameters
* userid - The unique identifier for the user.
* date - The date of the timesheet to return.

### Returns
Returns an array of timesheet objects for a specific week.

-------------

### The timesheet week object attributes:

| Attribute  | Description   |
| ---------- | ------------- |
| startDate   | Unique identifier for an expense.  |
| endDate       | Unique identifier of the owner of the expense.  |
| totalHours    | The date of the expense. |
| status       | The unique identifer of the project associated with the expense.  |
| days      | An array of timesheet day objects.  |
| comments        | The unique identifer of the category associated with the expense.  |

### The timesheet day object attributes:

| Attribute  | Description   |
| ---------- | ------------- |
| specificDate   | Unique identifier for an expense.  |
| totalHours       | Unique identifier of the owner of the expense.  |
| status       | The unique identifer of the project associated with the expense.  |
| tasks      | An array of timesheet task objects.  |
| clockInOut        | The unique identifer of the category associated with the expense.  |

## The timesheet task object attribues:
| Attribute  | Description   |
| ---------- | ------------- |
| hrsWorkedId    | The name of the expense category associated with the expenese.  |
| specificDate   | The URL of receipt image.  |
| projectName  | The amount of the expense.  |
| projectTaskId    | Flag indicating if the expense is billable. 1 = billable, 0 = not billable |
| longDesc    | The unique identifier of the status of the expense. |
| shortDesc    | The name of the status of the expense. |
| hours    | The notes associated with the expense. |
| comment    | The notes associated with the expense. |
| isApproved    | The notes associated with the expense. |

-------------

##### Example JSON Response
```SAMPLE RESPONSE
WILL
GO HERE```
