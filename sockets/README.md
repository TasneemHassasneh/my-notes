## Web Sockets

**What is a Web Socket?**

Web Socket is a communication protocol that provides full-duplex communication channels over a single TCP connection between a client (usually a web browser) and a server. Unlike traditional HTTP requests, Web Sockets allow for real-time, bidirectional communication between the client and server.

**Web Socket Request/Response Handshake**

The Web Socket handshake starts with an HTTP-based handshake request from the client to the server, known as the WebSocket handshake. The client sends an HTTP request with specific headers, including the "Upgrade" header with the value "websocket", to indicate the intention to upgrade the connection. If the server supports Web Sockets, it responds with an HTTP 101 status code (Switching Protocols) and includes specific headers to confirm the upgrade. Once the connection is established, both the client and server can send messages to each other in real-time over the Web Socket connection.

**Web Sockets Without Request from Client**

Web Sockets provide a standardized way for the server to send content to a client without first receiving a request (such as an HTTP request) from the client. The server can initiate the communication and send data to the client at any time once the Web Socket connection is established.

## Socket.io Tutorial

**What does the event handler io.on() do?**

The event handler `io.on()` is used in Socket.io to listen for events that are emitted from the client or server. It allows you to define the callback function that will be executed when a particular event is received. For example, `io.on('connection', callback)` listens for the 'connection' event when a client establishes a connection with the server, and the provided callback function is executed.

**Describe some possible proof of life or proof that the code works as expected**

To demonstrate proof that the code works as expected in a Socket.io application, you can:
- Print messages to the console or log files indicating the occurrence of specific events.
- Display real-time updates or notifications on the client-side interface.
- Use debugging tools to inspect the network traffic and confirm the communication between the client and server.

**What does socket.emit() do?**

In Socket.io, `socket.emit()` is used to send a custom event from the client to the server or from the server to a specific client. It allows the client or server to emit a custom event with optional data as the payload.

## Socket.io vs Web Sockets

**What is the difference between WebSocket and Socket.IO?**

WebSocket is a communication protocol standardized by the W3C and provides a low-level API for full-duplex communication over a single TCP connection. Socket.IO is a library that builds on top of WebSockets and provides additional features, including fallback mechanisms, real-time event-based communication, and support for various transports like WebSockets, AJAX, and Long Polling.

**When would you use Socket.IO?**

Socket.IO is suitable when you need real-time, bidirectional communication between the client and server and want to ensure compatibility across different browsers and platforms. It provides a higher-level API and fallback options for environments where WebSockets may not be available.

**When would you use WebSockets?**

WebSockets should be used when you require low-level, full-duplex communication between the client and server. If you have control over the client and server implementation and don't need the additional features provided by Socket.IO, using raw WebSockets can be more lightweight and efficient.
