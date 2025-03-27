1. # Cloud-portofolio
## Azure VM Deployment with NSG and Backup

### Objective
Deploy a secure Windows VM in Azure with attached storage, NSG, and backup configured.

### Tools Used
- Azure Portal
- Azure CLI
- Azure Resource Manager (ARM) Templates (optional)

### Steps
1. Created a Resource Group: `cloud-rg`
2. Deployed a Windows VM with Standard B2s size
3. Attached a 64 GB data disk
4. Applied NSG rules (RDP only from my IP)
5. Enabled Backup with default policy

### Learnings
- Configuring security rules
- Managing storage
- Backup setup using Recovery Services Vault
2. # Project: Azure VM Auto-Shutdown with Email Notification

## 🔹 Objective
Save costs by automatically shutting down Azure VMs after work hours and notifying the administrator via email using Logic Apps.

## 🔧 Tools Used
- Azure Automation Account
- PowerShell Runbook
- Logic Apps
- Azure Monitor (optional)

## 🔁 Workflow
1. Automation Runbook shuts down the VM
2. Logic App sends an email to notify shutdown status
3. (Optional) Azure Monitor tracks if shutdown fails

## 💻 PowerShell Script (Runbook)
```powershell
$rg = "Myfirstproject"
$vmName = "1stVirtualMachi"
Stop-AzVM -ResourceGroupName $rg -Name $vmName -Force



