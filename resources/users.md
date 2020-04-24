
# Users
The user resource allows you to retrieve individual users as well as a list of all the users on your account.

## Endpoints
* [Retrieve a user](#retrieve-a-client)
* [List all users](#list-all-clients)

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

### The client object attributes:

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
| VATNumber  | The client's VAT number  |
| contact    | The main client's point of contact  |

-------------

##### Example JSON Response
```SAMPLE RESPONSE
WILL
GO HERE```


