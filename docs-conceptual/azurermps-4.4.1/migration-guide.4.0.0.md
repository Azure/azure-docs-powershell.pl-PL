---
title: Istotne zmiany dotyczące programu Microsoft Azure PowerShell 4.0.0
description: Ten przewodnik po migracji zawiera listę zmian powodujących niezgodność wprowadzonych w programie Azure PowerShell w wersji 4.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 2f61e41b701dfc263df18064f6ac2cc4c6e4021e
ms.sourcegitcommit: 0b644bfecf4224b2ea83520d1a6a956734d9fba4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/12/2019
ms.locfileid: "67863552"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a><span data-ttu-id="5d3fc-103">Istotne zmiany dotyczące programu Microsoft Azure PowerShell 4.0.0</span><span class="sxs-lookup"><span data-stu-id="5d3fc-103">Breaking changes for Microsoft Azure PowerShell 4.0.0</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="5d3fc-104">Ten dokument służy jako przewodnik zarówno po powiadomieniach o istotnych zmianach, jak i migracji dla użytkowników poleceń cmdlet programu Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5d3fc-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="5d3fc-105">Każda sekcja opisuje zarówno tempo istotnej zmiany, jak i ścieżkę migracji najmniejszego oporu.</span><span class="sxs-lookup"><span data-stu-id="5d3fc-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="5d3fc-106">Aby uzyskać szczegółowy kontekst, zapoznaj się z żądaniem ściągnięcia skojarzonym z każdą zmianą.</span><span class="sxs-lookup"><span data-stu-id="5d3fc-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="5d3fc-107">Spis treści</span><span class="sxs-lookup"><span data-stu-id="5d3fc-107">Table of Contents</span></span>

- [<span data-ttu-id="5d3fc-108">Istotne zmiany w poleceniach cmdlet usługi Compute</span><span class="sxs-lookup"><span data-stu-id="5d3fc-108">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="5d3fc-109">Istotne zmiany w poleceniach cmdlet usługi EventHub</span><span class="sxs-lookup"><span data-stu-id="5d3fc-109">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="5d3fc-110">Istotne zmiany w poleceniach cmdlet usługi Insights</span><span class="sxs-lookup"><span data-stu-id="5d3fc-110">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="5d3fc-111">Istotne zmiany w poleceniach cmdlet usługi Network</span><span class="sxs-lookup"><span data-stu-id="5d3fc-111">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="5d3fc-112">Istotne zmiany w poleceniach cmdlet usługi ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5d3fc-112">Breaking changes to ServiceBus cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)
- [<span data-ttu-id="5d3fc-113">Istotne zmiany w poleceniach cmdlet usługi Sql</span><span class="sxs-lookup"><span data-stu-id="5d3fc-113">Breaking changes to Sql cmdlets</span></span>](#breaking-changes-to-sql-cmdlets)
- [<span data-ttu-id="5d3fc-114">Istotne zmiany w poleceniach cmdlet usługi Storage</span><span class="sxs-lookup"><span data-stu-id="5d3fc-114">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
- [<span data-ttu-id="5d3fc-115">Istotne zmiany w poleceniach cmdlet profilu</span><span class="sxs-lookup"><span data-stu-id="5d3fc-115">Breaking Changes to Profile Cmdlets</span></span>](#breaking-changes-to-profile-cmdlets)
  ## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="5d3fc-116">Istotne zmiany w poleceniach cmdlet usługi Compute</span><span class="sxs-lookup"><span data-stu-id="5d3fc-116">Breaking changes to Compute cmdlets</span></span>

<span data-ttu-id="5d3fc-117">Następujące typy danych wyjściowych miały wpływ na tę wersję:</span><span class="sxs-lookup"><span data-stu-id="5d3fc-117">The following output types were affected this release:</span></span>

### <a name="psvirtualmachine"></a><span data-ttu-id="5d3fc-118">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5d3fc-118">PSVirtualMachine</span></span>
- <span data-ttu-id="5d3fc-119">Właściwości najwyższego poziomu `DataDiskNames` i `NetworkInterfaceIDs` obiektu `PSVirtualMachine` zostały usunięte z typu danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5d3fc-119">Top level properties `DataDiskNames` and `NetworkInterfaceIDs` of nthe `PSVirtualMachine` object have been removed from the output type.</span></span> <span data-ttu-id="5d3fc-120">Te właściwości zawsze były dostępne we właściwościach `StorageProfile` i `NetworkProfile` obiektu `PSVirtualMachine` i będzie sposób, w jaki będą dostępne w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="5d3fc-120">These properties have always been available in the `StorageProfile` and `NetworkProfile` properties of the `PSVirtualMachine` object and will be the way they will need to be accessed going forward.</span></span>
- <span data-ttu-id="5d3fc-121">Ta zmiana ma wpływ na następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5d3fc-121">This change affects the following cmdlets:</span></span>
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

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="5d3fc-122">Istotne zmiany w poleceniach cmdlet usługi EventHub</span><span class="sxs-lookup"><span data-stu-id="5d3fc-122">Breaking changes to EventHub cmdlets</span></span>

<span data-ttu-id="5d3fc-123">Następujące polecenia cmdlet miały wpływ na tę wersję:</span><span class="sxs-lookup"><span data-stu-id="5d3fc-123">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="5d3fc-124">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="5d3fc-124">Get-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="5d3fc-125">Właściwość `ResourceGroupName` została usunięta z typu danych wyjściowych `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="5d3fc-125">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="5d3fc-126">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="5d3fc-126">New-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="5d3fc-127">Właściwość `ResourceGroupName` została usunięta z typu danych wyjściowych `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="5d3fc-127">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="5d3fc-128">Istotne zmiany w poleceniach cmdlet usługi Insights</span><span class="sxs-lookup"><span data-stu-id="5d3fc-128">Breaking changes to Insights cmdlets</span></span>

<span data-ttu-id="5d3fc-129">Następujące polecenia cmdlet miały wpływ na tę wersję:</span><span class="sxs-lookup"><span data-stu-id="5d3fc-129">The following cmdlets were affected this release:</span></span>
    
### <a name="get-azurermusage"></a><span data-ttu-id="5d3fc-130">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="5d3fc-130">Get-AzureRmUsage</span></span>
- <span data-ttu-id="5d3fc-131">To polecenie cmdlet jest przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="5d3fc-131">This cmdlet has been deprecated.</span></span>

### <a name="remove-azurermalertrule"></a><span data-ttu-id="5d3fc-132">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="5d3fc-132">Remove-AzureRmAlertRule</span></span>
- <span data-ttu-id="5d3fc-133">Dane wyjściowe tego polecenia cmdlet zmieniły się z listy z pojedynczym obiektem na pojedynczy obiekt. Ten obiekt zawiera identyfikator żądania i kod stanu.</span><span class="sxs-lookup"><span data-stu-id="5d3fc-133">The output of this cmdlet has changed from a list with a single object to a single object; this object includes the requestId, and status code.</span></span>
    
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
    
### <a name="add-azurermlogalertrule"></a><span data-ttu-id="5d3fc-134">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="5d3fc-134">Add-AzureRmLogAlertRule</span></span>
- <span data-ttu-id="5d3fc-135">To polecenie cmdlet jest przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="5d3fc-135">This cmdlet has been deprecated.</span></span>
    
### <a name="get-azurermalertrule"></a><span data-ttu-id="5d3fc-136">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="5d3fc-136">Get-AzureRmAlertRule</span></span>
- <span data-ttu-id="5d3fc-137">Każdy element danych wyjściowych (lista obiektów) tego polecenia cmdlet jest spłaszczany, tzn. zamiast zwracać obiekty o strukturze `{ Id, Location, Name, Tags, Properties }`, będzie zwracać obiekty o strukturze `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, czyli wszystkie atrybuty zasobu platformy Azure oraz wszystkie atrybuty AlertRuleResource na najwyższym poziomie.</span><span class="sxs-lookup"><span data-stu-id="5d3fc-137">Each element of the output (a list of objects) of this cmdlet is flattened, i.e. instead of returning objects with the structure `{ Id, Location, Name, Tags, Properties }` it will return objects with the structure `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, which is all of the attributes of an Azure Resource plus all of the attributes of an AlertRuleResource at the top level.</span></span>
    
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
    
### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="5d3fc-138">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5d3fc-138">Get-AzureRmAutoscaleSetting</span></span>
- <span data-ttu-id="5d3fc-139">Pole `AutoscaleSettingResourceName` jest przestarzałe, ponieważ zawsze ma taką samą wartość jak pole `Name`.</span><span class="sxs-lookup"><span data-stu-id="5d3fc-139">The `AutoscaleSettingResourceName` field is deprecated since it always has the same value as the `Name` field.</span></span>

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
    
### <a name="remove-azurermlogprofile"></a><span data-ttu-id="5d3fc-140">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="5d3fc-140">Remove-AzureRmLogProfile</span></span>
- <span data-ttu-id="5d3fc-141">Dane wyjściowe tego polecenia cmdlet zmienią się z `Boolean` na obiekt zawierający `RequestId` i `StatusCode`</span><span class="sxs-lookup"><span data-stu-id="5d3fc-141">The output of this cmdlet will change from `Boolean` to and object containing `RequestId` and `StatusCode`</span></span>

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
    
### <a name="add-azurermlogprofile"></a><span data-ttu-id="5d3fc-142">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="5d3fc-142">Add-AzureRmLogProfile</span></span>
- <span data-ttu-id="5d3fc-143">Dane wyjściowe tego polecenia cmdlet zmienią się z obiektu, który zawiera identyfikator żądania, kod stanu i zaktualizowany lub nowo utworzony zasób</span><span class="sxs-lookup"><span data-stu-id="5d3fc-143">The output of this cmdlet will change from an object that includes the requestId, status code, and the updated or newly created resource</span></span>
    
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
    
### <a name="set-azurermdiagnosticsettings"></a><span data-ttu-id="5d3fc-144">Set-AzureRmDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="5d3fc-144">Set-AzureRmDiagnosticSettings</span></span>
- <span data-ttu-id="5d3fc-145">Nazwa polecenia zostanie zmieniona na `Update-AzureRmDiagnosticSettings`</span><span class="sxs-lookup"><span data-stu-id="5d3fc-145">The command is going to be renamed to `Update-AzureRmDiagnosticSettings`</span></span>

```powershell-interactive
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="5d3fc-146">Istotne zmiany w poleceniach cmdlet usługi Network</span><span class="sxs-lookup"><span data-stu-id="5d3fc-146">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="5d3fc-147">Następujące polecenia cmdlet miały wpływ na tę wersję:</span><span class="sxs-lookup"><span data-stu-id="5d3fc-147">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermvirtualnetworkgatewayconnection"></a><span data-ttu-id="5d3fc-148">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5d3fc-148">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="5d3fc-149">Parametr `EnableBgp` został zmieniony, aby pobierać `boolean` zamiast `string`</span><span class="sxs-lookup"><span data-stu-id="5d3fc-149">`EnableBgp` parameter has been changed to take a `boolean` instead of a `string`</span></span>

```powershell-interactive
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="5d3fc-150">Istotne zmiany w poleceniach cmdlet usługi ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5d3fc-150">Breaking changes to ServiceBus cmdlets</span></span>

<span data-ttu-id="5d3fc-151">Następujące polecenia cmdlet miały wpływ na tę wersję:</span><span class="sxs-lookup"><span data-stu-id="5d3fc-151">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermservicebusnamespace"></a><span data-ttu-id="5d3fc-152">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="5d3fc-152">Get-AzureRmServiceBusNamespace</span></span>
- <span data-ttu-id="5d3fc-153">Właściwość `ResourceGroupName` została usunięta z typu danych wyjściowych `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="5d3fc-153">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermservicebusnamespace"></a><span data-ttu-id="5d3fc-154">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="5d3fc-154">New-AzureRmServiceBusNamespace</span></span>

- <span data-ttu-id="5d3fc-155">Właściwość `ResourceGroupName` została usunięta z typu danych wyjściowych `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="5d3fc-155">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-sql-cmdlets"></a><span data-ttu-id="5d3fc-156">Istotne zmiany w poleceniach cmdlet usługi Sql</span><span class="sxs-lookup"><span data-stu-id="5d3fc-156">Breaking changes to Sql cmdlets</span></span>

<span data-ttu-id="5d3fc-157">Następujące polecenia cmdlet miały wpływ na tę wersję:</span><span class="sxs-lookup"><span data-stu-id="5d3fc-157">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermsqldatabasefailovergroup"></a><span data-ttu-id="5d3fc-158">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d3fc-158">New-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="5d3fc-159">Parametr `Tag` został usunięty</span><span class="sxs-lookup"><span data-stu-id="5d3fc-159">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="5d3fc-160">Nazwa parametru `GracePeriodWithDataLossHour` została zmieniona na `GracePeriodWithDataLossHours`</span><span class="sxs-lookup"><span data-stu-id="5d3fc-160">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell-interactive
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a><span data-ttu-id="5d3fc-161">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d3fc-161">Set-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="5d3fc-162">Parametr `Tag` został usunięty</span><span class="sxs-lookup"><span data-stu-id="5d3fc-162">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="5d3fc-163">Nazwa parametru `GracePeriodWithDataLossHour` została zmieniona na `GracePeriodWithDataLossHours`</span><span class="sxs-lookup"><span data-stu-id="5d3fc-163">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell-interactive
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a><span data-ttu-id="5d3fc-164">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d3fc-164">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>
- <span data-ttu-id="5d3fc-165">Parametr `Tag` został usunięty</span><span class="sxs-lookup"><span data-stu-id="5d3fc-165">`Tag` parameter has been removed</span></span>

```powershell-interactive
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a><span data-ttu-id="5d3fc-166">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d3fc-166">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>
- <span data-ttu-id="5d3fc-167">Parametr `Tag` został usunięty</span><span class="sxs-lookup"><span data-stu-id="5d3fc-167">`Tag` parameter has been removed</span></span>

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a><span data-ttu-id="5d3fc-168">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5d3fc-168">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="5d3fc-169">Parametr `PartnerResourceGroupName` został usunięty</span><span class="sxs-lookup"><span data-stu-id="5d3fc-169">`PartnerResourceGroupName` parameter has been removed</span></span>
- <span data-ttu-id="5d3fc-170">Parametr `PartnerServerName` został usunięty</span><span class="sxs-lookup"><span data-stu-id="5d3fc-170">`PartnerServerName` parameter has been removed</span></span>

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a><span data-ttu-id="5d3fc-171">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5d3fc-171">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>
- <span data-ttu-id="5d3fc-172">Wartość `Usage_Anomaly` nie jest już prawidłowa dla parametru `ExcludedDetectionType`</span><span class="sxs-lookup"><span data-stu-id="5d3fc-172">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a><span data-ttu-id="5d3fc-173">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5d3fc-173">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
- <span data-ttu-id="5d3fc-174">Wartość `Usage_Anomaly` nie jest już prawidłowa dla parametru `ExcludedDetectionType`</span><span class="sxs-lookup"><span data-stu-id="5d3fc-174">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="5d3fc-175">Istotne zmiany w poleceniach cmdlet usługi Storage</span><span class="sxs-lookup"><span data-stu-id="5d3fc-175">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="5d3fc-176">Następujące właściwości danych wyjściowych miały wpływ na tę wersję:</span><span class="sxs-lookup"><span data-stu-id="5d3fc-176">The following output type properties were affected this release:</span></span>

### <a name="azurestorageblobicloudblobserviceclient"></a><span data-ttu-id="5d3fc-177">AzureStorageBlob.ICloudBlob.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="5d3fc-177">AzureStorageBlob.ICloudBlob.ServiceClient</span></span>
- <span data-ttu-id="5d3fc-178">Następujące właściwości zostały usunięte z tego typu (_uwaga_: nadal można je znaleźć we właściwości `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="5d3fc-178">The following properties were removed from this type (_note_: they can still be found in `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="5d3fc-179">Ta zmiana ma wpływ na następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5d3fc-179">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a><span data-ttu-id="5d3fc-180">AzureStorageContainer.CloudBlobContainer.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="5d3fc-180">AzureStorageContainer.CloudBlobContainer.ServiceClient</span></span>
- <span data-ttu-id="5d3fc-181">Następujące właściwości zostały usunięte z tego typu (_uwaga_: nadal można je znaleźć we właściwości `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="5d3fc-181">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="5d3fc-182">Ta zmiana ma wpływ na następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5d3fc-182">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a><span data-ttu-id="5d3fc-183">AzureStorageQueue.CloudQueue.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="5d3fc-183">AzureStorageQueue.CloudQueue.ServiceClient</span></span>
- <span data-ttu-id="5d3fc-184">Następujące właściwości zostały usunięte z tego typu (_uwaga_: nadal można je znaleźć we właściwości `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="5d3fc-184">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="5d3fc-185">Ta zmiana ma wpływ na następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5d3fc-185">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a><span data-ttu-id="5d3fc-186">AzureStorageTable.CloudTable.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="5d3fc-186">AzureStorageTable.CloudTable.ServiceClient</span></span>
- <span data-ttu-id="5d3fc-187">Następujące właściwości zostały usunięte z tego typu (_uwaga_: nadal można je znaleźć we właściwości `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="5d3fc-187">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="5d3fc-188">Ta zmiana ma wpływ na następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5d3fc-188">This change affects the following cmdlets:</span></span>
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

## <a name="breaking-changes-to-profile-cmdlets"></a><span data-ttu-id="5d3fc-189">Istotne zmiany w poleceniach cmdlet profilu</span><span class="sxs-lookup"><span data-stu-id="5d3fc-189">Breaking Changes to Profile Cmdlets</span></span>

<span data-ttu-id="5d3fc-190">Następujące polecenia cmdlet i typy danych wyjściowych polecenia cmdlet zostały zmienione w tej wersji.</span><span class="sxs-lookup"><span data-stu-id="5d3fc-190">The following cmdlets and cmdlet output types were changed in this release.</span></span>

### <a name="add-azurermaccount-breaking-changes"></a><span data-ttu-id="5d3fc-191">Istotne zmiany polecenia Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="5d3fc-191">Add-AzureRmAccount breaking changes</span></span>

- <span data-ttu-id="5d3fc-192">Parametr ```EnvironmentName``` został usunięty i zastąpiony parametrem ```Environment```; parametr ```Environment``` teraz przyjmuje ciąg, a nie obiekt ```AzureEnvironment```</span><span class="sxs-lookup"><span data-stu-id="5d3fc-192">```EnvironmentName``` parameter has been removed and replaced with ```Environment```, the ```Environment``` now takes a string and not an ```AzureEnvironment``` object</span></span>

```powershell-interactive
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a><span data-ttu-id="5d3fc-193">Nazwę polecenia Select-AzureRmProfile zmieniono na Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="5d3fc-193">Select-AzureRmProfile was renamed to Import-AzureRmContext</span></span>

<span data-ttu-id="5d3fc-194">Nazwę polecenia ```Select-AzureRmProfile``` zmieniono na ```Import-AzureRmContext```</span><span class="sxs-lookup"><span data-stu-id="5d3fc-194">```Select-AzureRmProfile``` was renamed to ```Import-AzureRmContext```</span></span>

```powershell-interactive
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a><span data-ttu-id="5d3fc-195">Nazwę polecenia Save-AzureRmProfile zmieniono na Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="5d3fc-195">Save-AzureRmProfile was renamed to Save-AzureRmContext</span></span>

<span data-ttu-id="5d3fc-196">Nazwę polecenia ```Save-AzureRmProfile``` zmieniono na ```Save-AzureRmContext```</span><span class="sxs-lookup"><span data-stu-id="5d3fc-196">```Save-AzureRmProfile``` was renamed to ```Save-AzureRmContext```</span></span>

```powershell-interactive
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a><span data-ttu-id="5d3fc-197">Istotne zmiany w typie danych wyjściowych PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="5d3fc-197">Breaking Changes to output PSAzureContext Type</span></span>

- <span data-ttu-id="5d3fc-198">Właściwość ```TokenCache``` zmieniono na typ, który implementuje ```IAzureTokenCache``` zamiast ```byte[]```</span><span class="sxs-lookup"><span data-stu-id="5d3fc-198">The ```TokenCache``` property changed to a type that implements ```IAzureTokenCache``` instead of a ```byte[]```</span></span>

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

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a><span data-ttu-id="5d3fc-199">Istotne zmiany w typie danych wyjściowych PSAzureAccount</span><span class="sxs-lookup"><span data-stu-id="5d3fc-199">Breaking Changes to the output PSAzureAccount Type</span></span>

- <span data-ttu-id="5d3fc-200">Właściwość ```AccountType``` została zmieniona na ```Type```</span><span class="sxs-lookup"><span data-stu-id="5d3fc-200">The ```AccountType``` property was changed to ```Type```</span></span>

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

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a><span data-ttu-id="5d3fc-201">Istotne zmiany w typie danych wyjściowych PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="5d3fc-201">Breaking Changes to the output PSAzureSubscription Type</span></span>
- <span data-ttu-id="5d3fc-202">Właściwość ```SubscriptionId``` została zmieniona na ```Id```</span><span class="sxs-lookup"><span data-stu-id="5d3fc-202">The ```SubscriptionId``` property was changed to ```Id```</span></span>

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

- <span data-ttu-id="5d3fc-203">Właściwość ```SubscriptionName``` została zmieniona na ```Name```</span><span class="sxs-lookup"><span data-stu-id="5d3fc-203">The ```SubscriptionName``` property was changed to ```Name```</span></span>

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

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a><span data-ttu-id="5d3fc-204">Istotne zmiany w typie danych wyjściowych PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="5d3fc-204">Breaking Changes to the output PSAzureTenant Type</span></span>

- <span data-ttu-id="5d3fc-205">Właściwość ```TenantId``` została zmieniona na ```Id```</span><span class="sxs-lookup"><span data-stu-id="5d3fc-205">The ```TenantId``` property was changed to ```Id```</span></span>

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

- <span data-ttu-id="5d3fc-206">Właściwość ```Domain``` została zmieniona na ```Directory```</span><span class="sxs-lookup"><span data-stu-id="5d3fc-206">The ```Domain``` property was changed to ```Directory```</span></span>

```powershell-interactive
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
