Docker NFS Server
================

Usage
----
```bash
docker run -d --name nfs --privileged cpuguy83/nfs-server /path/to/share /path/to/share2 /path/to/shareN
```

```bash
docker run -d --name nfs-client --privileged --link nfs:nfs cpuguy83/nfs-client /path/on/nfs/server:/path/on/client
``` 

Troubleshooting
---------------

1. `modprobe nfs` to ensure the kernel module is loaded
1. `service nfs start` to ensure nfs services are running on the host


More Info
=========

See http://www.tech-d.net/2014/03/29/docker-quicktip-4-remote-volumes/
