# Create a Windows VM + RDP + Initialize a Data Disk

This repository supports my lab walkthrough video on deploying a **Windows virtual machine** in Azure, connecting via **RDP**, and completing a common admin task: **initializing and formatting an attached data disk** inside the VM.  
📺 **Watch the lab video on YouTube:** https://youtu.be/h2MgvY1IDmo

---

## 🔍 Lab Overview

In this lab, you’ll learn how to:

- Create a **Windows Server VM** using the Azure portal
- Configure basic VM settings (region, size, admin credentials, inbound ports)
- Attach a **managed data disk** during or after VM creation
- Connect to the VM using **Remote Desktop (RDP)**
- Use **Disk Management** to initialize, partition, and format the data disk (NTFS)
- Verify the disk is mounted and usable in File Explorer

These tasks are foundational for **AZ-104 compute** and day-to-day Azure VM administration.

---

## 🧪 Lab Scenario

Your company processes video content on Windows VMs. A new customer requires proprietary codecs and additional storage for processing workloads. You must deploy a new Windows VM, connect to it securely for administration, and prepare a data disk for application storage.

---

## 🛠️ Key Tasks

✅ **Task 1: Create the Lab Resource Group**
- Create a resource group (example: `rg-vm-rdp-lab`)
- Use a dedicated RG to simplify cleanup and cost control

✅ **Task 2: Create a Windows Virtual Machine**
- Create a Windows Server VM (2019/2022)
- Choose a small lab size (example: `Standard_DS1_v2`)
- Allow inbound **RDP (3389)** (lab/demo purposes)

✅ **Task 3: Attach a Data Disk**
- Create and attach a new **managed disk**
- Confirm the disk appears under the VM’s storage configuration

✅ **Task 4: Connect to the VM using RDP**
- Download the RDP file from the Azure portal
- Connect and sign in with the local admin credentials

✅ **Task 5: Initialize + Format the Data Disk**
- Open **Disk Management**
- Initialize the disk (GPT recommended)
- Create a **New Simple Volume**
- Format as **NTFS**, assign a drive letter (ex: `E:`)
- Verify the new drive appears in **This PC**

✅ **Task 6: Cleanup**
- Stop/deallocate the VM OR delete the resource group to avoid charges

---

## 📁 Suggested Files

- `lab-guide.md`: Full step-by-step lab instructions  
- `screenshots/`: Portal/RDP/Disk Management screenshots (recommended)  
- `notes.md` (optional): Quick exam takeaways (OS disk vs data disk, RDP security notes)

---

## 🔗 Learn More

- [Create a Windows VM in Azure](https://learn.microsoft.com/training/modules/create-windows-virtual-machine-in-azure/)
- [Connect to a Windows VM using RDP](https://learn.microsoft.com/azure/virtual-machines/windows/connect-rdp)
- [Azure managed disks overview](https://learn.microsoft.com/azure/virtual-machines/managed-disks-overview)
- [Create a snapshot of a managed disk (related)](https://learn.microsoft.com/azure/virtual-machines/snapshot-copy-managed-disk)

---

## 🧵 Tags

`#Azure` `#AzureVM` `#WindowsServer` `#RDP` `#ManagedDisks` `#AZ104` `#AzureLabs`

Created by: **Zion Spearman**  
Use and modify this lab freely for study and practice.
