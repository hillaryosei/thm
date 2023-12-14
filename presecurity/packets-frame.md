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
* Examples of TCP packets include:
  * Source Port: value is the port opened by the sender to send the TCP packet from. This value is chosen randomly (out of the ports from 0-65535 that aren't already in use at the time)
  * Destination Port: the port number that an application or service is running on the remote host (the one receiving data)
  * Source IP: IP address of the device that is sending the packet
  * Destination IP: IP address of the device that the packet is destined for
  * Sequence Number: random number given to the first piece of data transmitted when a connection is established
  * Acknowledgement Number: the number for the next piece of data after a piece of data is given a sequence number
  * Checksum: gives TCP integrity. A mathematical calculation is made where the output is remembered. When the receiving device performs the mathematical calculation, the data must be corrupt if the output is different from what was sent
  * Data: where the data is stored
  * Flag: determines how the packet should be handled by either device during the handshake process
