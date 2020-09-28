# Building A Secure Swarm

Swarm is integral to the future for Docker

There is two main parts of swarm:

## Secure Clustering
- Add nodes as managers and workers.
    - Managers are in charge of the cluster and they make all of the control plane decisions
    - Workers do the application legwork

### To build a swarm use the command:

```bash
$ docker swarm init
```

There are a lot of security things that are needed but swarm configures all the security things just by using that command.

### To add more nodes use the command:

```bash
docker swarm join
```

## Orchestrator

Swarm cluster

Deploy apps on a swarm cluster

Records the desired state of the web front end in their containers and deployes the app.
