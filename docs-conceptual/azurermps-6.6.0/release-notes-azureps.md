---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 3961f5c37869d0dc877b85bad535f399181040db
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/02/2018
ms.locfileid: "39368181"
---
# <a name="release-notes"></a>Informacje o wersji

To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.

---
## <a name="660---july-2018"></a>6.6.0 — lipiec 2018 r.
#### <a name="general"></a>Ogólne
* Zaktualizowano wszystkie pliki pomocy, aby uwzględniały pełne typy parametrów i poprawne typy wejściowe/wyjściowe.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Zaktualizowano bibliotekę Common.Strategy, aby mogła ona weryfikować, czy bieżąca konfiguracja zasobu jest zgodna z zasobem docelowym. Domyślnie wartość to zawsze true, a poszczególne zasoby mogą przesłaniać wartość domyślną.
* Dodano typy ps1xml do biblioteki Common.Storage

#### <a name="azurestorage"></a>Azure.Storage
* Obsługa uzyskiwania kontekstu magazynu z profilu DefaultProfile
* Dodanie atrybutu Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6370
    - Usunięto usterkę w maperze Automapper dotyczącą translacji obiektu PsApiManagementApi na obiekt ApiContract
* Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6515
    - Usunięto usterkę w elemencie File.Save dotyczącą przeciążania typem kodowania
* Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6560
    - Uaktualniono menedżer NuGet do wersji 4.0.3, co rozwiązuje problem z występowaniem wyjątku dotyczącego wzorca w parametrze apiId

#### <a name="azurermcompute"></a>AzureRM.Compute
* Rozwiązanie problemu powodującego zakończenie niepowodzeniem tworzenia maszyny wirtualnej przy użyciu zestawu DiskFileParameterSet w poleceniu New-AzureRmVm z powodu zmiany nazwy typu konta magazynu PremiumLRS.
* Poprawienie polecenia cmdlet Invoke-AzureRmVMRunCommand
* Zaktualizowanie polecenia Get-AzureRmAvailabilitySet, aby umożliwić zwrócenie listy wszystkich zestawów dostępności w subskrypcji.  (Parametr ResouceGroupName jest teraz opcjonalny).
* Zaktualizowanie zestawu SimpleParameterSet polecenia „New-AzureRmVm”, aby umożliwić korzystanie z przyspieszonej łączności sieciowej na kwalifikujących się maszynach wirtualnych.
* Zaktualizowanie prostego zestawu parametrów polecenia New-AzureRmVmss w taki sposób, aby tworzenie zestawu skalowania maszyn wirtualnych kończyło się niepowodzeniem, gdy moduł równoważenia obciążenia określony przez użytkownika już istnieje.
* Zaktualizowanie przykładu dla polecenia New-AzureRmDisk
* Dodanie przykładu dla polecenia „New-AzureRmVM”
* Zaktualizowanie opisu polecenia Set-AzureRmVMOSDisk
* Zaktualizowanie przykładu 1 dla polecenia Set-AzureRmVMBginfoExtension przez poprawienie pisowni i prefiksu. 

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Zaktualizowano zestaw ADF .Net SDK do wersji 1.1.0.
* Obsługa udostępniania własnego środowiska Integration Runtime dla wielu fabryk danych.
     - Dodanie nowego parametru -SharedIntegrationRuntimeResourceId do polecenia cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.
     - Dodanie nowego opcjonalnego parametru -LinkedDataFactoryName do polecenia cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Zaktualizowano zestaw SDK płaszczyzny danych (Microsoft.Azure.DataLake.Store) do wersji 1.1.9

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania

#### <a name="azurerminsights"></a>AzureRM.Insights
* Naprawiono formatowanie typu OutputType w plikach pomocy
* Użycie zestawu Microsoft.Azure.Management.Monitor SDK w wersji 0.19.1-preview

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Rozwiązanie problemu z potokowaniem w poleceniu Set-AzureRmKeyVaultAccessPolicy

#### <a name="azurermnetwork"></a>AzureRM.Network
* Dodano przykłady dla poleceń cmdlet LoadBalancerInboundNatPoolConfig.

#### <a name="azurermresources"></a>AzureRM.Resources
* Rozwiązanie problemu w przypadku podawania zarówno wartości, jak i nazwy tagu w poleceniu „Get-AzureRmResource”
    - https://github.com/Azure/azure-powershell/issues/6765
* Naprawienie scenariusza potokowania w poleceniu „Set-AzureRmResource”

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania
* Rozwiązano kilka problemów
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a>AzureRM.Sql
* Dodanie obsługi zaawansowanej ochrony serwera przed zagrożeniami przy użyciu następujących poleceń cmdlet:
    - Enable-AzureRmSqlServerAdvancedThreatProtection, Disable-AzureRmSqlServerAdvancedThreatProtection, Get-AzureRmSqlServerAdvancedThreatProtectionPolicy
* Dodanie obsługi oceny luk w zabezpieczeniach przy użyciu następujących poleceń cmdlet:
    - Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings
    - Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline
    - Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan, Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord, Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan
* Poprawiono przykład w poleceniu Remove-AzureRmSqlServerFirewallRule
* Naprawienie niepoprawnej obsługi daty/godziny w przypadku podstawowej kultury innej niż Stany Zjednoczone w poleceniu Get-AzureSqlSyncGroupLog

#### <a name="azurermstorage"></a>AzureRM.Storage
* Dodanie atrybutu Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet
* Pokazywanie danych wyjściowych polecenia cmdlet StorageAccount w widoku tabeli
    - Get-AzureRmStorageAccount
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermtags"></a>AzureRM.Tags
* Usunięcie niepoprawnej informacji z pomocy polecenia cmdlet Tag
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a>6.5.0 — lipiec 2018 r.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Zaktualizowano pomoc dotyczącą polecenia „Get-AzureRmContextAutosaveSetting”

#### <a name="azurestorage"></a>Azure.Storage
* Dodano obsługę przekazywania obiektu blob lub pliku z tokenem sygnatury dostępu współdzielonego tylko do odczytu
- Set-AzureStorageBlobContent
- Set-AzureStorageFileContent

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Dodano wymaganą właściwość ResourceGroupName do usługi AS.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Zaktualizowano pomoc i dodano przykład polecenia „New-AzureRMAutomationSchedule”

#### <a name="azurermcompute"></a>AzureRM.Compute
* Dodano parametr -Tag do polecenia Update/New-AzureRmAvailabilitySet
* Dodano przykład polecenia „Add-AzureRmVmssExtension”
* Dodano przykłady polecenia „Remove-AzureRmVmssExtension”
* Zaktualizowano pomoc dotyczącą polecenia „Set-AzureRmVMAccessExtension”
* Zaktualizowano atrybut SimpleParameterSet dla polecenia New-AzureRmVmss, aby domyślnie ustawiał parametr SinglePlacementGroup na wartość false oraz dodano parametr przełącznika „SinglePlacementGroup” umożliwiający użytkownikowi tworzenie zestawów VMSS w pojedynczej grupie umieszczania.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSEventHubDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Zaktualizowano komunikat o błędzie dla polecenia Set-AzureRmKeyVaultAccessPolicy

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Naprawiono błąd „nie można rozpoznać zestawu parametrów” w poleceniu New-AzureRmLogicApp

#### <a name="azurermnetwork"></a>AzureRM.Network
* Włączono komunikację równorzędną między sieciami wirtualnymi w wielu dzierżawach dla polecenia Set/Add-AzureRmVirtualNetworkPeering
* Zaktualizowano poniższe polecenia cmdlet usługi Application Gateway
    - New-AzureRmApplicationGateway: dodano obsługę flagi EnableFIPS i stref
    - New-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2
    - Set-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2
* Ponownie wygenerowano polecenia cmdlet RouteTable z użyciem najnowszej wersji generatora

#### <a name="azurermrelay"></a>AzureRM.Relay
* Zaktualizowano pliki markdown, naprawiono problem z nazwą parametru w przykładzie

#### <a name="azurermresources"></a>AzureRM.Resources
* Zaktualizowano polecenia cmdlet Roleassignment i roledefinition:
    - Usunięto dodatkowe wywołania polecenia roledefinition wykonywane w ramach stronicowania.
* Naprawiono polecenie cmdlet Get-AzureRmRoleAssignment
    - Naprawiono funkcjonalność parametru polecenia -ExpandPrincipalGroups
* Rozwiązano problem z poleceniem „Get-AzureRmResource”, który polegał na tym, że w parametrze „-ResourceType” była uwzględniana wielkość liter

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Dodano parametry top i skip do poleceń cmdlet „list”
* Dodano polecenia cmdlet migracji przestrzeni nazw z warstwy Standardowa do warstwy Premium:
    - Start-AzureRmServiceBusMigration
    - Get-AzureRmServiceBusMigration
    - Complete-AzureRmServiceBusMigration
    - Stop-AzureRmServiceBusMigration
    - Remove-AzureRmServiceBusMigration
* Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSServiceBusDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Zaktualizowano przykład dotyczący polecenia „New-AzureRmServiceFabricCluster”

#### <a name="azurermsql"></a>AzureRM.Sql
* Dodano nowe polecenia cmdlet dla przestrzeni nazw Management.Sql, aby umożliwić klientom dodawanie certyfikatu TDE do wystąpienia programu SQL Server lub wystąpienia zarządzanego
    - Add-AzureRmSqlServerTransparentDataEncryptionCertificate
    - Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Polecenia `Set-AzureRmWebApp -AssignIdentity` i `Set-AzureRmWebAppSlot -AssignIdentity` po ustawieniu na wartość false spowodują teraz usunięcie właściwości Identity z obiektu lokacji. Usuwany jest także tag podglądu.
* Zaktualizowano przykład dotyczący poleceń `Get-AzureRmWebAppMetrics` i `Get-AzureRmAppServicePlanMetrics`
* Polecenie `Set-AzureRmWebApp -PhpVersion` obsługuje wartość off jako prawidłową wersję języka PHP

## <a name="640---july-2018"></a>6.4.0 — lipiec 2018 r.
#### <a name="general"></a>Ogólne
* Naprawiono formatowanie typu OutputType w plikach pomocy dotyczących większości modułów

#### <a name="azurermprofile"></a>AzureRM.Profile
* Dodano atrybut Ps1Xml do podstawowych typów danych wyjściowych

#### <a name="azurermcompute"></a>AzureRM.Compute
* Funkcja tagów adresów IP dla zestawu skalowania maszyn wirtualnych
    - Dodano polecenie cmdlet „New-AzureRmVmssIpTagConfig”
    - Dodano parametr IpTag do polecenia New-AzureRmVmssIpConfig
* Funkcja automatycznego wycofywania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych
    - Dodano parametry DisableAutoRollback do poleceń New-AzureRmVmssConfig i Update-AzureRmVmss
* Funkcja historii uaktualniania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych
    - Dodano parametr przełącznika OSUpgradeHistory do polecenia Get-AzureRmVmss

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Dodano obsługę list ACL wykazu przy użyciu następujących poleceń:
    - Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Dodano obsługę anulowania i śledzenia postępu dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl
* Dodano obsługę anulowania dla polecenia Export-AzureRmDataLakeStoreChildItemProperties
* Naprawiono opróżnianie komunikatów debugowania dla poleceń cmdlet wykonujących operacje cykliczne
* Naprawiono lokalizację testu poleceń cmdlet DataLake

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Dodano opcjonalny parametr MaxCount do poleceń cmdlet tworzących listę operacji: Get-AzureRmEventHub i Get-AzureRmEventHubConsumerGroup
* Rozwiązano problem z poleceniem cmdlet New-AzureRmEventHub polegający na tym, że podczas tworzenia nowego centrum EventHub był wymagany co najmniej jeden parametr. Udostępniono zestaw parametrów domyślnych.
* Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmEventHubKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Rozwiązano problem polegający na tym, że wszystkie zasoby były zwracane przez polecenie Get-AzureRmKeyVault -Tag

#### <a name="azurermnetwork"></a>AzureRM.Network
* Uwidoczniono nowe jednostki SKU dla strefowo nadmiarowych bram VirtualNetworkGateways
* Dodano nowe polecenia dla funkcji interfejsów API partnerów usługi ExpressRoute za pośrednictwem usługi ARM
    - Dodano polecenie Get-AzureRmExpressRouteCrossConnection
    - Dodano polecenie Set-AzureRmExpressRouteCrossConnection
    - Dodano polecenie Add-AzureRmExpressRouteCrossConnectionPeering
    - Dodano polecenie Get-AzureRmExpressRouteCrossConnectionPeering
    - Dodano polecenie Remove-AzureRmExpressRouteCrossConnectionPeering
    - Dodano polecenie Get-AzureRMExpressRouteCrossConnectionArpTable
    - Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTable
    - Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTableSummary

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Dodano polecenie cmdlet Get-AzureRmRecoveryServicesBackupStatus. To polecenie cmdlet pobiera identyfikator maszyny wirtualnej i sprawdza, czy maszyna wirtualna jest chroniona przez magazyn w ramach subskrypcji. Jeśli taki magazyn istnieje, polecenie cmdlet wyświetla jego szczegóły.

#### <a name="azurermresources"></a>AzureRM.Resources
* Zaktualizowano polecenia cmdlet Get-AzureRmPolicyAssignment:
    - Dodano obsługę wyświetlania listy wartości -Scope na poziomie grupy zarządzania
    - Dodano obsługę pobierania poszczególnych przydziałów za pomocą wartości -Scope na poziomie grupy zarządzania
    - Dodano przełączniki -Effective i -All do parametru kontroli
* Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition
    - Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania
    - Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji
* Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition
    - Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania
    - Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji
* Dodano obsługę odwołania do wpisu tajnego KeyVault w parametrach w przypadku używania elementu „TemplateParameterObject” w poleceniu „New-AzureRmResourceGroupDeployment”
* Rozwiązano problem polegający na tym, że parametr „-EndDate” był ignorowany w poleceniu „New-AzureRmADAppCredential”
    - https://github.com/Azure/azure-powershell/issues/6505
* Rozwiązano problem polegający na tym, że w poleceniu „Add-AzureRmADGroupMember” używano nieprawidłowego adres URL podczas zgłaszania żądania
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmServiceBusKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.

#### <a name="azurermsql"></a>AzureRM.Sql
* Objaśniono punkty przywracania zdefiniowane przez użytkownika dla usługi SQLDW w pomocy polecenia New-AzureRmSqlDatabaseRestorePoint
* Zaktualizowano dokumentację parametru -ComputeGeneration w kilku poleceniach cmdlet

## <a name="630---june-2018"></a>6.3.0 — czerwiec 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Zaktualizowano komunikaty o błędach dotyczące polecenia Enable-AzureRmContextAutoSave
* Tworzenie kontekstu dla każdej subskrypcji w przypadku uruchomienia polecenia „Connect-AzureRmAccount” bez wcześniejszego kontekstu

#### <a name="azurestorage"></a>Azure.Storage
* Dodano informacje dotyczące parametru -Permissions w plikach pomocy.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Polecenie „Get-AzureRmVmDiskEncryptionStatus” — rozwiązano problem zaobserwowany w przypadku maszyn wirtualnych bez dysków z danymi 
* Aktualizacja wersji biblioteki klienckiej obliczeń w celu naprawy następujących poleceń cmdlet:
    - Grant-AzureRmDiskAccess
    - Grant-AzureRmSnapshotAccess
    - Save-AzureRmVMImage
* Naprawiono następujące polecenia cmdlet w celu poprawnego wyświetlania identyfikatora operacji i stanu operacji:
    - Start-AzureRmVM
    - Stop-AzureRmVM
    - Restart-AzureRmVM
    - Set-AzureRmVM
    - Remove-AzuerRmVM
    - Set-AzureRmVmss
    - Start-AzureRmVmssRollingOSUpgrade
    - Stop-AzureRmVmssRollingUpgrade
    - Start-AzureRmVmss
    - Restart-AzureRmVmss
    - Stop-AzureRmVmss
    - Remove-AzureRmVmss
    - ConvertTo-AzureRmVMManagedDisk
    - Revoke-AzureRmSnapshotAccess
    - Remove-AzureRmSnapshot
    - Revoke-AzureRmDiskAccess
    - Remove-AzureRmDisk
    - Remove-AzureRmContainerService
    - Remove-AzureRmAvailabilitySet

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Usunięto warunki weryfikacji ValidateNotNullOrEmpty dla elementów SubjectBeginsWith/SubjectEndsWith w poleceniu cmdlet Update-AzureRmEventGridSubscription w celu umożliwienia zmiany tych parametrów na pusty ciąg w razie potrzeby.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Rozwiązano problem polegający na tym, że nie były zwracane tagi w przypadku uruchomienia polecenia Get-AzureRmKeyVault -Tag

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Publiczne udostępnienie poleceń cmdlet usługi Policy Insights
    - Użycie interfejsu API w wersji z 4.04.2018
    - Dodano element PolicyDefinitionReferenceId do wyników polecenia Get-AzureRmPolicyStateSummary

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Dodano parametr -Vault do poleceń cmdlet RecoveryServices.Backup. W przypadku przekazania to polecenie przesłania polecenie cmdlet Set-AzureRmRecoveryServicesContext.

#### <a name="azurermsql"></a>AzureRM.Sql
* Zaktualizowano przykład w pliku pomocy polecenia Get-AzureRmSqlDatabaseExpanded

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Zaktualizowano plik pomocy polecenia Add-AzureRmTrafficManagerEndpointConfig

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Zaktualizowano polecenie „Set-AzureRmWebApp”, aby nie zastępowało elementu AppSettings w przypadku użycia parametru -AssignIdentity
* Zaktualizowano polecenie „New-AzureRmWebAppSlot” w celu umożliwienia obsługi parametru AppServicePlan jako parametru opcjonalnego

## <a name="621---june-2018"></a>6.2.1 — czerwiec 2018
### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Zaktualizowano model PSWorkspace w celu umożliwienia użycia typu jako parametru w sieci

## <a name="620---june-2018"></a>6.2.0 — czerwiec 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Naprawiono problem, który polegał na tym, że wersja 10.0.3 pliku Newtonsoft.Json nie była ładowana podczas importowania modułu

#### <a name="azurermcompute"></a>AzureRM.Compute
* Funkcja aktualizacji maszyny wirtualnej usługi VMSS
    - Dodano polecenia cmdlet „Update-AzureRmVmssVM” i „New-AzureRmVMDataDisk”
    - Dodano parametr VirtualMachineScaleSetVM do polecenia cmdlet „Add-AzureRmVMDataDisk” w celu obsługi dodawania dysku danych do maszyny wirtualnej usługi VMSS.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Zaktualizowano zestaw ADF .Net SDK do wersji 0.8.0-preview zawierającej następujące zmiany:
    - Dodano operację repozytorium do konfigurowania fabryki
    - Zaktualizowano usługę QuickBooks LinkedService w celu ujawnienia właściwości consumerKey i consumerSecret
    - Zaktualizowano wiele typów modeli, od SecretBase do Object
    - Dodano wyzwalacz zdarzeń obiektów blob

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Zaktualizowano dokumentację o przykładowe dane wyjściowe

### <a name="azurermnetwork"></a>AzureRM.Network
* Parametry włączania analizy ruchu w poleceniach cmdlet narzędzia Network Watcher

#### <a name="azurermresources"></a>AzureRM.Resources
* Rozwiązano problem z właściwością „Properties” obiektu „PSResource” zwracanego z polecenia „Get-AzureRmResource”

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Rozwiązano problem z aktualizacją ServiceBusQueueJob, która nie ustawiała nowych wartości uwierzytelniania

### <a name="azurermsql"></a>AzureRM.Sql
* Zaktualizowano następujące polecenia cmdlet o opcjonalny parametr LicenseType
    - New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Polecenie „New-AzureRMWebApp” zostało zaktualizowane w celu używania typowych algorytmów z biblioteki strategii.

## <a name="610---may-2018"></a>6.1.0 — maj 2018 r.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Rozwiązano problem polegający na tym, że po uruchomieniu polecenia „Clear-AzureRmContext” pozostawał pusty kontekst o nazwie takiej jak poprzedni kontekst domyślny, co uniemożliwiało użytkownikowi utworzenie nowego kontekstu ze starą nazwą

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Włączono operacje kojarzenia/usuwania skojarzenia bramy w usłudze AS.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Dodano obsługę elementów ApiVersion, ApiRelease oraz ApiRevision
* Dodano obsługę zaplecza ServiceFabric
* Dodano obsługę rejestratora usługi Application Insights
* Dodano obsługę rozpoznawania jednostki SKU „Podstawowa” jako prawidłowej jednostki SKU usługi API Management
* Dodano obsługę instalowania certyfikatów wystawionych przez prywatny urząd certyfikacji jako certyfikatów głównych lub certyfikatów urzędu certyfikacji
* Dodano obsługę akceptowania niestandardowych certyfikatów SSL za pomocą magazynu kluczy i wielu nazw hostów serwera proxy
* Dodano obsługę tożsamości MSI
* Dodano obsługę akceptowania zasad za pomocą adresu URL. UWAGA: następujące polecenia cmdlet staną się przestarzałe w przyszłym wydaniu
   - Import-AzureRmApiManagementHostnameCertificate
   - New-AzureRmApiManagementHostnameConfiguration
   - Set-AzureRmApiManagementHostnames
   - Update-AzureRmApiManagementDeployment

#### <a name="azurermbatch"></a>AzureRM.Batch
* Wydano nowe polecenie cmdlet Get-AzureBatchPoolNodeCounts
* Wydano nowe polecenie cmdlet Start-AzureBatchComputeNodeServiceLogUpload

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* Dodano nowe parametry polecenia cmdlet Get-AzureRmConsumptionUsageDetail: Expand, ResourceGroup, InstanceName, InstanceId, Tags oraz Top

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Poprawiono przykład dla polecenia Export-AzureRmDataLakeStoreChildItemProperties
* Rozwiązano problem powodujący wyjątek parametru o wartości null dla przypadku Recurse w poleceniu Set-AzureRmDataLakeStoreItemAclEntry 
* Poprawiono pliki pomocy dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl oraz Remove-AzureRmDataLakeStoreItemAclEntry 

#### <a name="azurermnetwork"></a>AzureRM.Network
* Podniesiono wersję zestawu SDK sieci z 18.0.0-preview do 19.0.0-preview
* Dodano polecenie cmdlet służące do tworzenia konfiguracji protokołu
    - New-AzureRmNetworkWatcherProtocolConfiguration
* Dodano polecenie cmdlet służące do dodawania nowego połączenia obwodu do istniejącego obwodu usługi ExpressRoute
    - Add-AzureRmExpressRouteCircuitConnectionConfig
* Dodano polecenie cmdlet służące do usuwania połączenia obwodu z istniejącego obwodu usługi ExpressRoute
    - Remove-AzureRmExpressRouteCircuitConnectionConfig
* Dodano polecenie cmdlet służące do pobierania połączenia obwodu
    - Get-AzureRmExpressRouteCircuitConnectionConfig

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Naprawiono użycie uwierzytelniania serwera za pomocą wygenerowanych certyfikatów (problem nr 5998)

#### <a name="azurermsql"></a>AzureRM.Sql
* Zaktualizowano polecenia cmdlet inspekcji w celu umożliwienia usuwania elementów AuditAction lub AuditActionGroup
* Rozwiązano problem z poleceniem Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, który powodował zakończenie polecenia niepowodzeniem podczas ustawiania nowych, elastycznych zasad przechowywania oraz zwrócenie komunikatu „Konfigurowanie zasad przechowywania długoterminowego za pomocą magazynu usługi Azure Recovery Service i zasad nie jest już obsługiwane. Prześlij żądanie z nowymi, elastycznymi zasadami przechowywania”.
* Zaktualizowano wszystkie polecenia cmdlet służące do tworzenia/aktualizowania elastycznej puli/bazy danych usługi Azure SQL Database w taki sposób, aby korzystały z nowego interfejsu API bazy danych, który obsługuje właściwość SKU na potrzeby właściwości powiązanych ze skalowaniem i warstwą.
* Zaktualizowane polecenia cmdlet to: 
    - New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Zaktualizowano parametry polecenia „Get-AzureRmTrafficManagerProfile”, aby parametr -ResourceGroupName był wymagany, gdy został podany parametr -Name.