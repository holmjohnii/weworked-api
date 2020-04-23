# The WeWorked API
Welcome to API reference for WeWorked! 

The WeWorked API is organized around [REST](https://en.wikipedia.org/wiki/Representational_state_transfer). The API provides read-only predictable resource-structured URLs that return [JSON-encoded](https://www.json.org/json-en.html) responses with standard HTTP response codes, authentication and verbs.

The WeWorked API is **read-only** for now, meaning you can only pull data. Changing data in WeWorked may become available in the future.

## Authentication
The WeWorked API uses API keys to authenticate requests. Every request must include the API key assigned to your company's account. API Keys grant access at the company level. User-level API calls are not permitted. Do not share your API key. Keep it in a secure location. Do not place in publicly available areas such as GitHub or in client-side code. 

You must include two header keys in every request:
1. **`x-api-key`** - Your API key from WeWorked. This is requested and viewed from the administration section of your WeWorked account.
2. **`x-ww-user`** - The email address of your WeWorked administrator account.

## Making a Request
All requests must be made using HTTPS. All URLs start with **`https://api.weworked.com/`**. For example, to request a list of all your clients, append the clients resoure path to the base URL. It complete URL should look like `https://api.weworked.com/clients`. 

## Errors 
WeWorked uses standard HTTP response codes to indicate success and failure of an API request. If WeWorked is having problems, you will get a response with a 5xx status code. We recommend writing code that gracefully processes all possible exceptions.

## JSON Responses 
We always return JSON structured data with no root element.

## Rate Limits
The WeWorked API employs several safeguards against bursts of incoming traffic to help maintain stability for across accounts. Sending too many requests in a short period will result in a `429 Too Many Requests` status code response. You may perform up to 200 calls in a 5 minute window. This limit is subject to change.

## Versioning
TBD

## Core Resources
* [Clients](endpoints/clients.md)
* [Expenses](endpoints/clients.md)
* [Invoices](endpoints/clients.md)
* [Projects](endpoints/clients.md)
* [Reports](endpoints/clients.md)
* [Timesheets](endpoints/clients.md)
* [Users](endpoints/clients.md)

