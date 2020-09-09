# Working with containers

- Containers are isolated application, execution environmenn - An environment for apps.

- Containers are a bunch of group namespaces that look and feel like a standalone OS

- Containers are OS specific
    - Linux containers should not run on windows and vice versa since containers do not contain a kernel, they can only use the kernal of the host

Containers are a thin writable layer that gets lashed on top of a read only image that use union mounts and copy on writes.

Containers need to be ephemral and immutable. 
- Ephemral - Shortlived
- Immutable - Once they are deployed, we should leave them alone

If you want to fix a container - you should build a new image and deploy another version.

