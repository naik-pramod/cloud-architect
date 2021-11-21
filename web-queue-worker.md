# Web-Queue-Worker
![Web-Queue-Worker!](/images/web-queue-worker.png)

- Web front end that serves client requests
- worker that performs resource-intensive tasks, long-running workflows, or batch jobs.
- The web front end communicates with the worker through a message queue  
  The worker can be triggered by messages on the queue


  ## When to use this architecture
  Typically implemented using managed compute services, either Azure App Service or Azure Cloud Services

- Applications with a relatively simple domain.
- Applications with some long-running workflows or batch operations.
- When you want to use managed services, rather than infrastructure as a service (IaaS).

## Benefits
- Relatively simple architecture that is easy to understand.
- Easy to deploy and manage.
- Clear separation of concerns.
- The front end is decoupled from the worker using asynchronous messaging.
- The front end and the worker can be scaled independently.

## Challenges
- Without careful design, the front end and the worker can become large, monolithic components that are
difficult to maintain and update. 

## Best Practices
![Web-Queue-Worker!](/images/web-queue-worker-example.png)
- Expose a well-designed API to the client.  
- Autoscale to handle changes in load.  
- Cache semi-static data. 
- Use a CDN to host static content. 
- Use polyglot persistence when appropriate. 
- Partition data to improve scalability, reduce contention, and optimize performance

