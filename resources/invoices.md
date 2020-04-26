
# Invoices
The invoice resource allows you to retrieve individual invoices as well as a list of all your invoices.

## Endpoints
* [Retrieve an invoice](#retrieve-an-invoice)
* [List all invoices](#list-all-invoices)

## Retrieve an invoice
Retrieves the details of an existing project. Simply provide the unique project id.

`GET /v1/invoices/:id`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/invoices/9802"`

### Parameters
No parameters

### Returns
Returns an invoice object if a valid identifier was provided. 

-------------

## List all invoices
Returns a list of your invoices in order by the invoice date.

`GET /v1/invoices`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/invoices"`

### Parameters
No parameters

### Returns
Returns an array of invoice objects.

-------------

### The invoice object attributes:

| Attribute  | Description   |
| ---------- | ------------- |
| invoiceId   | Unique identifier for the client associated with the project.  |
| companyId       | The name of the client associated with the project.  |
| invoiceDate    | The unique identifier of the project. |
| invoiceNum       | The name of the project.  |
| dueDate      | The project code.  |
| billTo        | The overview description of the project.  |
| clientId    | The time stamp when the project was created.  |
| paymentTerms   | Flag indicating if the project is billable. 1 = billable, 0 = non-billable  |
| currencySymbol  | The budgeted cost for the project.  |
| tax    | The budgeted hours for the project. |
| discount    | The invoice method unique identifier set for the project.  |
| isActive    | The name of the invoice method set for the project.  |
| isPaid    | The project's billable rate.  |
| notes    | Flag indicating if the project is used to track leave. 1 = yes, 0 = no  |
| subject    | An array of the users assigned to the project.  |
| attn    | An array of task objects associated to the project.  |
| createdBy    | An array of task objects associated to the project.  |
| createdOn    | An array of task objects associated to the project.  |
| lineItems    | An array of task objects associated to the project.  |
| subTotal    | An array of task objects associated to the project.  |
| taxAmount    | An array of task objects associated to the project.  |
| discountAmount    | An array of task objects associated to the project.  |
| amountDue    | An array of task objects associated to the project.  |

### The invoice line item object attributes:

| Attribute  | Description   |
| ---------- | ------------- |
| invoiceLineItemId   | Unique identifier of the task.  |
| invoiceId       | Unique identifier of the project associated with the task.  |
| quantity    | The task code description. |
| description       | The name of the task.  |
| unitPrice      | Flag indicating if the task is billable. 1 = billable, 0 = non-billable  |
| total      | The hourly rate of the task.  |
| createdBy      | The unique identifier of the user that created the task.  |
| createdOn      | The time stamp of when the task was created.  |

-------------

##### Example JSON Response
```SAMPLE RESPONSE
WILL
GO HERE```




