# LVM Management on RHEL 6

## 📌 Project Overview

This project demonstrates the implementation and administration of **Logical Volume Manager (LVM)** on **Red Hat Enterprise Linux 6 (RHEL 6)**. LVM is a storage management technology that provides flexibility in allocating disk space compared to traditional disk partitioning.

In this project, an additional hard disk was configured as a **Physical Volume (PV)**, grouped into a **Volume Group (VG)**, and used to create a **Logical Volume (LV)**. The logical volume was formatted with the **ext4** file system, mounted to the system, and configured for permanent mounting. The project also demonstrates extending and reducing logical volumes along with resizing the file system while maintaining data integrity.

This hands-on project helped strengthen practical knowledge of Linux storage administration, disk management, and troubleshooting.

---

# 🎯 Project Information

**Project Name:** LVM Management on RHEL 6

**Operating System:** Red Hat Enterprise Linux 6 (RHEL 6)

**Technology:** Logical Volume Manager (LVM)

**File System:** ext4

**Project Type:** Linux System Administration

**Tools Used:**

- LVM Utilities
- Linux Command Line
- ext4 File System
- fdisk
- mount
- resize2fs

---

# 🎯 Objective

The primary objective of this project is to understand and implement Logical Volume Manager (LVM) for efficient storage management in Linux.

The project includes:

- Creating Physical Volumes (PV)
- Creating Volume Groups (VG)
- Creating Logical Volumes (LV)
- Formatting Logical Volumes with the ext4 file system
- Mounting Logical Volumes
- Configuring permanent mounting using `/etc/fstab`
- Extending Logical Volumes without data loss
- Resizing the file system after extending storage
- Reducing Logical Volumes safely
- Verifying the complete LVM configuration

---

# 🖥️ Environment

- Operating System: Red Hat Enterprise Linux 6 (RHEL 6)
- Storage Management: Logical Volume Manager (LVM)
- File System: ext4
- Additional Disk: Virtual Hard Disk
- User: Root

---

# 📋 Prerequisites

Before starting this project, the following requirements were completed:

- Installed Red Hat Enterprise Linux 6
- Root user access
- Additional virtual hard disk attached
- Basic knowledge of Linux commands
- Available free disk space for LVM configuration

---

# ⚙️ Project Workflow

### Step 1 – Verify Available Disks

Verified the available storage devices using Linux disk management commands.

### Step 2 – Create Physical Volume (PV)

Initialized the additional disk as a Physical Volume using the `pvcreate` command.

### Step 3 – Create Volume Group (VG)

Created a Volume Group by combining the available Physical Volume.

### Step 4 – Create Logical Volume (LV)

Allocated storage from the Volume Group to create a Logical Volume.

### Step 5 – Create File System

Formatted the Logical Volume using the ext4 file system.

### Step 6 – Create Mount Point

Created a directory that acts as the mount point for the Logical Volume.

### Step 7 – Mount Logical Volume

Mounted the formatted Logical Volume to make it accessible by the operating system.

### Step 8 – Configure Permanent Mount

Updated the `/etc/fstab` file so that the Logical Volume is automatically mounted after every system reboot.

### Step 9 – Extend Logical Volume

Extended the size of the Logical Volume by allocating additional free space from the Volume Group.

### Step 10 – Resize File System

Resized the ext4 file system to utilize the newly allocated storage space.

### Step 11 – Reduce Logical Volume

Safely reduced the size of the Logical Volume after checking the file system integrity.

### Step 12 – Verify Configuration

Verified the complete LVM configuration using Linux administration commands.

---

# ✅ Testing

The following tests were performed successfully:

- Verified Physical Volume creation
- Verified Volume Group creation
- Verified Logical Volume creation
- Successfully formatted the Logical Volume
- Mounted the Logical Volume successfully
- Configured permanent mounting
- Extended the Logical Volume
- Resized the file system successfully
- Reduced the Logical Volume safely
- Verified updated storage capacity
- Confirmed all mounted file systems

---

# 📂 Project Structure

```
LVM-Management-on-RHEL6/
│── README.md
│── commands.md
│── screenshots/
│── scripts/
│── architecture/
```

---

# 🛠️ Commands Used

The following Linux commands were used during this project:

- fdisk
- lsblk
- pvcreate
- pvs
- pvdisplay
- vgcreate
- vgs
- vgdisplay
- lvcreate
- lvs
- lvdisplay
- mkfs.ext4
- mkdir
- mount
- umount
- df
- blkid
- lvextend
- lvreduce
- resize2fs
- e2fsck
- cat
- vi

> Complete command details are available in the **commands.md** file.

---

# 🎯 Expected Output

After completing this project:

- Physical Volume created successfully.
- Volume Group created successfully.
- Logical Volume created successfully.
- ext4 file system created successfully.
- Logical Volume mounted successfully.
- Permanent mounting configured.
- Logical Volume extended successfully.
- File system resized successfully.
- Logical Volume reduced safely.
- Storage configuration verified successfully.

---

# 📚 Skills Demonstrated

- Linux Administration
- Red Hat Enterprise Linux 6
- Logical Volume Manager (LVM)
- Linux Storage Administration
- Disk Partitioning
- Volume Management
- File System Management
- Mounting and Permanent Mount Configuration
- Storage Expansion and Reduction
- Linux Troubleshooting

---

# 🎓 Learning Outcomes

After completing this project, I gained practical experience in:

- Understanding the architecture of Logical Volume Manager (LVM).
- Managing Linux storage using PV, VG, and LV.
- Creating and formatting logical volumes.
- Mounting storage devices permanently.
- Extending storage without interrupting system operations.
- Reducing logical volumes safely.
- Resizing Linux file systems.
- Troubleshooting LVM-related issues.
- Managing Linux storage efficiently in real-world environments.

---

# 🏁 Conclusion

This project successfully demonstrates the complete implementation and management of Logical Volume Manager (LVM) on Red Hat Enterprise Linux 6. It covers the complete storage lifecycle, including Physical Volume creation, Volume Group configuration, Logical Volume management, file system creation, mounting, storage extension, storage reduction, and verification.

By completing this project, I strengthened my practical knowledge of Linux storage administration, LVM management, and system administration, which are essential skills for Linux Administrator, System Administrator, Cloud, and DevOps roles.
