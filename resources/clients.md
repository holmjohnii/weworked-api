
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

### Example JSON Response
```json 
{
        "clientId": "18111",
        "name": "Books II Read Inc.",
        "address": "222 Lemons Road",
        "address2": "Suite 200",
        "city": "Southbank Victoria",
        "state": "Australia",
        "zip": "3006",
        "country": "AU",
        "isActive": "1",
        "VATNumber": "",
        "contact": "Maria Michele"
}
```

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

| Attribute  | Description   |
| ---------- | ------------- |
| clientId   | Unique identifier for the client.  |
| name       | The client's name.  |
| address    | The client's address line 1. |
| address2    | The client's address line 2. |
| city       | The client's city.  |
| state      | The client's state.  |
| zip        | The client's zipcode.  |
| country    | The client's country.  |
| isActive   | Flag indicating if the client is active or disabled. 1 = active, 0 = disabled  |
| VATNumber  | The client's VAT number.  |
| contact    | The main client's point of contact.  |

-------------

##### Example JSON Response
```json 
[
    {
        "clientId": "18111",
        "name": "Books II Read Inc.",
        "address": "222 Lemons Road",
        "address2": "Suite 200",
        "city": "Southbank Victoria",
        "state": "Australia",
        "zip": "3006",
        "country": "AU",
        "isActive": "1",
        "VATNumber": "",
        "contact": "Maria Michele"
    },
    {
        "clientId": "46",
        "name": "Armory Lite",
        "address": "555 Painter Way",
        "address2": "",
        "city": "Capitol Heights",
        "state": "MD",
        "zip": "20743",
        "country": "US",
        "isActive": "1",
        "VATNumber": "",
        "contact": "John Dutchinson"
    }
]
```


