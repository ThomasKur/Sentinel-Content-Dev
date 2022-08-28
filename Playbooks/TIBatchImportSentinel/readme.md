# BatchImportSentinel

## Description

The BatchImportSentinel playbook is used to submit multiple threat indicators to the Sentinel Intelligence Platform.

![](./images/BatchImportToSentinel1.png)

## Grant Permissions to Managed Identity






```powershell

# The objectID of the Managed Identity
$spObjectID = "84bf5e8e-4d9d-44d9-b9e0-6668e41d05be"

# The app ID of the Microsoft Graph
$appId = "00000003-0000-0000-c000-000000000000"

# Permissions required to add ThreatIndicators
$permissionsToAdd = "ThreatIndicators.ReadWrite.OwnedBy"

Connect-AzureAD
$app = Get-AzureADServicePrincipal -Filter "AppId eq '$appId'"
foreach ($permission in $permissionsToAdd)
{
   $role = $app.AppRoles | where Value -Like $permission | Select-Object -First 1
   New-AzureADServiceAppRoleAssignment -Id $role.Id -ObjectId $spObjectID -PrincipalId $spObjectID -ResourceId $app.ObjectId
}
```


