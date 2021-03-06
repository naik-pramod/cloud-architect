### Hybrid Network

Networks that connect on-premises resources and virtual resources are known as hybrid networks
In a hybrid model, we must ensure that communication between the on-premises environment and Azure workloads is both secure and reliable.

#### How do we connect hybrid networks
We use VPN - Virtual Private Network
VPNs use an encrypted tunnel within another network.
They are typically deployed to connect two or more trusted private networks to one another over an untrusted network, usually the public Internet.

#### VPN Gateways
VPN Gateway is used to :
 - integrate your on-premises network with Azure.
 - integrate your virtual networks in Azure.

A VPN gateway can send encrypted traffic between the two networks.

Within each virtual network gateway there are two or more virtual machines (VMs).

These VMs have been deployed to a special subnet that you specify, called the gateway subnet. 

They contain routing tables for connections to other networks, along with specific gateway services

#### Topologies using VPN Gateways

- Site-to-Site

  ![site-to-site!](/networking/az-networks/images/site-to-site.PNG)



- Multi-Site 

  ![multi-site!](/networking/az-networks/images/multi-site.PNG)





- Point-to-Site 

  ![point-to-site!](/networking/az-networks/images/point-to-site.PNG)

#### Design and implement Azure VPN Gateway

- We need 
