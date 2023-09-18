## Mounting an NFS share

In `/etc/fstab`:
```
<file system> <mount point> <type> <options> <dump> <pass>
192.168.55.5:/mnt/piccolo/nfs/docker-volumes /nfs rw,async,noatime,hard 0 0
```
