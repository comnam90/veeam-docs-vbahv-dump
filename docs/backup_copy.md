---
title: "Copying Backups"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/backup_copy.html"
last_updated: "11/25/2025"
product_version: "13.9.0.212"
---

# Copying Backups


With backup copy, you can create several instances of a backup and copy them to secondary (target) backup repositories for long-term storage. Target backup repositories can be located in the same site as the source backup repository or can be deployed off-site. Since the backup copy has the same format as the original backup, you can restore VM data directly from the backup copy in case a disaster strikes. For more information on the backup copy functionality, see the Veeam Backup & Replication User Guide, section [Backup Copy](https://helpcenter.veeam.com/docs/vbr/userguide/backup_copy.html?ver=13).

To copy backups to a secondary backup repository, do the following:

1. In the Veeam Backup & Replication console, open the Home view.
2. In the inventory pane, select Jobs and click Backup Copy on the ribbon.
3. Create a backup copy job as described in the Veeam Backup & Replication User Guide, section [Creating Backup Copy Jobs](https://helpcenter.veeam.com/docs/vbr/userguide/backup_copy_create.html?ver=13).

|  |
| --- |
| NotE |
| Veeam Plug-in for Nutanix AHV copies all backups produced by a source backup job — you cannot select backups of specific VMs. |

Alternatively, you can create a copy of a backup without configuring a job as described in the Veeam Backup & Replication User Guide, section [Copying Backups](https://helpcenter.veeam.com/docs/vbr/userguide/copy_backup.html?ver=13).

[![Copying Backups](images/backup_copy.webp)](images/backup_copy.webp "Copying Backups")


