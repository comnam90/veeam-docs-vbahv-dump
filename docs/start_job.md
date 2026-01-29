---
title: "Starting and Stopping Jobs"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/start_job.html"
last_updated: "8/8/2025"
product_version: "13.9.0.212"
---

# Starting and Stopping Jobs


You can start a job manually, for example, if you want to create an additional restore point and do not want to modify the configured job schedule. You can also stop a job manually if processing of a VM is about to take too long, and you do not want the job to have an impact on the production environment during business hours. When you stop a running job, Veeam Backup & Replication creates a new restore point only for those VMs that have already been processed by the time you stop the job.

To start or stop a job, do the following:

1. Open the Home view.
2. In the inventory pane, select Jobs.
3. In the working area, select the necessary job and click Start or Stop on the ribbon.

Alternatively, right-click the job and select Start or Stop.

[![Starting and Stopping Jobs](images/job_start.webp)](images/job_start.webp "Starting and Stopping Jobs")


