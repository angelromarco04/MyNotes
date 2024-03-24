---
Author: AAM
Date: 2024-03-15
tags:
  - linux
  - other
---
# Manual mounting

```bash
sudo lsblk
sudo mount /dev/sdb1 /mnt
```
# Automatic mounting

```bash
sudo blkid
sudo nano /etc/fstab
sudo mount -a
```

# Unmounting