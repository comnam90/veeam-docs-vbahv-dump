---
title: "Exporting Backups"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/export_backups.html"
last_updated: "8/8/2025"
product_version: "13.9.0.212"
---

# Exporting Backups


Exporting backups allows you to synthesize a complete and independent full backup file using restore points located in your backup repositories. That is, you can transform any backup chain into a standalone full backup file and save it to the same repository where the selected restore points reside.

To export a backup, do the following:

1. In the Veeam Backup & Replication console, open the Home view.
2. In the inventory pane, select Backups.
3. In the working area, right-click a VM for which you want to synthesize a full backup file, and select Export Backup.
4. Complete the New Export wizard as described in the Veeam Backup & Replication User Guide, section [Performing Export](https://helpcenter.veeam.com/docs/vbr/userguide/performing_full_export.html?ver=13).

Once the export operation completes, the exported backup will be displayed under the Backups > Disk (Exported) node in the Home view of the Veeam Backup & Replication console.

[![Exporting Backup](images/backup_export.webp)](images/backup_export.webp "Exporting Backup")


