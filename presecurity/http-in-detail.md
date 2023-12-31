## What is HTTP(S)?
* HTTP: set of rules used for communicating with web servers for the transmission of webpage data (HTML, images, videos, etc)
* HTTPS: secured version of HTTP
* HTTPS data is encrypted so it stops people from seeing data you send and receive as well as give assurance that you're communicating with the right web server

## Requests and Resources
* URL (Uniform Resource Locator) gives instruction on how to access a resource on the Internet
* Parts of the URL:
  * Scheme: instructs what protocol to use when accessing resource (HTTP, HTTPS, FTP)
  * User: some services require authentication to log in, so you can put in the username and password into the URL to log in
  * Host: domain name or IP address of server you wish to access
  * Port: port you're trying to access
  * Path: file name or location of resource trying to access
  * Query string: extra info that can be sent to the requested path (ex: /blog?id=1 would tell the blog path that you wish to receive the blog article with the id of 
  * Fragment: reference to a location on the actual page requested
* A request can be made just by doing "GET / HTTP/1.1"

## HTTP Methods
* GET request is used for getting information from a web server
* POST request is used for submitting data to the web server and create new records
* PUT request is used for submitting data to a web server to update info
* DELETE request is used for delecting information and records from a web server

## HTTP Status Codes
* 100-199 (Information response): tells the client the first part of their request has been accepted and they should continue sending the rest of their request
* 200-299 (Success): tells the client their request was successful
  * 200 (OK): request was completed successfully
  * 201 (Created): resource has been created (ex: new user or new blog post) 
* 300-399 (Redirection): redirects the client's request to another resource (different webpage or website)
  * 301 (Moved permanently): redirects the client's browser to a new webpage or tells search engines that the page has moved somewhere else and to look there instead
  * 302 (Found): temporary redirection that may change again in the near future 
* 400-499 (Client errors): informs the client that there was an error with their request
  * 400 (Bad request): tells the browser that something was either wrong or missing in their request
  * 401 (Not authorized): user isn't currently allowed to view the resource until they've been authorized with the web application
  * 403 (Forbidden): user doesn't have permission to view this resource whether you are logged in or not
  * 404 (Page not found): page/resource requested doesn't exist
  * 405 (Method not allowed): resource doesn't allow this method request (ex: GET request is sent to the resource /create-account when it was expecting a POST request instead)
* 500-599 (Server errors): reserved for errors happening on the server-side, usually indicating a major problem with the server handling the request
  * 500 (Internal service error): server encountered an error with your request that it doesn't know how to handle properly
  * 503 (Service unavailable): server can't handle your request because it's either overloaded or down for maintenance

## Headers
* Common Request Headers:
  * Host: some web servers host multiple websites so by providing the host headers you can tell it which one you require, otherwise you'll just receive the default website for the server
  * User-Agent: your browser software and version number
  * Content-Length: tells the web server how much data to expect in the web request
  * Accept-Encoding: tells the web server what types of compression methods the browser supports so the data can be made smaller for transmitting over the internet





