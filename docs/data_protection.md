---
title: "Performing Backup"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/data_protection.html"
last_updated: "8/8/2025"
product_version: "13.9.0.212"
---

# Performing Backup


To produce VM backups, Veeam Backup & Replication runs backup jobs. A backup job is a collection of settings that define the way backup operations are performed: what data to back up, where to store backups, when to start the backup process, and so on.

One backup job can be used to process multiple VMs, but you can back up each VM with one backup job at a time. If a VM is added to more than one backup job, it will be processed only by the backup job that started earlier.

|  |
| --- |
| Note |
| To back up data that resides on Nutanix Files, use the Veeam Backup & Replication file share backup functionality described in the Veeam Backup & Replication User Guide, section [Unstructured Data](https://helpcenter.veeam.com/docs/vbr/userguide/unstructured_data_backup.html?ver=13). |


