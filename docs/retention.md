---
title: "Deleting Backups"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/retention.html"
last_updated: "8/11/2025"
product_version: "13.9.0.212"
---

# Deleting Backups


By default, Veeam Plug-in for Nutanix AHV maintains backups in backup repositories according to retention policy settings saved in the backup metadata. If Veeam Plug-in for Nutanix AHV detects that the number of restore points in the backup chain exceeds the allowed number, it automatically removes obsolete backups. If necessary, you can delete backups manually.

To delete backup files created for a Nutanix AHV VM by a backup job, do the following:

1. In the Veeam Backup & Replication console, open the Home view.
2. In the inventory pane of the Home view, select Backups.
3. In the working area, expand the job that created the backup, right-click the VM name and select Remove from > Disk.

|  |
| --- |
| Note |
| [Applies only to Veeam Backup & Replication version 12.1 and later] If [4-eyes authorization](https://helpcenter.veeam.com/docs/vbr/userguide/four_eyes_authorization.html?ver=13) is enabled in Veeam Backup & Replication, deleting backup files will require additional approval from another user with the Veeam Backup Administrator role. |

[![Deleting Backups](images/backup_delete_from_disk.webp)](images/backup_delete_from_disk.webp "Deleting Backups")


