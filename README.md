# ipsec-tunnel-create
This skillet will take input variables and configure an IPSec Tunnnel and IKE Gateway.  

Limitations:  This particular skillet is designed to configure IPv4 routes and gateways and would need to be adapted to support IPv6.  It is also designed to configure static tunnel routes, but dynamic configuration can be added using a dynamic routing skillet.  Authentication is designed to be handled with a preshared key and if ProxyIDs are necessary, they must be added after the skillet is deployed.    

The skillet supports use of the following variables, each of which have default values that support the most common tunnel configurations:

ike_gateway_name - Name for the IKE Gateway

ike_version - List of IKEv1, IKEv2, or IKEv2-Preferred

local_interface - IKE Interface on the local firewall

local_interface_address - IKE Interface address on the local firewall

peer_address - IKE Peer Address

preshared_key - Preshared Key in plaintext 

remote_network_tunnel_route - The Destination Network/CIDR routed into the IPSec tunnel.

tunnel_interface - The tunnel interface (tunnel.Number)

tunnel_interface_zone - Zone applied to the Tunnel Interface (must exist)

tunnel_route_name - Name for the route-based tunnel route

virtual_router_name - Name of the virtual router (must exist)

vsys - VsysID
