# Free Code Camp HTTP Networking Course Notes

* ## Chapter 1 - Why HTTP
  * HTTP is the most widely used protocol for communicating over the internet
  * Defn: Protocol -
    * A protocol is a set of rules agreed upon for communication over the internet. Rules for parsing binary string of data that is sent from computer to computer.
  * The heart of HTTP is a simple request-response system.
    * The requesting computer, the client, requests some information from another computer, the server. The server will send back a response with the information requested.
    * In some cases, the server can make its own HTTP request to another server, therefore becoming a client in that new request-response interaction.
  * Javascript's Fetch API provides functionality for making HTTP requests from the client
    * `const response = await fetch(url, settings) `
    * Need to use `await` keyword to "pause" code until the response is received
    * What is returned is a Response object, JSON from response can be retrieved via the following
    * ` const responseData = await response.json() `
  * Good servers are always on and listening for HTTP requests
    * In modern era, many companies' servers are hosted in "cloud"/data centers, which are optimized for running server software
* ## Chapter 2 - DNS
  * Internet Protocol (IP) Address's are assigned to each unique device connected to the internet
    * Example IPv4 Address: 8.13.156.7; 4-sections separated by a '.' the contain a byte of data each
    * Example IPv6 Address: _:_:_:_:_:_:_:_
  * DNS (Domain Name System)
    * Maps human readable address to IP addresses
  * Two steps when making HTTP request to a server
    * 1. Resolve DNS
    * 2. Use obtained IP address to make HTTP request
  * Domain is just one part of a url, the part that is associated with an IP address
  * Javascript URL API lets you create a Url object
    * ``` const urlObj = new URL('https://example.com/example-path') ```
  * ICANN manages DNS for the entire internet
    * ICANN root name servers resolve IP addresses
  * Subdomains are prefixes that can be tacked on to the beginning of a domain for information that is hosted on another computer
* ## Chapter 3 - URIs and URLs
  * 8 Sections of a URL:
    * 1. Protocol
    * 2. Username
    * 3. Password
    * 4. Domain
    * 5. Port
    * 6. Path
    * 7. Search/Query Parameters
    * 8. Hash/Fragment
  * Not all protocols end with "//" like HTTP
    * Example: mailto:noreply@testdomain.com
  * Ports are virtual "hubs" managed by the operating system that allow us to segment incoming requests/data streams to the server

