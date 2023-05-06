# DevOps Tooling Website Solution

 ## A.  **Preparing The NFS Server**

> I utilised AWS EC2 as my server for this project. 

1. I created 3 additional volumes and attched them to the NFS server.

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/main/6.%20Project%206%20Web%20Solution%20with%20WordPress/Volumes.png)

2. I used the `gdisk` utility to create a single partition on each of the 3 disks attached to the NFS Server.
 ```bash 
sudo gdisk /dev/xvdf
```
3. I ran the `lsblk` command to view the newly configured partition on each of the 3 disks on both servers.

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/main/6.%20Project%206%20Web%20Solution%20with%20WordPress/DrivesPartitioned.png)

4. I installed the `lvm2` utility by running;
```bash
sudo yum install lvm2
```
I then checked for avalable partitons by running;
```bash 
sudo lvmdiskscan
```
5.  I used the `pvcreate` utility to mark each of 3 disks as physical volumes (PVs) to be used by LVM.

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/main/6.%20Project%206%20Web%20Solution%20with%20WordPress/PhysicalVolumes.png)


![Screenshot](https://github.com/ardamz/PersonalDemos/blob/main/6.%20Project%206%20Web%20Solution%20with%20WordPress/SudoPvs.png)
> I verified creation PVs by running ` sudo pvs`

6.  I used the `vgcreate` utility to add all 3 PVs to a volume group (VG) called `nfsdata-vg`

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/main/6.%20Project%206%20Web%20Solution%20with%20WordPress/VGCreate.png)

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/main/6.%20Project%206%20Web%20Solution%20with%20WordPress/SudoVGS.png)

7. On the Web Server, I used th `lvcreate` utility to create 2 logical volumes. apps-lv (using half of the PV size), and logs-lv using the remaining space of the PV size. 

```bash
sudo lvcreate -n apps-lv -L 9.7G nfsdata-vg
sudo lvcreate -n logs-lv 9.7G nfsdata-vg
sudo lvcreate -n opt-lv 9.7G nfsdata-vg
```
# apps-lv will be used to store data for the Website while, logs-lv will be used to store data for logs.

<!---
apps-lv will be used to store data for the Website while, logs-lv will be used to store data for logs.
-->


[apps-lv will be used to store data for the Website while, logs-lv will be used to store data for logs.]: #

apps-lv will be used to store data for the Website while, logs-lv will be used to store data for logs.