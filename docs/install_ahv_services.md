---
title: "Installing Nutanix AHV Plug-In Manually"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/install_ahv_services.html"
last_updated: "11/18/2025"
product_version: "13.9.0.212"
---

# Installing Nutanix AHV Plug-In Manually


The plug-in that allows you to protect Nutanix AHV resources comes pre-installed with the default installation package of Veeam Backup & Replication. However, you may require to install a new plug-in version on the backup server manually if some updates or patches become available.

|  |
| --- |
| Note |
| If you use a remote Veeam Backup & Replication console, you do not need to install Nutanix AHV Plug-in on the workstation where the remote Veeam Backup & Replication console is deployed. |

To install Veeam Plug-in for Nutanix AHV, do the following:

1. Log in to the backup server using an account with the local Administrator permissions.
2. Download the product installation file VeeamPluginNutanixAHV\_13.9.0.212.zip from the [Veeam downloads page](https://www.veeam.com/availability-nutanix-ahv-download.html).
3. Open the downloaded archive file and launch the VeeamPluginNutanixAHV\_13.9.0.212.exe installation file.

Before proceeding with installation, the installer will check whether you have Microsoft .NET Core Runtime installed on the backup server. In case the required version is missing, the installer will offer to install it automatically. To do that, click OK.

1. At the License Agreement step of the Veeam Plug-In for Nutanix AHV setup wizard, read and accept the Veeam license agreement, licensing policy, the 3rd party components and required software license agreement. If you reject the agreements, you will not be able to continue installation.

![Installing Nutanix AHV Plug-In Manually](images/install_ahv_services_agreement.webp "Installing Nutanix AHV Plug-In")

1. At the Data Location step of the wizard, you can change the installation directory if necessary.

![Installing Nutanix AHV Plug-In Manually](images/install_ahv_services_custom.webp "Installing Nutanix AHV Plug-In")

1. Click Install to begin installation.

![Installing Nutanix AHV Plug-In Manually](images/install_ahv_services.webp "Installing RHV Plug-In")


