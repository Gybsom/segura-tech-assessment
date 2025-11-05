# How to configure a remote backup using CIFS/NFS

This guide explains how to configure Segura® to store backups on an external server using the CIFS or NFS protocol.


## Requirements

Before you begin, make sure the following conditions are met:

- Administrative access to the Segura® web interface.
- An active CIFS or NFS file server accessible from the appliance network.
- Network path, credentials (for CIFS), and proper permissions to read/write to the shared directory.


## Getting started

Follow the steps below to configure a CIFS or NFS remote partition.

### Step 1. Open Backup Settings

1. In the upper-left corner of the interface, click the **Grid Menu** (four-square icon).  
2. Select **Orbit Server Manager**.
3. In the left-hand menu, go to **Settings > Backup**.
4. In the upper-right corner of the interface, click the **Edit** button.


### Step 2. Ensure backup options are enabled

1. Set the **Enable application backup?** button to **On**.
2. Set the **Enable sessions file backup?** button to **On**.
3. Set the **Add a remote partition** button to **On**.
4. Under **How will backup files be sent?**, choose:  
   **Mounting a remote partition (via CIFS or NFS)**.


### Step 3. Configure Remote Connection

Fill in the fields as follows:

| Field | Description | Example |
|--------|--------------|---------|
| **Remote host** | IP address or hostname of the backup server | `10.0.1.50` or `myserver.com` |
| **Remote path** | Directory path on the remote server where backups will be stored | `/bkp/segura` |


### 4. Choose the Protocol

#### **Option 1 – Samba (CIFS)**
- Enter the credentials of a user with **write access** to the remote path.  
- If your environment requires it, specify the **domain name**.
- Inform any **Additional options** you require.

> **Important:**
> 
> Without sufficient privileges, Segura® will not be able to create backups.

#### **Option 2 – Network File System (NFS)**
- Inform any **Additional options** you require.

> **Important:**
> 
> When using NFS, add the senhasegura appliance’s IP address to the Remote NFS Host configuration.
> Without this access permission, Segura® cannot mount or write to the remote partition.
> 

---
[Back to Home](../README.md)