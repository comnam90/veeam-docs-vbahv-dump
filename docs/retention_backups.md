---
title: "Backup Retention"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/retention_backups.html"
last_updated: "8/14/2025"
product_version: "13.9.0.212"
---

# Backup Retention


Veeam Plug-in for Nutanix AHV retains the number of latest restore points defined in job scheduling settings as described in section [Creating Backup Jobs](backup_job_vbr_destination.md). For backup chains created by jobs without scheduled active or synthetic full backups, Veeam Plug-in for Nutanix AHV applies forever forward incremental backup retention policy. For backup chains created by jobs that regularly produce active or synthetic full backups, Veeam Plug-in for Nutanix AHV applies forward incremental backup retention policy.

|  |
| --- |
| Note |
| For backup chains created by jobs that no longer exist, Veeam Plug-in for Nutanix AHV applies a separate retention mechanism as described in the Veeam Backup & Replication User Guide, section [Background Retention](https://helpcenter.veeam.com/docs/vbr/userguide/background_retention_job.html?ver=13). |

Forever Forward Incremental Backup Retention Policy

To track and remove redundant restore points from a forever forward incremental backup chain, Veeam Plug-in for Nutanix AHV performs the following actions at the end of each backup session:

1. Veeam Plug-in for Nutanix AHV checks the configuration database to detects backup chains with restore points that are older than the specified time limit.
2. If a redundant restore point exists in a backup chain, Veeam Plug-in for Nutanix AHV transforms the backup chain in the following way:

1. Rebuilds the full backup to include there data of the incremental backup that follows the full backup. To do that, Veeam Plug-in for Nutanix AHV injects into the full backup data blocks from the earliest incremental backup in the chain. This way, the full backup ‘moves’ forward in the standard backup chain.

![Backup Retention](images/backup_retention_injecting_blocks.webp)

1. Removes the earliest incremental backup from the chain as redundant — this data has already been injected into the full backup.

![Backup Retention](images/backup_retention_removing_data.webp)

1. Veeam Plug-in for Nutanix AHV repeats step 2 for all other redundant restore points found in the backup chain until all the restore points are removed. As data from multiple restore points is injected into the rebuilt full backup, Veeam Plug-in for Nutanix AHV ensures that the backup chain is not broken and that you will be able to recover your data when needed.

![Backup Retention](images/backup_retention_multiple_points.webp)

Forward Incremental Backup Retention Policy

To track and remove redundant restore points from a forward incremental backup chain, Veeam Plug-in for Nutanix AHV performs the following actions at the end of each backup session:

1. Veeam Plug-in for Nutanix AHV checks the configuration database to detect forward incremental backup chains where a new full backup has been created (which starts a new backup chain fragment).
2. Veeam Plug-in for Nutanix AHV checks whether the period to keep restore points in the new chain fragment has reached the allowed time limit.

1. If the new backup chain fragment has reached the limit of allowed restore points, Veeam Plug-in for Nutanix AHV removes all restore points of the older backup chain fragment.

![Backup Retention](images/retention_policy_forward.webp)


