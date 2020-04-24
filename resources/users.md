
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
| userId   | Unique identifier for the user.  |
| email       | The user's email.  |
| approvesFor    | Description of the people who the user approves time for. Everyone, Nobody, Group, or People. |
| companyId       | The unique identier of the user's company.  |
| isAdmin      | Flag indicating if the user is an admin. 1 = yes, 0 = no  |
| firstName        | The user's first name.  |
| lastName    | The users's last name.  |
| title   | The user's title.  |
| internalId  | The user's custom id.  |
| trackLeave    | Flag indicating if leave is tracked for the user. 1 = yes, 0 = no |
| isActive    | Flag indicating if the user's account is active or disabled. 1 = active, 0 = disabled  |
| hireDate    | The user's hire date. |
| hourlyRate    | The user's hourly billable rate  |
| payType    | The user's pay type. S = salary, H = hourly  |
| hourlyPayRate    | The user's hourly pay rate. |
| projectsAssigned    | An array of the user's assigned projects. |
| country    | The user's country.  |
| phone    | The user's phone.  |
| address    | The user's address.  |
| city    | The user's city.  |
| state    | The user's state.  |
| zip    | The user's zip.  |

-------------

##### Example JSON Response
```SAMPLE RESPONSE
WILL
GO HERE```


