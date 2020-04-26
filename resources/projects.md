
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
| name       | The client's name.  |
| address    | The client's street address. |
| city       | The client's city.  |
| state      | The client's state.  |
| zip        | The client's zipcode.  |
| country    | The client's country.  |
| isActive   | Flag indicating if the client is active or disabled. 1 = active, 0 = disabled  |
| VATNumber  | The client's VAT number.  |
| contact    | The main client's point of contact.  |

-------------

##### Example JSON Response
```SAMPLE RESPONSE
WILL
GO HERE```



