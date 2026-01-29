---
title: "Creating VeeamZIP Backups"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/veeamzip_backup_create.html"
last_updated: "11/25/2025"
product_version: "13.9.0.212"
---

# Creating VeeamZIP Backups


You can back up one or multiple Nutanix AHV VMs without configuring backup jobs. To do that, you can leverage the VeeamZIP feature — it can be helpful, for example, if you want to create backups for VMs immediately, archive VMs before decommissioning and so on. VeeamZIP produces a full backup that acts as an independent restore point. You can store the backup in a repository added to the backup infrastructure, in a local folder on the backup server or in a network share.

|  |
| --- |
| Note |
| You cannot store VeeamZIP backups in [Veeam Cloud Connect](https://helpcenter.veeam.com/docs/vbr/cloud/cloud_overview.html?ver=13) and [HPE Cloud Bank Storage](https://helpcenter.veeam.com/docs/vbr/userguide/storeonce_supported_features.html?ver=13#cloud-bank-storage) repositories. |

To create a VeeamZIP backup, do the following:

1. In the Veeam Backup & Replication console, open the Inventory view.
2. In the inventory pane, select Nutanix AHV and expand the Prism Central or cluster where the VM resides.
3. It the working area, select the VM that you want to back up and click VeeamZIP on the ribbon.

Alternatively, right-click the VM and select VeeamZIP.

1. Select the destination where the VeeamZIP backup will be stored.

|  |
| --- |
| Tip |
| You cannot specify an SMB share that requires authentication as a local or shared folder. However, you can [add the SMB share to the backup infrastructure](https://helpcenter.veeam.com/docs/vbr/userguide/repo_add.html?ver=13) and specify it as backup repository. |

The created VeeamZIP backup will be displayed under the Backups > Disk (Exported) node in the Home view of the Veeam Backup & Replication console.

[![Creating VeeamZIP Backups](images/veeamzip_launch.webp)](images/veeamzip_launch.webp)


