## EBS volume size expansion script
1. Check free disk space (Size:10GB)
```
$ df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
devtmpfs       devtmpfs  474M     0  474M   0% /dev
tmpfs          tmpfs     492M     0  492M   0% /dev/shm
tmpfs          tmpfs     492M  456K  492M   1% /run
tmpfs          tmpfs     492M     0  492M   0% /sys/fs/cgroup
/dev/xvda1     xfs        10G  8.4G  1.7G  84% /
tmpfs          tmpfs      99M     0   99M   0% /run/user/1000
```
2. Run script (ex. Expand size to 50GB)
```
$ sh resize.sh 50
```
3. Check free disk space (Size:50GB)
```
$ df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
devtmpfs       devtmpfs  474M     0  474M   0% /dev
tmpfs          tmpfs     492M     0  492M   0% /dev/shm
tmpfs          tmpfs     492M  456K  492M   1% /run
tmpfs          tmpfs     492M     0  492M   0% /sys/fs/cgroup
/dev/xvda1     xfs        50G  8.5G   42G  17% /
tmpfs          tmpfs      99M     0   99M   0% /run/user/1000
```