* What is Networking?
  * Network are devices connected and can be formed by anywhere from 2 devices to 2 billion
 
* What is the Internet?
  * The Internet is a giant network made of smaller networks
    * These smaller networks can be placed into two categories: private network and public network
  * First iteration of the Internet was created in the late 60s within the US DoD-funded project ARAPNET
  * The "modern" Internet invented by Tim Berners-Lee by the creation of the World Wide Web
 
* Identifying Devices on a Network
  * Device's two types of identification: IP addresses & MAC addresses
    * IP (Internet Protocol) address: way of identifying a host on a network for a period of time, consists of a set of numbers that are divided into four octets
      * Each octet is a number 0-255, calculated through IP addressing & subnetting
      * Public address: used to identify the device on the Internet, given by your ISP (Internet Service Provider)
      * Private address: used to identify a device amongst other devices
      * There is a shortage of IPv4 addresses. There are 2**32 billion IP addresses, and it is estimated that there would be ~50 billion devices conencted to the internet
        * IPv6 addresses this shortage by supporting up to 2**128 addresses
    * MAC (Media Access Control) address: unique address assigned to physical network interfaces (microchip board found on the device's motherboard) by the vendor who created the interface
      * Is 12 characters, consisting of hexadecimal numbers split into 2 and separated by colons
        * The first 6 characters represent the company that created the network interface, the last 6 are unique numbers
      * Can be spoofed (when a networked device pretends to identify as another using its MAC address) and break poorly implemented security designs that assume that devices talking on a network are trustworthy 

* Ping (ICMP)
  * Ping uses ICMP (Internet Control Message Protocol) packets to determine performance of a connection between devices
  * Ping: measures time taken for ICMP packets travelling between devices
  * How to do a ping: `ping [IP address or website URL]` 
