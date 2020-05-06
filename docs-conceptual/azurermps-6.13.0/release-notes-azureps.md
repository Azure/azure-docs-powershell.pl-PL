---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: eecd66ddf433cc2543ceeaef1519d69179f2f099
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534453"
---
# <a name="release-notes"></a>Informacje o wersji

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.

---
## <a name="6130---november-2018"></a>6.13.0 — listopad 2018 r.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Aktualizacja zależności w związku z problemem dotyczącym mapowania typów

#### <a name="azurermautomation"></a>AzureRM.Automation
* Polecenia cmdlet usługi Azure Automation oparte na programie Swagger
* Dodano polecenia cmdlet rozwiązania Update Management
* Dodano polecenia cmdlet kontroli kodu źródłowego
* Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup
* Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła

#### <a name="azurermcompute"></a>AzureRM.Compute
* Rozwiązano problem dotyczący tożsamości SystemAssigned
* Aktualizacja zależności w związku z problemem dotyczącym mapowania typów

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Aktualizacja zależności w związku z problemem dotyczącym mapowania typów

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace

#### <a name="azurermnetwork"></a>AzureRM.Network
* Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError
* Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall
* Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego. 
* Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.
* Przekonwertowano strefę czasową zasad na wielkie litery.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem
* Aktualizacja zależności w związku z problemem dotyczącym mapowania typów

#### <a name="azurermrelay"></a>AzureRM.Relay
* Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.

#### <a name="azurermresources"></a>AzureRM.Resources
* Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`
* Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata
* Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność

#### <a name="azurermsql"></a>AzureRM.Sql
* Dodano nowe polecenia cmdlet dla operacji CRUD w wystąpieniu zarządzanym usługi Azure SQL Database i zarządzanej bazie danych Azure SQL
    - Get-AzureRmSqlInstance
    - New-AzureRmSqlInstance
    - Set-AzureRmSqlInstance
    - Remove-AzureRmSqlInstance
    - Get-AzureRmSqlInstanceDatabase
    - New-AzureRmSqlInstanceDatabase
    - Restore-AzureRmSqlInstanceDatabase
    - Remove-AzureRmSqlInstanceDatabase
* Włączono rozszerzone zarządzanie zasadami inspekcji na serwerze lub w bazie danych.
    - Dodano nowy parametr (PredicateExpression), aby umożliwić filtrowanie dzienników inspekcji.
    - Zmodyfikowano polecenia cmdlet tak, aby korzystały z klientów SQL zamiast starszych klientów.
    - Set-AzureRmSqlServerAuditing.
    - Get-AzureRmSqlServerAuditing.
    - Set-AzureRmSqlDatabaseAuditing.
    - Get-AzureRmSqlDatabaseAuditing.
* Rozwiązano problem występujący podczas używania polecenia Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings z ustawionym parametrem nazwy konta magazynu

## <a name="6120---november-2018"></a>6.12.0 — listopad 2018 r.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta
* Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzureRmAccount na Tenant i dodano alias dla parametru TenantId
* Zaktualizowano opis parametru TenantId dla polecenia Connect-AzureRmAccount
* Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy
    - https://github.com/Azure/azure-powershell/issues/6936
* Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie
    - https://github.com/Azure/azure-powershell/issues/7453
* Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej
    - https://github.com/Azure/azure-powershell/issues/7462
* Rozwiązano problem polegający na zgłaszaniu elementu „Disconnect-AzureRmAccount” w przypadku braku połączenia
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a>AzureRM.Automation
* Zmieniono nazwę biblioteki DLL polecenia cmdlet na Microsoft.Azure.Commands.Automation.dll

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Dodano operację Get-AzureRmCognitiveServicesAccountSkus.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Dodano polecenia cmdlet Add-AzureRmVmssVMDataDisk i Remove-AzureRmVmssVMDataDisk
* Polecenie Get-AzureRmVMImage wyświetla element AutomaticOSUpgradeProperties
* Rozwiązano problem polegający na tym, że wartości opcji SetAzureRmVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.
* Dodano domyślną współbieżność do operacji wielowątkowych.

#### <a name="azurerminsights"></a>AzureRM.Insights
* Rozwiązano problem nr 7267 (obszar autoskalowania)
    - Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).
* Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzureRMDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia
    - Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji

#### <a name="azurermnetwork"></a>AzureRM.Network
* Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:
    - Get-AzureRmExpressRouteCircuitRouteTable
    - Get-AzureRmExpressRouteCircuitARPTable
    - Get-AzureRmExpressRouteCircuitRouteTableSummary
    - Get-AzureRMExpressRouteCrossConnectionArpTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTableSummary

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Dodano polecenia cmdlet korygowania zasad

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Dodano obsługę udziałów plików platformy Azure do usług odzyskiwania.

#### <a name="azurermresources"></a>AzureRM.Resources
* Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402
    - Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzureRmResource”

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.
* Rozwiązano problem z poleceniem „Add-AzureRmServiceFabricClusterCertificate”
    - Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).
    - Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).
* Rozwiązano problem z poleceniem „Update-AzureRmServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.

## <a name="6110---october-2018"></a>6.11.0 — październik 2018 r.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Rozwiązano problem z poleceniem Get-AzureRmSubscription w usłudze CloudShell
* Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta

#### <a name="azurermbackup"></a>AzureRM.Backup
* Przestarzałe polecenia cmdlet usługi Azure Backup.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzureRmVm”
* Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Dodawanie obsługi dla reguł sieci wirtualnej
    - Get-AzureRmDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.
    - Add-AzureRmDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.
    - Set-AzureRmDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.
    - Remove-AzureRmDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.
* Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.

#### <a name="azurermresources"></a>AzureRM.Resources
* Rozwiązano problem polegający na tym, że polecenie Get-AzureRMRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza. Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.

## <a name="6100---october-2018"></a>6.10.0 — październik 2018 r.
#### <a name="azurestorage"></a>Azure.Storage
* Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Obsługa polecenia Get-AzureRmCognitiveServicesAccountSkus bez istniejącego konta.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Rozwiązano problem z poleceniem Get-AzureRmVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne
* Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzureRmVmss.
* Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Dodano funkcję NetworkProfile. Dodano nowe polecenia cmdlet
    - Get-AzureRMNetworkProfile
    - New-AzureRMNetworkProfile
    - Remove-AzureRMNetworkProfile
    - Set-AzureRMNetworkProfile
    - New-AzureRMContainerNicConfig
    - New-AzureRmContainerNicConfigIpConfig
* Dodano link skojarzenia usługi w modelu podsieci
* Dodano polecenia cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap i Remove-AzureRmVirtualNetworkTap
* Dodano polecenia cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig i Remove-AzureRmNEtworkInterfaceTapConfig

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Jako parametru Size będzie można użyć dowolnego ciągu. Dodano element P5 w menu podręcznym PSArgumentCompleter

#### <a name="azurermresources"></a>AzureRM.Resources
* Dodano brakujący parametr -Mode do polecenia Set-AzureRmPolicyDefinition
* Usunięto błąd polecenia Get-AzureRmProviderOperation w operacjach ze źródłem zawierającym użytkownika

#### <a name="azurermsql"></a>AzureRM.Sql
* Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure

#### <a name="azurermstorage"></a>AzureRM.Storage
* Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.
    - Get-AzureRmStorageUsage

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Nowe polecenie cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłe wdrażania kontenera
* Nowe polecenia cmdlet New-AzureRMWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows

## <a name="690---september-2018"></a>6.9.0 — wrzesień 2018 r.
#### <a name="general"></a>Ogólne
* Element AzureRM.SignalR został dodany do modułu zbiorczego AzureRM

#### <a name="azurermprofile"></a>AzureRM.Profile
* Drobne zmiany wspólnego kodu magazynu
* Zaktualizowano pliki pomocy w celu uwzględnienia pełnych typów parametrów.
* Zmieniono opcję -ServicePrincipal na nieobowiązkową w zestawie parametrów ServicePrincipalCertificateWithSubscriptionId 

#### <a name="azurestorage"></a>Azure.Storage
* Obsługa tworzenia kontekstu magazynu przy użyciu protokołu OAuth. 
    - New-AzureStorageContext

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Dodano element Standard_Microsoft w jednostce SKU cen usługi CDN. 

#### <a name="azurermcompute"></a>AzureRM.Compute
* Przeniesiono zależności magazynu kluczy i magazynu do zależności wspólnych
* Dodano obsługę kolejnych rozmiarów maszyn wirtualnych do poleceń cmdlet funkcji AEM
* Dodano parametr PublicIPPrefix do polecenia New-AzureRmVmssIpConfig
* Dodano parametr ResourceId do polecenia cmdlet Invoke-AzureRmVMRunCommand
* Dodano polecenie cmdlet Invoke-AzureRmVmssVMRunCommand

#### <a name="azurermdns"></a>AzureRM.Dns
* Dodano obsługę rekordu aliasu podczas tworzenia rekordów DNS

#### <a name="azurerminsights"></a>AzureRM.Insights
* Rozwiązano problemy nr 6833 i 7102 (obszar ustawień diagnostycznych)
    - Problemy z nazwą domyślną, np. „usługa”, podczas tworzenia i tworzenia/pobierania listy ustawień diagnostycznych
    - Problemy z tworzeniem ustawień diagnostycznych przy użyciu kategorii
* Dodano komunikat o zakończeniu obsługi parametrów ziarn czasu metryk
    - Parametry typu Timegrain są nadal akceptowane (jest to zmiana niepowodująca niezgodności), ale są one ignorowane w zapleczu, ponieważ tylko wersja PT1M jest prawidłowa

#### <a name="azurermnetwork"></a>AzureRM.Network
* Zmiany poleceń cmdlet usługi LoadBalancer
  - LoadBalancerInboundNatPoolConfig: dodano parametry IdleTimeoutInMinutes, EnableFloatingIp i EnableTcpReset
  - LoadBalancerInboundNatRuleConfig: dodano parametr EnableTcpReset
  - LoadBalancerRuleConfig: dodano parametr EnableTcpReset
  - LoadBalancerProbeConfig: dodano obsługę wartości „Https” dla parametru Protocol
* Dodano nowe polecenia dla nowego zasobu podrzędnego OutboundRule usługi LoadBalancer
  - Add-AzureRmLoadBalancerOutboundRuleConfig
  - Get-AzureRmLoadBalancerOutboundRuleConfig
  - New-AzureRmLoadBalancerOutboundRuleConfig
  - Set-AzureRmLoadBalancerOutboundRuleConfig
  - Remove-AzureRmLoadBalancerOutboundRuleConfig
* Dodano nową właściwość HostedWorkloads dla interfejsu PSNetworkInterface
* Dodano nowe polecenia cmdlet dla funkcji Azure Firewall za pośrednictwem usługi ARM
  - Dodano polecenie Get-AzureRmFirewall
  - Dodano polecenie Set-AzureRmFirewall
  - Dodano polecenie New-AzureRmFirewall
  - Dodano polecenie Remove-AzureRmFirewall
  - Dodano polecenie New-AzureRmFirewallApplicationRuleCollection
  - Dodano polecenie New-AzureRmFirewallApplicationRule
  - Dodano polecenie New-AzureRmFirewallNatRuleCollection
  - Dodano polecenie New-AzureRmFirewallNatRule
  - Dodano polecenie New-AzureRmFirewallNetworkRuleCollection
  - Dodano polecenie New-AzureRmFirewallNetworkRule
* Dodano obsługę zaufanego certyfikatu głównego i konfiguracji skalowania automatycznego w usłudze Application Gateway
  - Dodano nowe polecenia cmdlet:
      - Add-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayTrustedRootCertificate
      - New-AzureRmApplicationGatewayTrustedRootCertificate
      - Remove-AzureRmApplicationGatewayTrustedRootCertificate
      - Set-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayAutoscaleConfiguration
      - New-AzureRmApplicationGatewayAutoscaleConfiguration
      - Remove-AzureRmApplicationGatewayAutoscaleConfiguration
      - Set-AzureRmApplicationGatewayAutoscaleConfiguration
  - Zaktualizowano polecenia cmdlet przy użyciu opcjonalnego parametru -TrustedRootCertificate
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
      - New-AzureRmApplicationGatewayBackendHttpSetting
      - Set-AzureRmApplicationGatewayBackendHttpSetting
  - Zaktualizowano polecenia cmdlet przy użyciu opcjonalnego parametru -AutoscaleConfiguration
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
* Dodano polecenie cmdlet dla punktu końcowego interfejsu Get-AzureInterfaceEndpoint
* Dodano obsługę wielu prefiksów adresów w podsieci. Zaktualizowano następujące polecenia cmdlet:
  - New-AzureRmVirtualNetworkSubnetConfig
  - Set-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmVirtualNetworkSubnetConfig
  - Get-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmApplicationGatewayAuthenticationCertificate
  - Add-AzureRmApplicationGatewayFrontendIPConfig
  - New-AzureRmApplicationGatewayFrontendIPConfig
  - Set-AzureRmApplicationGatewayFrontendIPConfig
  - Add-AzureRmApplicationGatewayIPConfiguration
  - New-AzureRmApplicationGatewayIPConfiguration
  - Set-AzureRmApplicationGatewayIPConfiguration
  - Add-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmNetworkInterfaceIpConfig — Set-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmVirtualNetworkGatewayIpConfig
  - Add-AzureRmVirtualNetworkGatewayIpConfig
  - Set-AzureRmLoadBalancerFrontendIpConfig
  - Add-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmNetworkInterface
* Dodano polecenia cmdlet na potrzeby delegowania podsieci.
  - New-AzureRmDelegation: tworzy nowe delegowanie, które można dodać do podsieci
  - Remove-AzureRmDelegation: pobiera podsieć i usuwa z niej podaną nazwę delegowania
  - Add-AzureRmDelegation: pobiera podsieć i dodaje do niej podaną nazwę usługi jako delegowanie
  - Get-AzureRmDelegation
  - Get-AzureRmAvailableServiceDelegations

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Obsługa dysków zarządzanych

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Zaktualizowano zależność szczegółowych informacji.

#### <a name="azurermresources"></a>AzureRM.Resources
* Zaktualizowano polecenie New-AzureRmResourceGroupDeployment przy użyciu nowego parametru RollbackAction
    - Dodano obsługę elementu OnErrorDeployment przy użyciu nowego parametru.
* Obsługa tożsamości zarządzanej w przypisaniach zasad.
* Parametry z wartościami domyślnymi nie są już wymagane podczas przypisywania zasad za pomocą polecenia „New-AzureRmPolicyAssignment”
* Dodano nowe polecenie cmdlet Get-AzureRmPolicyAlias służące do pobierania aliasów zasad

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Rozwiązano problem nr 7161

#### <a name="azurermsignalr"></a>AzureRM.SignalR
* Zaktualizowano nazwy jednostek SKU Bezpłatna_F1 i Standardowa_S1
* Dodano pole wersji do obiektu PSSignalRResource i parametry połączenia do obiektu PSSignalRKeys.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Obsługa zasad niezmienności w elemencie AzureRm.Storage 
    - Remove-AzureRmStorageAccountNetworkRule
    - Get-AzureRmStorageContainer
    - Update-AzureRmStorageContainer
    - New-AzureRmStorageContainer
    - Remove-AzureRmStorageContainer
    - Add-AzureRmStorageContainerLegalHold
    - Remove-AzureRmStorageContainerLegalHold
    - Set-AzureRmStorageContainerImmutabilityPolicy
    - Get-AzureRmStorageContainerImmutabilityPolicy
    - Remove-AzureRmStorageContainerImmutabilityPolicy
    - Lock-AzureRmStorageContainerImmutabilityPolicy

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Dodano dwa nowe polecenia cmdlet: Get-AzureRmDeletedWebApp i Restore-AzureRmDeletedWebApp
* New-AzureRmAppServicePlan — dodano przełącznik funkcji Hyper-V na potrzeby tworzenia planu usługi App Service przy użyciu kontenera systemu Windows
* New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot — dodano nowe parametry (ciąg –ContainerRegistryUser -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) na potrzeby tworzenia aplikacji kontenera systemu Windows oraz zarządzania nią

## <a name="681---august-2018"></a>6.8.1 — sierpień 2018 r.
#### <a name="general"></a>Ogólne
* Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.
* Zaktualizowano wspólne zestawy środowiska uruchomieniowego

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.
* Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6603
    - Polecenia cmdlet Import-AzureRmApiManagementApi i *-AzureRmApiManagementCertificate teraz obsługują ścieżki względne
* Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6879
    - CertificateInformation to możliwa do ustawienia właściwość pozwalająca poleceniu cmdlet Set-AzureRmApiManagement poprawnie działać. Rozwiązano przez aktualizację do pakietu nuget 4.0.4-preview
* Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6853
    - W filtrze Odata naprawiono wyszukiwanie według nazwy dla produktu
* Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6814
    - W filtrze Odata naprawiono wyszukiwanie według nazwy dla interfejsu API
* Dodano obsługę rejestratora AzureMonitor


#### <a name="azurermcompute"></a>AzureRM.Compute
* Naprawiono problem polegający na braku elementu docelowego w danych wyjściowych błędu.
* Rozwiązano problem z typem konta magazynu dla maszyny wirtualnej z dyskiem zarządzanym
* Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.
* Naprawiono polecenia cmdlet rozszerzenia AEM dla innych środowisk, na przykład Azure — Chiny

#### <a name="azurermnetwork"></a>AzureRM.Network
* Zmieniono domyślną prezentację danych wyjściowych polecenia cmdlet na widok tabeli

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Naprawiono błąd w poleceniu Update-AzureRmPowerBIEmbeddedCapacity występujący podczas próby skalowania wstrzymanej pojemności


#### <a name="azurermresources"></a>AzureRM.Resources
* Rozwiązano problem z tworzeniem aplikacji zarządzanych z witryny MarketPlace.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Rozwiązane problemy
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Dodano obsługę metody routingu MultiValue
    - Nowy parametr „MaxReturn” dla routingu MultiValue
* Dodano obsługę metody routingu Subnet
    - Obsługa zakresów adresów IP (podsieci) w punktach końcowych
* Dodano obsługę nagłówków niestandardowych w profilach
* Dodano obsługę zakresów kodów oczekiwanego stanu w profilach
* Dodano obsługę nagłówków niestandardowych w punktach końcowych

## <a name="680---august-2018"></a>6.8.0 — sierpień 2018 r.
#### <a name="general"></a>Ogólne
* Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Dodano właściwość wygasania do tokenów zwracanych podczas operacji Connect-AzureRmAccount

#### <a name="azurermcompute"></a>AzureRM.Compute
* Naprawiono problem polegający na braku elementu docelowego w danych wyjściowych błędu.
* Rozwiązano problem z typem konta magazynu dla maszyny wirtualnej z dyskiem zarządzanym
* Naprawiono polecenia cmdlet rozszerzenia AEM dla innych środowisk, na przykład Azure — Chiny

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Naprawiono przykłady dla poleceń New-AzureRmIotHubExportDevices i New-AzureRmIotHubImportDevices

#### <a name="azurermnetwork"></a>AzureRM.Network
* Zmieniono domyślną reprezentację modeli na widok tabeli

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Naprawiono błąd w poleceniu Update-AzureRmPowerBIEmbeddedCapacity występujący podczas próby skalowania wstrzymanej pojemności

#### <a name="azurermresources"></a>AzureRM.Resources
* Rozwiązano problem z tworzeniem aplikacji zarządzanej z witryny MarketPlace.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Rozwiązano problemy
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Obsługa metody routingu MultiValue
    - Nowy parametr „MaxReturn” dla routingu MultiValue
* Obsługa metody routingu Subnet
    - Obsługa zakresów adresów IP (podsieci) w punktach końcowych
* Obsługa nagłówków niestandardowych w profilach
* Obsługa zakresów kodów oczekiwanego stanu w profilach
* Obsługa nagłówków niestandardowych w punktach końcowych

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Rozwiązano problem z niepoprawnie ustawionymi domyślnymi grupami zasobów.

## <a name="670---august-2018"></a>6.7.0 — sierpień 2018 r.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.
* Dodaj identyfikator użytkownika do domyślnej nazwy kontekstu, aby uniknąć konfliktów kontekstów
    - https://github.com/Azure/azure-powershell/issues/6489
* Rozwiązanie problemu z poleceniem Clear-AzureRmContext, który powodował problemy w przypadku wybrania kontekstu nr 6398
* Umożliwienie przekazywania domeny dzierżawy do parametru „-TenantId” polecenia „Connect-AzureRmAccount”
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a>Azure.Storage
* Usunięcie ograniczenia limitu przydziału udziału plików platformy Azure do 5 TB
* Set-AzureStorageShareQuota

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azureanalysisservices"></a>Azure.AnalysisServices
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermbackup"></a>AzureRM.Backup
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermbatch"></a>AzureRM.Batch
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermbilling"></a>AzureRM.Billing
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.
* Dodanie parametru EvictionPolicy do polecenia New-AzureRmVmssConfig
* Użycie domyślnej lokalizacji w parametrze DiskFileParameterSet polecenia New-AzureRmVm, jeśli nie określono lokalizacji.
* Naprawienie opisu parametru w poleceniu Save-AzureRmVMImage
* Naprawienie działania polecenia cmdlet Get-AzureRmVMDiskEncryptionStatus w przypadku niektórych scenariuszy powiązanych z pojedynczym przebiegiem

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Naprawienie debugowania, gdy parametr DebugPreference jest ustawiany w wierszu polecenia programu PowerShell
* Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAcl
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.
* Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAclEntry

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermdns"></a>AzureRM.Dns
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurerminsights"></a>AzureRM.Insights
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermmedia"></a>AzureRM.Media
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Dodano przykład dla polecenia Set-AzureRmLocalNetworkGateway
* Dodano przykłady i opisy dla poleceń Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey oraz New-AzureRmVirtualNetworkGatewayConnection
* Dodano przykłady dla poleceń Remove-AzureRmVirtualNetworkGatewayIpConfig i Reset-AzureRmVirtualNetworkGateway
* Dodano przykład dla polecenia Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey
* Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnectionSharedKey
* Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnection
* Ponownie wygenerowano polecenia cmdlet ApplicationSecurityGroup, RouteTable i Usage z użyciem najnowszej wersji generatora
* Poprawiono czytelność komunikatu o błędzie dla polecenia Get-AzureRmVirtualNetworkSubnetConfig podczas próby pobrania podsieci, która nie istnieje

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Dodano filtr zasad do polecenia cmdlet Get-AzureRmRecoveryServicesBackItem. Polecenie zwraca listę elementów kopii zapasowej chronionych przez zasady o danym identyfikatorze.
* Zaktualizowano przestrzeń nazw Microsoft.Azure.Management.RecoveryServices.Backup do wersji 3.0.0-preview.
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.
* Dodano parametr TargetResourceGroupName do polecenia Restore-AzureRmRecoveryServicesBackupItem. Grupa zasobów, do której są przywracane dyski zarządzane. Ma zastosowanie do wykonywania kopii zapasowych maszyn wirtualnych z dyskami zarządzanymi.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermrelay"></a>AzureRM.Relay
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermresources"></a>AzureRM.Resources
* Obsługa wdrażania szablonów w zakresie subskrypcji. Dodanie nowych poleceń cmdlet:
    - New-AzureRmDeployment
    - Get-AzureRmDeployment
    - Test-AzureRmDeployment
    - Remove-AzureRmDeployment
    - Stop-AzureRmDeployment
    - Save-AzureRmDeploymentTemplate
    - Get-AzureRmDeploymentOperation
* Rozwiązanie problemu, w przypadku którego podczas przekazywania kontekstu do polecenia Set-AzureRmResource jest zgłaszany błąd
    - https://github.com/Azure/azure-powershell/issues/5705
* Naprawienie przykładu polecenia New-AzureRmResourceGroupDeployment
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermsql"></a>AzureRM.Sql
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermtags"></a>AzureRM.Tags
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.

## <a name="660---july-2018"></a>6.6.0 — lipiec 2018 r.
#### <a name="general"></a>Ogólne
* Zaktualizowano wszystkie pliki pomocy, aby uwzględniały pełne typy parametrów i poprawne typy wejściowe/wyjściowe.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Zaktualizowano bibliotekę Common.Strategy, aby mogła ona weryfikować, czy bieżąca konfiguracja zasobu jest zgodna z zasobem docelowym.
* Dodano typy ps1xml do biblioteki Common.Storage

#### <a name="azurestorage"></a>Azure.Storage
* Dodano obsługę pobierania kontekstu magazynu z profilu DefaultProfile
* Dodano atrybut Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet.

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
* Set-AzureStorageBlobContent
* Set-AzureStorageFileContent

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
