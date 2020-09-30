# Working with volumes and persistent data

All containers are given a little piece of local driver storage. It is what stacks the image layers and adds the writable container layer. However, it is bound to the container and if the container is deleted, the storage is gone too. Persistent data is needed and here is where volumes come in.

## Volumes

- Volumes stay outside the driver and have a lifecycle outside the container.
- Even if the container is deleted, the volume will stay.
- It can be attatched to any container.

```bash
$ docker volume create | ls | inspect...
```

These are some of the commands that manage the volumes