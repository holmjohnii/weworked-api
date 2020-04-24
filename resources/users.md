
# Users
The user resource allows you to retrieve individual users as well as a list of all the users on your account.

## Endpoints
* [Retrieve a user](#retrieve-a-user)
* [List all users](#list-all-users)

## Retrieve a user
Retrieves the details of an existing user. Simply provide the unique user id.

`GET /v1/users/:id`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/users/501"`

### Parameters
No parameters

### Returns
Returns a user object if a valid identifier was provided. 

-------------

## List all users
Returns a list of your users in alphabetical order.

`GET /v1/users`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/users"`

### Parameters
No parameters

### Returns
Returns an array of user objects.

-------------

### The user object attributes:

| Attribute  | Description   |
| ---------- | ------------- |
| userId   | Unique identifier for the client.  |
| email       | The client's name.  |
| approvesFor    | The client's street address. |
| companyId       | The client's city.  |
| isAdmin      | The client's state.  |
| firstName        | The client's zipcode.  |
| lastName    | The client's country.  |
| title   | Flag indicating if the client is active or disabled. 1 = active, 0 = disabled  |
| internalId  | The client's VAT number  |
| trackLeave    | The main client's point of contact  |
| isActive    | The main client's point of contact  |
| hireDate    | The main client's point of contact  |
| hourlyRate    | The main client's point of contact  |
| payType    | The main client's point of contact  |
| hourlyPayRate    | The main client's point of contact  |
| projectsAssigned    | The main client's point of contact  |
| country    | The main client's point of contact  |
| phone    | The main client's point of contact  |
| address    | The main client's point of contact  |
| city    | The main client's point of contact  |
| state    | The main client's point of contact  |
| zip    | The main client's point of contact  |

-------------

##### Example JSON Response
```SAMPLE RESPONSE
WILL
GO HERE```


