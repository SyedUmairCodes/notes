A RESTful API is just a set of simple web rules that let any client ask a server to do something. Get, create, change, or delete information. The fancy name `REpresentational State Transfer` only means the server sends back the current representation (the latest version) of whatever you asked for, and then forgets about you until you ask again.

When you make a request to a server, you will get your response in JSON, a simple format that pairs labels (keys) with their values, such as `"name": "John Doe"` or `"Weather": "Humid"` . Each endpoint gives it's own data and each time the server returns a tidy bundle of facts you can use however you like in your own app or website.

## HTTP Requests

- A GET request is used to return the current data available on the server from the specified endpoint.
- A POST request is used to send new data to the server about the specified endpoint using JSON.
- A PUT request is used to update all of the available data on the specified endpoint.
- A PATCH request is used to a single part of the available data on the specified endpoint.
- A DELETE request is used to delete the data available on the specified endpoint.

>[!NOTE]
>Any language that can send HTTP (GET, POST, PUT, PATCH, DELETE) requests can talk to an API, and the API will answer with either JSON or XML. In practice, browsers use JavaScript to call APIs, while servers can use whatever language they like.

JSON has become the common “middle language” because every modern stack
can read it, so the only thing that matters is that the response is valid JSON your
code can parse.

Status codes are what the server returns to the client that tell how the request went.
They are a three digit code that tell you what happened to the request that you sent.

- `2xx` codes means that everything went right as you wanted it to.
- `3xx `codes means that the server has been removed or changed to another IP address.
- `4xx` codes means that the client has made a mistake in their request or requested the wrong resource.
- `5xx `codes means that the server is having troubles resolving your requests, try again later.

> [!IMPORTANT]
> APIs in production are secured and require you to prove who you are before the server will talk to you. That proof is an API Key, a long, secret string you add to every request. Without it, the server refuses to serve you and usually answers with a `4xx` status.



