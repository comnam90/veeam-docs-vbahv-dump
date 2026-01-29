---
title: "Publishing Disks"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/publish_disk.html"
last_updated: "10/28/2025"
product_version: "13.9.0.212"
---

# Publishing Disks


Veeam Backup & Replication allows you to mount specific disks of backed-up Nutanix AHV VMs to any server and to instantly access data in the read-only mode. This can be helpful when you want to copy files and folders as of a point-in-time state to the target server, and perform an antivirus scan of the backed-up data. For more information, see the Veeam Backup & Replication User Guide, section [Disk Publishing (Data Integration API)](https://helpcenter.veeam.com/docs/vbr/userguide/data_integration_api.html?ver=13).

To publish disks of a Nutanix AHV VM, do the following:

1. In the Veeam Backup & Replication console, open the Home view.
2. In the inventory pane, select Backups.
3. In the working area, expand the necessary backup job, right-click the VM that contains disks you want to mount and select Publish disks.

Alternatively, expand the necessary backup job, select the VM and click Publish disks on the ribbon.

1. Complete the Publish Disk wizard as described in the Veeam Backup & Replication User Guide, section [Publishing Disks](https://helpcenter.veeam.com/docs/vbr/userguide/publishing_disks.html?ver=13).

[![Publishing disks](images/publish_disks.webp)](images/publish_disks.webp "Publishing disks")


