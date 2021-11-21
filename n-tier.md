# N-Tier

![N-Tier!](/images/n-tier.png)

- Each layer has specific functionality
- A higher layer like Web Tier can use services of lower layer like middle layer, but not the other way
- Tiers are physically seperated, running on different machines.
- Physically seperating tier improves scalability and resilence but adds latency.

## When to use this architecture
N-tier architectures are typically implemented as infrastructure-as-service (IaaS) applications, with each tier
running on a separate set of VMs.

### Consider an N-tier architecture for:
- Simple web applications.
- Migrating an on-premises application to Azure with minimal refactoring.
- Unified development of on-premises and cloud applications.

### Benefits
- Portability between cloud and on-premises, and between cloud platforms.
- Less learning curve for most developers.
- Natural evolution from the traditional application model.
- Open to heterogeneous environment (Windows/Linux)

### Challenges
- It's easy to end up with a middle tier that just does CRUD operations on the database, adding extra latency
without doing any useful work.
- Monolithic design prevents independent deployment of features.
- Managing an IaaS application is more work than an application that uses only managed services.
- It can be difficult to manage network security in a large system.

### Best Practices
- Use autoscaling to handle changes in load.
- Use asynchronous messaging to decouple tiers.
- Cache semistatic data.
- Configure the database tier for high availability
- Place a web application firewall (WAF) between the front end and the Internet.
- Place each tier in its own subnet, and use subnets as a security boundary.
- Restrict access to the data tier, by allowing requests only from the middle tier(s).

## Example : N-tier architecture running on VMs
![N-Tier!](/images/n-tier-example.png)

- Each tier consists of two or more VMs, placed in an availability set or virtual machine scale set.
- Each tier is also placed inside its own subnet, meaning their internal IP addresses fall within the same address
range.
- The web and business tiers are stateless. Any VM can handle any request for that tier. The data tier should
consist of a replicated database.
- Network security groups restrict access to each tier. For example, the database tier only allows access from the
business tier.

