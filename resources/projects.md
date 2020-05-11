
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

### Examples JSON Response

```json
{
    "clientId": "46",
    "clientName": "Company Name",
    "projectId": "124732",
    "projectName": "Landscape Design",
    "projectCode": "",
    "overview": "Landscape design for Westfield Lane",
    "createdBy": "501",
    "companyId": "416",
    "isBillable": "1",
    "budgetedCost": "1200.00",
    "budgetedHours": "30.00",
    "invoiceMethod": "1",
    "invoiceMethodName": "Task Hourly Rate",
    "projectRate": "20.00",
    "isSystemProject": "0",
    "peopleAssigned": [
        {
            "userId": "2815",
            "email": "smith@theemail.com",
            "firstName": "Smith",
            "lastName": "Lee",
            "title": "Architect",
            "isActive": "1"
        },
        {
            "userId": "501",
            "email": "john@theemail.com",
            "firstName": "John",
            "lastName": "Doe",
            "title": "Account Owner",
            "isActive": "1"
        }
    ],
    "tasks": [
        {
            "projectTaskId": "841428",
            "projectId": "124732",
            "shortDesc": "DEZ101",
            "longDesc": "Design",
            "isBillable": "1",
            "companyId": "416",
            "isActive": "1",
            "taskRate": "75.00",
            "isLeaveField": "0",
            "budgetedCost": null,
            "budgetedHours": null,
            "createdBy": "501",
            "createdOn": "2015-05-11 16:41:06"
        },
        {
            "projectTaskId": "841424",
            "projectId": "124732",
            "shortDesc": "",
            "longDesc": "Meetings",
            "isBillable": "1",
            "companyId": "416",
            "isActive": "1",
            "taskRate": "20.00",
            "isLeaveField": "0",
            "budgetedCost": null,
            "budgetedHours": null,
            "createdBy": "501",
            "createdOn": "2012-10-10 19:24:31"
        }
    ]
}
```
-------------

## List all projects
Returns a list of your projects in alphabetical order.

`GET /v1/projects`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/projects"`

### Parameters
No parameters

### Returns
Returns an array of projects.

## Example JSON Response
```json
[
    {
        "Active": [
            {
                "ProjectId": "124732",
                "CompanyId": "416",
                "ClientId": "46",
                "ProjectName": "General Store",
                "ProjectCode": "",
                "Overview": "",
                "InvoiceMethodId": "1",
                "ProjectRate": "20.00",
                "BudgetCost": "9500.00",
                "BudgetHours": "68.00",
                "IsBillable": "1",
                "IsSysProject": "0",
                "IsActive": "1",
                "CreatedBy": "501",
                "CreatedOn": "2012-10-10 19:24:31"
            },
            {
                "ProjectId": "121",
                "CompanyId": "416",
                "ClientId": "46",
                "ProjectName": "Perry Design",
                "ProjectCode": "",
                "Overview": "Perry buildout",
                "InvoiceMethodId": "1",
                "ProjectRate": "20.00",
                "BudgetCost": 130000.00",
                "BudgetHours": "0.00",
                "IsBillable": "1",
                "IsSysProject": "0",
                "IsActive": "1",
                "CreatedBy": "501",
                "CreatedOn": "2012-10-10 19:24:31"
            }
        ],
        "Archived": [
            {
                "ProjectId": "4168",
                "CompanyId": "416",
                "ClientId": "46",
                "ProjectName": "Sams",
                "ProjectCode": "SAM990",
                "Overview": "Sams Construction",
                "InvoiceMethodId": "2",
                "ProjectRate": "0.00",
                "BudgetCost": "5000.00",
                "BudgetHours": "100.00",
                "IsBillable": "1",
                "IsSysProject": "0",
                "IsActive": "0",
                "CreatedBy": "0",
                "CreatedOn": "2013-02-25 11:13:09"
            }
        ],
        "Leave": [
            {
                "ProjectId": "120",
                "CompanyId": "416",
                "ClientId": "46",
                "ProjectName": "Leave",
                "ProjectCode": "",
                "Overview": "Default for leave DO NOT REMOVE",
                "InvoiceMethodId": null,
                "ProjectRate": null,
                "BudgetCost": null,
                "BudgetHours": null,
                "IsBillable": "0",
                "IsSysProject": "1",
                "IsActive": "1",
                "CreatedBy": "501",
                "CreatedOn": "2012-10-10 19:24:31"
            }
        ]
    }
]
```

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



