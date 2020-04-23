
# Clients
The client resource allows you to retrieve individual clients as well as a list of all your clients.

## Endpoints
* Retrieve a client
* List all clients

## Retrieve a client
Retrieves the details of an existing client. Simply provide the unique customer id.

`GET /v1/clients/:id`

### Parameters
No parameters

### Returns
Returns a client object if a valid identifier was provided. 

## List all clients
Returns a list of your clients in alphabetical order.

`GET /v1/clients`

### Parameters
No parameters

### Returns
Returns an array of client objects.

# The client object attributes:


