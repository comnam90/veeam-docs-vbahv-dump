---
title: "Adding VMs to Job"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/ahv_resources_job.html"
last_updated: "8/8/2025"
product_version: "13.9.0.212"
---

# Adding VMs to Job


If you want to protect additional VMs by configured jobs, you can either [edit the backup job settings](editing_jobs.md), or quickly add the VMs to the jobs from the Inventory view.

|  |
| --- |
| Note |
| If a VM is already added to the exclusion list in the job, the VM will not be protected. |

To add a VM to a backup job, do the following:

1. In the Veeam Backup & Replication console, open the Inventory view.
2. In the inventory pane, select Nutanix AHV and expand the Prism Central or cluster where the VM resides.
3. It the working area, select the VM that you want to back up, click Add to backup job on the ribbon and choose the necessary job.

Alternatively, right-click the VM, select Add to backup job and choose the necessary job.

[![Adding VMs to Job](images/ahv_resources_job.webp)](images/ahv_resources_job.webp "Adding VMs to Job")


