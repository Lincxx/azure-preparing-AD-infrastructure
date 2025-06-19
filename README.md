Azure Preparing AD Infrastructure
---
In this lab we are going to setup our Active Directory, along with a user
---
#### Setup Domain Controller in Azure
---
### **Create a Resource Group**

![step1](https://github.com/user-attachments/assets/bc3baf6a-f0b4-4e0d-9ac6-da44c1e6d677)

![step2](https://github.com/user-attachments/assets/5c9ea2ca-331b-497f-9fd5-4eb6b8d40836)

### **Create a Virtual Network and Subnet**

![step3](https://github.com/user-attachments/assets/2a047934-f683-41e3-9b96-ad011951143e)

![step4](https://github.com/user-attachments/assets/2903baeb-dcbb-4e4a-ad93-fb3a640a3f0c)

### **Create the Domain Controller VM (Windows Server 2022) named “DC-1”**

![step5](https://github.com/user-attachments/assets/4ea0afc7-09d9-45f0-911b-cc9195307d6e)

![step6](https://github.com/user-attachments/assets/2560bed2-c68e-4cb6-92b8-d5bb97e3075b)

![step7](https://github.com/user-attachments/assets/d9eadf2c-7adb-4347-b316-a6c37a175434)

![step8](https://github.com/user-attachments/assets/1b293775-f84d-4004-8275-3d37c65400ad)

#### Username: labuser
#### Password: Cyberlab123!
**After VM is created, set Domain Controller’s NIC Private IP address to be static
Log into the VM and disable the Windows Firewall (for testing connectivity)**

#### Setup Client-1 in Azure
---
### Create the Client VM (Windows 10) named “Client-1”
![step9](https://github.com/user-attachments/assets/f0c02ac3-2a0c-4fca-b903-a22c4c0e1e92)

![step10](https://github.com/user-attachments/assets/e5f478f2-7ad9-476d-959d-6ff592c9999b)

![step11](https://github.com/user-attachments/assets/fcdec8a4-e10d-4667-beea-f917b1f63a5e)



#### Username: labuser
#### Password: Cyberlab123!


### Attach it to the same region and Virtual Network as DC-1

### After VM is created, set Client-1’s DNS settings to DC-1’s Private IP address

![step12](https://github.com/user-attachments/assets/9c0c67ee-c179-4246-aa8d-ba641db32d27)

![step13](https://github.com/user-attachments/assets/66720a6c-d188-4ed5-b289-0c06324387a7)

![step14](https://github.com/user-attachments/assets/586ef396-2f97-4ea7-9497-08c48aa64a94)

![step15](https://github.com/user-attachments/assets/00eaa7b6-7efb-485c-a551-d2faa379b03d)


### From the Azure Portal, restart Client-1
![step16](https://github.com/user-attachments/assets/9aa552b1-f26d-4579-8b2c-c82f804d284a)
### This is you help set the DNS correctly

### Login to Client-1
### Attempt to ping DC-1’s private IP address
### Ensure the ping succeeded
### From Client-1, open PowerShell and run ipconfig /all
### The output for the DNS settings should show DC-1’s private IP Address