# Uniform Resource Locator (URL)
A URL (Uniform Resource Locator) is used to uniquely identify a resource over the web. URL has the following syntax:

_protocol_://_hostname_:_port_/_path-and-file-name_

There are 4 parts in a URL:

1. _Protocol_: The application-level protocol used by the client and server, e.g., HTTP, FTP, and telnet.
2. _Hostname_: The DNS domain name (e.g., `www.nowhere123.com`) or IP address (e.g., 192.128.1.2) of the server.
3. _Port_: The TCP port number that the server is listening for incoming requests from the clients.
4. _Path-and-file-name_: The name and location of the requested resource, under the server document base directory.

For example, in the URL `http://www.nowhere123.com/docs/index.html`, the communication protocol is HTTP; the hostname is `www.nowhere123.com`. The port number was not specified in the URL, and takes on the default number, which is TCP port 80 for HTTP. The path and file name for the resource to be located is "`/docs/index.html`".

Other examples of URL are:

ftp://www.ftp.org/docs/test.txt
mailto:user@test101.com
news:soc.culture.Singapore
telnet://www.nowhere123.com/
