* Introduction to LAN Topologies
  * LAN (Local Area Network) 
  * Star Topology
    * Pros: commonly used because of its reliability and scalability
    * Cons: more expensive because it requires more cabling and purchase of dedicated network equipment, requires more maintenance to keep it functional, still prone to failure
  * Bus Topology
    * Relies on a single connection (backbone cable)
    * Pros: one of the easier and more cost-efficient topologies to set up
    * Cons: little redundancy in place in case of failures because of its backbone cable, prone to become slow and bottlenecked if devices within the topology are simultaneously requesting data, difficult to troubleshoot
  * Ring/Token Topology
    * Devices are connected directly to each other to form a loop, meaning that there is little cabling required and less dependence on dedicated hardware
    * Sends data across the loop until it reaches the destined device, using other devices along the loop to forward the data
    * Pros: less prone to bottlenecks
    * Cons: isn't an efficient way of data travelling across a network because it goes in one direction, a fault (ex: cut cable, broken device) results in the entire networking breaking
  * Switches
    * Dedicated devices within a network that are designed to aggregate multiple other devices such as computers, printers, or any other networking-capable device using ethernet
    * Keep track of what device is connected to which port
    * Can connect a large number of devices by having ports of 4, 8, 16, 24, 32, and 64 for devices to plug into
  * Routers
    * Connect networks and pass data between them
    * Routing: process of data travelling across networks, involves creating a path between networks so that this data can be successfully delivered
   
* A Primer on Subnetting
 * Subnetting: splitting up a network into smaller, miniature networks within itself
 * Network admins use subnetting to categorize and assign specific parts of a network
 * Subnets use IP addresses to identify the network address, host address, and default gateway
 * Network address: identifies the start of the actual network; used to identify a network's existence
 * Host address: used to identify a device on the subnet
 * Default gateway: special address assigned to a device on the network that is capable of sending information to another network
 * Benefits of subnets: efficiency, security, and control
 * There are 32 bits in a subnet mask

* The ARP Protocol
 * ARP (Address Resolution Protocol): responsible for allowing devices to identify themselves on a network; allows a device to associate its MAC address with an IP address on the network
 * Each device keeps track of the MAC addresses associated with other devices
 * How ARP works
  * Each device within a network has cache (ledger to store information)
  * For ARP protocol, cache stores the identifiers of other devices on the network
  * To map these identifiers, ARP protocol sends out two messages: ARP request & ARP reply
   * When an ARP request is sent, a message is broadcasted to every other device found on a network by the device, asking whether the device's MAC address matches the requested IP address
   * ARP reply is returned to the initial device if the device does have the requested IP address. It will also now remember this and store it within its cache (an ARP entry)

* The DHCP Protocol
 * IP addresses can be assigned manually, by entering them into a device, or automatically by using DHCP (Dynamic Host Configuration Control)
 * If a device is connected to a network and has not been manually assigned an IP address, a request is sent (DHCP discover) to see if any DHCP servers are on the network
 * DHCP server responds with an IP address the device can use (DHCP offer)
 * Device sends reply confirming it wants the offered IP address (DHCP request)
 * DHCP server responds acknowledging request and device starts using IP address (DHCP ACK)



