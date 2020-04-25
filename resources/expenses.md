
# Expenses
The expense resource allows you to retrieve individual expenses as well as a list of all expenses on your account.

## Endpoints
* [Retrieve an expense](#retrieve-an-expense)
* [List all expenses](#list-all-expenses)

## Retrieve an expense
Retrieves the details of an existing expense. Simply provide the unique expense id.

`GET /v1/expenses/:id`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/expenses/4203"`

### Parameters
No parameters

### Returns
Returns an expense object if a valid identifier was provided. 

-------------

## List all expenses
Returns a list of your expenses in alphabetical order.

`GET /v1/expenses`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/expenses"`

### Parameters
* status - A filter on the list based on the name of the expense's status. Expense statuses are all, pending, approved, and invoiced.

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

