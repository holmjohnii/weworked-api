
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

### Example JSON Response
```json
  {
      "expenseId": "57873",
      "userId": "70240",
      "expenseDate": "2019-06-19",
      "projectId": "121",
      "projectName": "Salon Rebuild",
      "expenseCategoryId": "131069",
      "expenseCategoryName": "Meals",
      "receiptURL": "211yo4rq_app.jpg",
      "amount": "50.00",
      "isBillable": "1",
      "statusId": "1",
      "statusName": "Pending",
      "notes": ""
  }
```
-------------

## List all expenses
Returns a list of your expenses in alphabetical order.

`GET /v1/expenses`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/expenses"`

### Parameters
##### * = Required
* `* status` - A filter on the list based on the name of the expense's status. Expense statuses are all, pending, approved, and invoiced.

### Returns
Returns an array of expense objects.

-------------

### Example JSON Response
```json
  [
    {
        "expenseId": "57873",
        "userId": "70240",
        "expenseDate": "2019-06-19",
        "projectId": "121",
        "projectName": "Salon Rebuild",
        "expenseCategoryId": "131069",
        "expenseCategoryName": "Meals",
        "receiptURL": "211yo4rq_app.jpg",
        "amount": "50.00",
        "isBillable": "1",
        "statusId": "1",
        "statusName": "Pending",
        "notes": ""
    },
    {
        "expenseId": "57823",
        "userId": "70240",
        "expenseDate": "2019-06-20",
        "projectId": "123",
        "projectName": "Chemical Site",
        "expenseCategoryId": "131070",
        "expenseCategoryName": "Travel",
        "receiptURL": "250yo4rq_app.jpg",
        "amount": "350.00",
        "isBillable": "0",
        "statusId": "1",
        "statusName": "Approved",
        "notes": "Flight to FL"
    }
]
```
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

