## Putting It All Together
* Ehen you request a website, your computer needs to know the server's IP address it needs to talk to by using DNS
* Your computer  talks to the web server using a special set of commands called the HTTP protocol
* The webserver returns HTML, JavaScript, CSS, etc. which your browser then uses to correctly format and display the website to you

## Other Components
* When a website's traffic starts getting quite large or is running an application that needs to have high availability, one web server might no longer do the job
* Load balancers ensure that high traffic websites can handle the load and providing a failover if a server becomes unresponsive
* When you request a website with a load balancer, the load balancer will receive your request first and then forward it to one of the multiple servers behind it
* Load balancers use different algorithms, like round-robin & weighted, to help it decide which server is best to deal with the request
* Load balancers perform health checks which are periodic checks with each server to ensure they are running correctly
* If a server doesn't respond appropriately or doesn't respond, the load balancer will stop sending traffic until it responds normally again
* CDN (Content Delivery Networks): resource for cutting down traffic to a busy website, allowing users to host static files from websites from thousands of servers
  * When a user requests one of the hosted files, the CDN figures out where the nearest server is physicaly located and sends the request there instead of the other side of the world
* Databases: stores information for users
  * Common databases: MySQL, MSSQL, MongoDB, GraphQL, PostgreSQL
* WAF (Web Application Firewall): sits between your web request and the web server, protecting the webserver from hacking or denial of service attacks
  * Analyzes the web requests for common attack techniques, whether the request is from a real browser rather than a bot
  * Checks if an excessive amount of web requests are being sent by using rate limiting, which only allows a certain amount of requests from an IP per second
  * If a request is deemed a potential attack, it will be dropped and never sent to the webserver
 
## How Web Servers Work
* Web server: software that listens for incoming connections and then utilises the HTTP protocol to deliver web content to its clients
* Common web server softwares are Apache, Nginx, IIS and NodeJS
* Web servers use virtual hosts to ost multiple websites with different domain names, checking the hostname being requested from the HTTP headers and matches that against its virtual hosts
* Static content: content that never changes
* Dynamic content: content that could change with different request
* Examples of backend languages: PHP, Python, Ruby, NodeJS, Perl
* Backend languages: can interact with databases, call external services, process data from the user
