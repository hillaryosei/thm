## What is the OSI Model?
* OSI (Open Systems Interconnection) model provides a framework for how networked devices send, receive, and interpret data
* One of the benefits of the OSI model is that devices can have different functions and designs on a network while communicating with other devices
* There are 7 layers in the OSI model (from top to bottom): Application, Presentation, Session, Transport, Network, Data Link, and Physical
* At each layer that data travels through, specific processes take place, and pieces of information are added to that data (this is called encapsulation)

## Application Layer
* Where protocols and rules are in place to determine how the user should interact with data sent or received
* Here, users can interact with applications such as email clients, browsers, or file-sharing browsing software
* GUI and DNS

## Presentation Layer
* This layer acts as a translator for data to and from the application layer - The receiving computer will also understand data sent to a computer in one format destined for another format
* Security features like data encryption (HTTPS) occur here

## Session Layer
* Once data has been correctly translated or formatted from the presentation layer, this layer creates a connection to the other computer that the data is destined for
* When this connection is created, a session begins
* This layer syncs the two computers to ensure that they are on the same page before data is sent and received. Then, it'll begin dividing the data sent into smaller chunks of data and begin to send these chunks (packets) one at a time
* Sessions are unique, so data can't travel over different sessions

## Transport Layer
* This layer plays an important role in transmitting data over a network
* When data is sent between devices, it follows two different protocols: TCP (Transmission Control Protocol) and UDP (User Datagram Protocol)
  * TCP is a connection-oriented protocol requiring a TCP three-way-handshake to establish a connection. It is used for file sharing, internet browsing, sending an email, etc because they require data to be complete and accurate. Protocols such as HTTP, POP3, IMAP and SMTP use TCP
    * Advantages of TCP
      * Guarantees accuracy of data 
      * Capable of syncing 2 devices to prevent each other from being flooded with data
      * Performs a lot more processes for reliability such as error checking (how TCP can guarantee that data sent from the small chunks in the session layer has then been received and reassembled in the same order)
    * Disadvantages of TCP
      * Requires a reliable connection between the two devices, so if one small chunk of data is not received, then the entire chunk of data cannot be used
      * A slow connection can bottleneck another device as the connection will be reserved on the receiving computer the whole time
      * TCP is much slower than UDP because more work has to be done by devices using this protocol
  * UDP is a connectionless protocol. It's suitable for protocols that rely on fast queries, such as DNS, for protocols that prioritise real-time communications, such as audio/video conferencing and streaming/broadcast, and for protocols used for discovering devices such as ARP and DHCP use UDP
    * Advantages of UDP
      * Much faster than TCP
      * Leaves the application layer to decide if there is any control over how quickly packets are sent
      * Does not reserve a continuous connection on a device like TCP does
    * Disadvantages of UDP
      * Doesn't care if the data is received
      * Because it doesn't reserve a continuous connection, unstable connections result in a terrible experience for the user
     
## Network Layer
* Where routing and the re-assembly of data (from small chunks to large chunks) occur
* Routing: determines the most optimal path in which of these chunks of data should be sent
* OSPF (Open Shortest Path First) protocol & RIP (Routing Information Protocol) determine the "optimal" path that data should take to reach a device
* Factors that decide which path to take include:
  * What path is the shortest? (ex: has the least amount of devices that the packet needs to travel across)
  * What path is the most reliable? (ex: have packets been lost on that path before?)
  * Which path has the faster physical connection? (ex: is one path using a copper connection (slower) or a fibre (considerably faster))
* IP addresses are dealt with at this layer
* Devices such as routers capable of delivering packets using IP addresses are known as Layer 3 devices

## Data Link Layer
* This layer focuses on the physical addressing of the transmission
* It receives a packet & IP address for the remote computer from the network layer and adds in the physical MAC address of the receiving endpoint
* Inside every network-enabled computer is a Network Interface Card (NIC) which comes with a unique MAC address to identify it

## Physical Layer
* This layer refers to the physical components of the hardware used in networking (ex: ethernet cables)
* Devices use electrical signals to transfer data between each other in a binary numbering system (1's and 0's)
