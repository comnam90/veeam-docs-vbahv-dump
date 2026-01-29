---
title: "Viewing Backup Properties"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/view_backup_properties.html"
last_updated: "11/18/2025"
product_version: "13.9.0.212"
---

# Viewing Backup Properties


After a backup job successfully creates a backup of a Nutanix AHV VM according to the specified schedule, or after you create an active full backup of a VM manually, the backup is displayed under the Backups node in the Home view of the Veeam Backup & Replication console. Each backup and the collection of restore points created for this backup is represented with a set of properties, such as:

* Object Name — the name of a protected VM.
* Original Size — the total amount of disk space allocated to the VM.
* File Name — the name of a restore point.
* Data Size — the amount of processed VM data.
* Backup Size — the amount of backed-up VM data.
* Data Reduction — the ratio between the data size and backup size.
* Date — the date and time when the restore point was created.
* Immutable Until — the date when the immutability period for the restore point will expire.
* Status — the result of the most recent [malware scan](verify_backups.md) performed for the restore point.

|  |
| --- |
| Tip |
| If a restore point is marked as Infected but you know that this point is clean, you can change its status manually. To do that, select the restore point and click Malware > Mark as clean. To learn how to manage infected restore points, see Veeam Backup & Replication User Guide, section [Managing Malware Status](https://helpcenter.veeam.com/docs/vbr/userguide/malware_detection_managing_status.html?ver=13). |

To view backup properties, do the following:

1. In the Veeam Backup & Replication console, open the Home view.
2. In the inventory pane, select Backups.
3. In the working area, right-click the backup job name and select Properties.

[![Viewing Backup Properties](images/backup_properties.webp)](images/backup_properties.webp "Viewing Backup Properties")


