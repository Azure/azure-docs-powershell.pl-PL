---
title: Istotne zmiany dotyczące programu Microsoft Azure PowerShell 4.0.0
description: Ten przewodnik po migracji zawiera listę zmian powodujących niezgodność wprowadzonych w programie Azure PowerShell w wersji 4.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 379bbc788e530598f51e893a2bad71f09b059193
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153442"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a>Istotne zmiany dotyczące programu Microsoft Azure PowerShell 4.0.0

Ten dokument służy jako przewodnik zarówno po powiadomieniach o istotnych zmianach, jak i migracji dla użytkowników poleceń cmdlet programu Microsoft Azure PowerShell. Każda sekcja opisuje zarówno tempo istotnej zmiany, jak i ścieżkę migracji najmniejszego oporu. Aby uzyskać szczegółowy kontekst, zapoznaj się z żądaniem ściągnięcia skojarzonym z każdą zmianą.

## <a name="table-of-contents"></a>Spis treści

- [Istotne zmiany w poleceniach cmdlet usługi Compute](#breaking-changes-to-compute-cmdlets)
- [Istotne zmiany w poleceniach cmdlet usługi EventHub](#breaking-changes-to-eventhub-cmdlets)
- [Istotne zmiany w poleceniach cmdlet usługi Insights](#breaking-changes-to-insights-cmdlets)
- [Istotne zmiany w poleceniach cmdlet usługi Network](#breaking-changes-to-network-cmdlets)
- [Istotne zmiany w poleceniach cmdlet usługi ServiceBus](#breaking-changes-to-servicebus-cmdlets)
- [Istotne zmiany w poleceniach cmdlet usługi Sql](#breaking-changes-to-sql-cmdlets)
- [Istotne zmiany w poleceniach cmdlet usługi Storage](#breaking-changes-to-storage-cmdlets)
- [Istotne zmiany w poleceniach cmdlet profilu](#breaking-changes-to-profile-cmdlets)
  ## <a name="breaking-changes-to-compute-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi Compute

Następujące typy danych wyjściowych miały wpływ na tę wersję:

### <a name="psvirtualmachine"></a>PSVirtualMachine
- Właściwości najwyższego poziomu `DataDiskNames` i `NetworkInterfaceIDs` obiektu `PSVirtualMachine` zostały usunięte z typu danych wyjściowych. Te właściwości zawsze były dostępne we właściwościach `StorageProfile` i `NetworkProfile` obiektu `PSVirtualMachine` i będzie sposób, w jaki będą dostępne w przyszłości.
- Ta zmiana ma wpływ na następujące polecenia cmdlet:
    - `Add-AzureRmVMDataDisk`
    - `Add-AzureRmVMNetworkInterface`
    - `Get-AzureRmVM`
    - `Remove-AzureRmVMDataDisk`
    - `Remove-AzureRmVMNetworkInterface`
    - `Set-AzureRmVMDataDisk`

```powershell-interactive
# Old
$vm.DataDiskNames
$vm.NetworkInterfaceIDs

# New
$vm.StorageProfile.DataDisks | Select -Property Name
$vm.NetworkProfile.NetworkInterfaces | Select -Property Id
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi EventHub

Następujące polecenia cmdlet miały wpływ na tę wersję:

### <a name="get-azurermeventhubnamespace"></a>Get-AzureRmEventHubNamespace
- Właściwość `ResourceGroupName` została usunięta z typu danych wyjściowych `NamespaceAttributes`

### <a name="new-azurermeventhubnamespace"></a>New-AzureRmEventHubNamespace
- Właściwość `ResourceGroupName` została usunięta z typu danych wyjściowych `NamespaceAttributes`

## <a name="breaking-changes-to-insights-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi Insights

Następujące polecenia cmdlet miały wpływ na tę wersję:
    
### <a name="get-azurermusage"></a>Get-AzureRmUsage
- To polecenie cmdlet jest przestarzałe.

### <a name="remove-azurermalertrule"></a>Remove-AzureRmAlertRule
- Dane wyjściowe tego polecenia cmdlet zmieniły się z listy z pojedynczym obiektem na pojedynczy obiekt. Ten obiekt zawiera identyfikator żądania i kod stanu.
    
```powershell-interactive
# Old  
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
if ($s1 -ne $null)
{
    $r = $s1(0).RequestId
    $s = $s1(0).StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogalertrule"></a>Add-AzureRmLogAlertRule
- To polecenie cmdlet jest przestarzałe.
    
### <a name="get-azurermalertrule"></a>Get-AzureRmAlertRule
- Każdy element danych wyjściowych (lista obiektów) tego polecenia cmdlet jest spłaszczany, tzn. zamiast zwracać obiekty o strukturze `{ Id, Location, Name, Tags, Properties }`, będzie zwracać obiekty o strukturze `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, czyli wszystkie atrybuty zasobu platformy Azure oraz wszystkie atrybuty AlertRuleResource na najwyższym poziomie.
    
```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
      
    Write-Host $rules(0).Id
    Write-Host $rules(0).Properties.IsEnabled
    Write-Host $rules(0).Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
 
    Write-Host $rules(0).Id
      
    # Properties will remain for a while
    Write-Host $rules(0).Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules(0).IsEnabled
    Write-Host $rules(0).Condition
}
```
    
### <a name="get-azurermautoscalesetting"></a>Get-AzureRmAutoscaleSetting
- Pole `AutoscaleSettingResourceName` jest przestarzałe, ponieważ zawsze ma taką samą wartość jak pole `Name`.

```powershell-interactive
# Old  
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# There won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```
    
### <a name="remove-azurermlogprofile"></a>Remove-AzureRmLogProfile
- Dane wyjściowe tego polecenia cmdlet zmienią się z `Boolean` na obiekt zawierający `RequestId` i `StatusCode`

```powershell-interactive
# Old  
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
if ($s1 -eq $true)
{
    Write-Host "Removed"
}
else
{
    Write-Host "Failed"
}

# New
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogprofile"></a>Add-AzureRmLogProfile
- Dane wyjściowe tego polecenia cmdlet zmienią się z obiektu, który zawiera identyfikator żądania, kod stanu i zaktualizowany lub nowo utworzony zasób
    
```powershell-interactive
# Old  
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.ServiceBusRuleId

# New
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.RequestId
$s = $s1.StatusCode
$a = $s1.NewResource.ServiceBusRuleId
    
```
    
### <a name="set-azurermdiagnosticsettings"></a>Set-AzureRmDiagnosticSettings
- Nazwa polecenia zostanie zmieniona na `Update-AzureRmDiagnsoticSettings`

```powershell-interactive
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi Network

Następujące polecenia cmdlet miały wpływ na tę wersję:

### <a name="new-azurermvirtualnetworkgatewayconnection"></a>New-AzureRmVirtualNetworkGatewayConnection
- Parametr `EnableBgp` został zmieniony, aby pobierać `boolean` zamiast `string`

```powershell-interactive
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi ServiceBus

Następujące polecenia cmdlet miały wpływ na tę wersję:

### <a name="get-azurermservicebusnamespace"></a>Get-AzureRmServiceBusNamespace
- Właściwość `ResourceGroupName` została usunięta z typu danych wyjściowych `NamespaceAttributes`

### <a name="new-azurermservicebusnamespace"></a>New-AzureRmServiceBusNamespace

- Właściwość `ResourceGroupName` została usunięta z typu danych wyjściowych `NamespaceAttributes`

## <a name="breaking-changes-to-sql-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi Sql

Następujące polecenia cmdlet miały wpływ na tę wersję:

### <a name="new-azurermsqldatabasefailovergroup"></a>New-AzureRmSqlDatabaseFailoverGroup
- Parametr `Tag` został usunięty
- Nazwa parametru `GracePeriodWithDataLossHour` została zmieniona na `GracePeriodWithDataLossHours`

```powershell-interactive
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a>Set-AzureRmSqlDatabaseFailoverGroup
- Parametr `Tag` został usunięty
- Nazwa parametru `GracePeriodWithDataLossHour` została zmieniona na `GracePeriodWithDataLossHours`

```powershell-interactive
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a>Add-AzureRmSqlDatabaseToFailoverGroup
- Parametr `Tag` został usunięty

```powershell-interactive
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a>Remove-AzureRmSqlDatabaseFromFailoverGroup
- Parametr `Tag` został usunięty

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a>Remove-AzureRmSqlDatabaseFailoverGroup
- Parametr `PartnerResourceGroupName` został usunięty
- Parametr `PartnerServerName` został usunięty

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a>Set-AzureRmSqlDatabaseThreatDetectionPolicy
- Wartość `Usage_Anomaly` nie jest już prawidłowa dla parametru `ExcludedDetectionType`

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a>Set-AzureRmSqlServerThreatDetectionPolicy
- Wartość `Usage_Anomaly` nie jest już prawidłowa dla parametru `ExcludedDetectionType`

## <a name="breaking-changes-to-storage-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi Storage

Następujące właściwości danych wyjściowych miały wpływ na tę wersję:

### <a name="azurestorageblobicloudblobserviceclient"></a>AzureStorageBlob.ICloudBlob.ServiceClient
- Następujące właściwości zostały usunięte z tego typu (_uwaga_: nadal można je znaleźć we właściwości `DefaultRequestOptions`):
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- Ta zmiana ma wpływ na następujące polecenia cmdlet:
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a>AzureStorageContainer.CloudBlobContainer.ServiceClient
- Następujące właściwości zostały usunięte z tego typu (_uwaga_: nadal można je znaleźć we właściwości `DefaultRequestOptions`):
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- Ta zmiana ma wpływ na następujące polecenia cmdlet:
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a>AzureStorageQueue.CloudQueue.ServiceClient
- Następujące właściwości zostały usunięte z tego typu (_uwaga_: nadal można je znaleźć we właściwości `DefaultRequestOptions`):
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- Ta zmiana ma wpływ na następujące polecenia cmdlet:
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a>AzureStorageTable.CloudTable.ServiceClient
- Następujące właściwości zostały usunięte z tego typu (_uwaga_: nadal można je znaleźć we właściwości `DefaultRequestOptions`):
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- Ta zmiana ma wpływ na następujące polecenia cmdlet:
    - `Get-AzureStorageTable`
    - `New-AzureStorageTable`
    
```powershell-interactive
# Old
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.LocationMode       
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.RetryPolicy

# New
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.DefaultRequestOptions.LocationMode     
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.DefaultRequestOptions.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.DefaultRequestOptions.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.DefaultRequestOptions.RetryPolicy
```

## <a name="breaking-changes-to-profile-cmdlets"></a>Istotne zmiany w poleceniach cmdlet profilu

Następujące polecenia cmdlet i typy danych wyjściowych polecenia cmdlet zostały zmienione w tej wersji.

### <a name="add-azurermaccount-breaking-changes"></a>Istotne zmiany polecenia Add-AzureRmAccount

- Parametr ```EnvironmentName``` został usunięty i zastąpiony parametrem ```Environment```; parametr ```Environment``` teraz przyjmuje ciąg, a nie obiekt ```AzureEnvironment```

```powershell-interactive
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a>Nazwę polecenia Select-AzureRmProfile zmieniono na Import-AzureRmContext

Nazwę polecenia ```Select-AzureRmProfile``` zmieniono na ```Import-AzureRmContext```

```powershell-interactive
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a>Nazwę polecenia Save-AzureRmProfile zmieniono na Import-AzureRmContext

Nazwę polecenia ```Save-AzureRmProfile``` zmieniono na ```Save-AzureRmContext```

```powershell-interactive
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a>Istotne zmiany w typie danych wyjściowych PSAzureContext

- Właściwość ```TokenCache``` zmieniono na typ, który implementuje ```IAzureTokenCache``` zamiast ```byte[]```

```powershell-interactive
# Old
$bytes = (Get-AzureRmContext).TokenCache
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache
$bytes = (Add-AzureRmAccount).Context.TokenCache

# New
$bytes = (Get-AzureRmContext).TokenCache.CacheData
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache.CacheData
$bytes = (Add-AzureRmAccount).Context.TokenCache.CacheData
```

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a>Istotne zmiany w typie danych wyjściowych PSAzureAccount

- Właściwość ```AccountType``` została zmieniona na ```Type```

```powershell-interactive
# Old
$type = (Get-AzureRmContext).Account.AccountType
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.AccountType
$type = (Add-AzureRmAccount).Context.Account.AccountType

# New 
$type = (Get-AzureRmContext).Account.Type
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.Type
$type = (Add-AzureRmAccount).Context.Account.Type
```

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a>Istotne zmiany w typie danych wyjściowych PSAzureSubscription
- Właściwość ```SubscriptionId``` została zmieniona na ```Id```

```powershell-interactive
# Old
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId

# New
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
```

- Właściwość ```SubscriptionName``` została zmieniona na ```Name```

```powershell-interactive
# Old
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionName
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionName
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName

# New
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Name
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Name
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
```

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a>Istotne zmiany w typie danych wyjściowych PSAzureTenant

- Właściwość ```TenantId``` została zmieniona na ```Id```

```powershell-interactive
# Old
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).TenantId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.TenantId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId

# New
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
```

- Właściwość ```Domain``` została zmieniona na ```Directory```

```powershell-interactive
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
