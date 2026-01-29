---
title: "File-Level Recovery"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/restore_how_flr.html"
last_updated: "8/21/2025"
product_version: "13.9.0.212"
---

# File-Level Recovery


To recover VM files and folders from a backup, Veeam Backup & Replication performs the following steps:

1. Mounts disks of the backed-up VM to the [mount host](https://helpcenter.veeam.com/docs/vbr/userguide/guest_file_recovery.html?ver=13#mount-hosts) specified for the recovery operation.
2. Launches the Veeam Backup Browser.

The Veeam Backup Browser displays the file system tree of the backed-up VM. In the browser, you select the necessary files and folders to restore.

1. Restores the selected files and folders to the original location or to a new location.
2. Detaches the disks from the mount host.

To recover VM files and folders from a backup snapshot, snapshot or PD snapshot, Veeam Backup & Replication performs the following steps:

1. Deploys a [helper appliance](https://helpcenter.veeam.com/docs/vbr/userguide/guest_file_recovery.html?ver=13#mount-hosts) in the Nutanix AHV cluster.
2. [Applies only if you perform restore from a snapshot or PD snapshot] Creates a temporary VM on the Nutanix AHV cluster.
3. Creates a volume group using disks of the original VM (for a backup snapshot) or of the temporary VM (for a snapshot or PD snapshot).
4. Attaches the volume group to the helper appliance.
5. [Applies only if you perform restore from a snapshot or PD snapshot] Deletes the temporary VM.
6. Launches the Veeam Backup Browser.

The Veeam Backup Browser displays the file system tree of the backed-up VM. In the browser, you select the necessary files and folders to restore.

1. Restores the selected files and folders to the original location or to a new location.
2. Detaches the volume group from the helper appliance.
3. Deletes the volume group and removes the helper appliance.

To learn how to recover individual VM files and folders, see [Performing File-Level Restore](restoring_guest_os_files.md).


