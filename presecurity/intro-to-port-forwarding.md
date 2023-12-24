## Introduction to Port Forwarding
* Port forwarding helps connect applications and services to the Internet. Without it, applications and services would only be available to
devices within the same network
* Port forwarding opens specific ports and firewalls determine whether traffic can go through these ports
* Port forwarding is configured at the router

## Firewalls 101
* Firewall: device within a network responsible for determining what traffic is allowed to enter and exit
* Firewalls operate on Layer 3 and Layer 4 of the OSI model
* Administrators can configure a firewall to permit or deny traffic based on numerous factors:
  * Where is the traffic coming from?
  * Where is the traffic going to?
  * What port is the traffic for?
  * What protocol is the traffic using?
* Here are the primary categories of firewall:
  * Stateful: determines the behaviour of a device based upon the entire connection, consumes many resources in comparison to stateless firewalls,
if a connection from a host is bad, it will block the entire device
  * Stateless: uses a static set of rules to determine whether or not individual packets are acceptable or not, use much fewer resources but are only
effective as the rules that are defined within them, are good when receiving large amounts of traffic from a set of hosts

## VPN Basics
* Virtual Private Network (VPN): technology that allows devices on separate networks to communicate securely by creating a dedicated path between
each other over the Internet (known as a tunnel)
* Benefits of using a VPN:
  * Allows networks in different geographical locations to be connected
  * Offers privacy
  * Offers anonymity
* Examples of VPN technologies:
  * PPP: used by PPTP to allow for authentication and provide encryption of data. works by using a private key and public certificate that must match
before connecting. it is non-routable (not capable of leaving a network by itself)
  * Point-to-Point Turning Point (PPTP): technology that allows the data from PPP to travel and leave a network, very easy to set up and is supported by most devices
but is weakly encrypted 
  * Internet Protocol Security (IPSec): encrypts data using the existing IP framework. it's difficult to set up, but when it is, it has strong encryption and is
supported on many devices

## LAN Networking Devices
* 
