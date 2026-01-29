---
title: "Prism Central Deployment Scenario"
product: "vbahv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbahv/userguide/infrastructure_prism_central.html"
last_updated: "12/4/2025"
product_version: "13.9.0.212"
---

# Prism Central Deployment Scenario


Since Veeam Plug-in for Nutanix AHV is integrated with Veeam Backup & Replication, the solution architecture in the Prism Central deployment scenario comprises the following set of components:

* [Nutanix AHV Prism Central](#prism)
* [Nutanix AHV clusters](#cluster)
* [Backup server](#server)
* [Veeam Plug-in for Nutanix AHV](#plugin)
* [Backup repositories](#repositories)
* [Workers](#workers)

Nutanix AHV  Prism Central

The Prism Central is a software appliance that provides a centralized interface for managing multiple clusters in the Nutanix hyper-converged infrastructure (HCI) environment. Veeam Plug-in for Nutanix AHV uses the Prism Central to access all the registered clusters.

Nutanix AHV Clusters

A Nutanix AHV cluster is a logical group of Nutanix HCI nodes managed by Nutanix Controller VMs (CVMs). Veeam Plug-in for Nutanix AHV accesses cluster resources (such as VMs, volume groups, protection domains, storage containers and networks) to perform backup and restore operations.

Backup Server

A backup server is either a Windows-based or Linux-based physical or virtual machine on which Veeam Backup & Replication is installed. The backup server is the configuration, administration and management core of the backup infrastructure. It coordinates backup and restore operations, controls job scheduling and manages resource allocation.

Veeam Plug-in for Nutanix AHV

Veeam Plug-in for Nutanix AHV is an architecture component that enables integration between the backup server and other components of the backup infrastructure. Veeam Plug-in for Nutanix AHV allows Veeam Backup & Replication to connect to the Nutanix AHV Prism Central, and to perform data protection and disaster recovery tasks with Nutanix AHV resources.

Backup Repositories

A backup repository is a storage location where Veeam Plug-in for Nutanix AHV stores backups of protected Nutanix AHV VMs.

To communicate with backup repositories, Veeam Plug-in for Nutanix AHV uses Veeam Data Mover — the service that is responsible for data processing and transfer. By default, Veeam Data Mover runs on the repositories themselves. If a repository cannot host Veeam Data Mover, it starts on a gateway server — a dedicated component that “bridges” the backup server and workers. For more information, see the Veeam Backup & Replication User Guide, section [Gateway Server](https://helpcenter.veeam.com/docs/vbr/userguide/gateway_server.html?ver=13).

Workers

A worker is a Linux-based VM that resides on the Nutanix AHV host and processes backup workloads when transferring data to and from backup repositories. For optimal performance, workers can be deployed in all Nutanix AHV Prism Central clusters and can be distributed among cluster hosts (nodes). For more information on deployment sizing considerations, see [Sizing Guidelines](sizing_guide.md).

[![Prism Central Deployment Scenario](images/infrastructure_prism_central.webp)](images/infrastructure_prism_central.webp)


