---
title: Zmiany powodujące niezgodność dotyczące programu Microsoft Azure PowerShell 6.0.0.
description: Ten przewodnik po migracji zawiera listę zmian powodujących niezgodność wprowadzonych w programie Azure PowerShell w wersji 6.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 5/1/2018
ms.openlocfilehash: 4f9c99152fd6ddc23aec005c8e8957e545e65246
ms.sourcegitcommit: 9cb98f055a0525c2061f65149965d5e7c3e03ddc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/30/2018
ms.locfileid: "43117358"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a>Zmiany powodujące niezgodność dotyczące programu Microsoft Azure PowerShell 6.0.0.

Ten dokument służy jako przewodnik zarówno po powiadomieniach o istotnych zmianach, jak i migracji dla użytkowników poleceń cmdlet programu Microsoft Azure PowerShell. Każda sekcja opisuje zarówno tempo istotnej zmiany, jak i ścieżkę migracji najmniejszego oporu. Aby uzyskać szczegółowy kontekst, zapoznaj się z żądaniem ściągnięcia skojarzonym z każdą zmianą.

## <a name="table-of-contents"></a>Spis treści

- [Ogólne zmiany powodujące niezgodność](#general-breaking-changes)
    - [Minimalna wymagana wersja programu PowerShell została podniesiona do wersji 5.0](#minimum-powershell-version-required-bumped-to-50)
    - [Automatyczne zapisywanie kontekstu jest domyślnie włączone](#context-autosaved-enabled-by-default)
    - [Usunięcie aliasów Tags](#removal-of-tags-alias)
- [Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Compute](#breaking-changes-to-azurermcompute-cmdlets)
- [Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Compute AzureRM.DataLakeStore](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Compute AzureRM.Dns](#breaking-changes-to-azurermdns-cmdlets)
- [Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Compute AzureRM.Insights](#breaking-changes-to-azurerminsights-cmdlets)
- [Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.KeyVault](#breaking-changes-to-azurermkeyvault-cmdlets)
- [Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Network](#breaking-changes-to-azurermnetwork-cmdlets)
- [Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.RedisCache](#breaking-changes-to-azurermrediscache-cmdlets)
- [Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Resources](#breaking-changes-to-azurermresources-cmdlets)
- [Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Storage](#breaking-changes-to-azurermstorage-cmdlets)
- [Usunięte moduły](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a>Ogólne zmiany powodujące niezgodność

### <a name="minimum-powershell-version-required-bumped-to-50"></a>Minimalna wymagana wersja programu PowerShell została podniesiona do wersji 5.0

Wcześniej w usłudze Azure PowerShell wymagany był program PowerShell w wersji _co najmniej_ 3.0, aby możliwe było uruchamianie jakichkolwiek poleceń cmdlet. W przyszłości to wymaganie zostanie podniesione do wersji 5.0 programu PowerShell. Informacje o uaktualnianiu programu PowerShell 5.0 znajdują się w [tej tabeli](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

### <a name="context-autosave-enabled-by-default"></a>Automatyczne zapisywanie kontekstu jest domyślnie włączone

Automatyczne zapisywanie kontekstu służy do zapisywania na platformie Azure informacji logowania, których można użyć między nowymi i różnymi sesjami programu PowerShell. Więcej informacji na temat automatycznego zapisywania kontekstu zawiera [ten dokument](https://docs.microsoft.com/en-us/powershell/azure/context-persistence).

Wcześniej automatyczne zapisywanie kontekstu było domyślnie wyłączone, co oznacza, że informacje użytkownika dotyczące uwierzytelniania na platformie Azure nie były przechowywane między sesjami, dopóki użytkownik nie uruchomił polecenia cmdlet `Enable-AzureRmContextAutosave` w celu włączenia trwałości kontekstu. W przyszłości automatyczne zapisywanie kontekstu będzie domyślnie włączone, co oznacza, że dla użytkowników _bez zapisanych ustawień automatycznego zapisywania kontekstu_ kontekst będzie przechowywany do czasu ich następnego zalogowania się. Użytkownicy mogą zrezygnować z tej funkcji przy użyciu polecenia cmdlet `Disable-AzureRmContextAutosave`.

_Uwaga_: ta zmiana nie będzie dotyczyła użytkowników, którzy wcześniej wyłączyli automatyczne zapisywanie kontekstu, użytkowników z włączonym automatycznym zapisywaniem kontekstu ani istniejących kontekstów

### <a name="removal-of-tags-alias"></a>Usunięcie aliasów Tags

Alias `Tags` dla parametru `Tag` został usunięty z wielu poleceń cmdlet. Poniżej przedstawiono listę modułów (i odpowiednich poleceń cmdlet), na które ta zmiana ma wpływ:

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a>Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Compute

**Różne**
- Właściwość nazwy jednostki SKU zagnieżdżona w typach `PSDisk` i `PSSnapshot` została zmieniona z wartości `StandardLRS` i `PremiumLRS` odpowiednio na wartości `Standard_LRS` i `Premium_LRS`

```powershell
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- Właściwość typu konta magazynu zagnieżdżona w typach `PSVirtualMachine`, `PSVirtualMachineScaleSet` i `PSImage` została zmieniona z wartości `StandardLRS` i `PremiumLRS` odpowiednio na wartości `Standard_LRS` i `Premium_LRS`

```powershell
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

**Add-AzureRmImageDataDisk**
- Dopuszczalne wartości dla parametru `StorageAccountType` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`

**Add-AzureRmVMDataDisk**
- Dopuszczalne wartości dla parametru `StorageAccountType` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`

**Add-AzureRmVmssDataDisk**
- Dopuszczalne wartości dla parametru `StorageAccountType` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`

**New-AzureRmAvailabilitySet**
- Parametr `Managed` został usunięty i wprowadzono parametr `Sku`

```powershell
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

**New-AzureRmDiskConfig**
- Dopuszczalne wartości dla parametru `SkuName` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`

**New-AzureRmDiskUpdateConfig**
- Dopuszczalne wartości dla parametru `SkuName` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`

**New-AzureRmSnapshotConfig**
- Dopuszczalne wartości dla parametru `SkuName` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`

**New-AzureRmSnapshotUpdateConfig**
- Dopuszczalne wartości dla parametru `SkuName` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`

**Set-AzureRmImageOsDisk**
- Dopuszczalne wartości dla parametru `StorageAccountType` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`

**Set-AzureRmVMAEMExtension**
- Parametr `DisableWAD` został usunięty
    -  Usługa Diagnostyka Microsoft Azure jest domyślnie wyłączona

**Set-AzureRmVMDataDisk**
- Dopuszczalne wartości dla parametru `StorageAccountType` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`

**Set-AzureRmVMOSDisk**
- Dopuszczalne wartości dla parametru `StorageAccountType` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`

**Set-AzureRmVmssStorageProfile**
- Dopuszczalne wartości dla parametru `ManagedDisk` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`

**Update-AzureRmVmss**
- Dopuszczalne wartości dla parametru `ManagedDiskStorageAccountType` zostały zmienione z `StandardLRS` i `PremiumLRS` na odpowiednio `Standard_LRS` i `Premium_LRS`

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a>Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.DataLakeStore

**Export-AzureRmDataLakeStoreItem**
- Parametry `PerFileThreadCount` i `ConcurrentFileCount` zostały usunięte. W przyszłości użyj parametru `Concurrency`

```powershell
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

**Import-AzureRmDataLakeStoreItem**
- Parametry `PerFileThreadCount` i `ConcurrentFileCount` zostały usunięte. W przyszłości użyj parametru `Concurrency`

```powershell
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

**Remove-AzureRmDataLakeStoreItem**
- Parametr `Clean` został usunięty

```powershell
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a>Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Dns

**New-AzureRmDnsRecordSet**
- Parametr `Force` został usunięty

**Remove-AzureRmDnsRecordSet**
- Parametr `Force` został usunięty

**Remove-AzureRmDnsZone**
- Parametr `Force` został usunięty

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a>Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Insights

**Add-AzureRmAutoscaleSetting**
- Aliasy parametrów `AutoscaleProfiles` i `Notifications` zostały usunięte

**Add-AzureRmLogProfile**
- Aliasy parametrów `Categories` i `Locations` zostały usunięte

**Add-AzureRmMetricAlertRule**
- Alias parametru `Actions` został usunięty

**Add-AzureRmWebtestAlertRule**
- Alias parametru `Actions` został usunięty

**Get-AzureRmLog**
- Aliasy parametrów `MaxRecords` i `MaxEvents` zostały usunięte

**Get-AzureRmMetricDefinition**
- Alias parametru `MetricNames` został usunięty

**New-AzureRmAlertRuleEmail**
- Aliasy parametrów `CustomEmails` i `SendToServiceOwners` zostały usunięte

**New-AzureRmAlertRuleWebhook**
- Alias parametru `Properties` został usunięty

**New-AzureRmAutoscaleNotification**
- Aliasy parametrów `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` i `Webhooks` zostały usunięte

**New-AzureRmAutoscaleProfile**
- Aliasy parametrów `Rules`, `ScheduleDays`, `ScheduleHours` i `ScheduleMinutes` zostały usunięte

**New-AzureRmAutoscaleWebhook**
- Alias parametru `Properties` został usunięty

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a>Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.KeyVault

**Add-AzureKeyVaultCertificate**
- Parametr `CertificatePolicy` stał się obowiązkowy.

**Set-AzureKeyVaultManagedStorageSasDefinition**
- W poleceniu cmdlet nie są już akceptowane pojedyncze parametry, które tworzą token dostępu. Zamiast tego w poleceniach cmdlet jawne parametry tokenu, takie jak `Service` lub `Permissions`, zostały zastąpione ogólnym parametrem `TemplateUri` odpowiadającym przykładowemu tokenowi dostępu zdefiniowanemu w innym miejscu (prawdopodobnie za pomocą poleceń cmdlet programu PowerShell lub utworzonemu ręcznie zgodnie z dokumentacją usługi Storage) W poleceniu cmdlet zachowano parametr `ValidityPeriod`.

Więcej informacji dotyczących tworzenia tokenów dostępu współdzielonego dla usługi Azure Storage można znaleźć na stronach dokumentacji, czyli odpowiednio:
- [Tworzenie sygnatury dostępu współdzielonego usługi] (https://docs.microsoft.com/en-us/rest/api/storageservices/Constructing-a-Service-SAS)
- [Tworzenia sygnatury dostępu współdzielonego konta] (https://docs.microsoft.com/en-us/rest/api/storageservices/constructing-an-account-sas)

```powershell
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

**Set-AzureKeyVaultCertificateIssuer**
- Parametr `IssuerProvider` stał się obowiązkowy.

**Undo-AzureKeyVaultCertificateRemoval**
- Dane wyjściowe tego polecenia cmdlet zmieniły się z wartości `CertificateBundle` na `PSKeyVaultCertificate`.

**Undo-AzureRmKeyVaultRemoval**
- Parametr `ResourceGroupName` został usunięty z zestawu parametrów `InputObject` i zamiast tego jest pobierany z właściwości `ResourceId` parametru `InputObject`.

**Set-AzureRmKeyVaultAccessPolicy**
- Uprawnienie `all` zostało usunięte z parametrów `PermissionsToKeys`, `PermissionsToSecrets`, i `PermissionsToCertificates`.

**Ogólne**
- Właściwość `ValueFromPipelineByPropertyName` została usunięta ze wszystkich poleceń cmdlet, w których włączone było potokowanie za pomocą parametru `InputObject`.  Polecenia cmdlet, których to dotyczy, są następujące:
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- Poziomy `ConfirmImpact` zostały usunięte ze wszystkich poleceń cmdlet.  Polecenia cmdlet, których to dotyczy, są następujące:
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- Parametr `IKeyVaultDataServiceClient` został zaktualizowany, więc wszystkie operacje certyfikatu zwracają typy PSTypes zamiast typów SDK. Obejmuje to:
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a>Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Network


**Add-AzureRmApplicationGatewayBackendHttpSettings**
- Parametr `ProbeEnabled` został usunięty

**Add-AzureRmVirtualNetworkPeering**
- Alias parametru `AlloowGatewayTransit` został usunięty

**New-AzureRmApplicationGatewayBackendHttpSettings**
- Parametr `ProbeEnabled` został usunięty

**Set-AzureRmApplicationGatewayBackendHttpSettings**
- Parametr `ProbeEnabled` został usunięty

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a>Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.RedisCache

**New-AzureRmRedisCache**
- Parametry `Subnet` oraz `VirtualNetwork` zostały usunięte i wprowadzono parametr `SubnetId`
- Parametr `RedisVersion` został usunięty
- Parametr `MaxMemoryPolicy` został usunięty i wprowadzono parametr `RedisConfiguration`

```powershell
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

**Set-AzureRmRedisCache**
- Parametr `MaxMemoryPolicy` został usunięty i wprowadzono parametr `RedisConfiguration`

```powershell
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a>Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Resources

**Find-AzureRmResource**
- To polecenie cmdlet zostało usunięte, a jego funkcjonalność została przeniesiona do polecenia `Get-AzureRmResource`

```powershell
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

**Find-AzureRmResourceGroup**
- To polecenie cmdlet zostało usunięte, a jego funkcjonalność została przeniesiona do polecenia `Get-AzureRmResourceGroup`

```powershell
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

**Get-AzureRmRoleDefinition**
- Parametr `AtScopeAndBelow` został usunięty.

```powershell

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a>Zmiany powodujące niezgodność dotyczące poleceń cmdlet AzureRM.Storage

**New-AzureRmStorageAccount**
- Parametr `EnableEncryptionService` został usunięty

**Set-AzureRmStorageAccount**
- Parametry `EnableEncryptionService` i `DisableEncryptionService` zostały usunięte

## <a name="removed-modules"></a>Usunięte moduły

### `AzureRM.ServerManagement`

Usługa Server Management Tools została [wycofana w zeszłym roku](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), w wyniku czego odpowiedni moduł dla usługi SMT, `AzureRM.ServerManagement`, został usunięty z modułu `AzureRM` i nie będzie w przyszłości dostarczany.

### `AzureRM.SiteRecovery`

Moduł `AzureRM.SiteRecovery` jest zastępowany przez moduł `AzureRM.RecoveryServices.SiteRecovery`, który jest funkcjonalnym nadzbiorem modułu `AzureRM.SiteRecovery` i obejmuje nowy zestaw równoważnych poleceń cmdlet. Poniżej znajduje się pełna lista mapowań ze starych na nowe polecenia cmdlet:

| Przestarzałe polecenie cmdlet                                        | Równoważne polecenie cmdlet                                                | Aliasy                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |
