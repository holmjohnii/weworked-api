# The WeWorked API
Welcome to the API reference for WeWorked! [WeWorked](https://www.weworked.com) is timesheet and invoicing software enjoyed by companies around the world. 

The current version of the API is **`v1`**. 

The WeWorked API is organized around [REST](https://en.wikipedia.org/wiki/Representational_state_transfer). The API provides read-only predictable resource-structured URLs that return [JSON-encoded](https://www.json.org/json-en.html) responses with standard HTTP response codes, authentication, and verbs.

The WeWorked API is **read-only** for now, meaning you can only GET data. Changing data in WeWorked may become available in the future.

## Authentication
The WeWorked API uses API keys to authenticate requests. Every request must include the API key assigned to your company's account. API Keys grant access at the company level. User-level API calls are not permitted. Do not share your API key. Keep it in a secure location. Do not place in publicly available areas such as GitHub or in client-side code. 

You must include two header keys in every request:
1. **`x-api-key`** - Your API key from WeWorked. This is requested and viewed from the administration section of your WeWorked account.
2. **`x-ww-user`** - The email address of your WeWorked administrator account.

## Making a Request
All requests must be made using HTTPS. All URLs start with **`https://api.weworked.com/`**. The API version number and resource is appened to the path. For example, to request a list of all your clients, append the clients resoure path to the base URL. The complete URL would look like `https://api.weworked.com/v1/clients`. 

##### cURL Example
`curl -H "x-api-key: YOURAPIKEY" -H "x-ww-user: YOUREMAIL" GET "https://api.weworked.com/v1/clients"`

## Errors 
WeWorked uses standard HTTP response codes to indicate success and failure of an API request. If WeWorked is having problems, you will get a response with a 5xx status code. We recommend writing code that gracefully processes all possible exceptions.

## JSON Responses 
We always return JSON structured data with no root element.

## Rate Limits
The WeWorked API employs several safeguards against bursts of incoming traffic to help maintain stability for across accounts. Sending too many requests in a short period will result in a `429 Too Many Requests` status code response. You may perform up to 20 request per second. This limit is subject to change.

## Core Resources
* [Clients](resources/clients.md)
* [Expenses](resources/expenses.md)
* [Invoices](resources/invoices.md)
* [Projects](resources/projects.md)
* [Reports](resources/reports.md)
* [Timesheets](resources/timesheets.md)
* [Users](resources/users.md)

