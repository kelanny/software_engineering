 # HTTP-HyperText Transfer Protocol
 
 HTTP is an _asymmetric request-response client-server_ protocol as illustrated.  An HTTP client sends a request message to an HTTP server.  The server, in turn, returns a response message.  In other words, HTTP is a _pull protocol_, the client _pulls_ information from the server (instead of server _pushes_ information down to the client).
 ![[http_protocol.png]]

HTTP is a stateless protocol. In other words, the current request does not know what has been done in the previous requests.

 HTTP permits negotiating of data type and representation, so as to allow systems to be built independently of the data being transferred.
 
 Quoting from the RFC2616: "The Hypertext Transfer Protocol (HTTP) is an application-level protocol for distributed, collaborative, hypermedia information systems. It is a generic, stateless, protocol which can be used for many tasks beyond its use for hypertext, such as name servers and distributed object management systems, through extension of its request methods, error codes and headers."

As mentioned, whenever you enter a [[URL]] in the address box of the browser, the browser translates the [[URL]] into a request message according to the specified protocol; and sends the request message to the server.

For example, the browser translated the URL `http://www.nowhere123.com/doc/index.html` into the following request message:
![[http_request_message.png]]

When this request message reaches the server, the server can take either one of these actions:

1. The server interprets the request received, maps the request into a _file_ under the server's document directory, and returns the file requested to the client.
2. The server interprets the request received, maps the request into a _program_ kept in the server, executes the program, and returns the output of the program to the client.
3. The request cannot be satisfied, the server returns an error message.

An example of the HTTP response message is as shown:
![[http_response_message.png]]

The browser receives the response message, interprets the message and displays the contents of the message on the browser's window according to the media type of the response (as in the Content-Type response header). Common media type include "`text/plain`", "`text/html`", "`image/gif`", "`image/jpeg`", "`audio/mpeg`", "`video/mpeg`", "`application/msword`", and "`application/pdf`".

In its idling state, an HTTP server does nothing but listening to the IP address(es) and port(s) specified in the configuration for incoming request. When a request arrives, the server analyzes the message header, applies rules specified in the configuration, and takes the appropriate action. The webmaster's main control over the action of web server is via the configuration, which will be dealt with in greater details in the later sections.

