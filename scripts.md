Managing Azure resources via PowerShell is a powerful way to automate and streamline your workflows. Here are the basics:

### 1. **Setting Up Azure PowerShell**
   - **Install Azure PowerShell Module**: Use the command `Install-Module -Name Az` to install the Azure PowerShell module.
   - **Connect to Azure Account**: Use `Connect-AzAccount` to authenticate and connect to your Azure subscription.

### 2. **Resource Group Management**
   - **Create a Resource Group**: 
     ```powershell
     New-AzResourceGroup -Name "MyResourceGroup" -Location "EastUS"
     ```
   - **List Resource Groups**: 
     ```powershell
     Get-AzResourceGroup
     ```
   - **Delete a Resource Group**: 
     ```powershell
     Remove-AzResourceGroup -Name "MyResourceGroup"
     ```

### 3. **Managing Resources**
   - **Create a Resource**: For example, to create a storage account:
     ```powershell
     New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -Location "EastUS" -SkuName "Standard_LRS"
     ```
   - **List Resources**: 
     ```powershell
     Get-AzResource -ResourceGroupName "MyResourceGroup"
     ```
   - **Delete a Resource**: 
     ```powershell
     Remove-AzResource -ResourceGroupName "MyResourceGroup" -ResourceName "mystorageaccount" -ResourceType "Microsoft.Storage/storageAccounts"
     ```

### 4. **Tagging Resources**
   - **Add Tags to a Resource**: 
     ```powershell
     Set-AzResource -ResourceGroupName "MyResourceGroup" -ResourceName "mystorageaccount" -ResourceType "Microsoft.Storage/storageAccounts" -Tag @{Environment="Production"; Department="Finance"}
     ```
   - **List Tags**: 
     ```powershell
     Get-AzTag
     ```

### 5. **Monitoring and Alerts**
   - **View Activity Logs**: 
     ```powershell
     Get-AzLog -ResourceGroupName "MyResourceGroup"
     ```
   - **Set Up Alerts**: Use Azure Monitor to create and manage alerts based on resource metrics and logs.

### 6. **Automation and Scripting**
   - **Runbooks**: Use Azure Automation to create and manage runbooks for automating repetitive tasks.
   - **Scripts**: Write and execute PowerShell scripts to automate complex workflows and resource management tasks.

These basics should help you get started with managing Azure resources using PowerShell¹². If you need more detailed information or specific examples, feel free to ask!

Source: Conversation with Copilot, 21/08/2024
(1) Manage resources - Azure PowerShell - Azure Resource Manager. https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/manage-resources-powershell.
(2) PowerShell Basics: How to Manage Azure Resources via PowerShell. https://techcommunity.microsoft.com/t5/itops-talk-blog/powershell-basics-how-to-manage-azure-resources-via-powershell/ba-p/1036671.
(3) Manage Azure Resources using PowerShell Function App with Managed .... https://techcommunity.microsoft.com/t5/apps-on-azure-blog/manage-azure-resources-using-powershell-function-app-with/ba-p/3099282.
(4) Manage Azure resources with Windows PowerShell - Training. https://learn.microsoft.com/en-us/training/modules/manage-azure-resources-windows-powershell/.
(5) powershell-azure-resource-manager.md - GitHub. https://github.com/toddkitta/azure-content/blob/master/articles/powershell-azure-resource-manager.md.
(6) undefined. https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/quickstarts/microsoft.storage/storage-account-create/azuredeploy.json.