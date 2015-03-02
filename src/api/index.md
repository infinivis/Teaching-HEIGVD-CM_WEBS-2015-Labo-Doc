---
title: Overview
sectionName: API Reference
template: api.jade
menuIndex: 3
---

This pages contains general documentation about the API. Use the links on the
right to navigate to specific resources.

### Content-type

The API uses the JSON format. Unless specified otherwise, all requests and
response should have the `Content-Type: application/json` header.

### HTTP verbs

The API uses the standard HTTP verbs to perform CRUD operations (**C**reate,
**R**etrieve, **U**pdate, **D**elete) on resources, following standard RESTful
API practices.

Find below a quick summary of how HTTP verbs are used in the API:

| Verb     | Description |
|----------|--------
| `GET`    | Used for retrieving a resource or a collection of resources.
| `POST`   | Used for creating a new resource or performing a non-CRUD operation on a resource.
| `PUT`    | Used to perform a full update of a resource (replacing the resource by the JSON data provided in the request).
| `DELETE` | Used for deleting resources.

`HEAD` and `PATCH` are not currently used.

### Some examples

In the `path` part, is all the pathes that come after this url: `https://mighty-hamlet-9493.herokuapp.com/api/`.
For example: `https://mighty-hamlet-9493.herokuapp.com/api/users`

| Path    | http-verb | Description | 
|----------|--------|-----------
| `issues` | GET | Used for retrieving all the issues.
| `issues`   | POST  |Used for creating a new issue.
| `issue/{id}` | GET  |Used to get one specific issue.
| `issue/{id}/action` | POST/PUT |Used to make an action on a specific issue.

The app is working like that. Checkout the resources to get more details to how to get with it. 


### Authentication

To interact with the API, your client will need to be authenticated for few resources. This isn't yet implemented. This will be done by using the **x-user-id** header with the user id of the client and gives something that looks like:

	x-user-id: <id>

### Authorizations

| Role      | Description |
|-----------|--------
| `any`     | Authenticated user is enough.
| `various` | Complex authorization scheme detailed directly in the resource.
| `citizen` | Any user with citizen role.
| `staff`   | Any user with staff role.

### Errors

The errors are not properly handled at the moment. Do not try to have errors!
