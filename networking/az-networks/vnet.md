### Networks
 - Public Network : Uses Public IP addresses. example: Internet
 - Private Network : Uses Public IP addresses. example : Az VNet

#### Public IP Addresses
 - Public IP can be allocated to below resources in Azure

    Virtual machine network interfaces
    Virtual machine scale sets
    Public Load Balancers
    Virtual Network Gateways (VPN/ER)
    NAT gateways
    Application Gateways
    Azure Firewall
    Bastion Host

##### Public IP Types
 - Dynamic IP : A dynamic public IP address is an assigned address that can change over the lifespan of the Azure resource. ex: when you stop or retstart a VM, its public IP is changed by default.
 - Static IP : A static public IP address is an assigned address that will not change over the lifespan of the Azure resource. 


##### Static public IP addresses are commonly used in the following scenarios:
- When you must update firewall rules to communicate with your Azure resources.
- DNS name resolution, where a change in IP address would require updating A records.
- Your Azure resources communicate with other apps or services that use an IP address-based security model.
- You use TLS/SSL certificates linked to an IP address.

##### Limitations for IPv6
- VPN gateways cannot be used in a virtual network with IPv6 enabled, either directly or peered with "UseRemoteGateway".
- Public IPv6 addresses are locked at an idle timeout of 4 minutes.
- Azure doesn't support IPv6 communication for containers.
- Use of IPv6-only virtual machines or virtual machines scale sets aren't supported. Each NIC must include at least one IPv4 IP configuration (dual-stack).
- When adding IPv6 to existing IPv4 deployments, IPv6 ranges can't be added to a virtual network with existing resource navigation links.
- Forward DNS for IPv6 is supported for Azure public DNS. Reverse DNS isn't supported.
- Routing Preference and cross-region load-balancing isn't supported.

### NAT
NAT allows multiple companies to use the exact same private IP network, using the same IP addresses as other companies while still connecting to the Internet. 
![NAT!](/networking/az-networks/images/NAT.PNG)

## Hub and Spoke Topology

Azure Virtual Networks (VNets) are the fundamental building block of your private network in Azure

### Capabilities of Azure Virtual Networks

Azure VNets enable 
- resources in Azure to securely communicate with each other, 
- the internet, and 
- on-premises networks 
- Filtering network traffic
- Routing network traffic

