# LVM Management on RHEL 6 - Commands Reference

This document contains all the commands used to configure and manage Logical Volume Manager (LVM) on Red Hat Enterprise Linux 6 (RHEL 6).

---

# Verify Available Disks

Check the available disks before creating LVM.

```bash
fdisk -l
```

```bash
lsblk
```

---

# Create Physical Volume (PV)

Create a Physical Volume on the additional disk.

```bash
pvcreate /dev/sdb
```

Verify the Physical Volume.

```bash
pvs
```

```bash
pvdisplay
```

---

# Create Volume Group (VG)

Create a Volume Group using the Physical Volume.

```bash
vgcreate vg_data /dev/sdb
```

Verify the Volume Group.

```bash
vgs
```

```bash
vgdisplay
```

---

# Create Logical Volume (LV)

Create a 2 GB Logical Volume.

```bash
lvcreate -L 2G -n lv_data vg_data
```

Verify the Logical Volume.

```bash
lvs
```

```bash
lvdisplay
```

---

# Create File System

Format the Logical Volume using the ext4 file system.

```bash
mkfs.ext4 /dev/vg_data/lv_data
```

---

# Create Mount Point

```bash
mkdir /lvm_data
```

---

# Mount Logical Volume

```bash
mount /dev/vg_data/lv_data /lvm_data
```

Verify the mount.

```bash
df -h
```

```bash
mount
```

---

# Configure Permanent Mount

Edit the fstab file.

```bash
vi /etc/fstab
```

Add the following entry.

```text
/dev/vg_data/lv_data   /lvm_data   ext4   defaults   0   0
```

Apply the changes.

```bash
mount -a
```

Verify.

```bash
df -h
```

---

# Extend Logical Volume

Increase the Logical Volume by 1 GB.

```bash
lvextend -L +1G /dev/vg_data/lv_data
```

Resize the ext4 file system.

```bash
resize2fs /dev/vg_data/lv_data
```

Verify.

```bash
df -h
```

```bash
lvs
```

---

# Reduce Logical Volume

Unmount the file system.

```bash
umount /lvm_data
```

Check the file system.

```bash
e2fsck -f /dev/vg_data/lv_data
```

Resize the file system.

```bash
resize2fs /dev/vg_data/lv_data 2G
```

Reduce the Logical Volume.

```bash
lvreduce -L 2G /dev/vg_data/lv_data
```

Mount the Logical Volume again.

```bash
mount /dev/vg_data/lv_data /lvm_data
```

Verify.

```bash
df -h
```

---

# Verification Commands

Verify Physical Volumes.

```bash
pvs
```

Verify Volume Groups.

```bash
vgs
```

Verify Logical Volumes.

```bash
lvs
```

Detailed Physical Volume information.

```bash
pvdisplay
```

Detailed Volume Group information.

```bash
vgdisplay
```

Detailed Logical Volume information.

```bash
lvdisplay
```

Verify mounted file systems.

```bash
df -h
```

```bash
mount
```

---

# Useful Troubleshooting Commands

Check available block devices.

```bash
lsblk
```

Check UUID information.

```bash
blkid
```

View the fstab configuration.

```bash
cat /etc/fstab
```

Check mounted file systems.

```bash
mount
```

Check disk usage.

```bash
df -h
```

---

# Notes

- Operating System: Red Hat Enterprise Linux 6 (RHEL 6)
- Physical Volume: /dev/sdb
- Volume Group: vg_data
- Logical Volume: lv_data
- Mount Point: /lvm_data
- File System: ext4
