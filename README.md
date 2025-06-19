Azure Preparing AD Infrastructure
---
In this lab we are going to setup our Active Directory, along with a user
---
Setup Domain Controller in Azure
---
### **Create a Resource Group**

![step1](https://github.com/user-attachments/assets/bc3baf6a-f0b4-4e0d-9ac6-da44c1e6d677)

![step2](https://github.com/user-attachments/assets/5c9ea2ca-331b-497f-9fd5-4eb6b8d40836)

### **Create a Virtual Network and Subnet**

![step3](https://github.com/user-attachments/assets/2a047934-f683-41e3-9b96-ad011951143e)

![step4](https://github.com/user-attachments/assets/2903baeb-dcbb-4e4a-ad93-fb3a640a3f0c)

### **Create the Domain Controller VM (Windows Server 2022) named “DC-1”**

![step5](https://github.com/user-attachments/assets/4ea0afc7-09d9-45f0-911b-cc9195307d6e)

#### Username: labuser
#### Password: Cyberlab123!
After VM is created, set Domain Controller’s NIC Private IP address to be static
Log into the VM and disable the Windows Firewall (for testing connectivity)

Setup Client-1 in Azure
—
Create the Client VM (Windows 10) named “Client-1”
Username: labuser
Password: Cyberlab123!
Attach it to the same region and Virtual Network as DC-1
After VM is created, set Client-1’s DNS settings to DC-1’s Private IP address
From the Azure Portal, restart Client-1
Login to Client-1
Attempt to ping DC-1’s private IP address
Ensure the ping succeeded
From Client-1, open PowerShell and run ipconfig /all
The output for the DNS settings should show DC-1’s private IP Address
