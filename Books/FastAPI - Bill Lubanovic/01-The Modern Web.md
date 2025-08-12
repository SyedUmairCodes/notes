# The Modern Web

The web has transformed into a complex network where the focus is shifting from static content (HTML, JavaScript, images) to the dynamic connections facilitated by APIs. Modern web applications typically separate into distinct "frontend" and "backend" worlds.

> [!NOTE]
> The backend, often managed by a web service, handles low-level database access and middle-level business logic. The frontend, usually a JavaScript or mobile application, provides the rich and interactive user interface.

APIs serve as the crucial communication link between these two worlds. In today's web development, API design is considered as vital as website design itself. An API functions as a contract, similar to a database schema, defining the rules and structure for interaction. Consequently, defining and modifying APIs has become a significant and specialized role.

Each API is defined by two core components:

- **Protocol:** This dictates the control structure of the communication.
- **Format:** This specifies the content structure of the data being exchanged.

As technology has progressed from isolated machines to networked servers, various API methods have emerged to facilitate different communication patterns:

- Traditional APIs were used locally, within modules and libraries only.
- Remote Procedure Calls were developed for connecting separate processes together. Whether on the same machine or different ones and to be called as if they were part of the calling application.
- Messaging APIs involve sending small data chunks through pipelines. Messages represent events or commands.
  - The simplest message queue is the request-response model where a sender sends a message to the receiver.
  - The pub-sub model is where a publisher sends the same message to multiple subscribers.
  - Queues are similar to pub-sub but from a pool of subscribers, only one subscriber picks up and processes the message.

> [!NOTE]
> These messaging patterns can be integrated with web services to handle slower backend tasks, such as sending emails or generating thumbnail images, by decoupling them from the immediate request-response cycle.

---

## HTTP and RESTFul APIs

Tim Berners-Lee, the creator of the World Wide Web, proposed three fundamental components that, despite their apparent simplicity in retrospect, proved to be an incredibly effective combination:

- HTML is a markup language designed for displaying data on the web.
- HTTP is a client-server protocol that governs communication.
- URLs are an addressing scheme used to locate and identify web resources.

> [!NOTE]
> As the web evolved, some experimental ideas, like the `IMG` tag for embedding images, survived and became standard. Over time, as web development needs became clearer, formal standards for these components were established.

Representational State Transfer (REST) is an architectural style for using HTTP, while the original concept is now much different it has become the dominant approach for modern web services.

- REST uses HTTP and client server protocol.
- Each request contains all the necessary information for the server to understand and fulfill the request.
- Responses can be cached on the client-side to improve performance and reduce server load for subsequent requests.

> [!IMPORTANT]
> A web service exposes its features through **endpoints**, also known as **routes**. Each endpoint is a distinct URL combined with an HTTP **verb** (action) that specifies the intended operation on the resource.

| HTTP Verb | CRUD Operation              | Description                                                                                                        |
| :-------- | :-------------------------- | :----------------------------------------------------------------------------------------------------------------- |
| `POST`    | Create (write)              | Used to submit an entity to the specified resource, often causing a change in state or side effects on the server. |
| `PUT`     | Modify completely (replace) | Used to update a resource, replacing the entire resource with the data provided in the request body.               |
| `PATCH`   | Modify partially (update)   | Used to apply partial modifications to a resource.                                                                 |
| `GET`     | Get (read, retrieve)        | Used to request data from a specified resource.                                                                    |
| `DELETE`  | Delete                      | Used to remove the specified resource.                                                                             |

A client sends an HTTP request to a RESTful endpoint, with data typically contained in one of the following parts of the HTTP message:

- Metadata about the request, such as content type or authentication tokens is stored in the header.
- The URL string that tells the address of the resource along with any query parameters for specific resources.
- The main content of the request, often used for sending data to be created or updated is sent in the body.

In return, an **HTTP response** is sent back, consisting of an integer **status code** that indicates the outcome of the request along with metadata about the request and the content it returned.

| Code Number | Description                                              |
| ----------- | -------------------------------------------------------- |
| 100         | Informational response                                   |
| 200         | The request was successful                               |
| 300         | The request is incomplete, the server needs more context |
| 400         | Client-side errors or invalid requests sent              |
| 500         | Server-side errors or server unavailable.                |
