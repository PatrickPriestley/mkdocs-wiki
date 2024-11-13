---
sidebar_label: 'How to resize a disk'
sidebar_position: 2
---
# How to resize an ubuntu vm disk in proxmox
#### A quick guide for resizing (increasing the size of a disk) 
## Changes within the Proxmox VM UI 
1. Shutdown VM 
2. Go to VM 
3. Go to Hardware 
4. Select ```Hard Disk``` 
5. From the top nav, select ```Disk Action``` then ```Resize``` 
6. Enter the amount you want to increase the disk by 
7. Start the VM 

## Changes within the Ubuntu VM
1. ssh into VM
2. run ```cfdisk``` (free space should be available)
3. select disk to resize
4. select Resize and Enter
5. select Write and Enter
6. hit Q to quit
7. Run ```sudo resize2fs /dev/vda2``` (replace ```/dev/vda2``` with correct disk name)
8. Confirm changes by running df -h
