---
title: "Licensing"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/licensing.html"
last_updated: "8/29/2025"
product_version: "13.9.0.212"
---

# Licensing


Veeam Plug-in for Nutanix AHV is licensed by the number of protected Nutanix AHV VMs. Each Nutanix AHV VM protected with backups consumes one Veeam Universal License instance from the license scope. A Nutanix AHV VM is considered protected if it has a restore point created during the past 31 days. If a Nutanix AHV VM is protected with snapshots only, no license is consumed.

By default, Veeam Plug-in for Nutanix AHV automatically revokes a license instance from a protected VM if no new restore points have been created during the past 31 days. However, you can manually revoke license instances from protected VMs as described in the Veeam Backup & Replication User Guide, section [Revoking License](https://helpcenter.veeam.com/docs/vbr/userguide/revoke_servers.html?ver=13).

Obtaining New License

You can obtain the following types of licenses for Veeam Plug-in for Nutanix AHV:

* Evaluation license is a free license that can be used for product evaluation. The license is valid for 30 days from the moment of the product download.

To obtain this license, request a trial key on the [Veeam downloads page](https://www.veeam.com/backup-red-hat-virtualization-download.html) as described in the Veeam Backup & Replication User Guide, section [Obtaining and Renewing License](https://helpcenter.veeam.com/docs/vbr/userguide/license_obtain.html?ver=13).

* Subscription license is a paid license with a limited subscription term. The expiration date of the Subscription license is set to the end of the subscription term. The Subscription license term is normally 1–5 years from the license issue date.

To obtain this license, choose the required subscription term on the [Veeam Backup & Replication Pricing](https://www.veeam.com/buy-veeam-backup-replication.html) page and contact the Veeam Sales Team.

* Perpetual license is a paid license without an expiration date. The Perpetual license typically includes one year period of basic support and maintenance that can be extended.

To obtain this license, [contact a reseller in your region](https://www.veeam.com/buy-veeam-products-pricing.html).

After you obtain a license, install it on the backup server as described in the Veeam Backup & Replication User Guide, section [Installing License](https://helpcenter.veeam.com/docs/vbr/userguide/install_license.html?ver=13).

Using Existing License

If you already use Veeam Backup & Replication and you have spare Veeam Universal License instances on your backup server, they can be used to protect Nutanix AHV VMs. You can check the number of available license instances in the Veeam Backup & Replication console as described in the Veeam Backup & Replication User Guide, section [Viewing License Information](https://helpcenter.veeam.com/docs/vbr/userguide/license_view.html?ver=13).


