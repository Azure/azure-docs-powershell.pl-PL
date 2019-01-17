---
title: Zmiany powodujące niezgodność dotyczące modułu Az 1.0.0 programu Microsoft Azure PowerShell
description: Ten przewodnik migracji zawiera listę zmian powodujących niezgodność wprowadzonych w wersji 1 modułu Az programu Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/14/2018
ms.openlocfilehash: be3e19dc4b689adbc63b933dd9f3454122d5344a
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342214"
---
# <a name="migration-guide-for-az-100"></a>Przewodnik migracji modułu Az 1.0.0

W tym dokumencie opisano różnice między wersjami 6.x modułu AzureRM i wersją 1.0.0 modułu Az.

## <a name="table-of-contents"></a>Spis treści
- [Ogólne zmiany powodujące niezgodność](#general-breaking-changes)
  - [Zmiany prefiksów poleceń cmdlet w postaci rzeczownika](#cmdlet-noun-prefix-changes)
  - [Zmiany nazw modułów](#module-name-changes)
  - [Usunięte moduły](#removed-modules)
  - [Windows PowerShell 5.1 i .NET 4.7.2](#windows-powershell-51-and-net-472)
  - [Tymczasowe usunięcie logowania użytkowników przy użyciu obiektu PSCredential](#temporary-removal-of-user-login-using-pscredential)
  - [Domyślne logowanie za pomocą kodu urządzenia zamiast monitu przeglądarki internetowej](#temporary-default-device-code-login-instead-of-web-browser-prompt)
- [Zmiany powodujące niezgodność modułów](#module-breaking-changes)
  - [Az.ApiManagement (wcześniej AzureRM.ApiManagement)](#azapimanagement-previously-azurermapimanagement)
  - [Az.Billing (wcześniej AzureRM.Billing, AzureRM.Consumption i AzureRM.UsageAggregates)](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [Az.CognitiveServices (wcześniej AzureRM.CognitiveServices)](#azcognitiveservices-previously-azurermcognitiveservices)
  - [Az.Compute (wcześniej AzureRM.Compute)](#azcompute-previously-azurermcompute)
  - [Az.DataFactory (wcześniej AzureRM.DataFactories i AzureRM.DataFactoryV2)](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [Az.DataLakeAnalytics (wcześniej AzureRM.DataLakeAnalytics)](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [Az.DataLakeStore (wcześniej AzureRM.DataLakeStore)](#azdatalakestore-previously-azurermdatalakestore)
  - [Az.KeyVault (wcześniej AzureRM.KeyVault)](#azkeyvault-previously-azurermkeyvault)
  - [Az.Media (wcześniej AzureRM.Media)](#azmedia-previously-azurermmedia)
  - [Az.Monitor (wcześniej AzureRM.Insights)](#azmonitor-previously-azurerminsights)
  - [Az.Network (wcześniej AzureRM.Network)](#aznetwork-previously-azurermnetwork)
  - [Az.OperationalInsights (wcześniej AzureRM.OperationalInsights)](#azoperationalinsights-previously-azurermoperationalinsights)
  - [Az.RecoveryServices (wcześniej AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup i AzureRM.RecoveryServices.SiteRecovery)](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [Az.Resources (wcześniej AzureRM.Resources)](#azresources-previously-azurermresources)
  - [Az.ServiceFabric (wcześniej AzureRM.ServiceFabric)](#azservicefabric-previously-azurermservicefabric)
  - [Az.Sql (wcześniej AzureRM.Sql)](#azsql-previously-azurermsql)
  - [Az.Storage (wcześniej Azure.Storage i AzureRM.Storage)](#azstorage-previously-azurestorage-and-azurermstorage)
  - [Az.Websites (wcześniej AzureRM.Websites)](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a>Ogólne zmiany powodujące niezgodność
### <a name="cmdlet-noun-prefix-changes"></a>Zmiany prefiksów poleceń cmdlet w postaci rzeczownika
W module AzureRM polecenia cmdlet używały prefiksu w postaci rzeczownika „AzureRM” lub „Azure”.  Moduł Az upraszcza i normalizuje nazwy poleceń cmdlet, więc wszystkie polecenia cmdlet mają prefiks w postaci rzeczownika „Az”. Na przykład:
```powershell
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

Zmieniono na:
```powershell
Get-AzVM
Get-AzKeyVaultSecret
```

Aby ułatwić przejście na te nowe nazwy poleceń cmdlet, moduł Az wprowadza dwa nowe polecenia cmdlet: ```Enable-AzureRmAlias``` i ```Disable-AzureRmAlias```.  Polecenie cmdlet ```Enable-AzureRmAlias``` tworzy aliasy dla starszych nazw poleceń cmdlet w module AzureRM wskazujące nowsze nazwy poleceń cmdlet w module Az.  Polecenie cmdlet umożliwia tworzenie aliasów w bieżącej sesji albo we wszystkich sesjach przez zmianę profilu użytkownika lub maszyny. 

Na przykład poniższy skrypt w module AzureRM:
```powershell
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Może zostać uruchomiony tylko z niewielkimi zmianami, jeśli zostanie użyte polecenie cmdlet ```Enable-AzureRmAlias```:
```powershell
#Requires -Modules Az.Storage
Enable-AzureRmAlias
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Uruchomienie polecenia cmdlet ```Enable-AzureRmAlias -Scope CurrentUser``` spowoduje włączenie aliasów dla wszystkich otwieranych sesji programu PowerShell, więc po jego wykonaniu nie trzeba w ogóle zmieniać skryptów podobnych do poniższego:
```powershell
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Aby uzyskać szczegółowe informacje dotyczące użycia aliasów poleceń cmdlet, wykonaj polecenie ```Get-Help -Online Enable-AzureRmAlias``` w wierszu polecenia programu PowerShell.

Polecenie ```Disable-AzureRmAlias``` usuwa aliasy poleceń cmdlet modułu AzureRM utworzone przez polecenie ```Enable-AzureRmAlias```.  Aby uzyskać szczegółowe informacje, wykonaj polecenie ```Get-Help -Online Disable-AzureRmAlias``` w wierszu polecenia programu PowerShell.

### <a name="module-name-changes"></a>Zmiany nazw modułów
- Nazwy modułów zostały zmienione z `AzureRM.*` na `Az.*`, z wyjątkiem następujących modułów:
```
AzureRM.Profile                       -> Az.Accounts
Azure.AnalysisServices                -> Az.AnalysisServices
AzureRM.Consumption                   -> Az.Billing
AzureRM.UsageAggregates               -> Az.Billing
AzureRM.DataFactories                 -> Az.DataFactory
AzureRM.DataFactoryV2                 -> Az.DataFactory
AzureRM.MachineLearningCompute        -> Az.MachineLearning
AzureRM.Insights                      -> Az.Monitor
AzureRM.RecoveryServices.Backup       -> Az.RecoveryServices
AzureRM.RecoveryServices.SiteRecovery -> Az.RecoveryServices
AzureRM.Tags                          -> Az.Resources
Azure.Storage                         -> Az.Storage
```

Zmiany nazw modułów oznaczają, że każdy skrypt, który używa instrukcji ```#Requires``` lub ```Import-Module``` do ładowania określonych modułów, będzie trzeba zmienić tak, aby używał nowego modułu.

#### <a name="migrating-requires-statements"></a>Migrowanie instrukcji #Requires
Skrypty używające instrukcji #Requires do deklarowania zależności od modułów AzureRM należy zaktualizować tak, aby używały nowych nazw modułów
```powershell
#Requires -Module AzureRM.Compute
```

Należy zmienić na
```powershell
#Requires -Module Az.Compute
```

#### <a name="migrating-import-module-statements"></a>Migrowanie instrukcji Import-Module
Skrypty używające instrukcji ```Import-Module``` do ładowania modułów AzureRM należy zaktualizować tak, aby odzwierciedlały nowe nazwy modułów.
```powershell
Import-Module -Name AzureRM.Compute
```

Należy zmienić na
```powershell
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a>Migrowanie w pełni kwalifikowanych wywołań poleceń cmdlet
Skrypty używające wywołań poleceń cmdlet kwalifikowanych za pomocą modułu, np.
```powershell
AzureRM.Compute\Get-AzureRmVM
```

Należy zmienić tak, aby używały nowych nazw modułów i poleceń cmdlet
```powershell
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a>Migrowanie zależności manifestu modułów
W przypadku modułów, w których zależności od modułów AzureRM są wyrażane za pomocą pliku manifestu modułów (psd1), należy zaktualizować nazwy modułów w sekcji „RequiredModules”

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

Należy zmienić na

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a>Usunięte moduły
- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

Narzędzia dla tych usług nie są już aktywnie wspierane.  Zachęcamy klientów do jak najszybszego przechodzenia do alternatywnych usług.

### <a name="windows-powershell-51-and-net-472"></a>Windows PowerShell 5.1 i .NET 4.7.2
- W celu korzystania z modułu Az w programie Windows PowerShell 5.1 konieczna jest instalacja programu .NET 4.7.2. Jednak używanie modułu Az w programie PowerShell Core nie wymaga programu .NET 4.7.2. 

### <a name="temporary-removal-of-user-login-using-pscredential"></a>Tymczasowe usunięcie logowania użytkowników przy użyciu obiektu PSCredential
- Ze względu na zmiany w przepływie uwierzytelniania dla platformy .NET Standard tymczasowo usuwamy możliwość logowania użytkownika za pomocą obiektu PSCredential. Ta możliwość zostanie ponownie udostępniona w wersji dla programu Windows PowerShell 5.1 opublikowanej 15.01.2019. Ta kwestia została szczegółowo omówiona w ramach [tego problemu.](https://github.com/Azure/azure-powershell/issues/7430)

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a>Domyślne logowanie za pomocą kodu urządzenia zamiast monitu przeglądarki internetowej
- Ze względu na zmiany w przepływie uwierzytelniania dla platformy .NET Standard używamy logowania urządzenia jako domyślnego przepływu logowania podczas logowania interakcyjnego. Logowanie oparte na przeglądarce internetowej ponownie stanie się domyślne dla programu Windows PowerShell 5.1 w wersji opublikowanej 15.01.2019. Użytkownicy będą wtedy mogli wybrać logowanie urządzenia za pomocą parametru przełącznika.

## <a name="module-breaking-changes"></a>Zmiany powodujące niezgodność modułów

### <a name="azapimanagement-previously-azurermapimanagement"></a>Az.ApiManagement (wcześniej AzureRM.ApiManagement)
- Usunięto następujące polecenia cmdlet:
  - New-AzureRmApiManagementHostnameConfiguration
  - Set-AzureRmApiManagementHostnames
  - Update-AzureRmApiManagementDeployment
  - Import-AzureRmApiManagementHostnameCertificate
  - Zamiast nich do ustawiania tych właściwości użyj polecenia cmdlet **Set-AzApiManagement**
- Usunięto następujące właściwości
  - Usunięto właściwości `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` i `ScmHostnameConfiguration` typu `PsApiManagementHostnameConfiguration` z klasy `PsApiManagementContext`. Zamiast nich używaj właściwości `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` i `ScmCustomHostnameConfiguration` typu `PsApiManagementCustomHostNameConfiguration`.
  - Usunięto właściwość `StaticIPs` z klasy PsApiManagementContext. Właściwość została podzielona na właściwości `PublicIPAddresses` i `PrivateIPAddresses`.
  - Usunięto wymaganą właściwość `Location` z polecenia cmdlet New-AzureApiManagementVirtualNetwork.

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a>Az.Billing (wcześniej AzureRM.Billing, AzureRM.Consumption i AzureRM.UsageAggregates)
- Parametr `InvoiceName` został usunięty z polecenia cmdlet `Get-AzConsumptionUsageDetail`.  W skryptach będzie trzeba używać innych parametrów tożsamości na potrzeby faktury.

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a>Az.CognitiveServices (wcześniej AzureRM.CognitiveServices)
- Usunięto zestaw parametrów `GetSkusWithAccountParamSetName` z polecenia cmdlet `Get-AzCognitiveServicesAccountSkus`.  Musisz uzyskiwać jednostki SKU według typu konta i lokalizacji, a nie nazwy grupy zasobów i nazwy konta.

### <a name="azcompute-previously-azurermcompute"></a>Az.Compute (wcześniej AzureRM.Compute)
- Pole `IdentityIds` zostało usunięte z właściwości `Identity` w obiektach `PSVirtualMachine` i `PSVirtualMachineScaleSet`. Skrypty nie powinny już używać wartości tego pola do podejmowania decyzji dotyczących przetwarzania.
- Typ właściwości `InstanceView` obiektu `PSVirtualMachineScaleSetVM` został zmieniony z `VirtualMachineInstanceView` na `VirtualMachineScaleSetVMInstanceView`
- Właściwości `AutoOSUpgradePolicy` i `AutomaticOSUpgrade` zostały usunięte z właściwości `UpgradePolicy`
- Typ właściwości `Sku` w obiekcie `PSSnapshotUpdate` został zmieniony z `DiskSku` na `SnapshotSku`
- Zestaw `VmScaleSetVMParameterSet` został usunięty z polecenia cmdlet `Add-AzVMDataDisk`. Nie można już dodawać pojedynczego dysku danych do maszyny wirtualnej w zestawie skalowania.

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a>Az.DataFactory (wcześniej AzureRM.DataFactories i AzureRM.DataFactoryV2)
- Parametr `GatewayName` stał się obowiązkowy w poleceniu cmdlet `New-AzDataFactoryEncryptValue`
- Usunięto polecenie cmdlet `New-AzDataFactoryGatewayKey`
- Usunięto parametr `LinkedServiceName` z polecenia cmdlet `Get-AzDataFactoryV2ActivityRun`. Skrypty nie powinny już używać wartości tego pola do podejmowania decyzji dotyczących przetwarzania.

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a>Az.DataLakeAnalytics (wcześniej AzureRM.DataLakeAnalytics)
- Usunięto przestarzałe polecenia cmdlet: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` i `Set-AzDataLakeAnalyticsCatalogSecret`

### <a name="azdatalakestore-previously-azurermdatalakestore"></a>Az.DataLakeStore (wcześniej AzureRM.DataLakeStore)
- W następujących poleceniach cmdlet typ parametru `Encoding` został zmieniony z `FileSystemCmdletProviderEncoding` na `System.Text.Encoding`. W ramach tej zmiany usunięto wartości kodowania `String` i `Oem`. Nadal dostępne są wszystkie pozostałe wcześniejsze wartości kodowania.
  - New-AzureRmDataLakeStoreItem
  - Add-AzureRmDataLakeStoreItemContent
  - Get-AzureRmDataLakeStoreItemContent
- Usunięto przestarzały alias właściwości `Tags` z poleceń cmdlet `New-AzDataLakeStoreAccount` i `Set-AzDataLakeStoreAccount`

  Skrypty używające kodu
  ```powershell
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  Należy zmienić na
  ```powershell
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- Usunięto przestarzałe właściwości ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier``` i ```FirewallAllowAzureIps``` z obiektu ```PSDataLakeStoreAccountBasic```.  Żaden skrypt, który używa obiektu ```PSDatalakeStoreAccount``` zwróconego przez polecenie ```Get-AzDataLakeStoreAccount```, nie powinien odwoływać się do tych właściwości.

### <a name="azkeyvault-previously-azurermkeyvault"></a>Az.KeyVault (wcześniej AzureRM.KeyVault)
- Właściwość `PurgeDisabled` została usunięta z obiektów `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` i `PSKeyVaultSecretAttributes`. Skrypty nie powinny już odwoływać się do właściwości ```PurgeDisabled``` w celu podejmowania decyzji dotyczących przetwarzania.

### <a name="azmedia-previously-azurermmedia"></a>Az.Media (wcześniej AzureRM.Media)
- Usunięto przestarzały alias właściwości `Tags` z polecenia cmdlet `New-AzMediaService`. Skrypty używające kodu
  ```powershell
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  Należy zmienić na
  ```powershell
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```
### <a name="azmonitor-previously-azurerminsights"></a>Az.Monitor (wcześniej AzureRM.Insights)
- Z polecenia cmdlet `Set-AzDiagnosticSetting` usunięto parametry o nazwach w liczbie mnogiej `Categories` i `Timegrains`, aby zastąpić je nazwami parametrów w liczbie pojedynczej. Skrypty używające kodu
  ```powershell
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  Należy zmienić na
  ```powershell
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```
### <a name="aznetwork-previously-azurermnetwork"></a>Az.Network (wcześniej AzureRM.Network)
- Usunięto przestarzały parametr `ResourceId` z polecenia cmdlet `Get-AzServiceEndpointPolicyDefinition`
- Usunięto przestarzałą właściwość `EnableVmProtection` z obiektu `PSVirtualNetwork`
- Usunięto przestarzałe polecenie cmdlet `Set-AzVirtualNetworkGatewayVpnClientConfig`
  
Skrypty nie powinny już podejmować decyzji dotyczących przetwarzania na podstawie wartości tych pól.

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a>Az.OperationalInsights (wcześniej AzureRM.OperationalInsights)
- Usunięto domyślny zestaw parametrów dla polecenia `Get-AzOperationalInsightsDataSource`, a zestaw `ByWorkspaceNameByKind` stał się domyślnym zestawem parametrów

  Skrypty zwracające listę źródeł danych przy użyciu polecenia
  ```powershell
  Get-AzureRmOperationalInsightsDataSource
  ```

  Należy zmienić tak, aby określały rodzaj
  ```powershell
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a>Az.RecoveryServices (wcześniej AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup i AzureRM.RecoveryServices.SiteRecovery)
- Usunięto parametr `Encryption` z polecenia cmdlet `New/Set-AzRecoveryServicesAsrPolicy`
- Parametr `TargetStorageAccountName` jest teraz obowiązkowy na potrzeby przywracania dysku zarządzanego w poleceniu cmdlet `Restore-AzRecoveryServicesBackupItem`
- Usunięto parametry `StorageAccountName` i `StorageAccountResourceGroupName` w poleceniu cmdlet `Restore-AzRecoveryServicesBackupItem`
- Usunięto parametr `Name` w poleceniu cmdlet `Get-AzRecoveryServicesBackupContainer`

### <a name="azresources-previously-azurermresources"></a>Az.Resources (wcześniej AzureRM.Resources)
- Usunięto parametr `Sku` z polecenia cmdlet `New/Set-AzPolicyAssignment`
- Usunięto parametr `Password` z poleceń cmdlet `New-AzADServicePrincipal` i `New-AzADSpCredential`. Hasła są generowane automatycznie, a skrypty, które podawały hasło:
  ```powershell
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  Należy zmienić tak, aby uzyskiwały hasło z danych wyjściowych:
  ```powershell
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a>Az.ServiceFabric (wcześniej AzureRM.ServiceFabric)
- Zmieniono następujące zwracane typy poleceń cmdlet:
  - Właściwość `SerivceTypeHealthPolicies` typu `ApplicationHealthPolicy` została usunięta.
  - Właściwość `ApplicationHealthPolicies` typu `ClusterUpgradeDeltaHealthPolicy` została usunięta.
  - Właściwość `OverrideUserUpgradePolicy` typu `ClusterUpgradePolicy` została usunięta.
  - Te zmiany mają wpływ na następujące polecenia cmdlet:
    - Add-AzServiceFabricClientCertificate
    - Add-AzServiceFabricClusterCertificate
    - Add-AzServiceFabricNode
    - Add-AzServiceFabricNodeType
    - Get-AzServiceFabricCluster
    - Remove-AzServiceFabricClientCertificate
    - Remove-AzServiceFabricClusterCertificate
    - Remove-AzServiceFabricNode
    - Remove-AzServiceFabricNodeType
    - Remove-AzServiceFabricSetting
    - Set-AzServiceFabricSetting
    - Set-AzServiceFabricUpgradeType
    - Update-AzServiceFabricDurability
    - Update-AzServiceFabricReliability

### <a name="azsql-previously-azurermsql"></a>Az.Sql (wcześniej AzureRM.Sql)
- Usunięto parametry `State` i `ResourceId` z polecenia cmdlet `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`
- Usunięto przestarzałe polecenia cmdlet: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing` i `Remove-AzSqlServerAuditing`
- Usunięto przestarzały parametr `Current` z polecenia cmdlet `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`
- Usunięto przestarzały parametr `DatabaseName` z polecenia cmdlet `Get-AzSqlServerServiceObjective`
- Usunięto przestarzały parametr `PrivilegedLogin` z polecenia cmdlet `Set-AzSqlDatabaseDataMaskingPolicy`

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a>Az.Storage (wcześniej Azure.Storage i AzureRM.Storage)
- Aby obsługiwać tworzenie kontekstu magazynu OAuth za pomocą tylko nazwy konta magazynu, domyślny zestaw parametrów został zmieniony na `OAuthParameterSet`
  - Przykład: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`
- Parametr `Location` stał się obowiązkowy w poleceniu cmdlet `Get-AzStorageUsage`
- Metody interfejsu API magazynu używają teraz wzorca asynchronicznego opartego na zadaniach zamiast synchronicznych wywołań interfejsu API.
#### <a name="1-blob-snapshot"></a>1. Migawka obiektu blob
##### <a name="before"></a>Przed:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

##### <a name="after"></a>Po:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="2-share-snapshot"></a>2. Udostępnianie migawki
##### <a name="before"></a>Przed:
```powershell
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```
#####  <a name="after"></a>Po:
```powershell

$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="3-undelete-a-soft-delete-blob"></a>3. Cofanie usuwania nietrwale usuniętego obiektu blob
##### <a name="before"></a>Przed:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```
##### <a name="after"></a>Po:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="4-set-blob-tier"></a>4. Ustawianie warstwy obiektu blob
##### <a name="before"></a>Przed:
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

##### <a name="after"></a>Po:
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a>Az.Websites (wcześniej AzureRM.Websites)
- Usunięto przestarzałe właściwości z obiektów `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` i `PSSite`