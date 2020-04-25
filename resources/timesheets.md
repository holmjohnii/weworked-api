
# Timesheets
The timesheet resource allows you to retrieve a daily timesheet and a weekly timesheet for a user on your account.

## Endpoints
* [Retrieve a daily timesheet](#retrieve-a-daily-timesheet)
* [Retrieve a weekly timesheet](#retrieve-a-weekly-timesheet)

## Retrieve a daily timesheet
Retrieves the details of a daily timesheet. 

`GET /v1/timesheets/daily`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/timesheets/daily"`

### Parameters
* userid - The unique identifier for the user.
* date - The date of the timesheet to return.

### Returns
Returns a week of timesheet objects.

-------------

## Retrieve a weekly timesheet
Returns a list of your expenses in alphabetical order.

`GET /v1/timesheets/weekly`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/expenses"`

### Parameters
* userid - The unique identifier for the user.
* date - The date of the timesheet to return.

### Returns
Returns an array of expense objects.

-------------

### The expense object attributes:

| Attribute  | Description   |
| ---------- | ------------- |
| expensesId   | Unique identifier for an expense.  |
| userId       | Unique identifier of the owner of the expense.  |
| expenseDate    | The date of the expense. |
| projectId       | The unique identifer of the project associated with the expense.  |
| projectName      | The name of the project associated with the expense.  |
| expenseCategoryId        | The unique identifer of the category associated with the expense.  |
| expenseCategoryName    | The name of the expense category associated with the expenese.  |
| receiptURL   | The URL of receipt image.  |
| amount  | The amount of the expense.  |
| isBillable    | Flag indicating if the expense is billable. 1 = billable, 0 = not billable |
| statusId    | The unique identifier of the status of the expense. |
| statusName    | The name of the status of the expense. |
| notes    | The notes associated with the expense. |

-------------

##### Example JSON Response
```SAMPLE RESPONSE
WILL
GO HERE```
