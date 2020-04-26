
# Projects
The project resource allows you to retrieve individual projects as well as a list of all your projects.

## Endpoints
* [Retrieve a project](#retrieve-a-project)
* [List all projects](#list-all-projects)

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

### The task object attributes:

| Attribute  | Description   |
| ---------- | ------------- |
| projectTaskId   | Unique identifier of the task.  |
| projectId       | Unique identifier of the project associated with the task.  |
| shortDesc    | The task code description. |
| longDesc       | The name of the task.  |
| isBillable      | Flag indicating if the task is billable. 1 = billable, 0 = non-billable  |
| taskRate      | The hourly rate of the task.  |
| isActive      | Flag indicating if the task is active. 1 = active, 0 = disabled  |
| companyId      | The unique identifier of the company.  |
| isLeaveField      | Flag indicating if the task is used to track leave. |
| budgetedCost      | The budgeted cost of the task. |
| budgetedHours      | The budgeted hours for the task.  |
| createdBy      | The unique identifier of the user that created the task.  |
| createdOn      | The time stamp of when the task was created.  |

-------------

##### Example JSON Response
```SAMPLE RESPONSE
WILL
GO HERE```



