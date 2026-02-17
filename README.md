# Day-13-Linux-Volume-Management-LVM-
What is LVM?
LVM (Logical Volume Management) is a system in Linux that allows you to create, resize, and manage disk storage easily.

LVM Structure:
1️)Physical Volume (PV)
→ Actual disk or partition (example: /dev/sdb)
2️)Volume Group (VG)
→ Collection of Physical Volumes
3️)Logical Volume (LV)
→ Virtual partition created from VG (used like normal partition)

Create Physical Volume:
pvcreate /dev/sdb
Create Volume Group:
vgcreate my_vg /dev/sdb
Create Logical Volume:
lvcreate -L 1G -n my_lv my_vg
Format LV:
mkfs.ext4 /dev/my_vg/my_lv
Mount LV:
mount /dev/my_vg/my_lv /mnt
