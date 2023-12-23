## What are Packets and Frames
* Packets and frames are small pieces of data that, when forming together, make a larger piece of information or message
* A frame is part of the second layer of the OSI model, data link layer, meaning it has no information such as IP addresses
* Packets are an efficient way of communicating data across networked devices. Because of its small size, there is a small chance of bottlenecking occurring across a network. It also has IP addressing information
* Packets using the Internet Protocol will have a set of headers that contain additional pieces of information to the data that is being sent across a network
* Examples of these packet headers include:
  * Time to Live: sets an expiry timer for the packet to not clog up your network if it never manages to reach a host or escape
  * Checksum: provides integrity checking for protocols such as TCP/IP. If any data is changed, this value will be different from what was expected and therefore corrupt
  * Source Address: IP address of the device that the packet is being sent from so that data knows where to return to
  * Destination Address: device's IP address the packet is being sent to so that data knows where to travel next
 
## TCP/IP Three-Way Handshake
* TCP packets contain various sections of information known as headers that are added from encapsulation
* Examples of crucial TCP packets include:
  * Source Port: value is the port opened by the sender to send the TCP packet from. This value is chosen randomly (out of the ports from 0-65535 that aren't already in use at the time)
  * Destination Port: the port number that an application or service is running on the remote host (the one receiving data)
  * Source IP: IP address of the device that is sending the packet
  * Destination IP: IP address of the device that the packet is destined for
  * Sequence Number: random number given to the first piece of data transmitted when a connection is established
  * Acknowledgement Number: the number for the next piece of data after a piece of data is given a sequence number
  * Checksum: gives TCP integrity. A mathematical calculation is made where the output is remembered. When the receiving device performs the mathematical calculation, the data must be corrupt if the output is different from what was sent
  * Data: where the data is stored
  * Flag: determines how the packet should be handled by either device during the handshake process
* Three-way handshake: process of establishing a connection between 2 devices. Here are ways the three-way handshake communicates:
  * SYN: the initial packet sent by client that's used to synchronize two devices together
  * SYN/ACK: packet sent by the server to acknowledge the synchronization attempt from the client
  * ACK: packet used by the client or server to acknowledge that a series of messages/packets have been received successfully
  * DATA: data is sent once a connection is established
  * FIN: packet used to properly close connection after it's complete
  * RST: packet that ends all communication. it indicates that there were some problems in the closing process
* Any sent data is given a random number sequence and is reconstructed using this number sequence and incrementing by 1

## UDP/IP
* UDP is a stateless protocol, unlike TCP
* UDP headers include:
  * Time to Live (TTL): sets an expiry timer for the packet so the network isn't clogged
  * Source address: IP address of the device that the packet is being sent from
  * Destination address: device's IP address the packet is being sent to
  * Source port: port that's opened by the sender to send the UDP packet from. value is randomly chosen (out of the ports from 0-65535 that aren't already in use at the time)
  * Destination port: port number that an application or service is running on the remote host (the one receiving the data). value is not randomly chosen
  * Data: header is where data is stored
 
## Ports 101
* Networking devices use ports to set restrictions when communicating with one another
* When a connection has been established, any data sent or received by a device will be sent through these ports
* Some common ports include:
  * File Transport Protocol (FTP) - 21: used by a file-sharing application built on a client-server model, meaning you can download files from a central location
  * Secure Shell (SSH) - 22: used to securely login to systems via a text-based interface for management
  * HyperText Transfer Protocol (HTTP) - 80: powers the World Wide Web. browser uses this to download text, images and videos of web pages
  * HyperText Transfer Protocol Secure (HTTPS) - 443: does the same with as port 80, but securely using encryption
  * Server Message Block (SMB) - 445: functions similar to FTP/port 21, but allows you to share devices like printers
  * Remote Desktop Protocol (RDP) - 3389: secure means of logging in to a system using a visual desktop interface
