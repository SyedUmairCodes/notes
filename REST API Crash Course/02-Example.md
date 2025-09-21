# Real Life Example

Skyscanner, a website that lists all available tickets to various flights shows how a RESTful API works in the real world. 

When you search for flights, Skyscanner doesn’t keep every airline’s prices in its own database. Instead, it fires off a quick REST-style message (an API request) to each airline’s server and each airline’s server replies with its current data, and Skyscanner simply gathers all the answers into one neat list for you. One request, many answers, all over standard web links. that’s the power and simplicity of RESTful APIs. 

A RESTful API is just a set of simple web rules that let any client ask a server to do something. Get, create, change, or delete information. 

The fancy name `REpresentational State Transfer` only means the server sends back the current representation (the latest version) of whatever you asked for, and then forgets about you until you ask again.

When you make a request to a server, you will get your response in JSON, a simple format that pairs labels (keys) with their values, such as `"name": "John Doe"` or `"Weather": "Humid"`. Each endpoint gives it's own data and each time the server returns a tidy bundle of facts you can use however you like in your own app or website.