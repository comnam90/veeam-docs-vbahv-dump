---
title: "How Health Check Works"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/how_health_check_works.html"
last_updated: "7/4/2025"
product_version: "13.9.0.212"
---

# How Health Check Works


When Veeam Plug-in for Nutanix AHV saves a new backup restore point to a backup repository, it calculates CRC values for metadata in the backup chain and saves these values to the chain metadata, together with the instance data. When performing a health check, Veeam Plug-in for Nutanix AHV verifies the availability of data blocks, which are required to restore from the recent point only, and uses the saved values to ensure that the full restore points being verified are consistent.

On the day scheduled for a health check to run, Veeam Plug-in for Nutanix AHV starts a new health check session. For each restore point in the backup chain, Veeam Plug-in for Nutanix AHV calculates CRC values for backup metadata and compares them to the CRC values that were previously saved to the restore point. Veeam Plug-in for Nutanix AHV also checks whether data blocks that are required to rebuild the restore point are available.

If Veeam Plug-in for Nutanix AHV does not detect data inconsistency, the health check session completes successfully. Otherwise, the session completes with an error. Depending on the detected data inconsistency, Veeam Plug-in for Nutanix AHV performs the following operations:

* If the health check detects corrupted metadata in a full restore point, Veeam Plug-in for Nutanix AHV marks the backup chain as corrupted in the configuration database. During the next backup job session, Veeam Plug-in for Nutanix AHV copies the full instance image, creates a full restore point in the backup repository and starts a new backup chain in the backup repository.

* If the health check detects corrupted disk blocks in a restore point, Veeam Plug-in for Nutanix AHV marks the restore point that includes the corrupted data blocks and all subsequent incremental restore points as incomplete in the configuration database. During the next backup job session, Veeam Plug-in for Nutanix AHV copies not only those data blocks that have changed since the previous backup session but also data blocks that have been corrupted, and saves these data blocks to the latest restore point that has been created during the current session.


