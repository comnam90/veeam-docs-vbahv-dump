---
title: "Step 5. Select Storage Container"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/restore_to_ahv_container.html"
last_updated: "1/27/2025"
product_version: "13.9.0.212"
---

# Step 5. Select Storage Container


[This step applies only if you have selected the Restore to a new location, or with different settings option at the Restore Mode step of the wizard]

At the Storage Container step of the wizard, choose the storage container where virtual disks of the recovered VM will be stored.

For a container to be displayed in the list of the available containers, it must be configured in the Nutanix AHV cluster as described in [Nutanix documentation](https://portal.nutanix.com/page/documents/details?targetId=Web-Console-Guide-Prism:wc-storage-management-wc-c.html).

|  |
| --- |
| Note |
| You cannot choose a storage container when restoring the VM from a snapshot. |

![Step 5. Select Storage Container](images/restore_vm_ahv_container.webp)


