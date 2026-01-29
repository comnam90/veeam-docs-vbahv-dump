---
title: "Step 3. Choose Restore Mode"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/ir_mode_ahv.html"
last_updated: "7/4/2025"
product_version: "13.9.0.212"
---

# Step 3. Choose Restore Mode


[This step applies only if you restore Nutanix AHV VMs]

At the Restore Mode step of the wizard, choose whether you want to restore the selected VM to the original or to a custom location.

To meet minimum requirements for VMs residing on a Nutanix AHV cluster, Veeam Plug-in for Nutanix AHV allocates 64 MB of RAM to the recovered VM if it originally had less amount of memory.

|  |
| --- |
| Important |
| If you recover a VM with original settings, and the original VM still exists in the virtual infrastructure, the original VM will be removed. |

![Step 3. Choose Restore Mode](images/ir_mode_ahv.webp)


