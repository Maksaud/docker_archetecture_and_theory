# Architecture and Theory of docker

`container` - Isolated area of an OS with resource usage limits applied

## Kernel primitives

Containers have 2 building blocks:

### Namespaces
- Isolation
- Take an operating system and carve them to multiple isolated virtual operating system.
    - PID, NET, Filesystem, ipc, uts, user
- All container share a single kernel on the host
- Each container do not know that the other containers exist.

        
### Control groups
- Grouping objects and setting limits
- Group processes and propose limits

## Docker Engine
- A docker engine exposes an API for us
- Interfaces all the Kernel primitives
- Then creates a container