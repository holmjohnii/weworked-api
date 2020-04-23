# The WeWorked API
Welcome to API reference for WeWorked! 

The WeWorked API is organized around REST. The API provides read-only predictable resource-structured URLs that return JSON-encoded responses with standard HTTP response codes, authentication and verbs.

The WeWorked API is read-only for now, meaning you can only pull data. Changing data in WeWorked may become available in the future.

## Authentication
The WeWorked API uses API keys to authenticate requests. Every request must include the API key assigned to your company's account. API Keys grant access at the company level. User-level API calls are not permitted. Do not share your API key. Keep it in a secure location. Do not place in publicly available areas such as GitHub or in client-side code. 

You can view and request your API key from the administration section of your WeWorked account. 

You must include a x-api-key header in every request. All API requests must be made over HTTPS.

## Errors 
WeWorked uses standard HTTP response codes to indicate success and failure of an API request. If WeWorked is having problems, you will get a response with a 5xx status code. We recommend writing code that gracefully processes all possible exceptions.

## JSON Responses 
We always return JSON structured data with no root element.

## Versioning
TBD

## Core Resources
* Clients
* Expenses
* Invoices
* Projects
* Reports
* Timesheets
* Users

