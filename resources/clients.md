
# Clients
The client resource allows you to retrieve individual clients as well as a list of all your clients.

## Endpoints
* [Retrieve a client](#retrieve-a-client)
* [List all clients](#list-all-clients)

## Retrieve a client
Retrieves the details of an existing client. Simply provide the unique customer id.

`GET /v1/clients/:id`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/clients/416"`

### Parameters
No parameters

### Returns
Returns a client object if a valid identifier was provided. 

-------------

## List all clients
Returns a list of your clients in alphabetical order.

`GET /v1/clients`

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/clients"`

### Parameters
No parameters

### Returns
Returns an array of client objects.

-------------

### The client object attributes:
- clientId
fdjsjdfsdfsf
- name
- address
- city
- state
- zip
- country
- isActive
- VATNumber
- contact


