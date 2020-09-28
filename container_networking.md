# Container networking

Container networking stack provides some drivers for different use cases.

### Bridge driver.
- Good for development and other simple use cases.
- It is all single host
- External access requires port mapping

### Overlays
- Multi host network
- Multi host, layer two network is created so that containers on different hosts can join the same secure network.
- Container only.

### MAC villans
- Allows you to put containers into existing VLANs.
- Gives containers its own MAC and IP address.
- Requires promiscuous mode

## Built in network services

### Service discovery

Service discovery makes every service on the swarm discoverable through built in swarm DNS

### Load balancing.

- Load Balancers makes every node in the swarm know about every service.
- Lets us point external load balancers at any node in the swarm.
- Whichever node is chosen, the intended service is present.