### HTTP & REST

#### Internet Highway - HTTP

It's the foundation of all modern software

#### A client-server protocol: HTTP

1. The beginning of everything - invented in 1991, HTTP is the start of Internet big bang, 5 years later the web already had more than 40 million users
2. At the core of the web - with the strong foundations of HTTP, it is applicable to both backend and frontend
3. HTTP as a protocol - under the hood we are still exchanging packets, bits and bytes. On a higher level we always talk about request, response, headers and body.

<img width="600" alt="image" src="https://user-images.githubusercontent.com/5379043/194435090-3403b98e-8177-47b5-9f2f-c39444251a04.png">

#### Anatonmy of the Request
<img width="400" alt="image" src="https://user-images.githubusercontent.com/5379043/194435373-e2cde0a1-af49-4ada-a4f4-ab3670944779.png">

#### Anatomy of the Response
<img width="400" alt="image" src="https://user-images.githubusercontent.com/5379043/194435226-fe558ab4-a321-48e5-b48f-a699c79351a3.png">

#### Client-Server Conversation
<img width="900" alt="image" src="https://user-images.githubusercontent.com/5379043/194435584-9841a87c-7202-4bc4-bd41-423da4d53fa1.png">

#### The Request/Response Anatomy
<img width="500" alt="image" src="https://user-images.githubusercontent.com/5379043/194435711-4d53ea40-6ac5-4c72-bedc-fc69822744c0.png">

#### Decoding HTTP Methods
- GET - used to retrieve data
- POST - used to submit a resource, usually changes data on the server side
- PUT - used to replace a resource
- PATCH - updates a resource partially
- DELETE - delete the resource
- OPTIONS, HEAD, TRACE, CONNECT - used for secondary tasks (CORS mechanism)

#### Decoding HTTP Status Codes
- 1xx - very rarely used, request received, process continues
- 2xx - request is successful
- 3xx - further steps are needed to fulfill the request (301 redirect)
- 4xx - an error caused by the client (bad request input, bad syntax, 401 Unauthorized)
- 5xx - an unexpected exception occured on the server side (500 server error)


