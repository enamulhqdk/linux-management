Azure Virtual Machine Setup Guide
Initial Setup

Registered an account on portal.azure.com using HAMK student credentials.
Accessed the Azure Portal homepage at portal.azure.com/#home.
Selected "Create a resource" from the available options.
Chose "Create" under the Virtual Machine category.
Basic Configuration

Resource Group: robotics
Virtual Machine Name: Linux-Management
Region: North Europe (Europe)
Availability Options: No redundancy for infrastructure required.
Image: Ubuntu Server 24.04 LTS – x64 Gen2.
VM Architecture: x64
Size: Standard_B2ls_v2 (2 vCPUs, 4 GiB RAM).
Authentication Settings

Authentication Type: SSH Public Key
Username: mrrafsan
SSH Key Source: Generate a new key pair.
Key Type: RSA (SSH Format).
Key Pair Name: linux-management_key
Allowed Inbound Ports:
HTTP (80)
HTTPS (443)
SSH (22)
Disk Configuration

OS Disk Type: Standard SSD with locally redundant storage.
Delete Disk with VM: Enabled.
Key Management: Platform-managed.
Networking

Default network settings applied.
Delete NIC with VM: Enabled.
Accelerated Networking: Not supported.
DNS Settings:
DNS Label: mrrafsan-lab-robotics
Management Settings

Auto-Shutdown: Enabled.
Timezone: Helsinki
Shutdown Time: 5:00 PM
Email Notification: Disabled.
Finalization

Reviewed all configurations carefully.
Successfully created the virtual machine.






