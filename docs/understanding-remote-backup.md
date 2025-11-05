# Understanding remote backups in Segura®

A core component of any Privileged Access Management (PAM) solution is the integrity and availability of its data. A Segura® instance holds critical information, including credentials, access policies, and audit logs. A remote backup strategy is essential for disaster recovery, ensuring you can restore operations quickly in the event of system failure, data corruption, or catastrophic error.

## What is remote backup?

The Remote Backup feature in Segura® allows you to automatically copy your instance's critical data to an external, network-accessible storage location. This moves your backup data "off-box," separating it from the live production appliance.

This process runs on a schedule, capturing a complete snapshot of the system state required for a full restore.

## Why is remote backup essential?

Relying solely on local snapshots or backups on the same host machine (or in the same data center) exposes you to significant risk. A remote backup strategy protects against:

* **Appliance failure:** If the virtual machine or physical host running Segura® fails, local backups will be lost with it.
* **Data corruption:** In the rare event the appliance's local storage becomes corrupted, an external backup provides a clean, uncorrupted version to restore from.
* **Site-level disasters:** If an entire data center becomes unavailable (due to fire, flood, or power loss), a geographically separate remote backup ensures your data is safe.

## Supported protocols: CIFS and NFS

Segura® supports the two most common network file-sharing protocols for configuring your backup target:

* **CIFS (Common Internet File System):** This is the standard protocol used by Windows servers and Samba services on Linux. It is the ideal choice if your organization's backup infrastructure is based on Windows file shares.
* **NFS (Network File System):** This is the native file-sharing protocol for Linux and UNIX-based systems. It is preferred when backing up to a Linux-based NAS (Network Attached Storage) or file server.


---
[Back to Home](../README.md)