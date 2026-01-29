---
title: "Configuring Backup Repositories"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/configure_repository.html"
last_updated: "11/25/2025"
product_version: "13.9.0.212"
---

# Configuring Backup Repositories


A backup repository is a storage location where Veeam Backup & Replication keeps backup files. By default, the backup server performs the role of a backup repository. To keep your backups in another storage location, you can configure the following types of repositories:

* Direct attached storage: [Microsoft Windows](https://helpcenter.veeam.com/docs/vbr/userguide/ms_server.html?ver=13) and [Linux](https://helpcenter.veeam.com/docs/vbr/userguide/linux_server.html?ver=13) virtual and physical machines. [Hardened repositories](https://helpcenter.veeam.com/docs/vbr/userguide/hardened_repository.html?ver=13) based on Linux servers are also supported.
* Network attached storage: [CIFS (SMB) shares](https://helpcenter.veeam.com/docs/vbr/userguide/smb_share.html?ver=13) and [NFS shares](https://helpcenter.veeam.com/docs/vbr/userguide/nfs_share.html?ver=13).
* Deduplicating storage appliances: [ExaGrid](https://helpcenter.veeam.com/docs/vbr/userguide/deduplicating_appliance_exgrid.html?ver=13), [Quantum DXi](https://helpcenter.veeam.com/docs/vbr/userguide/deduplicating_appliance_quantum.html?ver=13), [Dell Data Domain](https://helpcenter.veeam.com/docs/vbr/userguide/dell_dd.html?ver=13), [HPE StoreOnce](https://helpcenter.veeam.com/docs/vbr/userguide/deduplicating_appliance_storeonce.html?ver=13), [Fujitsu ETERNUS](https://helpcenter.veeam.com/docs/vbr/userguide/fujitsu.html?ver=13), [Infinidat InfiniGuard](https://helpcenter.veeam.com/docs/vbr/userguide/infinidat_infiniguard.html?ver=13).

* Cloud object storage: [11:11 Cloud Object Storage, Amazon S3, S3 compatible, Google Cloud, Wasabi Cloud Storage, Veeam Data Cloud Vault, IBM Cloud and Microsoft Azure Blob](https://helpcenter.veeam.com/docs/vbr/userguide/object_storage_repository.html?ver=13).

To combine repositories of different types in one repository, you can configure a [scale-out backup repository](https://helpcenter.veeam.com/docs/vbr/userguide/backup_repository_sobr.html?ver=13) and add any of supported repositories to its [performance tier](https://helpcenter.veeam.com/docs/vbr/userguide/backup_repository_sobr_extents.html?ver=13).

For Linux server, Microsoft Windows server, SMB share, ExaGrid, Quantum DXi, Fujitsu ETERNUS and Infinidat InfiniGuard repositories, you can enable the Fast Clone technology that increases the speed of synthetic backup creation and transformation, reduces disk space requirements and decreases the load on storage devices. With this technology, Veeam Backup & Replication references existing data blocks on volumes instead of copying data blocks between files. Data blocks are copied only when files are modified. To learn how to configure a repository to enable this functionality, see the Veeam Backup & Replication User Guide, section [Fast Clone](https://helpcenter.veeam.com/docs/vbr/userguide/backup_repository_block_cloning.html?ver=13).

|  |
| --- |
| Important |
| * Veeam Plug-in for Nutanix AHV does not support storing backups in [Veeam Cloud Connect](https://helpcenter.veeam.com/docs/vbr/cloud/cloud_overview.html?ver=13) and [HPE Cloud Bank Storage](https://helpcenter.veeam.com/docs/vbr/userguide/storeonce_supported_features.html?ver=13#cloud-bank-storage) repositories. However, you can use them for [storing copies of backups](backup_copy.md) created with Veeam Plug-in for Nutanix AHV.  * [For scale-out backup repositories] Due to specifics of backup jobs for Nutanix AHV VMs, Veeam Plug-in for Nutanix AHV always creates a separate backup chain for each VM added to a backup job. Thus, even if you clear the Use per-VM backup files check box in the [advanced settings of a scale-out backup repository](https://helpcenter.veeam.com/docs/vbr/userguide/sobr_add_extents.html?ver=13), backups of multiple Nutanix AHV VMs are not stored in a single backup file. |


