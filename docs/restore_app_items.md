---
title: "Performing Application Item Restore"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/restore_app_items.html"
last_updated: "10/29/2025"
product_version: "13.9.0.212"
---

# Performing Application Item Restore


With application item restore, you can use Nutanix AHV backups and snapshots to restore the following data:

* Microsoft Active Directory objects and containers
* Microsoft Exchange mailboxes, folders and messages
* Microsoft SharePoint sites and lists
* Microsoft SQL Server databases
* Oracle databases
* PostgreSQL databases

|  |
| --- |
| Note |
| It is recommended that you use [application-consistent backups](backup_job_vbr_guest_processing.md) for application item restore. |

To restore application items from a Nutanix AHV VM backup or snapshot, do the following:

1. In the Veeam Backup & Replication console, open the Home view.
2. In the inventory pane, select Backups.
3. In the working area, expand the necessary backup job, right-click the VM that contains an application you want to restore, select Restore application items and select the application.

Alternatively, expand the necessary backup job, select the VM, click Application Items on the ribbon and select the application.

|  |
| --- |
| Tip |
| To restore application items from a backup snapshot, expand the job that contains the snapshot of the VM, right-click the VM and select Restore application items. |

1. In the restore wizard, select a restore point that will be used to restore the application, specify a restore reason and click Browse.
2. In the Veeam Explorer application, perform the steps described in the [Veeam Explorers User Guide](https://helpcenter.veeam.com/docs/vbr/explorers/explorers_introduction.html?ver=13).

|  |
| --- |
| Tip |
| As an alternative to application item restore, you can also [perform file-level restore](restoring_guest_os_files.md) to recover standalone databases using Veeam Explorers. |

[![Performing Application Item Restore](images/restore_app_items.webp)](images/restore_app_items.webp)


