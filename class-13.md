# Reading Notes 301:

sources:https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/

## CRUD

### Status Codes:
- 100's: Informational status codess; they usually tell the client that the header part of the request has been received and the server will try to comply with a transmission demand of the client.
- 200's: Success codes. They tell the client that its request was accepted.
- 300's: Redirection codes. They tell the client that the resource they are requesting isn’t available at the expected location anymore.
- 400's: Client error codes. They are all about invalid requests a client sent to a server.
- 500's: Server error codes. Often they indicate problems with overwhelmed servers or unreachable servers behind proxies, but sometimes they can be directly related to client requests that trigger error exceptions on the server.

## CRUD (Create, Read, Update, Delete):

### Create:
- The create action is usually implemented via HTTPs POST method. In RESTful APIs, these endpoints are used to create new resources or access tokens.
### Read:
- The read action gets implemented via HTTPs GET method and used to fetch resource representations. Asynchronous responses aren’t much of a thing here, because the reason for asynchronous processing is often that the resource doesn’t exist yet and has to be created, so it’s a create action anyway.
### Update:
- An update can be implemented with an HTTP PUT or PATCH method. The difference lies in the amount of data the client has to send to the backend. PUT requires the client to send an entire representation of a resource to update it. (Replace the old one with the new one).
### Delete:
- The delete action can be implemented with the HTTP DELETE method.

