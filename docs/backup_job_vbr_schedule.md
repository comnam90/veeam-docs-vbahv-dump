---
title: "Step 6. Specify Job Scheduling Options"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/backup_job_vbr_schedule.html"
last_updated: "8/14/2025"
product_version: "13.9.0.212"
---

# Step 6. Specify Job Scheduling Options


At the Schedule step of the wizard, you can instruct Veeam Backup & Replication to start the backup job automatically according to a specific backup schedule. The backup schedule defines how often data of the VMs added to the backup job will be backed up.

To help you implement a comprehensive backup strategy, Veeam Backup & Replication allows you to create schedules of the following types:

* Daily at this time — the backup job will create restore points at a specific time on specific days.
* Monthly at this time — the backup job will create restore points once a month on a specific day.
* Periodically every — the backup job will create restore points repeatedly, with a specific time interval every day.

|  |
| --- |
| Tip |
| You can instruct Veeam Backup & Replication to run the backup job again if it fails on the first try. To do that, select the Retry failed items processing check box, and specify the maximum number of attempts to run the job and the time interval between retries. When retrying backup jobs, Veeam Backup & Replication processes only those VMs that failed to be backed up during the previous attempt. |

![Step 6. Specify Job Scheduling Options](images/backup_job_add_vbr_schedule.webp "Define Job Schedule")


