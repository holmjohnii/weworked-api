
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
| clientId   | Unique identifier for the client associated with the project.  |
| clientName       | The name of the client associated with the project.  |
| projectId    | The unique identifier of the project. |
| projectName       | The name of the project.  |
| projectCode      | The project code.  |
| overview        | The overview description of the project.  |
| createdBy    | The time stamp when the project was created.  |
| isBillable   | Flag indicating if the project is billable. 1 = billable, 0 = non-billable  |
| budgetedCost  | The budgeted cost for the project.  |
| budgetedHours    | The budgeted hours for the project. |
| invoiceMethod    | The invoice method unique identifier set for the project.  |
| invoiceMethodName    | The name of the invoice method set for the project.  |
| projectRate    | The project's billable rate.  |
| isSystemProject    | Flag indicating if the project is used to track leave. 1 = yes, 0 = no  |
| peopleAssigned    | An array of the users assigned to the project.  |
| tasks    | An array of task objects associated to the project.  |

-------------

##### Example JSON Response
```SAMPLE RESPONSE
WILL
GO HERE```



