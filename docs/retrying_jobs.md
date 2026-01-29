---
title: "Retrying Jobs"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/retrying_jobs.html"
last_updated: "7/22/2025"
product_version: "13.9.0.212"
---

# Retrying Jobs


If a job fails, you can retry the backup operation. When you perform a retry, Veeam Backup & Replication restarts the operation only for the failed resources added to the job and does not process VMs that have been processed successfully. As a result, retrying a job takes less time compared to restarting the job for all resources.

To retry a job, do the following:

1. Open the Home view.
2. In the inventory pane, select Jobs.
3. In the working area, select the necessary job and click Retry on the ribbon.

Alternatively, right-click the job and select Retry.

[![Retrying Job](images/job_retry.webp)](images/job_retry.webp "Retrying Job")


