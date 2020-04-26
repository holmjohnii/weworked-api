
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
| invoiceId   | Unique identifier of the invoice.  |
| companyId       | The unique identifier of the company.  |
| invoiceDate    | The date of the invoice. |
| invoiceNum       | The unique manual invoice number.  |
| dueDate      | The due date of the invoice.  |
| billTo        | The description of the bill to.  |
| clientId    | The unique identifier of the client assoicated with the invoice. |
| paymentTerms   | The payment terms of the invoice.  |
| currencySymbol  | The currency setting for the invoice.  |
| tax    | The tax percentage for the invoice. |
| discount    | The discount percentage for the invoice.  |
| isActive    | Flag indicating if the invoice is active. 1 = active, 0 = disabled  |
| isPaid    | Flag indicating if the invoice was paid. 1 = paid, 0 = not paid   |
| notes    | The notes for the invoice. |
| subject    | The subject of the invoice. |
| attn    | The attention description of the invoice. |
| createdBy    | The unique identifier of the user that created the invoice.  |
| createdOn    | The time stamp of when the invoice was created. |
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




