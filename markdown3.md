# Rest Architecture Report

## Project Scenario
# REST (Representational State Transfer) Architecture

REST  is an architectural style used for creating scalable web services. It utilizes HTTP as the communication protocol, making interactions between the client and server straightforward. REST is stateless, meaning each client request to the server must contain all the information needed for the server to process the request. The server does not keep any client session state between requests, which helps with scalability and performance.

## Key Principles of REST

### 1. Statelessness
Each request from the client to the server should be self-contained, meaning it must include all the necessary data for processing. The server does not store any session information, making each interaction independent. This leads to better scalability since the server does not need to keep track of users across requests.

### 2. Client-Server Architecture
In a RESTful system, the client and server are separate entities. The client handles the user interface and user experience, while the server manages data and business logic. This separation allows the system to evolve independently on both sides.

### 3. Uniform Interface
RESTful services use a consistent interface for interacting with resources. This involves the following components:
   - **Resource Identification**: Resources are uniquely identified by URLs (e.g., `/users/123` for user data).
   - **Manipulation Through Representations**: Clients interact with resources using representations like JSON or XML.
   - **Self-descriptive Messages**: HTTP methods (GET, POST, PUT, DELETE) tell the server what action to perform on the resource.
   - **Hypermedia as the Engine of Application State (HATEOAS)**: The server provides links (URLs) to related resources, guiding the client on possible next actions.

### 4. Layered System
REST architectures are built in layers. The client does not directly interact with the server but may go through multiple intermediaries (such as caches or load balancers) to improve scalability, security, and performance. Each layer can operate independently.

### 5. Cacheability
Responses from the server should specify whether they can be cached or not. If cacheable, the client can reuse previously retrieved responses, reducing the load on the server and improving performance.

### 6. Code on Demand (Optional)
Sometimes, the server can send code (such as JavaScript) to the client for execution. This adds flexibility by allowing the server to enhance the client's functionality dynamically.

## HTTP Methods in REST
RESTful services commonly use the following HTTP methods:
- **GET**: Fetches data from the server (e.g., retrieve a list of users).
- **POST**: Sends data to the server to create a new resource.
- **PUT**: Updates an existing resource.
- **DELETE**: Removes a resource from the server.

## Benefits of REST
- **Scalability**: REST’s stateless nature makes it easier to scale applications horizontally, adding more servers without complex session management.
- **Simplicity**: Using HTTP methods and standardized URIs makes REST simple and flexible to implement.
- **Performance**: The ability to cache responses reduces server load and enhances performance.

## Challenges of REST
- **Overhead**: Using HTTP introduces overhead compared to more lightweight protocols.
- **Statelessness**: Since the server does not maintain state, the client must manage session information and send necessary details with each request.

## References
* [REST Architecture Overview](https://restfulapi.net)
* [REST Principles by Roy Fielding](https://www.ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm)
* [HTTP Methods Explained](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)
* [What is HATEOAS?](https://restfulapi.net/hateoas/)

