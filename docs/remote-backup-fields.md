# Remote Backup Configuration Fields

This document provides a reference for the settings available on the [**Remote Backup configuration page**](/docs/how-to-configure-remote-backup.md) that are used when setting up a CIFS/NFS backup target.

### General Settings

**Enable application backup? (Toggle)**
* **Function:** The main switch to activate or deactivate the backup service.
* **Default:** Off.
* **Usage:** Must be set to 'On' for any backups to occur.

**Add a remote partition? (Toggle)**
* **Function:** The switch to activate or deactivate the remote partition service.
* **Default:** Off.
* **Usage:** Must be set to 'On' for any remote backups to occur.

### Target Configuration

**Protocol (Dropdown)**
* **Function:** Specifies the network protocol to be used for connecting to the external storage target.
* **Options:**
    * **CIFS:** Select this to back up to a Windows file share or a Samba share.
    * **NFS:** Select this to back up to a Linux/UNIX Network File System share.

**Remote host (Text field)**
* **Function:** Defines the location of the storage server.
* **Usage:** Enter the IP address or hostname of the server hosting the share (e.g., `10.0.1.50` or `myserver.com`).

**Remote path (Text field)**
* **Function:** Defines the specific directory on the remote server where backup files will be stored.
* **Usage:** Enter the path using forward slashes (`/`). Do not include the server address. For CIFS, this is the name of the share (e.g., `/bkp/segura`).

**User (Text field)**
* **Function:** The username for the service account used to authenticate against the CIFS share.
* **Usage:** This field is only editable and required when the **Protocol** is set to **CIFS**. The account must have read and write permissions.

**Password (Password field)**
* **Function:** The password for the service account specified in the **User** field.
* **Usage:** This field is only editable and required when the **Protocol** is set to **CIFS**.

**Domain (Text field)**
* **Function:** The domain for the environment, if necessary.
* **Usage:** This field is only editable when the **Protocol** is set to **CIFS**. The account must have read and write permissions.

### Actions

**Save (Button)**
* **Function:** Saves and applies all changes made to the Application Backup configuration.

---
[Back to Home](../)