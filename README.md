# Ragav-s-Task-Http


HTTP (HyperText Transfer Protocol) is the underlying protocol of the World Wide Web. Developed by Tim Berners-Lee and his team between 1989-1991
HTTP functions as a request–response protocol in the client–server computing model.
HTTP has four versions — HTTP/0.9, HTTP/1.0, HTTP/1.1, and HTTP/2.0. Today the version in common use is HTTP/1.1 and the future will be HTTP/2.0.


**HTTP/0.9 — The One-line Protocol**
Initial version of HTTP — a simple client-server, request-response, telenet-friendly protocol
Request nature: single-line (method + path for requested document)
Methods supported: GET only
Response type: hypertext only
Connection nature: terminated immediately after the response

Popular web servers (Apache, Nginx) still supports HTTP/0/9. Try opening up a Telnet session and accessing google.com



**HTTP/1.0 — Building extensibility**
Browser-friendly protocol
Provided header fields including rich metadata about both request and response (HTTP version number, status code, content type)
Response: not limited to hypertext (Content-Type header provided ability to transmit files other than plain HTML files — e.g. scripts, stylesheets, media)
Methods supported: GET , HEAD , POST
Connection nature: terminated immediately after the response


**Establishing a new connection for each request — major problem in both HTTP/0.9 and HTTP/1.0**
Both HTTP/0.9 and HTTP/1.0 required to open up a new connection for each request (and close it immediately after the response was sent). Each time a new connection establishes, a TCP three-way handshake should also occur. For better performance, it was crucial to reduce these round-trips between client and server. HTTP/1.1 solved this with persistent connections.



**HTTP/1.1 — The standardized protocol**
This is the HTTP version currently in common use.
Introduced critical performance optimizations and feature enhancements — persistent and pipelined connections, chunked transfers, compression/decompression, content negotiations, virtual hosting (a server with a single IP Address hosting multiple domains), faster response and great bandwidth savings by adding cache support.
Methods supported: GET , HEAD , POST , PUT , DELETE , TRACE , OPTIONS
Connection nature: long-lived


**HTTP/2 – A protocol for greater performance**
Over the years, Web pages have become much more complex, even becoming applications in their own right. The amount of visual media displayed, the volume and size of scripts adding interactivity, has also increased: much more data is transmitted over significantly more HTTP requests. HTTP/1.1 connections need requests sent in the correct order. Theoretically, several parallel connections could be used (typically between 5 and 8), bringing considerable overhead and complexity. For example, HTTP pipelining has emerged as a resource burden in Web development.

**The HTTP/2 protocol has several prime differences from the HTTP/1.1 version:**

It is a binary protocol rather than text. It can no longer be read and created manually. Despite this hurdle, improved optimization techniques can now be implemented.
It is a multiplexed protocol. Parallel requests can be handled over the same connection, removing the order and blocking constraints of the HTTP/1.x protocol.
It compresses headers. As these are often similar among a set of requests, this removes duplication and overhead of data transmitted.
It allows a server to populate data in a client cache, in advance of it being required, through a mechanism called the server push.


**Post-HTTP/2 evolution**
HTTP didn't stop evolving upon the release of HTTP/2. Like with HTTP/1.x previously, HTTP's extensibility is still being used to add new features. Notably, we can cite new extensions of the HTTP protocol appearing in 2016

**HTTP/3 - HTTP over QUIC**
The next major version of HTTP, HTTP/3, will use QUIC instead TCP/TLS for the transport layer portion.


























