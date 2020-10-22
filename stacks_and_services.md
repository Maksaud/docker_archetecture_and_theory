# Deploying in production with stacks and services

## Stacks
Apps are a collection of smaller services put together and become usefull

In docker, the apps are made of containers that are run as services and they are grouped into stacks.

A stack is aa bunch of services that make up the app and is defined in a YAML file.

## YAML
The YAML file would compose the stack.

Version 3 must be used in the YAML file spec.

Stacks must be in swarm mode

## To Deploy

with the YAML file ready, use the command:

```bash
docker stack deploy
```

This command records the desired state of the app on the cluster.

Then deploys the app which includes all the services, networks, volumes and etc.

## Background reconciliation loops

This allows swarm to manage the app because of the notion of desired state. 