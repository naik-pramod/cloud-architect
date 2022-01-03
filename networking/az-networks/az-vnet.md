### Azure Virtual Networks
- You can use VNets:
    - To provision and manage virtual private networks (VPNs) in Azure.
    - To link the VNets with other VNets in Azure, 
    - To Link with your on-premises IT infrastructure to create hybrid or cross-premises solutions. 

- Each VNet you create has its own CIDR block and can be linked to other VNets and on-premises networks as long as the CIDR blocks do not overlap. 

### Design considerations for Azure Virtual Networks

When creating a VNet, it is recommended that you use the address ranges for private, non-routable address spaces:

10.0.0.0 - 10.255.255.255 (10/8 prefix)
172.16.0.0 - 172.31.255.255 (172.16/12 prefix)
192.168.0.0 - 192.168.255.255 (192.168/16 prefix)

**Non-routable addresses**
They are range of IPs set aside for use for anyone and these cannot be routed/accessible on internet.

Azure assigns resources in a virtual network a private IP address from the address space that you provision.

It is important to note that Azure reserves 5 IP addresses within each subnet.

These are x.x.x.0-x.x.x.3 and the last address of the subnet.
x.x.x.1-x.x.x.3 is reserved in each subnet for Azure services.

x.x.x.0: Network address
x.x.x.1: Reserved by Azure for the default gateway
x.x.x.2, x.x.x.3: Reserved by Azure to map the Azure DNS IPs to the VNet space
x.x.x.255: Network broadcast address

The number of usable IP addresses per subnet is 2^H – 5.

### Determine a naming convention

Resource Type-Workload/Application-Envionment-AzureRegion

Envionment-Subscription-Workload/Application Name-Resource Type-AzureRegion

### Analyze Subnetting and Addressing Needs

- Which hosts should be grouped together into a subnet?
- How many subnets does this internetwork require?
- How many host IP addresses does each subnet require?
- Will we use a single subnet size for simplicity, or not?