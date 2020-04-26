
# Projects
The project resource allows you to retrieve individual projects as well as a list of all your projects.

## Endpoints
* [Retrieve a project](#retrieve-a-project)
* [List all projects](#list-all-projecxts)

## Retrieve a project
Retrieves the details of an existing project. Simply provide the unique project id.

`GET /v1/projects/:id`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/projects/324"`

### Parameters
No parameters

### Returns
Returns a project object if a valid identifier was provided. 

-------------

## List all projects
Returns a list of your projects in alphabetical order.

`GET /v1/projects`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/projects"`

### Parameters
No parameters

### Returns
Returns an array of client objects.

-------------

### The project object attributes:

| Attribute  | Description   |
| ---------- | ------------- |
| clientId   | Unique identifier for the client.  |
| clientName       | The client's name.  |
| projectId    | The client's street address. |
| projectName       | The client's city.  |
| projectCode      | The client's state.  |
| overview        | The client's zipcode.  |
| createdBy    | The client's country.  |
| isBillable   | Flag indicating if the client is active or disabled. 1 = active, 0 = disabled  |
| budgetedCost  | The client's VAT number.  |
| budgetedHours    | The main client's point of contact.  |
| invoiceMethod    | The main client's point of contact.  |
| invoiceMethodName    | The main client's point of contact.  |
| projectRate    | The main client's point of contact.  |
| isSystemProject    | The main client's point of contact.  |
| peopleAssigned    | The main client's point of contact.  |
| tasks    | The main client's point of contact.  |

-------------

##### Example JSON Response
```SAMPLE RESPONSE
WILL
GO HERE```



