# Working With Images

## Images

An image is a template for starting containers
- It is Read Only
- It is built by stacking layers
- The storage drivers make it look like a normal file system.
- It is a config file and a bunch of indipendent layers

```
Inside the layers are where all the application binaries, filed, libraries and etc are.

Config file has the instruction on how to run it as a container
```

Each container has its own thin writable layer where it stores changes and they can be linked back to a single image.

The data inside the layers never change as they are `Read Only`. If a container wants to change a file in one of them, then instead of editing, it makes a copy.
- The container finds an image from whatever layer it is in, copies it up to its container layer and makes the change there

## Registries

Images are housed in Registries which can be on cloud or on premisis

When an image is pulled to the host it stays in a local registry. eg:
- linux: `/var/lib/docker/<storage-driver>`
- windows: `c:\ProgramData\docker\windowsfilter`

### Content Addressable Storage Model

A content addressable storage model lets you run a cryptagraphic algorithm over the contents of a layer and using the hash that is found as the layer's ID mking the images in the layers immutable.

The Image ID is a hash of the image config file.

Make a change to the image config or any of the layers and the hashes will change.

### Pushing to registries

When images are pushed to registries, they are compressed, changing the content inside the images. Therefore, a second hash is needed so that it can be used with a registry for now.

some commands:

```bash
docker image push
```
Upload from a remote registry

```bash
docker image pull
```
Download from a remote registry

```bash
docker image inspect
```

This command gives the image config, including the layer data listed by content hash

```bash
docker image rm
```

Removes old images