---
title: "Getting Technical Support"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/export_logs.html"
last_updated: "12/8/2025"
product_version: "13.9.0.212"
---

# Getting Technical Support


If you have any questions or issues with Veeam Plug-in for Nutanix AHV, you can search for a resolution on [Veeam R&D Forums](https://forums.veeam.com/) or submit a support case in the [Veeam Customer Support Portal](https://www.veeam.com/support.html).

When you submit a support case, it is recommended that you provide the Veeam Customer Support Team with the following information:

* [Version information for the product and its infrastructure components](#ViewingProductDetails)
* The error message or an accurate description of the problem you are facing
* [Log files](#DownloadingLogs)

Viewing Product Details

To view the product details, do the following:

1. On the machine where the Veeam Backup & Replication console is installed, navigate to the Control Panel.
2. In the Control Panel window, navigate to Programs > Programs and Features.
3. In the program list, check the version of Veeam Plug-in for Nutanix AHV.

[![Viewing Product Details](images/plugin_version.webp)](images/plugin_version.webp "Viewing Product Details")

|  |
| --- |
| Tip |
| [Applies to Linux-based backup servers only] Alternatively, you can view product details in the Veeam Host Management Console as described in the Veeam Backup & Replication User Guide, section [Performing Maintenance Tasks](https://helpcenter.veeam.com/docs/vbr/userguide/hmc_perform_maintenance_tasks.html?ver=13#managing-veeam-components). |

Downloading Logs

To download the product logs, do the following:

1. From the main menu of the Veeam Backup & Replication console, select Help > Support Information.
2. At the Scope step of the Export Logs wizard, select the Export all logs for selected components option. Then, in the Managed servers list, select the backup server.

Complete the wizard as described in the Veeam Backup & Replication User Guide, section [Exporting Logs](https://helpcenter.veeam.com/docs/vbr/userguide/exporting_logs.html?ver=13).

[![Exporting Logs Using Veeam Backup & Replication Console](images/logs_vbr.webp)](images/logs_vbr.webp "Exporting Logs Using Veeam Backup & Replication Console")


