---
title: Istotne zmiany dotyczące programu Microsoft Azure PowerShell 5.0.0
description: Ten przewodnik po migracji zawiera listę zmian powodujących niezgodność wprowadzonych w programie Azure PowerShell w wersji 5.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 81f52ee8b84f60d59a7f2d53b6675129ac054fd6
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243739"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a>Istotne zmiany dotyczące programu Microsoft Azure PowerShell 5.0.0

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Ten dokument służy jako przewodnik zarówno po powiadomieniach o istotnych zmianach, jak i migracji dla użytkowników poleceń cmdlet programu Microsoft Azure PowerShell. Każda sekcja opisuje zarówno tempo istotnej zmiany, jak i ścieżkę migracji najmniejszego oporu. Aby uzyskać szczegółowy kontekst, zapoznaj się z żądaniem ściągnięcia skojarzonym z każdą zmianą.

## <a name="table-of-contents"></a>Spis treści

- [Istotne zmiany w poleceniach cmdlet usługi ApiManagement](#breaking-changes-to-apimanagement-cmdlets)
- [Istotne zmiany w poleceniach cmdlet usługi Batch](#breaking-changes-to-batch-cmdlets)
- [Istotne zmiany w poleceniach cmdlet usługi Compute](#breaking-changes-to-compute-cmdlets)
- [Istotne zmiany w poleceniach cmdlet usługi EventHub](#breaking-changes-to-eventhub-cmdlets)
- [Istotne zmiany w poleceniach cmdlet usługi Insights](#breaking-changes-to-insights-cmdlets)
- [Istotne zmiany w poleceniach cmdlet usługi Network](#breaking-changes-to-network-cmdlets)
- [Istotne zmiany w poleceniach cmdlet usługi zasobów](#breaking-changes-to-resources-cmdlets)
- [Istotne zmiany w poleceniach cmdlet usługi ServiceBus](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi ApiManagement

### <a name="new-azurermapimanagementbackendproxy"></a>**New-AzureRmApiManagementBackendProxy**
- Parametry „UserName” i „Password” są zastępowane na rzecz obiektu PSCredential

```powershell-interactive
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a>**New-AzureRmApiManagementUser**
- Parametr „Password” jest zastępowany na rzecz obiektu SecureString

```powershell-interactive
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a>**Set-AzureRmApiManagementUser**
- Parametr „Password” jest zastępowany na rzecz obiektu SecureString

```powershell-interactive
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi Batch

### <a name="new-azurebatchcertificate"></a>**New-AzureBatchCertificate**
- Parametr `Password` jest zastępowany na rzecz ciągu zabezpieczeń

```powershell-interactive
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a>**New-AzureBatchComputeNodeUser**
- Parametr `Password` jest zastępowany na rzecz ciągu zabezpieczeń

```powershell-interactive
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a>**Set-AzureRmBatchComputeNodeUser**
- Parametr `Password` jest zastępowany na rzecz ciągu zabezpieczeń

```powershell-interactive
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a>**New-AzureBatchTask**
 - Usunięto przełącznik `RunElevated` i zastąpiono go właściwością `UserIdentity`.

```powershell-interactive
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

Wpływa to również na właściwość `RunElevated` w obiektach `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` i `PSJobReleaseTask`.

### <a name="psmultiinstancesettings"></a>**PSMultiInstanceSettings**

- Konstruktor `PSMultiInstanceSettings` nie przyjmuje wymaganego parametru `numberOfInstances`; zamiast tego przyjmuje wymagany parametr `coordinationCommandLine`.

```powershell-interactive
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a>**Get-AzureBatchTask**
 - Usunięto właściwość `RunElevated` w elemencie `PSCloudTask`. Dodano właściwość `UserIdentity` w celu zastąpienia właściwości `RunElevated`.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

Wpływa to również na właściwość `RunElevated` w obiektach `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` i `PSJobReleaseTask`.

### <a name="multiple-types"></a>**Wiele typów**

- Nazwa właściwości `SchedulingError` w obiekcie `PSExitConditions` została zmieniona `PreProcessingError`.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a>**Wiele typów**

- Nazwa właściwości `SchedulingError` w obiektach `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` i `PSTaskExecutionInformation` została zmieniona na `FailureInformation`.
  - `FailureInformation` jest zwracany zawsze w przypadku niepowodzenia zadania. Obejmuje to wszystkie przypadki błędów planowania, a także kody zakończenia z wartością niezerową oraz błędy przekazywania plików z nowej funkcji plików wyjściowych.
  - Struktura jest taka sama jak wcześniej, a więc w przypadku używania tego typu nie są wymagane żadne zmiany kodu.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

Wpływa to również na polecenia: Get-AzureBatchPool, Get-AzureBatchSubtask i Get-AzureBatchJobPreparationAndReleaseTaskStatus

### <a name="new-azurebatchpool"></a>**New-AzureBatchPool**
 - Usunięto właściwość `TargetDedicated` i zastąpiono ją właściwościami `TargetDedicatedComputeNodes` i `TargetLowPriorityComputeNodes`.
 - `TargetDedicatedComputeNodes` ma alias `TargetDedicated`.

```powershell-interactive
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

Ma to również wpływ na polecenia: Start-AzureBatchPoolResize

### <a name="get-azurebatchpool"></a>**Get-AzureBatchPool**
 - Nazwa właściwości `TargetDedicated` i `CurrentDedicated` w obiekcie `PSCloudPool` została zmieniona na `TargetDedicatedComputeNodes` i `CurrentDedicatedComputeNodes`.

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a>**Type PSCloudPool**

- Zmieniono nazwę `ResizeError` na `ResizeErrors` w obiekcie `PSCloudPool` i teraz jest to kolekcja.

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a>**New-AzureBatchJob**
- Nazwa właściwości `TargetDedicated` w obiekcie `PSPoolSpecification` została zmieniona na `TargetDedicatedComputeNodes`.

```powershell-interactive
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a>**Get-AzureBatchNodeFile**
 - Usunięto właściwość `Name` i zastąpiono ją właściwością `Path`.
 - `Path` ma alias `Name`.

```powershell-interactive
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

Ma to również wpływ na polecenia: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile

### <a name="type-psnodefile"></a>Typ **PSNodeFile**

 - Nazwa właściwości `Name` w obiekcie `PSNodeFile` została zmieniona na `Path`.

```powershell-interactive
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a>**Get-AzureBatchSubtask**
- Właściwości `PreviousState` i `State` obiektu `PSSubtaskInformation` nie są już typu `TaskState`, lecz typu `SubtaskState`.
  - W odróżnieniu od typu `TaskState`, typ `SubtaskState` nie ma wartości `Active`, ponieważ podzadania nie mogą być w stanie `Active`.

```powershell-interactive
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi Compute

### <a name="set-azurermvmaccessextension"></a>**Set-AzureRmVMAccessExtension**
- Parametry „UserName” i „Password” są zastępowane na rzecz obiektu PSCredential

```powershell-interactive
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi EventHub

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a>**New-AzureRmEventHubNamespaceAuthorizationRule**
- Polecenie cmdlet „New-AzureRmEventHubNamespaceAuthorizationRule” zostało usunięte. Użyj polecenia cmdlet „New-AzureRmEventHubAuthorizationRule”

### <a name="get-azurermeventhubnamespaceauthorizationrule"></a>**Get-AzureRmEventHubNamespaceAuthorizationRule**
- Polecenie cmdlet „Get-AzureRmEventHubNamespaceAuthorizationRule” zostało usunięte. Użyj polecenia cmdlet „Get-AzureRmEventHubAuthorizationRule”

### <a name="set-azurermeventhubnamespaceauthorizationrule"></a>**Set-AzureRmEventHubNamespaceAuthorizationRule**
- Polecenie cmdlet „Set-AzureRmEventHubNamespaceAuthorizationRule” zostało usunięte. Użyj polecenia cmdlet „Set-AzureRmEventHubAuthorizationRule”

### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a>**Remove-AzureRmEventHubNamespaceAuthorizationRule**
- Polecenie cmdlet „Remove-AzureRmEventHubNamespaceAuthorizationRule” zostało usunięte. Użyj polecenia cmdlet „Remove-AzureRmEventHubAuthorizationRule”

### <a name="new-azurermeventhubnamespacekey"></a>**New-AzureRmEventHubNamespaceKey**
- Polecenie cmdlet „New-AzureRmEventHubNamespaceKey” zostało usunięte. Użyj polecenia cmdlet „New-AzureRmEventHubKey”

### <a name="get-azurermeventhubnamespacekey"></a>**Get-AzureRmEventHubNamespaceKey**
- Polecenie cmdlet „Get-AzureRmEventHubNamespaceKey” zostało usunięte. Użyj polecenia „Get-AzureRmEventHubKey”

### <a name="new-azurermeventhubnamespace"></a>**New-AzureRmEventHubNamespace**
- Właściwości „Status” i „Enabled” z atrybutów obszaru nazw zostaną usunięte.

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property
$namespace = Get-AzureRmEventHubNamespace <parameters>
```

### <a name="get-azurermeventhubnamespace"></a>**Get-AzureRmEventHubNamespace**
- Właściwości „Status” i „Enabled” z atrybutów obszaru nazw zostaną usunięte.

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property
$namespace = Get-AzureRmEventHubNamespace <parameters>
```

### <a name="set-azurermeventhubnamespace"></a>**Set-AzureRmEventHubNamespace**
- Właściwości „Status” i „Enabled” z atrybutów obszaru nazw zostaną usunięte.

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property
$namespace = Set-AzureRmEventHubNamespace <parameters>
```

### <a name="new-azurermeventhubconsumergroup"></a>**New-AzureRmEventHubConsumerGroup**
- Właściwość „EventHubPath” z elementu ConsumerGroupAttributes zostanie usunięta.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```

### <a name="set-azurermeventhubconsumergroup"></a>**Set-AzureRmEventHubConsumerGroup**
- Właściwość „EventHubPath” z elementu ConsumerGroupAttributes zostanie usunięta.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```

### <a name="get-azurermeventhubconsumergroup"></a>**Get-AzureRmEventHubConsumerGroup**
- Właściwość „EventHubPath” z elementu ConsumerGroupAttributes zostanie usunięta.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi Insights

### <a name="add-azurermlogalertrule"></a>**Add-AzureRMLogAlertRule**
- Polecenie cmdlet **Add-AzureRMLogAlertRule** jest przestarzałe
- Po 1 października użycie tego polecenia cmdlet nie będzie miało żadnego efektu, ponieważ ta funkcja zostanie przeniesiona do alertów dziennika aktywności. Aby uzyskać więcej informacji, zobacz https://aka.ms/migratemealerts.

### <a name="get-azurermusage"></a>**Get-AzureRMUsage**
- Polecenie **Get-AzureRMUsage** jest przestarzałe

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a>**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**
- Zmiana danych wyjściowych: pole EventChannels z obiektu EventData (zwracanego przez te polecenia cmdlet) jest przestarzałe, ponieważ obecnie zwraca wartość stałą (Admin,Operation).

### <a name="get-azurermalertrule"></a>**Get-AzureRmAlertRule**
- Zmiana danych wyjściowych: dane wyjściowe tego polecenia cmdlet zostaną spłaszczone, co oznacza eliminację pola właściwości, aby ulepszyć środowisko użytkownika.

```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled

    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a>**Get-AzureRmAutoscaleSetting**
- Zmiana danych wyjściowych: pole AutoscaleSettingResourceName zostanie wycofane, ponieważ zawsze jest równe polu Nazwa.

```powershell-interactive
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting

# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a>**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**
- Zmiana danych wyjściowych: typ danych wyjściowych zmieni się, aby zwracać pojedynczy obiekt zawierający identyfikator żądania i kod stanu.

```powershell-interactive
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi Network

### <a name="add-azurermapplicationgatewaysslcertificate"></a>**Add-AzureRmApplicationGatewaySslCertificate**
- Parametr „Password” jest zastępowany na rzecz obiektu SecureString

```powershell-interactive
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a>**New-AzureRmApplicationGatewaySslCertificate**
- Parametr „Password” jest zastępowany na rzecz obiektu SecureString

```powershell-interactive
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a>**Set-AzureRmApplicationGatewaySslCertificate**
- Parametr „Password” jest zastępowany na rzecz obiektu SecureString

```powershell-interactive
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a>Istotne zmiany w poleceniach cmdlet zasobów

### <a name="new-azurermadappcredential"></a>**New-AzureRmADAppCredential**
- Parametr „Password” jest zastępowany na rzecz obiektu SecureString

```powershell-interactive
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a>**New-AzureRmADApplication**
- Parametr „Password” jest zastępowany na rzecz obiektu SecureString

```powershell-interactive
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a>**New-AzureRmADServicePrincipal**
- Parametr „Password” jest zastępowany na rzecz obiektu SecureString

```powershell-interactive
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a>**New-AzureRmADSpCredential**
- Parametr „Password” jest zastępowany na rzecz obiektu SecureString

```powershell-interactive
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a>**New-AzureRmADUser**
- Parametr „Password” jest zastępowany na rzecz obiektu SecureString

```powershell-interactive
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a>**Set-AzureRmADUser**
- Parametr „Password” jest zastępowany na rzecz obiektu SecureString

```powershell-interactive
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi ServiceBus

### <a name="get-azurermservicebustopicauthorizationrule"></a>**Get-AzureRmServiceBusTopicAuthorizationRule**
- Polecenie cmdlet „Get-AzureRmServiceBusTopicAuthorizationRule” zostało usunięte. Użyj polecenia cmdlet „Get-AzureRmServiceBusAuthorizationRule”.

### <a name="get-azurermservicebustopickey"></a>**Get-AzureRmServiceBusTopicKey**
- Polecenie cmdlet „Get-AzureRmServiceBusTopicKey” zostało usunięte. Użyj polecenia cmdlet „Get-AzureRmServiceBusKey”.

### <a name="new-azurermservicebustopicauthorizationrule"></a>**New-AzureRmServiceBusTopicAuthorizationRule**
- Polecenie cmdlet „New-AzureRmServiceBusTopicAuthorizationRule” zostało usunięte. Użyj polecenia cmdlet „New-AzureRmServiceBusAuthorizationRule”.

### <a name="new-azurermservicebustopickey"></a>**New-AzureRmServiceBusTopicKey**
- Polecenie cmdlet „New-AzureRmServiceBusTopicKey” zostało usunięte. Użyj polecenia cmdlet „New-AzureRmServiceBusKey”.

### <a name="remove-azurermservicebustopicauthorizationrule"></a>**Remove-AzureRmServiceBusTopicAuthorizationRule**
- Polecenie cmdlet „Remove-AzureRmServiceBusTopicAuthorizationRule” zostało usunięte. Użyj polecenia cmdlet „Remove-AzureRmServiceBusAuthorizationRule”.

### <a name="set-azurermservicebustopicauthorizationrule"></a>**Set-AzureRmServiceBusTopicAuthorizationRule**
- Polecenie cmdlet „Set-AzureRmServiceBusTopicAuthorizationRule” zostało usunięte. Użyj polecenia cmdlet „Set-AzureRmServiceBusAuthorizationRule”.

### <a name="new-azurermservicebusnamespacekey"></a>**New-AzureRmServiceBusNamespaceKey**
- Polecenie cmdlet „New-AzureRmServiceBusNamespaceKey” zostało usunięte. Użyj polecenia cmdlet „New-AzureRmServiceBusKey”.

### <a name="get-azurermservicebusqueueauthorizationrule"></a>**Get-AzureRmServiceBusQueueAuthorizationRule**
- Polecenie cmdlet „Get-AzureRmServiceBusQueueAuthorizationRule” zostało usunięte. Użyj polecenia cmdlet „Get-AzureRmServiceBusAuthorizationRule”.

### <a name="get-azurermservicebusqueuekey"></a>**Get-AzureRmServiceBusQueueKey**
- Polecenie cmdlet „Get-AzureRmServiceBusQueueKey” zostało usunięte. Użyj polecenia cmdlet „Get-AzureRmServiceBusKey”.

### <a name="new-azurermservicebusqueueauthorizationrule"></a>**New-AzureRmServiceBusQueueAuthorizationRule**
- Polecenie cmdlet „New-AzureRmServiceBusQueueAuthorizationRule” zostało usunięte. Użyj polecenia cmdlet „New-AzureRmServiceBusAuthorizationRule”.

### <a name="new-azurermservicebusqueuekey"></a>**New-AzureRmServiceBusQueueKey**
- Polecenie cmdlet „New-AzureRmServiceBusQueueKey” zostało usunięte. Użyj polecenia cmdlet „New-AzureRmServiceBusKey”.

### <a name="remove-azurermservicebusqueueauthorizationrule"></a>**Remove-AzureRmServiceBusQueueAuthorizationRule**
- Polecenie cmdlet „Remove-AzureRmServiceBusQueueAuthorizationRule” zostało usunięte. Użyj polecenia cmdlet „GRemove-AzureRmServiceBusAuthorizationRule”.

### <a name="set-azurermservicebusqueueauthorizationrule"></a>**Set-AzureRmServiceBusQueueAuthorizationRule**
- Polecenie cmdlet „Set-AzureRmServiceBusQueueAuthorizationRule” zostało usunięte. Użyj polecenia cmdlet „Set-AzureRmServiceBusAuthorizationRule”.

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a>**Get-AzureRmServiceBusNamespaceAuthorizationRule**
- Polecenie cmdlet „Get-AzureRmServiceBusNamespaceAuthorizationRule” zostało usunięte. Użyj polecenia cmdlet „Get-AzureRmServiceBusAuthorizationRule”.

### <a name="get-azurermservicebusnamespacekey"></a>**Get-AzureRmServiceBusNamespaceKey**
- Polecenie cmdlet „Get-AzureRmServiceBusNamespaceKey” zostało usunięte. Użyj polecenia cmdlet „Get-AzureRmServiceBusKey”.

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a>**New-AzureRmServiceBusNamespaceAuthorizationRule**
- Polecenie cmdlet „New-AzureRmServiceBusNamespaceAuthorizationRule” zostało usunięte. Użyj polecenia cmdlet „New-AzureRmServiceBusAuthorizationRule”.

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a>**Remove-AzureRmServiceBusNamespaceAuthorizationRule**
- Polecenie cmdlet „Remove-AzureRmServiceBusNamespaceAuthorizationRule” zostało usunięte. Użyj polecenia cmdlet „Remove-AzureRmServiceBusAuthorizationRule”.

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a>**Set-AzureRmServiceBusNamespaceAuthorizationRule**
- Polecenie cmdlet „Set-AzureRmServiceBusNamespaceAuthorizationRule” zostało usunięte. Użyj polecenia cmdlet „Set-AzureRmServiceBusAuthorizationRule”.

### <a name="type-namespaceattributes"></a>**Typ NamespaceAttributes**
- Usunięto następujące właściwości
    - Enabled (Włączony)
    - Stan

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a>**Typ QueueAttribute**
- Następujące właściwości są oznaczone jako przestarzałe:
    - EnableBatchedOperations
    - EntityAvailabilityStatus
    - IsAnonymousAccessible
    - SupportOrdering

```powershell-interactive
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
```

### <a name="type-topicattribute"></a>**Typ TopicAttribute**
- Następujące właściwości są oznaczone jako przestarzałe:
    - Lokalizacja
    - IsExpress
    - IsAnonymousAccessible
    - FilteringMessagesBeforePublishing
    - EnableSubscriptionPartitioning
    - EntityAvailabilityStatus

```powershell-interactive
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$topic = Get-AzureRmServiceBusTopic <parameters>
```

### <a name="type-subscriptionattribute"></a>**Typ SubscriptionAttribute**
- Następujące właściwości są oznaczone jako przestarzałe
    - DeadLetteringOnFilterEvaluationExceptions
    - EntityAvailabilityStatus
    - IsReadOnly
    - Lokalizacja

```powershell-interactive
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
```
