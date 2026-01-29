---
title: "Before You Begin"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/byb_instant_recovery_ahv.html"
last_updated: "8/15/2025"
product_version: "13.9.0.212"
---

# Before You Begin


Before you perform Instant Recovery, do the following:

* Power off the original machine if it is still present in the target location.
* Deploy a [dedicated server](https://helpcenter.veeam.com/docs/vbr/userguide/mount_server.html?ver=13) to mount workload images directly from backups stored in backup repositories and allocate minimum 512 MB of additional RAM for each VM disk that you want to recover. Make sure that the Server for NFS role and the Client for NFS component are not installed on the server, and that the [Veeam vPower NFS Service](https://helpcenter.veeam.com/docs/vbr/userguide/vpower_nfs_service.html?ver=13) is running.

* [Applies only to VMs being restored from backups stored in the archive tier of scale-out backup repositories] Retrieve backup data as described in the Veeam Backup & Replication User Guide, section [Retrieving Backup Files](https://helpcenter.veeam.com/docs/vbr/userguide/retrieval_job_launch.html?ver=13). However, this requirement is not applicable to backups stored in the archive tier that consists of the Amazon S3 Glacier Instant Retrieval extent.

* [Applies only to Linux VMs] Make sure that the file systems (also referred to as devices or partitions) listed in the /etc/fstab file are mounted using UUIDs. Instant Recovery of file systems mounted using device names is not supported as the restored VMs may fail to boot.

* [Applies only to Windows VMs being restored from backups created by solutions other than Veeam Plug-in for Nutanix AHV] Make sure to install Nutanix VirtIO drivers and Nutanix Guest Tools on the VMs — before the backups are created. You will not be able to add or modify the VM drivers during the recovery operation.

* [Applies only to VMs being restored from backups created by solutions other than Veeam Plug-in for Nutanix AHV] Veeam Plug-in for Nutanix AHV attaches VM disks with the restored data to the target VM disk nodes using their original bus types. Veeam Plug-in for Nutanix AHV can attach to a VM up to 6 SATA, 256 SCSI, 4 IDE and 7 PCI disks. If the VM has more disks of any of those bus types, Nutanix AHV will attach the disks to remaining nodes of other bus types in the default priority: SATA, SCSI, IDE, PCI. You can [modify the Veeam Plug-in for Nutanix AHV configuration](bus_type_restore_order.md), to instruct Nutanix AHV to ignore source VM original bus types and to use a specific order of bus types.


