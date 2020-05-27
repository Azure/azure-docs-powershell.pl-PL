---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 2/20/2018
ms.openlocfilehash: 795aa938ec179bb6d845774cf25778bd2b7c1442
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387760"
---
# <a name="release-notes"></a>Informacje o wersji

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.

---

# <a name="azure-powershell-570"></a>Azure PowerShell 5.7.0

Instalator programu Azure PowerShell 5.7.0: [link](https://github.com/Azure/azure-powershell/releases/download/v5.7.0-April2018/azure-powershell.5.7.0.msi)

Moduł galerii dla poleceń cmdlet ARM: [link](https://www.powershellgallery.com/packages/AzureRM/5.7.0)

Aby zainstalować program `AzureRM` z galerii programu PowerShell, uruchom następujące polecenie:

```powershell-interactive
Install-Module -Name AzureRM -Repository PSGallery -Force
```

Aby zaktualizować starszą wersję programu `AzureRM`, uruchom następujące polecenie:

```powershell-interactive
Update-Module -Name AzureRM
```

## <a name="changes-since-last-release"></a>Zmiany od ostatniego wydania

#### <a name="general"></a>Ogólne
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime

#### <a name="azurestorage"></a>Azure.Storage
* Rozwiązanie problemu polegającego na tym, że polecenia cmdlet do przekazywania obiektów blob i plików kończą się niepowodzeniem na maszynach obsługujących zasady FIPS
    - Set-AzureStorageBlobContent
    - Set-AzureStorageFileContent

#### <a name="azurermbilling"></a>AzureRM.Billing
* Nowe polecenie cmdlet Get-AzureRmEnrollmentAccount
  - do pobierania kont rejestracji

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Integracja z zestawem Cognitive Services Management SDK w wersji 4.0.0.
* Dodanie operacji Get-AzureRmCognitiveServicesAccountUsage.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Operacja `Get-AzureRmVmssDiskEncryptionStatus` obsługuje stan szyfrowania na poziomie dysku danych
* Operacja `Get-AzureRmVmssVmDiskEncryptionStatus` obsługuje stan szyfrowania na poziomie dysku danych
* Aktualizacja pod kątem odporności strefowej
* Operacje „New-AzureRmVm” i „New-AzureRmVmss” (prosty zestaw parametrów) obsługują strefy dostępności.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Oddzielenie oparcia na elemencie Commands.Resources.Rest i zestawach SDK ARM/Storage.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Dodanie funkcji debugowania
* Aktualizacja wersji zestawu SDK płaszczyzny danych usługi ADLS do 1.1.2
* Polecenie Export-AzureRmDataLakeStoreItem — uznanie za przestarzałe parametrów PerFileThreadCount i ConcurrentFileCount oraz wprowadzenie parametru Concurrency
* Polecenie Import-AzureRMDataLakeStoreItem — uznanie za przestarzałe parametrów PerFileThreadCount i ConcurrentFileCount oraz wprowadzenie parametru Concurrency
* Polecenie Get-AzureRMDataLakeStoreItemContent — naprawiono działanie parametru tail dla zawartości większej od 4 MB
* Polecenie Set-AzureRMDataLakeStoreItemExpiry — wprowadzono nowy zestaw parametrów SetRelativeExpiry do ustawiania względnego czasu wygaśnięcia
* Polecenie Remove-AzureRmDataLakeStoreItem — parametr Clean został uznany za przestarzały.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Naprawiono parametr AlternameName polecenia New-AzureRmEventHubGeoDRConfiguration

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Zaktualizowano polecenia cmdlet w celu uwzględniania scenariuszy z potokami
* Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącą zmianą powodującą niezgodność

#### <a name="azurermnetwork"></a>AzureRM.Network
* Naprawa komunikatu o błędzie dotyczącego poleceń cmdlet dla sieci

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Dodano element „properties” w elemencie CorrelationFilter polecenia Rules w celu obsługi właściwości niestandardowych
* Zaktualizowano pomoc dla polecenia New-AzureRmServiceBusGeoDRConfiguration i naprawiono dane wyjściowe polecenia cmdlet Rules
* Naprawiono właściwości automatycznego przekazywania dalej w poleceniach cmdlet New-AzureRmServiceBusQueue i New-AzureRmServiceBusSubscription

#### <a name="azurermsql"></a>AzureRM.Sql
* Dodanie nowego polecenia cmdlet „Stop-AzureRmSqlElasticPoolActivity” w celu obsługi anulowania operacji asynchronicznych na elastycznych pulach
* Zaktualizowanie odpowiedzi dla poleceń cmdlet Get-AzureRmSqlDatabaseActivity i Get-AzureRmSqlElasticPoolActivity w celu uwzględniania w nich większej ilości informacji

Zmiany od ostatniego wydania: https://github.com/Azure/azure-powershell/compare/v5.6.0-March2018...v5.7.0-April2018

## <a name="560---march-2018"></a>5.6.0 — marzec 2018

#### <a name="general"></a>Ogólne
* Rozwiązanie problemu z domyślną grupą zasobów w usłudze CloudShell
* Rozwiązanie problemu z wykonywaniem niepoprawnych skryptów uruchamiania podczas importowania modułu

#### <a name="azurermprofile"></a>AzureRM.Profile
* Włączenie uwierzytelniania tożsamości usługi zarządzanej w nieobsługiwanych scenariuszach
* Dodawanie obsługi zdefiniowanej przez użytkownika tożsamości usługi zarządzanej

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Rozwiązano problem z czyszczeniem skryptów w kompilacji

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Rozwiązano problem z czyszczeniem skryptów w kompilacji

#### <a name="azurermcompute"></a>AzureRM.Compute
* Polecenia „New-AzureRmVM” i „New-AzureRmVMSS” obsługują dyski danych.
* Polecenia „New-AzureRmVM” i „New-AzureRmVMSS” obsługują obraz niestandardowy według nazwy lub identyfikatora.
* Funkcja analityczna dziennika
    - Dodano polecenie cmdlet „Export-AzureRmLogAnalyticRequestRateByInterval”
    - Dodano polecenie cmdlet „Export-AzureRmLogAnalyticThrottledRequests”

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Rozwiązanie problemu z zestawami parametrów dla rejestru kontenerów i instalacji woluminu plików platformy Azure

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Zaktualizowano zestaw ADF .Net SDK do wersji 0.6.0-preview zawierającej następujące zmiany:
    - Dodano nowy element AzureDatabricks LinkedService i działanie DatabricksNotebook
    - Dodano właściwości headNodeSize i dataNodeSize w elemencie HDInsightOnDemand LinkedService
    - Dodano elementy LinkedService, Dataset i CopySource dla elementu SalesforceMarketingCloud
    - Dodano obsługę elementu SecureOutput dla wszystkich działań
    - Dodano nową właściwość BatchCount działania ForEach, która steruje liczbą równocześnie uruchamianych działań
    - Dodano nowe działanie filtrowania
    - Dodano obsługę parametrów połączonej usługi

#### <a name="azurermdns"></a>AzureRM.Dns
* Obsługa prywatnych stref DNS (publiczna wersja zapoznawcza)
    - Dodaje możliwość tworzenia stref DNS, które są widoczne tylko dla skojarzonych sieci wirtualnych

#### <a name="azurermnetwork"></a>AzureRM.Network
* Aktualizowanie typów modeli na potrzeby zgodności z poleceniami cmdlet usługi DNS.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Zmiany dotyczące odzyskiwania witryn Azure–Azure w usłudze ASR (polecenia cmdlet obecnie obsługują operacje przedsiębiorstwo–przedsiębiorstwo, przedsiębiorstwo–Azure, HyperV–Azure, VMware–Azure)
    - New-AzureRmRecoveryServicesAsrProtectionContainer
    - New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig
    - Remove-AzureRmRecoveryServicesAsrProtectionContainer
    - Update-AzureRmRecoveryServicesAsrProtectionDirection

#### <a name="azurermstorage"></a>AzureRM.Storage
* Następujące parametry w poleceniach cmdlet do tworzenia i ustawiania dla konta usługi Storage zostały oznaczone jak przestarzałe: EnableEncryptionService i DisableEncryptionService, ponieważ szyfrowanie przechowywanych danych jest włączone domyślnie i nie można go wyłączyć.
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Naprawiono pomoc dla polecenia Remove-AzureRmWebAppSlot

## <a name="550---march-2018"></a>5.5.0 — marzec 2018 r.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Rozwiązano problem z importowaniem aliasów
* Wersja 10.0.3 pakietu Newtonsoft.Json jest ładowana obok wersji 6.0.8

#### <a name="azurestorage"></a>Azure.Storage
* Obsługa funkcji usuwania nietrwałego
    - Enable-AzureStorageDeleteRetentionPolicy
    - Disable-AzureStorageDeleteRetentionPolicy
    - Get-AzureStorageBlob

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Rozwiązano problem z importowaniem aliasów
* Dodano obsługę zapory i funkcji skalowania zapytań w poziomie, a także obsługę wersji 2017-08-01 interfejsu API.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Rozwiązano problem z importowaniem aliasów

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Rozwiązano problem z importowaniem aliasów

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Zaktualizowano plik notice.txt i komunikat powiadomienia.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Polecenie „New-AzureRmVMSS” wyświetla parametry połączenia w trybie informacji pełnej.
* Polecenie „New-AzureRmVmss” obsługuje publiczny adres IP, reguły równoważenia obciążenia i reguły NAT dla ruchu przychodzącego.
* Funkcja WriteAccelerator
    - Dodano parametr przełącznika WriteAccelerator do następujących poleceń cmdlet: Set-AzureRmVMOSDisk, Set-AzureRmVMDataDisk, Add-AzureRmVMDataDisk i Add-AzureRmVmssDataDisk
    - Dodano parametr przełącznika OsDiskWriteAccelerator do następujących poleceń cmdlet:     Set-AzureRmVmssStorageProfile.
    - Dodano parametr logiczny OsDiskWriteAccelerator do następujących poleceń cmdlet:     Update-AzureRmVM i Update-AzureRmVmss

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Rozwiązano problem z szyfrowaniem poświadczeń, który powodował brak zrozumiałego błędu w przypadku niektórych operacji szyfrowania
* Umożliwiono współdzielenie środowiska Integration Runtime w całej fabryce danych

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Dodano parametr „SetupScriptContainerSasUri” i „Edition” dla polecenia „Set-AzureRmDataFactoryV2IntegrationRuntime”, aby włączyć funkcję niestandardowej konfiguracji i wyboru wersji
* Rozwiązano problem z szyfrowaniem poświadczeń, który powodował brak zrozumiałego błędu w przypadku niektórych operacji szyfrowania.
* Umożliwiono współdzielenie środowiska Integration Runtime w całej fabryce danych

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Rozwiązano problem z importowaniem aliasów

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Poprawiono przykład polecenia Set-AzureRmKeyVaultAccessPolicy

#### <a name="azurermnetwork"></a>AzureRM.Network
* Rozwiązano problem z importowaniem aliasów

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Rozwiązano problem z importowaniem aliasów

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Rozwiązano problem z importowaniem aliasów

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Rozwiązano problem z importowaniem aliasów

#### <a name="azurermresources"></a>AzureRM.Resources
* Rozwiązano problem z importowaniem aliasów

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Dodano właściwość EnableBatchedOperations do elementu Queue
* Dodano właściwość DeadLetteringOnFilterEvaluationExceptions do elementu Subscriptions

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Odświeżenie poleceń cmdlet usługi Service Fabric
  - Zaktualizowano szablony usługi ARM
  - Operacje zakończone niepowodzeniem nie są już wycofywane
  - Add-AzureRmServiceFabricNodeType
    - Maszyny wirtualne domyślnie korzystają z dysków zarządzanych
    - Używana jest istniejąca podsieć zestawu skalowania maszyn wirtualnych
    - Wszystkie operacje są idempotentne
  - Polecenie Remove-AzureRmServiceFabricNodeType czyści częściowo utworzone zestawy skalowania maszyn wirtualnych i/lub typy węzłów klastra
  - Poprawiono dane wyjściowe obiektu PSCluster dla złożonych typów właściwości

#### <a name="azurermsql"></a>AzureRM.Sql
* Rozwiązano problem z importowaniem aliasów
* Odpowiedzi poleceń Get-AzureRmSqlServer, New-AzureRmSqlServer i Remove-AzureRmSqlServer obejmują teraz właściwość FullyQualifiedDomainName.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Rozwiązano problem z importowaniem aliasów
* New-AzureRMWebApp — dodano zestaw parametrów na potrzeby uproszczonego tworzenia aplikacji internetowych z obsługą lokalnego repozytorium Git.

## <a name="540---february-2018"></a>5.4.0 — luty 2018
#### <a name="azurermautomation"></a>AzureRM.Automation
* Dodano alias z elementu New-AzureRmAutomationModule do elementu Import-AzureRmAutomationModule

#### <a name="azurermcompute"></a>AzureRM.Compute
* Naprawiono problem ErrorAction dla niektórych poleceń cmdlet Get.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Zastosowano zestaw SDK wystąpienia kontenera platformy Azure (2018-02-01)
    - Obsługa etykiety nazwy usługi DNS

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Naprawiono wszystkie polecenia cmdlet GET, które wcześniej nie działały.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Naprawiano błąd w pomocy do elementu Get AzureRmEventHubGeoDRConfiguration

#### <a name="azurermnetwork"></a>AzureRM.Network
* Dodano polecenie cmdlet do tworzenia nowego monitora połączeń
    - New-AzureRmNetworkWatcherConnectionMonitor
* Dodano polecenie cmdlet do aktualizacji monitora połączeń
    - Set-AzureRmNetworkWatcherConnectionMonitor
* Dodano polecenie cmdlet do uzyskiwania monitora połączeń lub listy monitorów połączeń
    - Get-AzureRmNetworkWatcherConnectionMonitor
* Dodano polecenie cmdlet do wykonywania zapytań o monitor połączeń
    - Get-AzureRmNetworkWatcherConnectionMonitorReport
* Dodano polecenie cmdlet do uruchamiania monitora połączeń
    - Start-AzureRmNetworkWatcherConnectionMonitor
* Dodano polecenie cmdlet do zatrzymywania monitora połączeń
    - Stop-AzureRmNetworkWatcherConnectionMonitor
* Dodano polecenie cmdlet do usuwania monitora połączeń
    - Remove-AzureRmNetworkWatcherConnectionMonitor
* Zaktualizowano dokumentację elementu AzureRmApplicationGatewayBackendAddressPool, usuwając przestarzały przykład
* Dodano flagę EnableHttp2 do usługi Application Gateway
    - Zaktualizowano polecenie New-AzureRmApplicationGateway: Dodano opcjonalny parametr -EnableHttp2
* Dodano elementy IpTag do elementu PublicIpAddress
    - Zaktualizowano polecenie New-AzureRmPublicIpAddress: Dodano elementy Iptag
    - Element New-AzureRmPublicIpTag do dodawania elementu Iptag
* Dodano właściwość DisableBgpRoutePropagation do elementów RouteTable i effectiveRoute.

#### <a name="azurermresources"></a>AzureRM.Resources
* Register-AzureRmProviderFeature: Dodano brakujący przykład w dokumentacji
* Register-AzureRmResourceProvider: Dodano brakujący przykład w dokumentacji

#### <a name="azurermstorage"></a>AzureRM.Storage
* Następujące parametry w poleceniach cmdlet do tworzenia i ustawiania dla konta usługi Storage zostały oznaczone jak przestarzałe: EnableEncryptionService i DisableEncryptionService, ponieważ szyfrowanie przechowywanych danych jest włączone domyślnie i nie można go wyłączyć.
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount


## <a name="530---february-2018"></a>5.3.0 — luty 2018 r.
### <a name="azurermprofile"></a>AzureRM.Profile
* Dodano ostrzeżenie o zakończeniu obsługi programu PowerShell 3 i 4
* Zmieniono nazwę elementu `Add-AzureRmAccount` na `Connect-AzureRmAccount`. Dodano alias dla starej nazwy polecenia cmdlet, a inne aliasy (`Login-AzAccount` i `Login-AzureRmAccount`) przekierowano na nową nazwę polecenia cmdlet.
* Zmieniono nazwę elementu `Remove-AzureRmAccount` na `Disconnect-AzureRmAccount`. Dodano alias dla starej nazwy polecenia cmdlet, a inne aliasy (`Logout-AzAccount` i `Logout-AzureRmAccount`) przekierowano na nową nazwę polecenia cmdlet.
* Skorygowano ciągi zasobów, aby korzystały z elementu `Connect-AzureRmAccount` zamiast `Login-AzureRmAccount`
* `Add-AzureRmEnvironment` i `Set-AzureRmEnvironment`
  - Dodano parametry `-AzureOperationalInsightsEndpoint` i `-AzureOperationalInsightsEndpointResourceId` do użycia z RP płaszczyzny danych OperationalInsights.

### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Skorygowano użycie polecenia `Login-AzureRmAccount` do użycia z elementem `Connect-AzureRmAccount`

### <a name="azurermcompute"></a>AzureRM.Compute
* Dodano parametr `-AvailabilitySetName` do uproszczonego zestawu parametrów `New-AzureRmVM`.
* Skorygowano użycie polecenia `Login-AzureRmAccount` do użycia z elementem `Connect-AzureRmAccount`
* Obsługa tożsamości przypisanych przez użytkownika dla maszyn wirtualnych i zestawu skalowania maszyn wirtualnych
    - Dodano parametry `-IdentityType` i `-IdentityId` do elementów `New-AzureRmVMConfig`, `New-AzureRmVmssConfig`, `Update-AzureRmVM` i `Update-AzureRmVmss`
* Dodano parametr `-EnableIPForwarding` do elementu `Add-AzureRmVmssNetworkInterfaceConfig`
* Dodano parametr `-Priority` do elementu `New-AzureRmVmssConfig`

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Skorygowano użycie polecenia `Login-AzureRmAccount` do użycia z elementem `Connect-AzureRmAccount`

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Skorygowano użycie polecenia `Login-AzureRmAccount` do użycia z elementem `Connect-AzureRmAccount`
* Skorygowano komunikat o błędzie dotyczący polecenia `Test-AzureRmDataLakeStoreAccount` wyświetlany podczas uruchamiania tego polecenia cmdlet bez zalogowania się za pomocą polecenia `Login-AzureRmAccount`

### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2018-01-01.

### <a name="azurermeventhub"></a>AzureRM.EventHub

* Dodano wymienione poniżej nowe polecenia dla operacji odzyskiwania po awarii replikacji geograficznej.
  - Tworzenie nowego aliasu (konfiguracja odzyskiwania po awarii):
    - `New-AzureRmEventHubGeoDRConfiguration`
  - Pobieranie aliasu (konfiguracja odzyskiwania po awarii):
    - `Get-AzureRmEventHubGeoDRConfiguration`
  - Wyłączanie odzyskiwania po awarii i zatrzymywanie replikowania zmian z podstawowych do pomocniczych przestrzeni nazw
    - `Set-AzureRmEventHubGeoDRConfigurationBreakPair`
  - Wywoływanie trybu failover odzyskiwania po awarii i ponowne konfigurowanie aliasu w taki sposób, aby wskazywał pomocniczą przestrzeń nazw
    - `Set-AzureRmEventHubGeoDRConfigurationFailOver`
  - Usuwanie aliasu (konfiguracja odzyskiwania po awarii)
    - `Remove-AzureRmEventHubGeoDRConfiguration`
* Dodano wymienione poniżej nowe polecenia umożliwiające sprawdzanie nazwy przestrzeni nazw i nazwy konfiguracji odzyskiwania po awarii replikacji geograficznej — Dostępność aliasu.
  - Sprawdzanie dostępności nazwy przestrzeni nazw lub aliasu (konfiguracja odzyskiwania po awarii):
    - `Test-AzureRmEventHubName`

### <a name="azurerminsights"></a>AzureRM.Insights
* Skorygowano użycie polecenia `Login-AzureRmAccount` do użycia z elementem `Connect-AzureRmAccount`

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Skorygowano użycie polecenia `Login-AzureRmAccount` do użycia z elementem `Connect-AzureRmAccount`

### <a name="azurermnetwork"></a>AzureRM.Network
* Poprawiono komunikat o zastąpieniu „Czy na pewno chcesz zastąpić zasób”

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Dodano obsługę wykonywania zapytań interfejsu API w wersji 2 za pośrednictwem elementu `Invoke-AzureRmOperationalInsightsQuery`. Zobacz [https://dev.loganalytics.io/](https://dev.loganalytics.io/), aby uzyskać więcej informacji dotyczących nowego interfejsu API.

### <a name="azurermresources"></a>AzureRM.Resources
* `Get-AzureRmADServicePrincipal`: Usunięto parametr `-ServicePrincipalName` z domyślnego zestawu parametrów Empty, ponieważ znajdował się on już w zestawie parametrów SPN

### <a name="azurermservicebus"></a>AzureRM.ServiceBus

* Dodano poprawkę funkcjonalną dla elementów `Remove-AzureRmServiceBusRule` i `Get-AzureRmServiceBusKey`
* Dodano wymienione poniżej nowe polecenia cmdlet dla operacji odzyskiwania po awarii replikacji geograficznej.
  - Tworzenie nowego aliasu (konfiguracja odzyskiwania po awarii):
    - `New-AzureRmServiceBusDRConfigurations`
  - Pobieranie aliasu (konfiguracja odzyskiwania po awarii):
    - `Get-AzureRmServiceBusDRConfigurations`
  - Wyłączanie odzyskiwania po awarii i zatrzymywanie replikowania zmian z podstawowych do pomocniczych przestrzeni nazw
    - `Set-AzureRmServiceBusDRConfigurationsBreakPairing`
  - Wywoływanie trybu failover odzyskiwania po awarii i ponowne konfigurowanie aliasu w taki sposób, aby wskazywał pomocniczą przestrzeń nazw
    - `Set-AzureRmServiceBusDRConfigurationsFailOver`
  - Usuwanie aliasu (konfiguracja odzyskiwania po awarii)
    - `Remove-AzureRmServiceBusDRConfigurations`
* Zaktualizowano polecenia cmdlet `Test-AzureRmServiceBusName` na potrzeby obsługi odzyskiwania po awarii replikacji geograficznej — operacje sprawdzania dostępności nazwy aliasu.
  - Sprawdzanie dostępności nazwy przestrzeni nazw lub aliasu (konfiguracja odzyskiwania po awarii):
    - `Test-AzureRmServiceBusName`

### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* Skorygowano użycie polecenia `Login-AzureRmAccount` do użycia z elementem `Connect-AzureRmAccount`

## <a name="520---january-2018"></a>5.2.0 — styczeń 2018 r.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Add-AzureRmAccount
  * Dodano logowanie -MSI na potrzeby uwierzytelniania przy użyciu poświadczeń tożsamości usługi zarządzanej bieżącej maszyny wirtualnej/usługi
  * Naprawiono uwierzytelnianie magazynu kluczy w przypadku logowania się przy użyciu tokenów dostępu podanych przez użytkownika

#### <a name="azurestorage"></a>Azure.Storage
* Dodano polecenia cmdlet umożliwiające pobieranie i ustawianie właściwości usługi Storage
    - Get-AzureStorageServiceProperty
    - Update-AzureStorageServiceProperty

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Zamieniono przestarzały parametr -Tags na parametr -Tag w przypadku elementów New-AzureRmApiManagementProperty, Set-AzureRmApiManagementProperty i New-AzureRmApiManagement

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermautomation"></a>AzureRM.Automation
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Zamieniono przestarzały parametr -Tags na parametr -Tag w przypadku elementu Set-AzureRmAutomationRunbook

#### <a name="azurermbackup"></a>AzureRM.Backup
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermbatch"></a>AzureRM.Batch
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Zamieniono przestarzały parametr -Tags na parametr -Tag w przypadku elementów New-AzureRmCdnEndpoint i New-AzureRmCdnProfile

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Integracja z zestawem SDK zarządzania usługami Cognitive Services w wersji 3.0.0.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Dodano uproszczony zestaw parametrów do polecenia New-AzureRmVmss, który umożliwia utworzenie zestawu skalowania maszyn wirtualnych i wszystkich wymaganych zasobów przy użyciu inteligentnych wartości domyślnych
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Zamieniono przestarzały parametr -Tags na parametr -Tag w przypadku elementów New-AzureRmVm i Update-AzureRmVm
* Naprawiono polecenie cmdlet Get-AzureRmComputeResourceSku w przypadku dołączenia strefy do ograniczenia.
* Zaktualizowano schemat konfiguracji agenta diagnostyki na potrzeby obsługi ujścia usługi Azure Monitor.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Włączono obsługę usługi Azure Key Vault dla wszystkich połączonych usług magazynu danych
* Dodano właściwość typu licencji dla środowiska Azure SSIS Integration Runtime
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Zamieniono przestarzały parametr -Tags na parametr -Tag w przypadku elementu New-AzureRmDataFactory

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Włączono obsługę usługi Azure Key Vault dla wszystkich połączonych usług magazynu danych
* Dodano właściwość typu licencji dla środowiska Azure SSIS Integration Runtime
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Dodano parametr „LicenseType” dla polecenia „Set-AzureRmDataFactoryV2IntegrationRuntime” w celu włączenia funkcji AHUB

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Zamieniono przestarzały parametr -Tags na parametr -Tag w przypadku elementów New-AzureRmDataLakeAnalyticsAccount i Set-AzureRmDataLakeAnalyticsAccount

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Zamieniono przestarzały parametr -Tags na parametr -Tag w przypadku elementów New-AzureRmDataLakeStoreAccount i Set-AzureRmDataLakeStoreAccount

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermdns"></a>AzureRM.Dns
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Dodano następujące nowe polecenie cmdlet:
  - Update-AzureRmEventGridSubscription
    - Zaktualizuj właściwości subskrypcji zdarzeń usługi Event Grid.
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurerminsights"></a>AzureRM.Insights
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Dodano obsługę certyfikatów w przypadku poleceń cmdlet usługi IoTHub
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Dodano obsługę parametru -AsJob dla długotrwałych poleceń cmdlet magazynu kluczy. Umożliwia on działanie wybranych poleceń cmdlet w tle i zwrócenie zadania w celu śledzenia i kontrolowania postępu.
  * Polecenie cmdlet, którego to dotyczy: Remove-AzureRmKeyVault
* Usunięto błąd polecenia Set-AzureRmKeyVaultAccessPolicy polegający na tym, że filtr usługi AAD ustawiał podaną główną nazwę użytkownika jako nazwę jednostki usługi zamiast ustawić główną nazwę użytkownika
  - Więcej informacji można znaleźć w następującym opisie problemu: https://github.com/Azure/azure-powershell/issues/5201

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Zamieniono przestarzały parametr -Tags na parametr -Tag w przypadku elementu Update-AzureRmMlCommitmentPlan

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* Dodano parametr IncludeAllResources do polecenia cmdlet Remove-AzureRmMlOpCluster
  - Użycie tego parametru przełącznika spowoduje usunięcie wszystkich zasobów pierwotnie utworzonych za pomocą klastra
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermmedia"></a>AzureRM.Media
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Zamieniono przestarzały parametr -Tags na parametr -Tag w przypadku elementów Set-AzureRmMediaService i New-AzureRmMediaService

#### <a name="azurermnetwork"></a>AzureRM.Network
* Dodano obsługę parametru -AsJob dla długotrwałych poleceń cmdlet sieci. Umożliwia on działanie wybranych poleceń cmdlet w tle i zwrócenie zadania w celu śledzenia i kontrolowania postępu.
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Zamieniono przestarzały parametr -Tags na parametr -Tag w przypadku elementów New-AzureRmNotificationHubsNamespace i Set-AzureRmNotificationHubsNamespace

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Zamieniono przestarzały parametr -Tags na parametr -Tag w przypadku elementów New-AzureRmOperationalInsightsSavedSearch, Set-AzureRmOperationalInsightsSavedSearch, New-AzureRmOperationalInsightsWorkspace i Set-AzureRmOperationalInsightsWorkspace

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Dodano opcję -UseOriginalStorageAccount do polecenia cmdlet Restore-AzureRmRecoveryServicesBackupItem.
  - Włączenie tej flagi powoduje przywrócenie dysków do ich oryginalnych kont magazynu, co pozwala użytkownikom zachowanie konfiguracji przywróconej maszyny wirtualnej możliwie najbliższej konfiguracji oryginalnych maszyn wirtualnych.
  - Pomaga to też zwiększyć wydajność operacji przywracania.

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Dodano 3 nowych poleceń cmdlet dla reguł zapory
* Dodano 3 nowe polecenia cmdlet dla replikacji geograficznej
* Dodano obsługę stref i tagów
* Ustawiono grupę zasobów jako opcjonalną, kiedy jest to możliwe.

#### <a name="azurermrelay"></a>AzureRM.Relay
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermresources"></a>AzureRM.Resources
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Dodano obsługę parametru -AsJob dla długotrwałych poleceń cmdlet zasobów. Umożliwia on działanie wybranych poleceń cmdlet w tle i zwrócenie zadania w celu śledzenia i kontrolowania postępu.
* Dodano alias z polecenia Get-AzureRmProviderOperation do polecenia Get-AzureRmResourceProviderAction w celu zachowania zgodności z konwencjami nazewnictwa

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermservermanagement"></a>AzureRM.ServerManagement
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Zamieniono przestarzały parametr -Tags na parametr -Tag w przypadku elementów New-AzureRmServerManagementNode i New-AzureRmServerManagementGateway

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermsiterecovery"></a>AzureRM.SiteRecovery
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermsql"></a>AzureRM.Sql
* Zaktualizowano opis parametrów poleceń inspekcji
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Dodano parametr -AsJob do długotrwałych poleceń cmdlet
* Wycofano przestarzały parametr -DatabaseName z polecenia Get-AzureRmSqlServiceObjective

#### <a name="azurermstorage"></a>AzureRM.Storage
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Rozwiązano problem z odwołaniami o wartości null w przypadku uruchamiania polecenia cmdlet New-AzureRMStorageAccount z parametrem -EnableEncryptionService o wartości Brak
* Dodano obsługę parametru -AsJob dla długotrwałych poleceń cmdlet magazynu. Umożliwia on działanie wybranych poleceń cmdlet w tle i zwrócenie zadania w celu śledzenia i kontrolowania postępu.
    - Polecenia cmdlet, których to dotyczy: New-, Remove-, Add- i Update- w przypadku konta magazynu i reguły sieci konta magazynu.

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Dodano moduł wypełniania lokalizacji do parametrów -Location umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą prawidłowych lokalizacji
* Dodano moduł wypełniania grup zasobów do parametrów -ResourceGroup umożliwiający wypełnianie po naciśnięciu klawisza Tab za pomocą grup zasobów w ramach bieżącej subskrypcji
* Dodano obsługę parametru -AsJob dla długotrwałych poleceń cmdlet witryn internetowych. Umożliwia on działanie wybranych poleceń cmdlet w tle i zwrócenie zadania w celu śledzenia i kontrolowania postępu.
     - Polecenia cmdlet, których to dotyczy: New-, Remove-, Add- i Set- w przypadku elementów WebApps, AppServicePlan i Slots

## <a name="2017128-version-511"></a>2017.12.8, wersja 5.1.1
* AnalysisServices
  - Zmieniono weryfikację zestawu lokalizacji na wyszukiwanie dynamiczne, aby zapewnić obsługę wszystkich chmur.
* Automatyzacja
  - Aktualizacja polecenia Import-AzureRMAutomationRunbook
    - Teraz są obsługiwane elementy runbook programu Python2
* Batch
  - Usunięto usterkę uniemożliwiającą automatyczne wykrywanie grupy zasobów przez operacje na koncie bez grupy zasobów
* Wystąpienia obliczeniowe
  - Polecenie Get-AzureRmComputeResourceSku umożliwia wyświetlanie informacji o strefach.
  - Zaktualizowano polecenie Disable-AzureRmVmssDiskEncryption, aby rozwiązać problem https://github.com/Azure/azure-powershell/issues/5038
  - Dodano obsługę parametru -AsJob dla długotrwałych poleceń cmdlet obliczeń. Umożliwia on działanie wybranych poleceń cmdlet w tle i zwrócenie zadania w celu śledzenia i kontrolowania postępu.
    - Polecenia cmdlet, których to dotyczy: Polecenia cmdlet usług Virtual Machines i Virtual Machine Scale Sets — New-, Update-, Set-, Remove-, Start-, Restart- i Stop-
    - Dodano uproszczony zestaw parametrów do polecenia New-AzureRmVM, który umożliwia utworzenie maszyny wirtualnej i wszystkich wymaganych zasobów przy użyciu inteligentnych wartości domyślnych
* ContainerInstance
  - Zastosowano zestaw SDK wystąpienia kontenera platformy Azure (2017-10-01)
    - Obsługa kończenia działania kontenera
    - Obsługa instalacji woluminów plików platformy Azure
    - Obsługa otwierania wielu portów dla publicznego adresu IP
* ContainerRegistry
  - Nowe polecenia cmdlet dotyczące replikacji geograficznej i elementów webhook
    - Get/New/Remove-AzureRmContainerRegistryReplication
    - Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook
* DataFactories
    - Teraz funkcja szyfrowania poświadczeń działa, gdy dostęp zdalny jest włączony (przez sieć) i wyłączony (maszyna lokalna).
* DataFactoryV2
  - Dodano dwa nowe polecenia cmdlet: Update-AzureRmDataFactoryV2 i Stop-AzureRmDataFactoryV2PipelineRun
* DataLakeAnalytics
  - Dodano parametr o nazwie ScriptParameter do polecenia Submit-AzureRmDataLakeAnalyticsJob
    - Szczegółowe informacje o parametrze ScriptParameter można uzyskać, używając polecenia Get-Help dla polecenia Submit-AzureRmDataLakeAnalyticsJob
  - W przypadku polecenia New-AzureRmDataLakeAnalyticsAccount zmieniono parametr MaxDegreeOfParallelism na parametr MaxAnalyticsUnits
    - Dodano alias parametru MaxAnalyticsUnits: MaxDegreeOfParallelism
  - W przypadku polecenia New-AzureRmDataLakeAnalyticsComputePolicy zmieniono parametr MaxDegreeOfParallelismPerJob na parametr MaxAnalyticsUnitsPerJob
    - Dodano alias parametru MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob
  - W przypadku polecenia Set-AzureRmDataLakeAnalyticsAccount zmieniono parametr MaxDegreeOfParallelism na parametr MaxAnalyticsUnits
    - Dodano alias parametru MaxAnalyticsUnits: MaxDegreeOfParallelism
  - W przypadku polecenia Submit-AzureRmDataLakeAnalyticsJob zmieniono parametr DegreeOfParallelism na parametr AnalyticsUnits
    - Dodano alias parametru AnalyticsUnits: DegreeOfParallelism
  - W przypadku polecenia Update-AzureRmDataLakeAnalyticsComputePolicy zmieniono parametr MaxDegreeOfParallelismPerJob na parametr MaxAnalyticsUnitsPerJob
    - Dodano alias parametru MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob
* MachineLearningCompute
  - Dodano polecenie Set-AzureRmMlOpCluster
    - Zaktualizowano liczbę agentów klastra lub konfigurację protokołu SSL
  - Właściwości programu Orchestrator są opcjonalne
    - Usługa utworzy jednostkę usługi, jeśli jej nie podano, więc właściwości programu Orchestrator są teraz opcjonalne
* PowerBIEmbedded
  - Dodano obsługę poleceń cmdlet dotyczących pojemności usługi Power BI Embedded
  - Nowe polecenie cmdlet Get-AzureRmPowerBIEmbeddedCapacity — pobiera szczegóły pojemności usługi PowerBI Embedded.
  - Nowe polecenie cmdlet New-AzureRmPowerBIEmbeddedCapacity — tworzy nową pojemność usługi PowerBI Embedded
  - Nowe polecenie cmdlet Remove-AzureRmPowerBIEmbeddedCapacity — usuwa wystąpienie pojemności usługi PowerBI Embedded
  - Nowe polecenie cmdlet Resume-AzureRmPowerBIEmbeddedCapacity — wznawia wystąpienie pojemności usługi PowerBI Embedded
  - Nowe polecenie cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity — wstrzymuje wystąpienie pojemności usługi PowerBI Embedded
  - Nowe polecenie cmdlet Test-AzureRmPowerBIEmbeddedCapacity — sprawdza obecność wystąpienia pojemności usługi PowerBI Embedded
  - Nowe polecenie cmdlet Update-AzureRmPowerBIEmbeddedCapacity — modyfikuje wystąpienie pojemności usługi PowerBI Embedded
* Profil
  - Zaktualizowano element USGovernmentActiveDirectoryEndpoint na https://login.microsoftonline.us/
    - Aby uzyskać więcej informacji dotyczących mapowań punktu końcowego platformy Azure Government, zobacz: https://docs.microsoft.com/azure/azure-government/documentation-government-developer-guide#endpoint-mapping
    - Dodano obsługę parametru -AsJob w poleceniach cmdlet, aby umożliwić wykonywanie wybranych poleceń cmdlet w tle i zwrócenie zadania śledzenia i kontrolowania postępu
    - Dodano parametr -AsJob do polecenia cmdlet Get-AzureRmSubscription
* RecoveryServices.Backup
  - Usunięto usterkę — polecenie Get-AzureRmRecoveryServicesBackupItem powinno uwzględniać wielkość liter podczas porównywania za pomocą filtru nazwy kontenera.
  - Usunięto usterkę — element AzureVmItem ma teraz właściwość, która umożliwia pokazanie czasu ostatniej operacji wykonywania kopii zapasowej (LastBackupTime).
* Zasoby
  - Rozwiązano problem, w wyniku którego użycie polecenia Get-AzureRMRoleAssignment powodowało tworzenie przypisań ról niestandardowych bez nazwy definicji roli
    - Użytkownicy mogą teraz korzystać z polecenia Get-AzureRMRoleAssignment z przypisaniami mającymi nazwy definicji roli niezależnie od typu roli
  - Rozwiązano problem, w wyniku którego polecenie Set-AzureRMRoleRoleDefinition zgłaszało błąd (nie znaleziono definicji roli) w przypadku nowego zakresu we właściwości assignablescopes
    - Użytkownicy mogą teraz korzystać z polecenia Set-AzureRMRoleRoleDefinition z zakresami możliwymi do przypisania, w tym nowymi zakresami, niezależnie od położenia zakresu
  - Umożliwiono używanie znaku „/” na końcu zakresu
    - Użytkownicy mogą teraz korzystać z poleceń cmdlet definicji ról i przypisań ról z zakresami kończącymi się znakiem „/” zgodnie z interfejsem API i interfejsem wiersza polecenia
  - Umożliwiono użytkownikom tworzenie przypisań ról za pomocą flagi delegowania
    - Użytkownicy mogą teraz dodawać flagę delegowania do polecenia New-AzureRMRoleAssignment
  - Naprawiono polecenie pobierania przypisania roli w celu uwzględniania parametru zakresu
  - Dodano alias dla elementu ServicePrincipalName w poleceniu cmdlet New-AzureRmRoleAssignment
    - Użytkownicy mogą teraz korzystać z elementu ApplicationId zamiast elementu ServicePrincipalName w przypadku używania polecenia cmdlet New-AzureRmRoleAssignment
* SiteRecovery
  - Dodano ostrzeżenia dotyczące zakończenia obsługi dla wszystkich poleceń cmdlet w tym module w ramach przygotowania do następnej wersji zawierającej istotne zmiany.
    - Więcej informacji na temat migracji poleceń cmdlet z usługi AzureRM można znaleźć w przewodniku dotyczącym istotnych zmian.
* Sql
  - Dodano możliwość zmiany nazwy bazy danych przy użyciu polecenia Set-AzureRmSqlDatabase
  - Rozwiązano problem https://github.com/Azure/azure-powershell/issues/4974
    - Podanie nieprawidłowej wartości AUDIT_CHANGED_GROUP dla poleceń cmdlet inspekcji nie powoduje już zgłoszenia błędu i zostanie to usunięte w następnej wersji.
  - Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5046
    - Parametr AuditAction nie jest już ignorowany w poleceniach cmdlet inspekcji
  - Rozwiązano problem z poleceniami cmdlet inspekcji występujący w przypadku podania wartości „Secondary” dla elementu StorageKeyType
    - W przypadku ustawiania inspekcji obiektów blob zamiast klucza pomocniczego jako wartość „Secondary” parametru StorageKeyType był używany podstawowy klucz konta magazynu.
  - Zmieniono treść komunikatu potwierdzenia z polecenia Set-AzureRmSqlServerTransparentDataEncryptionProtector
* Azure (fronton RedDog)
    - Usunięto wszystkie polecenia cmdlet usługi RemoteApp
* Azure.Storage
    - Uaktualniono bibliotekę klienta usługi Azure Storage do wersji 8.6.0 i bibliotekę przenoszenia danych usługi Azure Storage do wersji 0.6.5

## <a name="20171110-version-501"></a>2017.11.10 — wersja 5.0.1
* Rozwiązano problem z ładowaniem zestawu, który powodował, że niektóre polecenia cmdlet powodowały błąd podczas wykonywania w następujących modułach:
  - AzureRM.ApiManagement
  - AzureRM.Backup
  - AzureRM.Batch
  - AzureRM.Compute
  - AzureRM.DataFactories
  - AzureRM.HDInsight
  - AzureRM.KeyVault
  - AzureRM.RecoveryServices
  - AzureRM.RecoveryServices.Backup
  - AzureRM.RecoveryServices.SiteRecovery
  - AzureRM.RedisCache
  - AzureRM.SiteRecovery
  - AzureRM.Sql
  - AzureRM.Storage
  - AzureRM.StreamAnalytics

## <a name="2017118---version-500"></a>2017.11.08 — wersja 5.0.0
* UWAGA: To jest wersja zawierająca zmiany powodujące niezgodność. Aby uzyskać pełną listę zmian powodujących niezgodność, które zostały wprowadzone, zobacz przewodnik migracji (https://aka.ms/azps-migration-guide).
* Wszystkie polecenia cmdlet w usłudze AzureRM obsługują teraz pomoc online
  - Uruchom polecenie Get-Help z parametrem -Online, aby otworzyć pomoc online w domyślnej przeglądarce internetowej
* AnalysisServices
  * Rozwiązano problem z poleceniem Synchronize-AzureAsInstance, aby umożliwić jego współpracę z nowym interfejsem API REST AsAzure dla celów synchronizacji
* ApiManagement
  * Aby uzyskać informacje na temat przełomowych zmian wprowadzonych w tej wersji usługi ApiManagement, zobacz przewodnik migracji
  * Zaktualizowano polecenie cmdlet Get-AzureRmApiManagementUser, aby rozwiązać problem https://github.com/Azure/azure-powershell/issues/4510
  * Zaktualizowano polecenie cmdlet New-AzureRmApiManagementApi, aby utworzyć interfejs API z pustą ścieżką https://github.com/Azure/azure-powershell/issues/4069
* ApplicationInsights
  * Dodano polecenia umożliwiające pobieranie/tworzenie/usuwanie zasobu usługi Application Insights
    - Get-AzureRmApplicationInsights
    - New-AzureRmApplicationInsights
    - Remove-AzureRmApplicationInsights
  * Dodano polecenia umożliwiające pobieranie/aktualizowanie cen/dziennego limitu zasobu usługi Applicaiton Insights
    - Get-AzureRmApplicationInsights -IncludeDailyCap
    - Set-AzureRmApplicationInsightsPricingPlan
    - Set-AzureRmApplicationInsightsDailyCap
  * Dodano polecenia umożliwiające pobieranie/tworzenie/aktualizowanie/usuwanie ciągłego eksportu zasobu usługi Application Insights
    - Get-AzureRmApplicationInsightsContinuousExport
    - Set-AzureRmApplicationInsightsContinuousExport
    - New-AzureRmApplicationInsightsContinuousExport
    - Remove-AzureRmApplicationInsightsContinuousExport
  * Dodano polecenia umożliwiające pobieranie/tworzenie/usuwanie kluczy interfejsu API zasobu usługi Application Insights
    - Get-AzureRmApplicationInsightsApiKey
    - New-AzureRmApplicationInsightsApiKey
    - Remove-AzureRmApplicationInsightsApiKey
* AzureBatch
  * Dodano nowe parametry do polecenia `New-AzureRmBatchAccount`.
    - `PoolAllocationMode`: Tryb alokacji na potrzeby tworzenia pul w ramach konta usługi Batch. Aby utworzyć konto usługi Batch, które przydziela węzły pul w subskrypcji użytkownika, ustaw tę wartość na `UserSubscription`.
    - `KeyVaultId`: Identyfikator zasobu usługi Azure Key Vault skojarzonego z kontem usługi Batch.
    - `KeyVaultUrl`: Adres URL usługi Azure Key Vault skojarzonego z kontem usługi Batch.
  * Zaktualizowano parametry polecenia `New-AzureBatchTask`.
    - Usunięto przełącznik `RunElevated`. Dodano parametr `UserIdentity` w celu zastąpienia przełącznika `RunElevated`, a równoważne zachowanie można uzyskać, konstruując parametr `PSUserIdentity` w sposób pokazany poniżej:
      - $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Zadanie", "Administrator")
      - $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
    - Dodano parametr `AuthenticationTokenSettings`. Ten parametr umożliwia żądanie, aby usługa Batch podawała token uwierzytelniania dla zadania po jego uruchomieniu, unikając w ten sposób konieczności przekazywania kluczy konta usługi Batch do zadania w celu wysyłania żądań do usługi Batch.
    - Dodano parametr `ContainerSettings`.
      - Ten parametr pozwala zażądać, aby usługa Batch uruchamiała zadanie wewnątrz kontenera.
    - Dodano parametr `OutputFiles`.
      - Ten parametr umożliwia skonfigurowanie zadania tak, aby po zakończeniu pracy pliki były przekazywane do usługi Azure Storage.
  * Zaktualizowano parametry polecenia `New-AzureBatchPool`.
    - Dodano parametr `UserAccounts`.
      - Ten parametr określa konta użytkowników utworzone na każdym węźle w puli.
    - Dodano parametr `TargetLowPriorityComputeNodes` i zmieniono nazwę parametru `TargetDedicated` na `TargetDedicatedComputeNodes`.
      - Utworzono alias `TargetDedicated` dla parametru `TargetDedicatedComputeNodes`.
    - Dodano parametr `NetworkConfiguration`.
      - Ten parametr umożliwia skonfigurowanie ustawień sieciowych pul.
  * Zaktualizowano parametry polecenia `New-AzureBatchCertificate`.
    - Parametr `Password` nosi teraz nazwę `SecureString`.
  * Zaktualizowano parametry polecenia `New-AzureBatchComputeNodeUser`.
    - Parametr `Password` nosi teraz nazwę `SecureString`.
  * Zaktualizowano parametry polecenia `Set-AzureBatchComputeNodeUser`.
    - Parametr `Password` nosi teraz nazwę `SecureString`.
  * Zmieniono nazwę parametru `Name` na `Path` w poleceniach `Get-AzureBatchNodeFile`, `Get-AzureBatchNodeFileContent` i `Remove-AzureBatchNodeFile`.
    - Utworzono alias `Name` dla parametru `Path`.
  * Zmiany obiektów
    - Aby uzyskać pełną listę, zobacz dziennik zmian usługi Batch
  * Dodano obsługę uwierzytelniania w oparciu o usługę Azure Active Directory.
    - Aby używać uwierzytelniania za pomocą usługi Azure Active Directory, pobierz obiekt `BatchAccountContext` przy użyciu polecenia cmdlet `Get-AzureRmBatchAccount` i podaj tę wartość `BatchAccountContext` dla parametru `-BatchContext` polecenia cmdlet usługi Batch. Uwierzytelnianie za pomocą usługi Azure Active Directory jest obowiązkowe w przypadku kont w trybie `PoolAllocationMode = UserSubscription`.
    - W przypadku istniejących kont lub nowych kont utworzonych przy użyciu trybu `PoolAllocationMode = BatchService` możesz nadal używać uwierzytelniania za pomocą klucza współużytkowanego, pobierając obiekt `BatchAccountContext` za pomocą polecenia cmdlet `Get-AzureRmBatchAccoutKeys`.
* Wystąpienia obliczeniowe
  * Polecenia rozszerzenia Azure Disk Encryption
    - Nowy parametr polecenia „Set-AzureRmVmDiskEncryptionExtension”: „-EncryptFormatAll” szyfruje formaty dysków z danymi
    - Nowe parametry polecenia „Set-AzureRmVmDiskEncryptionExtension”: „-ExtensionPublisherName” i „-ExtensionType” zezwalają na przełączanie na inne wersje rozszerzenia
    - Nowe parametry polecenia „Disable-AzureRmVmDiskEncryption”: „-ExtensionPublisherName” i „-ExtensionType” zezwalają na przełączanie na inne wersje rozszerzenia
    - Nowe parametry polecenia „Get-AzureRmVmDiskEncryptionStatus”: „-ExtensionPublisherName” i „-ExtensionType” zezwalają na przełączanie na inne wersje rozszerzenia
* DataLakeAnalytics
  * Aby uzyskać informacje na temat przełomowych zmian wprowadzonych w tej wersji usługi DataLakeAnalytics, zobacz przewodnik migracji
  * Zmieniono jeden z dwóch typów OutputType polecenia Get-AzureRmDataLakeAnalyticsAccount
    - List\<DataLakeAnalyticsAccount> na List\<PSDataLakeAnalyticsAccountBasic>
    - Właściwości typu PSDataLakeAnalyticsAccountBasic to ściśle określony podzbiór właściwości typu DataLakeAnalyticsAccount
    - Typ DataLakeAnalyticsAccount nie zwraca zawartych w nim właściwości dodatkowych.  W związku z tym ta zmiana ma na celu precyzyjne odzwierciedlenie tej sytuacji. Właściwości dodatkowe wciąż znajdują się w typie PSDataLakeAnalyticsAccountBasic, ale są oznaczone jako Obsolete.
  * Zmieniono jeden z dwóch typów OutputType polecenia Get-AzureRmDataLakeAnalyticsJob
    - List\<JobInformation> na List\<PSJobInformationBasic>
    - Właściwości typu PSJobInformationBasic to ściśle określony podzbiór właściwości typu JobInformation
    - Typ JobInformation nie zwraca zawartych w nim właściwości dodatkowych.  W związku z tym ta zmiana ma na celu precyzyjne odzwierciedlenie tej sytuacji. Właściwości dodatkowe wciąż znajdują się w typie PSJobInformationBasic, ale są oznaczone jako Obsolete.
* DataLakeStore
  * Aby uzyskać informacje na temat przełomowych zmian wprowadzonych w tej wersji usługi DataLakeStore, zobacz przewodnik migracji
  * Zmieniono jeden z dwóch typów OutputType polecenia Get-AzureRmDataLakeStoreAccount
    - List\<PSDataLakeStoreAccount> na List\<PSDataLakeStoreAccountBasic>
    - Właściwości typu PSDataLakeStoreAccountBasic to ściśle określony podzbiór właściwości typu PSDataLakeStoreAccount
    - Typ PSDataLakeStoreAccount nie zwraca zawartych w nim właściwości dodatkowych.  W związku z tym ta zmiana ma na celu precyzyjne odzwierciedlenie tej sytuacji. Właściwości dodatkowe wciąż znajdują się w typie PSDataLakeStoreAccountBasic, ale są oznaczone jako Obsolete.
* Dns
  * Obsługa typów rekordów CAA w usłudze Azure DNS
    - Obsługa wszystkich operacji na typie rekordu CAA
* EventHub
  * Aby uzyskać informacje na temat przełomowych zmian wprowadzonych w tej wersji usługi EventHub, zobacz przewodnik migracji
* Insights
  * Aby uzyskać informacje na temat przełomowych zmian wprowadzonych w tej wersji usługi Insights, zobacz przewodnik migracji
* Sieć
  * Aby uzyskać informacje na temat przełomowych zmian wprowadzonych w tej wersji usługi Network, zobacz przewodnik migracji
  * Dodano polecenie cmdlet umożliwiające wyświetlanie listy dostępnych usługodawców internetowych dla określonego regionu Azure
    - Get-AzureRmNetworkWatcherReachabilityProvidersList
  * Dodano polecenie cmdlet umożliwiające uzyskanie oceny opóźnienia względnego dla usługodawców internetowych z określonej lokalizacji do regionów Azure
    - Get-AzureRmNetworkWatcherReachabilityReport
* Profil
  - Set-AzureRmDefault
    - Użyj tego polecenia cmdlet, aby określić domyślną grupę zasobów.  Dzięki temu parametr -ResourceGroup stanie się opcjonalny dla niektórych poleceń cmdlet, a gdy grupa zasobów nie zostanie określona, będzie używana grupa domyślna
    - ```Set-AzureRmDefault -ResourceGroupName "ExampleResourceGroup"```
    - Jeśli określona grupa zasobów istnieje w subskrypcji, zostanie ona ustawiona jako domyślna.  W przeciwnym razie grupa zasobów zostanie utworzona, a następnie ustawiona jako domyślna.
  - Get-AzureRmDefault
    - Użyj tego polecenia cmdlet, aby uzyskać bieżącą domyślną grupę zasobów (oraz inne wartości domyślne w przyszłości).
    - ```Get-AzureRmDefault -ResourceGroup```
  - Clear-AzureRmDefault
    - Użyj tego polecenia cmdlet, aby usunąć bieżącą domyślną grupę zasobów
    - ```Clear-AzureRmDefault -ResourceGroup```
  - Add-AzureRmEnvironment i Set-AzureRmEnvironment
    - Dodaj parametr BatchAudience umożliwiający określenie odbiorców usługi Azure Batch Active Directory, którzy będą używani podczas uzyskiwania tokenów uwierzytelniania dla usługi Batch.
* RecoveryServices.Backup
  * Dodano polecenia cmdlet umożliwiające wykonywanie błyskawicznego odzyskiwania plików.
    - Get-AzureRmRecoveryServicesBackupRPMountScript
    - Disable-AzureRmRecoveryServicesBackupRPMountScript
  * Zaktualizowano wersję zestawu SDK RecoveryServices.Backup do najnowszej wersji
  * Zaktualizowano testy obciążenia maszyny wirtualnej platformy Azure VM, aby wszystkie konfiguracje niezbędne do uruchamiania testów były przeprowadzane przez same testy.
  * Rozwiązano problem https://github.com/Azure/azure-powershell/issues/3164
* RecoveryServices.SiteRecovery
  * Zmiany dotyczące operacji między usługami ASR VMware i Azure Site Recovery (polecenia cmdlet obsługują obecnie operacje Enterprise-Enterprise, Enterprise-Azure, HyperV-Azure)
    - New-AzureRmRecoveryServicesAsrPolicy
    - New-AzureRmRecoveryServicesAsrProtectedItem
    - Update-AzureRmRecoveryServicesAsrPolicy
    - Update-AzureRmRecoveryServicesAsrProtectionDirection
  * Dodano obsługę magazynu opartego na usłudze AAD
  * Dodano polecenia cmdlet umożliwiające zarządzanie zasobami VCenter
    - Get-AzureRmRecoveryServicesAsrVCenter
    - New-AzureRmRecoveryServicesAsrVCenter
    - Remove-AzureRmRecoveryServicesAsrVCenter
    - Update-AzureRmRecoveryServicesAsrVCenter
  * Dodano inne polecenia cmdlet
    - Get-AzureRmRecoveryServicesAsrAlertSetting
    - Get-AzureRmRecoveryServicesAsrEvent
    - New-AzureRmRecoveryServicesAsrProtectableItem
    - Set-AzureRmRecoveryServicesAsrAlertSetting
    - Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
    - Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob
    - Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob
    - Update-AzureRmRecoveryServicesAsrMobilityService
* ServiceBus
  - Aby uzyskać informacje na temat przełomowych zmian wprowadzonych w tej wersji usługi ServiceBus, zobacz przewodnik migracji
* Sql
  * Dodanie obsługi listy i anulowanie operacji asynchronicznej updateslo na bazie danych
    - Aktualizacja istniejącego polecenia cmdlet Get-AzureRmSqlDatabaseActivity tak, aby zwracało stan operacji updateslo bazy danych.
    - Dodanie nowego polecenia cmdlet Stop-AzureRmSqlDatabaseActivity umożliwiającego anulowanie operacji asynchronicznej updateslo na bazie danych.
  * Dodanie obsługi nadmiarowości strefy dla baz danych i pul elastycznych
    - Dodanie parametru przełącznika ZoneRedundant do polecenia New-AzureRmSqlDatabase
    - Dodanie parametru przełącznika ZoneRedundant do polecenia Set-AzureRmSqlDatabase
    - Dodanie parametru przełącznika ZoneRedundant do polecenia New-AzureRmSqlElasticPool
    - Dodanie parametru przełącznika ZoneRedundant do polecenia Set-AzureRmSqlElasticPool
  * Dodanie obsługi aliasów DNS serwera
    - Dodanie polecenia cmdlet Get-AzureRmSqlServerDnsAlias pobierającego aliasy DNS według serwerów oraz nazwę aliasu lub listę aliasów DNS serwera dla serwera SQL Azure.
    - Dodanie polecenia cmdlet New-AzureRmSqlServerDnsAlias tworzącego nowy alias DNS serwera dla danego serwera SQL Azure
    - Dodanie polecenia cmdlet Set-AzurermSqlServerDnsAlias umożliwiającego zaktualizowanie serwera SQL Azure, na który wskazuje alias DNS serwera
    - Dodanie polecenia cmdlet Remove-AzureRmSqlServerDnsAlias usuwającego alias DNS serwera dla danego serwera SQL Azure
* Azure.Storage
  * Uaktualniono bibliotekę klienta usługi Azure Storage do wersji 8.5.0 i bibliotekę przenoszenia danych usługi Azure Storage do wersji 0.6.3
  * Dodano funkcję obsługi migawki udziału plików
    - Dodano parametr „SnapshotTime” do polecenia Get-AzureStorageShare
    - Dodano parametr „IncludeAllSnapshot” do polecenia Remove-AzureStorageShare
