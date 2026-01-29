---
title: "Performing Disk Restore"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/restore_disks.html"
last_updated: "7/22/2025"
product_version: "13.9.0.212"
---

# Performing Disk Restore


In case a disaster strikes, you can restore disks of a Nutanix AHV VM from a backup or backup snapshot. Veeam Plug-in for Nutanix AHV allows you to attach the restored disks to the original VM or any other VM in the virtual infrastructure.

|  |
| --- |
| Note |
| You cannot restore disks of volume groups attached to the VM. |

To restore disks attached to a protected VM, do the following:

1. [Launch the Virtual Disk Restore wizard](restore_disks_launch.md).
2. [Select a VM](restore_disks_select_disks.md).
3. [Select a restore point](restore_disks_restore_point.md).
4. [Configure mapping settings](restore_disks_mapping.md).
5. [Specify a reason for the restore](restore_disks_reason.md).
6. [Finish working with the wizard](restore_disks_summary.md).


