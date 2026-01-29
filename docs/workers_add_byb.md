---
title: "Before You Begin"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/workers_add_byb.html"
last_updated: "8/11/2025"
product_version: "13.9.0.212"
---

# Before You Begin


Before you add a worker to the backup infrastructure, consider the following:

* It is recommended that workers are deployed in each Nutanix AHV cluster. If no worker is deployed in the cluster, performance of backup operations will be affected as Veeam Plug-in for Nutanix AHV will use a worker deployed in another cluster.
* It is recommended that the number of configured workers does not exceed the number of hosts in the Nutanix AHV cluster.
* Each worker must be provided with sufficient compute resources to handle backup and restore tasks in parallel. The maximum number of concurrent tasks is configured in worker settings — if this number is exceeded, the worker will not start a new task until one of the current tasks finishes.
* It is recommended the total number of concurrent tasks configured for all workers deployed in the cluster does not exceed the [number of physical disks added to the cluster](https://portal.nutanix.com/page/documents/details?targetId=Web-Console-Guide-Prism-v7_3:wc-hardware-dashboard-wc-r.html). You can change the maximum number of concurrent tasks (the best practice is to allocate 1 vCPU and 1 GB RAM for each additional task) while deploying a new worker or editing settings of an existing one.


