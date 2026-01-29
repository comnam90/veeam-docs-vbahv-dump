---
title: "Before You Begin"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/backup_job_prerequisites.html"
last_updated: "12/12/2025"
product_version: "13.9.0.212"
---

# Before You Begin


Before you create a backup job, consider the following limitations:

* You cannot back up workers and Nutanix Controller VMs and Prism Central VMs.
* You cannot use Veeam Plug-in for Nutanix AHV to back up iSCSI disks mounted to VMs — they are skipped from processing automatically. However, you can use [Veeam Agent for Microsoft Windows](https://helpcenter.veeam.com/docs/agentforwindows/userguide/overview.html) or [Veeam Agent for Linux](https://helpcenter.veeam.com/docs/agentforlinux/userguide/overview.html) to protect those disks.
* If the backup job includes individual virtual machines, as well as the whole Prism Central, category, protection domain or cluster, Veeam Backup & Replication creates a snapshot of each VM and a VG snapshot of each volume group, and then produces image-level backups using the created snapshots. This approach cannot guarantee full consistency of VM and volume group data.
* [Applies only to the [Prism Central deployment](infrastructure_prism_central.md)] If you want to back up VMs using data obtained from snapshots on replica clusters, ensure that you have scheduled Prism Central protection policies to take snapshots more frequent than the backup job runs.
* By default, [backup encryption](https://helpcenter.veeam.com/docs/vbr/userguide/data_encryption.html?ver=13) is disabled for backed-up data. However, you can enable encryption at the repository level as described in the Veeam Backup & Replication User Guide, section [Access Permissions](https://helpcenter.veeam.com/docs/vbr/userguide/access_permissions.html?ver=13).
* Since Veeam Backup & Replication does not allow you to assign [information about locations](https://helpcenter.veeam.com/docs/vbr/userguide/locations.html?ver=13) to Nutanix AHV clusters and workers, job statistics do not include information on the Nutanix AHV VM data migration between different geographic regions.


