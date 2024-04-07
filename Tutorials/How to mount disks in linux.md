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