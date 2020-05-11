
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

### Examples JSON Response
```json 
{
        "invoiceId": "627",
        "companyId": "416",
        "invoiceDate": "2020-01-03",
        "invoiceNum": "1401-2",
        "dueDate": "2020-01-03",
        "billTo": "Smithfield Supplies",
        "clientId": "46",
        "paymentTerms": "1",
        "currencySymbol": "USD",
        "tax": "",
        "discount": "",
        "isActive": "1",
        "isPaid": "1",
        "notes": "03/10/2010 - 03/10/2013 Projects: Smithline, Read Center, Sams",
        "subject": "Monthly invoice",
        "attn": "",
        "createdBy": "501",
        "createdOn": "2020-01-15 19:08:06",
        "lineItems": [
            {
                "invoiceLineItemId": "6473",
                "invoiceId": "627",
                "quantity": "1247.00",
                "description": "John Holmes II (Smithline: Hrs Worked)",
                "unitPrice": "20.00",
                "total": "24940.0000",
                "createdBy": "501",
                "createdOn": "2020-01-04 19:08:06"
            }
        ],
        "subTotal": "24940.00",
        "taxAmount": "0",
        "discountAmount": "0",
        "amountDue": "24940"
    }
```

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
| lineItems    | An array of invoice line item objects associated with the invoice.  |
| subTotal    | The subtotal of the invoice. |
| taxAmount    | The tax amount of the invoice.  |
| discountAmount    | The discount amount of the invoice.  |
| amountDue    | The total amount due for the invoice.  |

### The invoice line item object attributes:

| Attribute  | Description   |
| ---------- | ------------- |
| invoiceLineItemId   | Unique identifier of the invoice's line item.  |
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




