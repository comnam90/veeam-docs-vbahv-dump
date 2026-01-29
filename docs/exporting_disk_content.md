---
title: "Exporting Disks"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/exporting_disk_content.html"
last_updated: "10/28/2025"
product_version: "13.9.0.212"
---

# Exporting Disks


Veeam Plug-in for Nutanix AHV allows you to export disks, that is, restore disks from Nutanix AHV VM backups and convert them to the VMDK, VHD and VHDX formats. You can save the exported disks to any server added to the backup infrastructure or place the disks on a datastore connected to an ESXi host (for the VMDK disk format only). For more information, see the Veeam Backup & Replication User Guide, section [Disk Export](https://helpcenter.veeam.com/docs/vbr/userguide/disk_export.html?ver=13).

To export disks of a Nutanix AHV VM, do the following:

1. In the Veeam Backup & Replication console, open the Home view.
2. In the inventory pane, select Backups.
3. In the working area, expand the necessary backup job, right-click the VM that contains disks you want to export and select Export content as virtual disks.

Alternatively, expand the necessary backup job, select the VM and click Export Disks on the ribbon.

1. Complete the Export Disk wizard as described in the Veeam Backup & Replication User Guide, section [Exporting Disks](https://helpcenter.veeam.com/docs/vbr/userguide/exporting_disks.html?ver=13).

[![Exporting Disks](images/export_disk_content.webp)](images/export_disk_content.webp "Exporting Disks")


