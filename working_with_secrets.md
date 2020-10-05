# Worknig With Secrets

- Docker secrets is a safe and secure way to publish secrets, such as passwords, to applications

- It is platform independent

## Create a service.

- To create a service use this command:

```bash
$ docker service create
```

- The secret can only be a string of up to 500kb in size.

- After the Secret is created, it is sent to a swarm over a secured network connection.

## Where is the secret?

When the secret is sent to the swarm it is placed in the raft consensus group (this group is where the manager nodes are.) where it is encrypted at rest.

## Creating or updating a service.

When updateing or creating a service and for the service to contain the secret, the specific secret must be authoised. This causes the control plane to send it to nodes in the swarm that are running replicas for that service.

The secrets are encrypted in flight.

```bash
$ docker service create --name <name_of_service> --secret <name_of_secret> --replicas <amount_of_replicas>
```