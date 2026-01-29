---
title: "Retention Policies"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/retention_policy.html"
last_updated: "8/15/2025"
product_version: "13.9.0.212"
---

# Retention Policies


Image-level backups created by jobs are not kept forever — they are removed according to retention policy specified while creating the jobs as described in section [Creating Backup Jobs](backup_job_create.md).

Restore points in the backup chain are stored only for the allowed period of time (in days). If a restore point is older than the specified time limit, Veeam Backup & Replication removes it from the backup chain. To learn how Veeam Backup & Replication applies retention policies to forever forward incremental and forward incremental backup chains, see [Backup Retention](retention_backups.md).


