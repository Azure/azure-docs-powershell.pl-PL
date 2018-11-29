---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 07/26/2017
ms.openlocfilehash: 563f84c3af98de066611dd80102e552b31f12883
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587928"
---
# <a name="release-notes"></a>Informacje o wersji

To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.

## <a name="20170925---version-440"></a>2017.09.25 — wersja 4.4.0
* AnalysisServices
  * Dodano nowe polecenie cmdlet dataplane umożliwiające synchronizację baz danych z wystąpienia do odczytu i zapisu do wystąpień tylko do odczytu
    - Dołączono plik pomocy dla polecenia cmdlet
    - Dodano testy w pamięci i scenariusz testu (tylko na żywo)
  * Usunięto usterki w poleceniu cmdlet Add-AzureAsAccount
* Automatyzacja
  * Naprawiono dokumenty pomocy dla poleceń cmdlet naprawionych w poprzedniej wersji.
  * Dodano 4 nowe polecenia cmdlet w celu obsługi etapowego wprowadzenia konfiguracji węzła DSC.
    - Start-AzureRmAutomationDscNodeConfigurationDeployment
    - Stop-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule
* CognitiveServices
  * Integracja z zestawem SDK zarządzania usługami Cognitive Services w wersji 2.0.0.
  * Polecenie Get-AzureRmCognitiveServicesAccount może teraz poprawnie obsługiwać stronicowanie.
* Wystąpienia obliczeniowe
  * Funkcja polecenia uruchomienia:
    - Nowe polecenie cmdlet: polecenie „Invoke-AzureRmVMRunCommand” wywołuje polecenie uruchomienia na maszynie wirtualnej
    - Nowe polecenie cmdlet: polecenie „Get-AzureRmVMRunCommandDocument” pokazuje dostępne dokumenty polecenia uruchomienia
  * Dodano parametr „StorageAccountType” do polecenia Set-AzureRmDataDisk
  * Obsługa strefy dostępności dla maszyny wirtualnej, zestawu skalowania maszyn wirtualnych oraz dysku
    - Nowy parametr: parametr „Zone” został dodany do poleceń New-AzureRmVM, New-AzureRmVMConfig, New-AzureRmVmssConfig, New-AzureRmDiskConfig
  * Funkcja uaktualnienia stopniowego zestawu skalowania maszyn wirtualnych:
    - Nowe polecenie cmdlet: polecenie „Start-AzureRmVmssRollingOSUpgrade” wywołuje uaktualnienie stopniowe systemu operacyjnego zestawu skalowania maszyn wirtualnych
    - Nowe polecenie cmdlet: „Set-AzureRmVmssRollingUpgradePolicy” ustawia zasady uaktualnienia stopniowego zestawu skalowania maszyn wirtualnych.
    - Nowe polecenie cmdlet: polecenie „Stop-AzureRmVmssRollingUpgrade” anuluje uaktualnienie stopniowe zestawu skalowania maszyn wirtualnych
    - Nowe polecenie cmdlet: polecenie „Get-AzureRmVmssRollingUpgrade” powoduje pokazanie stanu uaktualnienia stopniowego zestawu skalowania maszyn wirtualnych.
  * Parametr przełącznika AssignIdentity został wprowadzony na potrzeby tożsamości przypisanej przez system.
    - Nowy parametr: parametr „AssignIdentity” został dodany do poleceń New-AzureRmVMConfig, New-AzureRmVmssConfig i Update-AzureRmVM
  * Funkcja szyfrowania dysku Vmss:
    - Nowe polecenie cmdlet: polecenie „Set-AzureRmVmssDiskEncryptionExtension” umożliwia szyfrowanie dysków w zestawie skalowania maszyn wirtualnych
    - Nowe polecenie cmdlet: polecenie „Disable-AzureRmVmssDiskEncryption” wyłącza szyfrowanie dysku w zestawie skalowania maszyn wirtualnych
    - Nowe polecenie cmdlet: polecenie „Set-AzureRmVmssDiskEncryptionExtension” powoduje pokazanie stanu szyfrowania dysków w zestawie skalowania maszyn wirtualnych
    - Nowe polecenie cmdlet: polecenie „Get-AzureRmVmssVMDiskEncryptionStatus” powoduje pokazanie stanu szyfrowania dysków maszyn wirtualnych w zestawie skalowania maszyn wirtualnych
* ContainerInstance
  * Dodano polecenia cmdlet programu PowerShell dla wystąpienia kontenera platformy Azure
    - New-AzureRmContainerGroup
    - Get-AzureRmContainerGroup
    - Remove-AzureRmContainerGroup
    - Get-AzureRmContainerInstanceLog
* Insights
  * Nowe polecenie cmdlet Disable-AzureRmActivityLogAlert
    - Nowe polecenie cmdlet do wyłączania istniejącego alertu dziennika aktywności.
    - Opcjonalnie za pomocą tego polecenia cmdlet można też ustawić tagi.
  * Nowe polecenie cmdlet Enable-AzureRmActivityLogAlert
    - Nowe polecenie cmdlet do włączania istniejącego alertu dziennika aktywności.
    - Opcjonalnie za pomocą tego polecenia cmdlet można też ustawić tagi.
  * Nowe polecenie cmdlet Get-AzureRmActivityLogAlert
    - Nowe polecenie cmdlet do pobierania co najmniej jednego alertu dziennika aktywności.
    - Alerty mogą być pobierane według nazw, grup zasobów lub subskrypcji.
  * Nowe polecenie cmdlet New-AzureRmActionGroup
    - Nowe polecenie cmdlet do tworzenia obiektu ActionGroup w pamięci (bez użycia żądań).
  * Nowe polecenie cmdlet New-AzureRmActivityLogAlertCondition
    - Nowe polecenie cmdlet do tworzenia obiektu warunku liścia alertu dziennika aktywności w pamięci (bez użycia żądań).
  * Nowe polecenie cmdlet Set-AzureRmActivityLogAlert
    - Nowe polecenie cmdlet do tworzenia lub aktualizacji alertu dziennika aktywności.
  * Nowe polecenie cmdlet Remove-AzureRmActivityLogAlert
    - Nowe polecenie cmdlet do usuwania jednego alertu dziennika aktywności.
  * Nowe polecenie cmdlet Set-AzureRmActionGroup
    - Nowe polecenie cmdlet do tworzenia nowej grupy akcji lub aktualizacji istniejącej grupy akcji.
  * Nowe polecenie Get-AzureRmActionGroup
    - Nowe polecenie cmdlet do pobierania co najmniej jednej grupy akcji.
    - Grupy akcji mogą być pobierane według nazw, grup zasobów lub subskrypcji.
  * Nowe polecenie cmdlet Remove-AzureRmActionGroup
    - Nowe polecenie cmdlet do usuwania jednej grupy akcji.
  * Nowe polecenie cmdlet New-AzureRmActionGroupReceiver
    - Nowe polecenie cmdlet do tworzenia w pamięci nowego odbiornika grupy akcji.
* KeyVault
  * Nowe/zaktualizowane polecenia cmdlet do obsługi nietrwałego usuwania certyfikatów usługi KeyVault
    * Get-AzureKeyVaultCertificate
    * Remove-AzureKeyVaultCertificate
    * Undo-AzureKeyVaultCertificateRemoval
* Sieć
  * Dodano obsługę dla usług punktu końcowego do podsieci sieci wirtualnej
    - Zaktualizowano polecenie Add-AzureRmVirtualSubnetConfig: dodano parametr opcjonalny -ServiceEndpoint
    - Zaktualizowano polecenie New-AzureRmVirtualSubnetConfig: dodano parametr opcjonalny -ServiceEndpoint
    - Zaktualizowano polecenie Set-AzureRmVirtualSubnetConfig: dodano parametr opcjonalny -ServiceEndpoint
  * Dodano polecenie cmdlet do wyświetlania listy dostępnych usług punktów końcowych w danej lokalizacji
    - Get-AzureRmVirtualNetworkAvailableEndpointService
  * Do następujących poleceń cmdlet dano możliwość konfigurowania zewnętrznego uwierzytelniania P2S opartego na usłudze Radius
    - New-AzureVirtualNetworkGateway
    - Set-AzureVirtualNetworkGateway
    - Set-AzureRmVirtualNetworkGatewayVpnClientConfig
  * Dodano polecenie cmdlet umożliwiające generowanie profilów VpnProfile dla zewnętrznego uwierzytelniania P2S opartego na usłudze Radius
    - New-AzureRmVpnClientConfiguration
    - Get-AzureRmVpnClientConfiguration
  * Dodano obsługę parametru SKU do publicznych adresów IP i modułów równoważenia obciążenia
    - Zaktualizowano polecenie New-AzureRMLoadBalancer: dodano opcjonalny parametr -Sku
    - Zaktualizowano polecenie New-AzureRMPublicIpAddress: dodano opcjonalny parametr -Sku
  * Dodano obsługę polecenia DisableOutboundSNAT do reguł usługi Load Balancer
    - Zaktualizowano polecenie New-AzureRMLoadBalancerRuleConfig: dodano opcjonalny parametr DisableOutboundSNAT
    - Zaktualizowano polecenie Add-AzureRMLoadBalancerRuleConfig: dodano opcjonalny parametr DisableOutboundSNAT
    - Zaktualizowano polecenie Set-AzureRMLoadBalancerRuleConfig: dodano opcjonalny parametr DisableOutboundSNAT
  * Dodano obsługę dla uwierzytelniania P2S protokołu IkeV2
    - Zaktualizowano polecenie New-AzureRmVirtualNetworkGateway: dodano opcjonalny parametr -VpnClientProtocol, który domyślnie przyjmuje wartość [ "SSTP", "IkeV2" ]
    - Zaktualizowano polecenie Set-AzureRmVirtualNetworkGateway: dodano opcjonalny parametr -VpnClientProtocol
  * Dodano obsługę reguł wielowartościowych w regułach zabezpieczeń sieci oraz w obowiązujących regułach zabezpieczeń sieci
    - Zaktualizowano polecenie Add-AzureRmNetworkSecurityRuleConfig: zaktualizowano parametry SourcePortRange, DestinationPortRange i SourceAddressPrefix, aby akceptowały listę ciągów
    - Zaktualizowano polecenie New-AzureRmNetworkSecurityRuleConfig: zaktualizowano parametry SourcePortRange, DestinationPortRange i SourceAddressPrefix, aby akceptowały listę ciągów
    - Zaktualizowano polecenie Set-AzureRmNetworkSecurityRuleConfig: zaktualizowano parametry SourcePortRange, DestinationPortRange i SourceAddressPrefix, aby akceptowały listę ciągów
    - Zaktualizowano polecenie Add-AzureRmNetworkSecurityRuleConfig: zaktualizowano parametry SourcePortRange, DestinationPortRange, SourceAddressPrefix i aby akceptowały listę ciągów
    - Zaktualizowano polecenie New-AzureRmNetworkSecurityGroup: zaktualizowano parametr SecurityRules, aby akceptował parametry SourcePortRange, DestinationPortRange i SourceAddressPrefix, które są listą ciągów w obiekcie PSSecurityRule
    - Zaktualizowano polecenie Get-AzureRmEffectiveNetworkSecurityGroup: dodano parametr TagMap
    - Zaktualizowano polecenie Get-AzureRmEffectiveNetworkSecurityGroup: zaktualizowano zwracany obiekt PSEffectiveSecurityRule o parametry SourcePortRange, DestinationPortRange i SourceAddressPrefix, które są listą ciągów.
  * Dodano obsługę ochrony przed atakami DDoS dla sieci wirtualnych
    - Zaktualizowano polecenie New-AzureRmVirtualNetwork: dodano parametry EnableDDoSProtection i EnableVmProtection przełącznika
    - Dodano właściwości EnableDDoSProtection i EnableVmProtection w obiekcie PSVirtualNetwork
  * Dodano obsługę wewnętrznego modułu równoważenia obciążenia o wysokiej dostępności
    - Zaktualizowano polecenie Add-AzureRmLoadBalancerRuleConfig: dodano All jako akceptowalną wartość parametru Protocol
    - Zaktualizowano polecenie New-AzureRmLoadBalancerRuleConfig: dodano All jako akceptowalną wartość parametru Protocol
    - Zaktualizowano polecenie Set-AzureRmLoadBalancerRuleConfig: dodano All jako akceptowalną wartość parametru Protocol
  * Dodano obsługę grup zabezpieczeń aplikacji
    - Dodano polecenie New-AzureRmApplicationSecurityGroup
    - Dodano polecenie Get-AzureRmApplicationSecurityGroup
    - Dodano polecenie Remove-AzureRmApplicationSecurityGroup
    - Zaktualizowano polecenie New-AzureRmNetworkInterface: dodano parametry opcjonalne ApplicationSecurityGroup i ApplicationSecurityGroupId
    - Zaktualizowano polecenie New-AzureRmNetworkInterfaceIpConfig: dodano parametry opcjonalne ApplicationSecurityGroup i ApplicationSecurityGroupId
    - Zaktualizowano polecenie Add-AzureRmNetworkInterfaceIpConfig: dodano parametry opcjonalne ApplicationSecurityGroup i ApplicationSecurityGroupId
    - Zaktualizowano polecenie Set-AzureRmNetworkInterfaceIpConfig: dodano parametry opcjonalne ApplicationSecurityGroup i ApplicationSecurityGroupId
    - Zaktualizowano polecenie New-AzureRmNetworkSecurityRuleConfig: dodano parametry opcjonalne SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup i DestinationApplicationSecurityGroupId
    - Zaktualizowano polecenie Add-AzureRmNetworkSecurityRuleConfig: dodano parametry opcjonalne SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup i DestinationApplicationSecurityGroupId
    - Zaktualizowano polecenie Set-AzureRmNetworkSecurityRuleConfig: dodano parametry opcjonalne SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup i DestinationApplicationSecurityGroupId
  * Dodano nowe polecenia dla skryptów VpnDeviceConfiguration
    - Get-AzureRmVirtualNetworkGatewaySupportedVpnDevices
    - Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript
* Profil
  * Obsługa uruchamiania zadania dla poleceń cmdlet usługi AzureRm.
    * Dla wszystkich poleceń cmdlet usługi AzureRm dodano parametr -AzureRmContext, który może akceptować kontekst (dane wyjściowe polecenia cmdlet Context).
      - Typowy wzorzec dla zadań z WYŁĄCZONĄ trwałością kontekstu: `Start-Job {param ($context) New-AzureRmVM -AzureRmContext $context [... other parameters]} -ArgumentList (Get-AzureRmContext)`
      - Typowy wzorzec dla zadań z WŁĄCZONĄ trwałością kontekstu:`Start-Job {New-AzureRmVM [... other parameters]}`
  * Trwałe dane logowania między sesjami — nowe polecenia cmdlet:
    - Enable-AzureRmContextAutosave — włączenie trwałości poświadczeń między sesjami.
    - Disable-AzureRmContextAutosave — wyłączenie trwałości poświadczeń między sesjami.
  * Zarządzanie informacjami kontekstu — nowe polecenia cmdlet
    - Select-AzureRmContext — wybór aktywnego nazwanego kontekstu.
    - Rename-AzureRmContext — zmiana nazwy istniejącego kontekstu celem łatwiejszego odwoływania się.
    - Remove-AzureRmContext — usunięcie istniejącego kontekstu.
    - Remove-AzureRmAccount — usunięcie wszystkich poświadczeń, subskrypcji i dzierżaw powiązanych z konkretnym kontem.
  * Zarządzanie informacjami kontekstu — zmiany poleceń cmdlet:
    - Dodano zakres = (Process | CurrentUser) do wszystkich poleceń cmdlet, które zmieniają poświadczenia
    - Get-AzureRmContext — dodano parametr ListAvailable w celu wyświetlania listy wszystkich zapisanych kontekstów
* Zasoby
  * Dodane polecenia cmdlet PolicySetDefinition
    - Polecenie cmdlet New-AzureRmPolicySetDefinition do tworzenia definicji zestawu zasad
    - Polecenie cmdlet Get-AzureRmPolicySetDefinition do wyświetlania listy wszystkich definicji zestawu zasad albo uzyskiwania definicji konkretnego zestawu zasad
    - Polecenie cmdlet Remove-AzureRmPolicySetDefinition do usuwania definicji zestawu zasad
    - Polecenie cmdlet Set-AzureRmPolicySetDefinition do aktualizowania istniejącej definicji zestawu zasad
  * Dodano parametry -PolicySetDefinition, -Sku i -NotScope do poleceń cmdlet New-AzureRmPolicyAssignment i Set-AzureRmPolicyAssignment
  * Dodano obsługę w celu przekazywania adresu URL zasad do poleceń cmdlet New-AzureRmPolicyDefinition i Set-AzureRmPolicyDefinition
  * Dodano parametr -Mode do polecenia cmdlet New-AzureRmPolicyDefinition
  * Dodano obsługę w celu usunięcia właściwości roleassignment za pomocą obiektu PSRoleAssignment
    - W celu usunięcia właściwości roleassignment użytkownicy mogą teraz użyć obiektu inputobject PSRoleassignmnet z poleceniem cmdlet Remove-AzureRMRoleAssignment.
  * Dodane polecenia cmdlet ManagedApplication
    - Polecenie cmdlet New-AzureRmManagedApplication do tworzenia aplikacji zarządzanej
    - Polecenie cmdlet Get-AzureRmManagedApplication do wyświetlania listy wszystkich zarządzanych aplikacji podlegających subskrypcji albo uzyskiwania konkretnej aplikacji zarządzanej
    - Polecenie cmdlet Remove-AzureRmManagedApplication do usuwania aplikacji zarządzanej
    - Polecenie cmdlet Set-AzureRmManagedApplication do aktualizowania istniejącej aplikacji zarządzanej
  * Dodano polecenia cmdlet ManagedApplicationDefinition
    - Polecenie cmdlet New-AzureRmManagedApplicationDefinition do tworzenia definicji aplikacji zarządzanej z użyciem identyfikatora URI pliku zip lub z użyciem plików json mainTemplate i createUiDefinition
    - Polecenie cmdlet Get-AzureRmManagedApplicationDefinition do wyświetlania listy definicji wszystkich aplikacji zarządzanych należących do grupy zasobów albo uzyskiwania definicji konkretnej aplikacji zarządzanej
    - Polecenie cmdlet Remove-AzureRmManagedApplicationDefinition do usuwania definicji aplikacji zarządzanej
    - Polecenie cmdlet Set-AzureRmManagedApplicationDefinition do aktualizowania istniejącej definicji aplikacji zarządzanej
* Sql
  * Dodawanie obsługi dla reguł sieci wirtualnej
    - Dodawane jest polecenie cmdlet Get-AzureRmSqlServerVirtualNetworkRule, które umożliwia uzyskanie reguł sieci wirtualnej według nazwy reguły albo wyświetlenie listy reguł sieci wirtualnej na serwerze Sql platformy Azure.
    - Dodawane jest polecenie cmdlet Set-AzureRmSqlServerVirtualNetworkRule, które zmienia sieć wirtualną wskazywaną przez regułę.
    - Dodawane jest polecenie cmdlet Remove-AzureRmSqlServerVirtualNetworkRule, które usuwa regułę sieci wirtualnej dla serwera Sql platformy Azure.
    - Dodawane jest polecenie cmdlet New-AzureRmSqlServerVirtualNetworkRule, które tworzy nową regułę sieci wirtualnej dla serwera Sql platformy Azure.
* Witryny internetowe
  * Dodano warstwę PremiumV2 dla planów usługi App Service
* Azure.Storage
  * Uaktualniono bibliotekę klienta usługi Azure Storage do wersji 8.4.0 i bibliotekę przenoszenia danych usługi Azure Storage do wersji 0.6.1
  * Dodano obsługę warstwy PremiumPageBlobTier w interfejsie API obiektu blob przekazywania i kopiowania
    - Set-AzureStorageBlobContent
    - Start-AzureStorageBlobCopy
  * Poprawiono format danych wyjściowych konsoli dla obiektów AzureStorageContainer, AzureStorageBlob, AzureStorageQueue, AzureStorageTable
    - Get-AzureStorageContainer
    - Get-AzureStorageBlob
    - Get-AzureStorageQueue
    - Get-AzureStorageTable

## <a name="20170810---version-431"></a>2017.08.10 — wersja 4.3.1
  * Aktualizacja w celu rozwiązania problemu z podpisywaniem zestawów

## <a name="20170807---version-430"></a>2017.08.07 — wersja 4.3.0
* AnalysisServices
  * Usunięto usterkę w poleceniu Set-AzureRmAnalysisServciesServer
    - Jeśli administrator nie został podany, administrator zostanie usunięty.
  * Dodano parametr BackupBlobContainerUri w poleceniach New-AzureRmAnalysisServicesServer i Set-AzureRmAnalysisServicesServer
    - Należy go włączyć, aby ustawić/wyłączyć kontener obiektów blob kopii zapasowej na potrzeby kopii zapasowej i przywracania serwera usług Azure Analysis Services
  * Zaktualizowano wyszukiwanie jednostek SKU w poleceniach New-AzureRmAnalysisServicesServer i Set-AzureRmAnalysisServicesServer
    - Zamieniono zakodowaną jednostkę SKU na wyszukiwanie dynamiczne.
  * Polecenie Add-AzureAnalysisServicesAccount obsługuje logowanie za pomocą jednostki usługi
* Automatyzacja
  * Wprowadzono zmiany w poleceniach cmdlet AutomationDSC* w celu pobierania więcej niż 100 rekordów
  * Rozwiązano problem polegający na tym, że strumienie pełne przestawały działać po wywołaniu niektórych poleceń cmdlet usługi Automation (na przykład Get-AzureRmAutomationVariable, Get-AzureRmAutomationJob).
  * Dodano obsługę wersji kompilacji konfiguracji węzła w poleceniach StartAzureAutomationDscCompilationJob i ImportAzureAutomationDscNodeConfiguration
  * Poprawki usterek dotyczące istniejących problemów — rozwiązano problem z aliasem (#3775), aliasem runOn oraz obsługą obiektów HybridWorker.
* Wystąpienia obliczeniowe
  * Set-AzureRmVMAEMExtension: dodano obsługę nowych rozmiarów dysków w warstwie Premium
  * Set-AzureRmVMAEMExtension: dodano obsługę serii M
  * Dodano parametr ForceUpdateTag do polecenia Add-AzureRmVmssExtension
  * Dodano parametr Primary do polecenia New-AzureRmVmssIpConfig
  * Dodano parametr EnableAcceleratedNetworking do polecenia Add-AzureRmVmssNetworkInterfaceConfig
  * Dodano parametr InstanceId do polecenia Set-AzureRmVmss
  * Udostępniono parametr MaintenanceRedeployStatus w danych wyjściowych polecenia Get-AzureRmVM -Status
  * Udostępniono parametry Restriction i Capability w formacie tabeli polecenia Get-AzureRmComputeResourceSku
* DataLakeStore
  * Rozwiązano problem: https://github.com/Azure/azure-powershell/issues/4323
* EventHub
  * Dodano właściwość ResourceGroup do parametru NamespaceAttributes
    - Do właściwości „ResourceGroup” jest pobierana nazwa grupy zasobów, w której znajduje się przestrzeń nazw
  * Zaktualizowano polecenia cmdlet przez dodanie zestawów parametrów dla przestrzeni nazw i centrów zdarzeń na potrzeby działania reguł autoryzacji
    - Polecenie New-AzureRmEventHubAuthorizationRule — dodaje nową regułę autoryzacji do istniejącej przestrzeni nazw lub centrum zdarzeń.
    - Polecenie Get-AzureRmEventHubAuthorizationRule — pobiera regułę autoryzacji albo listę reguł autoryzacji dla istniejącej przestrzeni nazw lub centrum zdarzeń.
    - Polecenie Set-AzureRmEventHubAuthorizationRule — aktualizuje właściwości istniejącej reguły autoryzacji dla przestrzeni nazw lub centrum zdarzeń.
    - Polecenie Remove-AzureRmEventHubAuthorizationRule — usuwa istniejącą regułę autoryzacji dla istniejącej przestrzeni nazw lub centrum zdarzeń.
    - Polecenie New-AzureRmEventHubKey — generuje nowy klucz podstawowy/pomocniczy dla reguły autoryzacji istniejącej przestrzeni nazw lub centrum zdarzeń.
    - Polecenie Get-AzureRmEventHubKey — pobiera klucz podstawowy/pomocniczy dla reguły autoryzacji istniejącej przestrzeni nazw lub centrum zdarzeń.
* Sieć
    * Dodano obsługę protokołu IPv6 oraz nowy parametr opcjonalny -PeerAddressType
      * New-AzureRmExpressRouteCircuitPeeringConfig:
      * Set-AzureRmExpressRouteCircuitPeeringConfig: dodano obsługę protokołu IPv6. Dodano nowy parametr opcjonalny
      * Remove-AzureRmExpressRouteCircuitPeeringConfig: dodano obsługę protokołu IPv6. Dodano nowy parametr opcjonalny
    * Oznaczono parametr -ProbeEnabled jako przestarzały
      - Add-AzureRmApplicationGatewayBackendHttpSettings
      - New-AzureRmApplicationGatewayBackendHttpSettings
      - Set-AzureRmApplicationGatewayBackendHttpSettings
* Profil
    * Zbieranie danych zostało domyślnie włączone. Firma Microsoft zbiera dane użycia, aby ulepszyć środowisko użytkownika. Dane są anonimowe i nie zawierają wartości argumentów wiersza polecenia.
      - Do wyłączania tej funkcji służy polecenie cmdlet Disable-AzureRmDataCollection
      - Do włączania tej funkcji służy polecenie cmdlet Enable-AzureRmDataCollection
* Zasoby
    * Dodano obsługę weryfikacji zakresów dla następujących poleceń cmdlet definiowania ról i przypisywania ról przed wysłaniem żądania do usługi ARM
      - Get-AzureRMRoleAssignment
      - New-AzureRMRoleAssignment
      - Remove-AzureRMRoleAssignment
      - Get-AzureRMRoleDefinition
      - New-AzureRMRoleDefinition
      - Remove-AzureRMRoleDefinition
      - Set-AzureRMRoleDefinition
* ServiceBus
  * Dodano poniższe nowe polecenia cmdlet dotyczące reguł autoryzacji dla przestrzeni nazw, kolejki i tematu. Wykonywane są operacje reguł autoryzacji zgodnie z zestawem parametrów.
    - Polecenie New-AzureRmServiceBusAuthorizationRule — dodaje nową regułę autoryzacji do istniejącej przestrzeni nazw, kolejki lub tematu magistrali usług.
    - Polecenie Get-AzureRmServiceBusAuthorizationRule — pobiera regułę autoryzacji albo listę reguł autoryzacji dla istniejącej przestrzeni nazw, kolejki lub tematu magistrali usług.
    - Polecenie Set-AzureRmServiceBusAuthorizationRule — aktualizuje właściwości istniejącej reguły autoryzacji dla przestrzeni nazw, kolejki lub tematu magistrali usług.
    - Polecenie New-AzureRmServiceBusKey — generuje nowy klucz podstawowy/pomocniczy dla reguły autoryzacji istniejącej przestrzeni nazw, kolejki lub tematu magistrali usług.
    - Polecenie Get-AzureRmServiceBusKey — pobiera klucz podstawowy/pomocniczy dla reguły autoryzacji istniejącej przestrzeni nazw, kolejki lub tematu magistrali usług.
    - Polecenie Remove-AzureRmServiceBusNamespaceAuthorizationRule — usuwa istniejącą regułę autoryzacji przestrzeni nazw, kolejki lub tematu magistrali usług.
  * Dodano właściwość grupy zasobów do atrybutów obszaru nazw

* Sql
    * Zaktualizowano polecenie Set-AzureRmSqlServerTransparentDataEncryptionProtector w celu wyświetlania ostrzeżenia i wymagania potwierdzenia, jeśli jako typ funkcji ochrony szyfrowania zostanie ustawiona wartość AzureKeyVault
    * Dodano nowe/zaktualizowane polecenia cmdlet dla ustawień inspekcji
      - Polecenie cmdlet Get-AzureRmSqlDatabaseAuditing, które pobiera ustawienia inspekcji bazy danych Azure SQL.
      - Polecenie cmdlet Get-AzureRmSqlServerAuditing, które pobiera ustawienia inspekcji serwera Azure SQL.
      - Polecenie cmdlet Set-AzureRmSqlDatabaseAuditing, które zmienia ustawienia inspekcji bazy danych Azure SQL.
      - Polecenie cmdlet Set-AzureRmSqlServerAuditing, które zmienia ustawienia inspekcji serwera Azure SQL.
    * Wycofano istniejące polecenia cmdlet zasad inspekcji
      - Get-AzureRmSqlDatabaseAuditingPolicy
      - Get-AzureRmSqlServerAuditingPolicy
      - Set-AzureRmSqlDatabaseAuditingPolicy
      - Set-AzureRmSqlServerAuditingPolicy
      - Use-AzureRmSqlServerAuditingPolicy
      - Remove-AzureRmSqlDatabaseAuditing
      - Remove-AzureRmSqlServerAuditing
    * Podczas analizowania plików schematu dla polecenia Update-AzureRmSqlSyncGroup jest teraz uwzględniana wielkość liter.
* Magazyn
    * Dodano obsługę reguł sieci do poleceń cmdlet konta magazynu trybu zasobu
      - New-AzureRmStorageAccount
      - Set-AzureRmStorageAccount
      - Get-AzureRmStorageAccountNetworkRuleSet
      - Update-AzureRmStorageAccountNetworkRuleSet
      - Add-AzureRmStorageAccountNetworkRule
      - Remove-AzureRmStorageAccountNetworkRule

## <a name="20170717---version-421"></a>2017.07.17 — wersja 4.2.1
* Wystąpienia obliczeniowe
  - Rozwiązano problem z poleceniami cmdlet służącymi do tworzenia oraz aktualizowania dysku maszyny wirtualnej i migawki dysku maszyny wirtualnej (link) [<https://github.com/azure/azure-powershell/issues/4309>]
    - New-AzureRmDisk
    - New-AzureRmSnapshot
    - Update-AzureRmDisk
    - Update-AzureRmSnapshot
* Profil
  - Rozwiązano problem z uwierzytelnianiem użytkowników nieinterakcyjnych we frontonie RDFE (link) [<https://github.com/Azure/azure-powershell/issues/4299>]

* ServiceManagement
  - Rozwiązano problem z uwierzytelnianiem użytkowników nieinterakcyjnych (link) [<https://github.com/Azure/azure-powershell/issues/4299>]

## <a name="2017711---version-420"></a>2017.7.11 — wersja 4.2.0
* AnalysisServices
    * Dodaj nowy interfejs API płaszczyzny danych
        - Wprowadzono interfejs API umożliwiający pobranie dziennika serwera usług AS, Export-AzureAnalysisServicesInstanceLog
* Automatyzacja
    * Odpowiednie ustawienie wartości strefy czasowej harmonogramu tygodniowego i miesięcznego dla polecenia New-AzureRmAutomationSchedule
        - Więcej informacji można znaleźć w ramach następującego problemu: https://github.com/Azure/azure-powershell/issues/3043
* AzureBatch
    - Dodano nowe polecenie cmdlet Get-AzureBatchJobPreparationAndReleaseTaskStatu.
    - Dodano początek i koniec zakresu bajtów do parametrów polecenia Get-AzureBatchNodeFileContent.
* CognitiveServices
    * Integracja z zestawem SDK zarządzania usługami Cognitive Services w wersji 1.0.0.
    * Usunięto błąd związany ze sprawdzaniem długości nazwy konta.
* Wystąpienia obliczeniowe
    * Obsługa typu konta magazynu w przypadku dysku obrazu:
        - Dodano parametr „StorageAccountType” do poleceń Set-AzureRmImageOsDisk i Add-AzureRmImageDataDisk
    * Funkcja PrivateIP i PublicIP w konfiguracji adresu IP zestawu skalowania maszyn wirtualnych:
        - Dodano nazwy „PrivateIPAddressVersion”, „PublicIPAddressConfigurationName”, „PublicIPAddressConfigurationIdleTimeoutInMinutes” i „DnsSetting” do polecenia New-AzureRmVmssIpConfig
        - Do polecenia New-AzureRmVmssIpConfig dodano parametr „PrivateIPAddressVersion” umożliwiający określenie adresu IPv4 lub IPv6
    * Funkcja konserwacji w zakresie wydajności:
        - Dodano parametr przełącznika „PerformMaintenance” do polecenia Restart-AzureRmVM.
        - Użycie polecenia Get-AzureRmVM -Status powoduje wyświetlenie informacji o konserwacji w zakresie wydajności danej maszyny wirtualnej
    * Funkcja tożsamości maszyny wirtualnej:
        - Dodano parametr „IdentityType” do poleceń New-AzureRmVMConfig i UpdateAzureRmVM
        - Użycie polecenia Get-AzureRmVM powoduje wyświetlenie informacji o tożsamości danej maszyny wirtualnej
    * Funkcja tożsamości zestawu skalowania maszyn wirtualnych:
        - Dodano parametr „IdentityType” do polecenia New-AzureRmVmssConfig
        - Użycie polecenia Get-AzureRmVmss powoduje wyświetlenie informacji o tożsamości danego zestawu skalowania maszyn wirtualnych
    * Funkcja diagnostyki rozruchu zestawu skalowania maszyn wirtualnych:
        - Nowe polecenie cmdlet umożliwiające ustawienie diagnostyki rozruchu obiektu zestawu skalowania maszyny wirtualnej: Set-AzureRmVmssBootDiagnostics
        - Dodano parametr „BootDiagnostic” do polecenia New-AzureRmVmssConfig
    * Funkcja LicenseType zestawu skalowania maszyn wirtualnych:
        - Dodano parametr „LicenseType” do polecenia New-AzureRmVmssConfig
    * Obsługa parametru RecoveryPolicyMode:
        - Dodano parametr „RecoveryPolicyMode” do polecenia New-AzureRmVmssConfig
    * Funkcja obliczania jednostki SKU zasobu:
        - Nowe polecenie cmdlet „Get-AzureRmComputeResourceSku” umożliwiające wyświetlenie listy wszystkich obliczonych jednostek SKU zasobów
* DataFactories
    * Wycofanie polecenia New-AzureRmDataFactoryGatewayKey
    * Wprowadzenie funkcji klucza uwierzytelniania bramy przez dodanie poleceń New-AzureRmDataFactoryGatewayAuthKey i Get-AzureRmDataFactoryGatewayAuthKey
* DataLakeAnalytics
    * Dodanie obsługi operacji CRUD zasad obliczania przy użyciu następujących poleceń:
        - New-AzureRMDataLakeAnalyticsComputePolicy
        - Get-AzureRMDataLakeAnalyticsComputePolicy
        - Remove-AzureRMDataLakeAnalyticsComputePolicy
        - Update-AzureRMDataLakeAnalyticsComputePolicy
    * Dodanie obsługi metadanych relacji zadań w celu ułatwienia wykonywania zadań cyklicznych i potoków zadań. Zaktualizowano lub dodano następujące polecenia:
        - Submit-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJobRecurrence
        - Get-AzureRMDataLakeAnalyticsJobPipeline
    * Zaktualizowano odbiorców tokenu interfejsów API zadań i wykazów w celu używania poprawnych odbiorców usługi Data Lake zamiast odbiorców zasobów platformy Azure.
* DataLakeStore
    * Dodano obsługę wymiany kluczy magazynu kluczy zarządzanych przez użytkowników w poleceniu cmdlet Set-AzureRMDataLakeStoreAccount
    * Dodano aktualizację ułatwiającą pracę, która powoduje automatyczne wyzwolenie elementu `enableKeyVault` w przypadku dodania klucza magazynu kluczy zarządzanego przez użytkownika lub wymiany klucza.
    * Zaktualizowano odbiorców tokenu interfejsów API zadań i wykazów w celu używania poprawnych odbiorców usługi Data Lake zamiast odbiorców zasobów platformy Azure.
    * Usunięto błąd ograniczający rozmiar plików tworzonych/dołączanych przy użyciu następujących poleceń cmdlet:
        - New-AzureRmDataLakeStoreItem
        - Add-AzureRmDataLakeStoreItemContent
* Dns
    * Usunięcie błędu w scenariuszu potoku dotyczącego polecenia Get-AzureRmDnsZone
        - Więcej informacji można znaleźć tutaj: https://github.com/Azure/azure-powershell/issues/4203
* HDInsight
    * Dodano obsługę włączania/wyłączania pakietu Operations Management Suite (OMS)
    * Nowe polecenia cmdlet
        - Enable-AzureRmHDInsightOperationsManagementSuite
        - Disable-AzureRmHDInsightOperationsManagementSuite
        - Get-AzureRmHDInsightOperationsManagementSuite
    * Dodanie do polecenia Add-AzureRmHDInsightConfigValues nowych parametrów umożliwiających ustawianie niestandardowych konfiguracji aparatu Spark
        - Parametry SparkDefaults i SparkThriftConf dla aparatu Spark 1.6
        - Parametry Spark2Defaults i Spark2ThriftConf dla aparatu Spark 2.0
* Insights
    * Problem 4215 (żądanie zmiany) powodujący usunięcie 15-dniowego limitu przedziału czasu polecenia cmdlet Get-AzureRmLog. Wprowadzono również drobne zmiany w nazwach testów jednostkowych.
    * Rozwiązano problem 3957 związany z poleceniem Get-AzureRmLog
        - Problem 1: zaplecze zwraca rekordy na stronach zawierających po 200 rekordów połączonych z następną stroną przez token kontynuacji. Polecenie cmdlet zwracało u klientów tylko 200 rekordów w sytuacji, gdy klienci wiedzieli, że istnieje więcej rekordów. Działo się tak niezależnie od ustawionej wartości elementu MaxEvents, gdy wartość nie była mniejsza niż 200.
        - Problem 2: dokumentacja zawierała niepoprawne dane dotyczące tego polecenia cmdlet, np. domyślny przedział czasu równy 1 godz.
        - Poprawka 1: polecenie cmdlet występuje teraz po tokenie kontynuacji zwróconym przez zaplecze do czasu osiągnięcia wartości elementu MaxEvents lub końca zestawu.<br>Wartość domyślna elementu MaxEvents to 1000, a wartość maksymalna to 100000. Każda wartość elementu MaxEvents mniejsza niż 1 jest ignorowana i zamiast niej jest używana wartość domyślna. Te wartości i zachowanie nie uległy zmianie. Są one teraz poprawnie udokumentowane.<br>Dodano alias elementu MaxEvents (MaxRecords), ponieważ nazwa polecenia cmdlet nie zawiera już informacji o zdarzeniach (zawiera tylko informacje o dziennikach).
        - Poprawka 2: dokumentacja zawiera poprawne i bardziej szczegółowe informacje — nowy alias, poprawny przedział czasu oraz poprawną wartość domyślną, minimalną i maksymalną.
* KeyVault
    * Usunięcie adresu e-mail z zapytania katalogu w przypadku określenia parametru -UserPrincipalName w poleceniach cmdlet Set-AzureRMKeyVaultAccessPolicy i Remove-AzureRMKeyVaultAccessPolicy.
      - Oba polecenia cmdlet zawierają już parametr -EmailAddress, którego może użyć zamiast parametru -UserPrincipalName podczas wykonywania zapytania dotyczącego adresu e-mail.  Jeśli w katalogu istnieje więcej niż jeden zgodny adres e-mail, polecenie cmdlet kończy się niepowodzeniem.
* Sieć
    * New-AzureRmIpsecPolicy: parametry SALifeTimeSeconds i SADataSizeKilobytes nie są już obowiązkowe
        - Wartość domyślna parametru SALifeTimeSeconds to 27000 sekund
        - Wartość domyślna parametru SADataSizeKilobytes to 102400000 KB
    * Dodano obsługę niestandardowej konfiguracji pakietu szyfrowania przy użyciu zasad SSL przez wyświetlenie listy wszystkich opcji interfejsu API protokołu SSL w usłudze Application Gateway
        - Dodano opcjonalne parametry -PolicyType, -PolicyName, -MinProtocolVersion i -Ciphersuite
            - Add-AzureRmApplicationGatewaySslPolicy
            - New-AzureRmApplicationGatewaySslPolicy
            - Set-AzureRmApplicationGatewaySslPolicy
        - Dodano polecenie Get-AzureRmApplicationGatewayAvailableSslOptions (alias: List-AzureRmApplicationGatewayAvailableSslOptions)
        - Dodano polecenie Get-AzureRmApplicationGatewaySslPredefinedPolicy (alias: List-AzureRmApplicationGatewaySslPredefinedPolicy)
    * Dodano obsługę przekierowywania w usłudze Application Gateway
        - Dodano polecenie Add-AzureRmApplicationGatewayRedirectConfiguration
        - Dodano polecenie Get-AzureRmApplicationGatewayRedirectConfiguration
        - Dodano polecenie New-AzureRmApplicationGatewayRedirectConfiguration
        - Dodano polecenie Remove-AzureRmApplicationGatewayRedirectConfiguration
        - Dodano polecenie Set-AzureRmApplicationGatewayRedirectConfiguration
        - Dodano opcjonalny parametr -RedirectConfiguration
            - Add-AzureRmApplicationGatewayRequestRoutingRule
            - New-AzureRmApplicationGatewayRequestRoutingRule
            - Set-AzureRmApplicationGatewayRequestRoutingRule
        - Dodano opcjonalny parametr -DefaultRedirectConfiguration
            - Add-AzureRmApplicationGatewayUrlPathMapConfig
            - New-AzureRmApplicationGatewayUrlPathMapConfig
            - Set-AzureRmApplicationGatewayUrlPathMapConfig
        - Dodano opcjonalny parametr -RedirectConfiguration
            - Add-AzureRmApplicationGatewayPathRuleConfig
            - New-AzureRmApplicationGatewayPathRuleConfig
            - Set-AzureRmApplicationGatewayPathRuleConfig
        - Dodano opcjonalny parametr -RedirectConfigurations
            - New-AzureRmApplicationGateway
            - Set-AzureRmApplicationGateway
    * Dodano obsługę witryn internetowych platformy Azure w usłudze Application Gateway
        - Dodano polecenie New-AzureRmApplicationGatewayProbeHealthResponseMatch
        - Dodano opcjonalne parametry -PickHostNameFromBackendHttpSettings, -MinServers i -Match
            - Add-AzureRmApplicationGatewayProbeConfig
            - New-AzureRmApplicationGatewayProbeConfig
            - Set-AzureRmApplicationGatewayProbeConfig
        - Dodano opcjonalne parametry -PickHostNameFromBackendAddress, -AffinityCookieName, -ProbeEnabled i -Path
            - Add-AzureRmApplicationGatewayBackendHttpSettings
            - New-AzureRmApplicationGatewayBackendHttpSettings
            - Set-AzureRmApplicationGatewayBackendHttpSettings
    * Aktualizacja polecenia Get-AzureRmPublicIPaddress w celu pobierania zasobów publicipaddress tworzonych przy użyciu zestawu skalowania maszyn wirtualnych
    * Dodano polecenie cmdlet umożliwiające pobranie bieżących danych użycia sieci wirtualnej
        - Get-AzureRmVirtualNetworkUsageList
* Profil
    * Usunięto błąd występujący w przypadku używania polecenia Import-AzureRmContext lub Save-AzureRmContext
        - Więcej informacji można znaleźć w ramach następującego problemu: https://github.com/Azure/azure-powershell/issues/3954
* RecoveryServices.SiteRecovery
    * Wprowadzono nowy moduł operacji usługi Azure Site Recovery.
        - Wszystkie polecenia cmdlet rozpoczynają się od ciągu AzureRmRecoveryServicesAsr*
* Sql
    * Dodanie poleceń cmdlet programu PowerShell synchronizacji danych do elementu AzureRM.Sql
    * Zaktualizowano polecenia cmdlet AzureRmSqlServer w celu używania nowej wersji interfejsu API REST, która pozwala uniknąć przekroczeń limitu czasu podczas tworzenia serwera.
    * Wycofano polecenia cmdlet uaktualniania serwera, ponieważ stara wersja serwera (2.0) już nie istnieje.
    * Dodanie nowego opcjonalnego parametru przełącznika „AssignIdentity” do poleceń cmdlet New-AzureRmSqlServer i Set-AzureRmSqlServer w celu obsługi aprowizacji tożsamości zasobu serwera SQL
    * Parametr ResourceGroupName jest teraz opcjonalny w przypadku polecenia Get-AzureRmSqlServer
        - Więcej informacji można znaleźć w ramach następującego problemu: https://github.com/Azure/azure-powershell/issues/635
* ServiceManagement dla usługi ExpressRoute:
    * Zaktualizowano polecenie cmdlet New-AzureBgpPeering przez dodanie następujących nowych opcji:
        - PeerAddressType: można określić wartość „IPv4” lub „IPv6” w celu utworzenia komunikacji równorzędnej BGP odpowiedniego typu rodziny adresów
    * Zaktualizowano polecenie cmdlet Set-AzureBgpPeering przez dodanie następujących nowych opcji:
        - PeerAddressType: można określić wartość „IPv4” lub „IPv6” w celu zaktualizowania komunikacji równorzędnej BGP odpowiedniego typu rodziny adresów
    * Zaktualizowano polecenie cmdlet Remove-AzureBgpPeering przez dodanie następujących nowych opcji:
        - PeerAddressType: można określić wartość „IPv4”, „IPv6” lub „Wszystkie” w celu usunięcia komunikacji równorzędnej BGP odpowiedniego typu rodziny adresów albo wszystkich typów

## <a name="20170607---version-410"></a>2017.06.07 — wersja 4.1.0
* AnalysisServices
    * Dodano nowe jednostki SKU: B1, B2 i S0
    * Dodano obsługę skalowania w górę i w dół
* CognitiveServices
    * Aktualizacja szczegółów umów licencyjnych wyświetlanych podczas tworzenia zasobów usług Cognitive Services
* Wystąpienia obliczeniowe
    * Usunięcie błędu związanego z poleceniem Test-AzureRmVMAEMExtension w przypadku maszyn wirtualnych z wieloma dyskami Managed Disks
    * Zaktualizowano polecenie Set-AzureRmVMAEMExtension: dodanie informacji dotyczących buforowania w przypadku dysków Managed Disks w wersji Premium
    * Add-AzureRmVhd: zwiększono limit rozmiaru wirtualnego dysku twardego do 4 TB.
    * Stop-AzureRmVM: doprecyzowanie dokumentacji dotyczącej parametru STayProvisioned
    * New-AzureRmDiskUpdateConfig
      * Wycofano parametry CreateOption, StorageAccountId, ImageReference, SourceUri i SourceResourceId
    * Set-AzureRmDiskUpdateImageReference: wycofano polecenie cmdlet
    * New-AzureRmSnapshotUpdateConfig
      * Wycofano parametry CreateOption, StorageAccountId, ImageReference, SourceUri i SourceResourceId
    * Set-AzureRmSnapshotUpdateImageReference: wycofano polecenie cmdlet
* DataLakeStore
    * Enable-AzureRmDataLakeStoreKeyVault (Enable-AdlStoreKeyVault)
      * Włączenie szyfrowania zarządzanego przez magazyn kluczy w przypadku magazynu usługi DataLake
* DevTestLabs
    * Aktualizacja poleceń cmdlet w celu współdziałania z bieżącą i zaktualizowaną wersją interfejsu API usługi DevTest Labs.
* IotHub
    * Dodanie obsługi routingu w przypadku poleceń cmdlet usługi IoTHub
* KeyVault
  * Nowe polecenia cmdlet umożliwiające obsługę kluczy kont magazynu zarządzanych przez magazyn kluczy
    * Get-AzureKeyVaultManagedStorageAccount
    * Add-AzureKeyVaultManagedStorageAccount
    * Remove-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccountKey
    * Get-AzureKeyVaultManagedStorageSasDefinition
    * Set-AzureKeyVaultManagedStorageSasDefinition
    * Remove-AzureKeyVaultManagedStorageSasDefinition
* Sieć
    * Get-AzureRmNetworkUsage: nowe polecenie cmdlet umożliwiające wyświetlenie szczegółowych informacji dotyczących użycia i pojemności
    * Dodano nowe opcje GatewaySku dla elementów VirtualNetworkGateway
        * VpnGw1, VpnGw2 i VpnGw3 to nowe jednostki SKU dodane do bram sieci VPN
    * Set-AzureRmNetworkWatcherConfigFlowLog
      * Przykłady pomocy w rozwiązaniu problemu
* NotificationHubs
    * Przezroczysta aktualizacja poleceń cmdlet usługi NotificationHubs pod kątem nowego interfejsu API
* Profil
    * Resolve-AzureRmError
      * Nowe polecenie cmdlet umożliwiające wyświetlenie szczegółów błędów i wyjątków zgłaszanych przez polecenia cmdlet, łącznie z danymi żądań/odpowiedzi serwera
    * Send-Feedback
      * Włączono wysyłanie opinii bez potrzeby logowania
    * Get-AzureRmSubscription
      * Usunięcie błędu występującego podczas pobierania subskrypcji dostawcy CSP
* Zasoby
    * Rozwiązano problem polegający na tym, że polecenie Get-AzureRMRoleAssignment powodowało wystąpienie nieprawidłowego żądania, gdy liczba przypisań ról była większa niż 1000
        * Użytkownicy mogą teraz używać polecenia Get-AzureRMRoleAssignment nawet wtedy, gdy zwrócona liczba przypisań ról jest większa niż 1000
* Sql
    * Restore-AzureRmSqlDatabase: aktualizacja przykładu dokumentacji
* Magazyn
    * Dodanie obsługi ustawienia AssignIdentity do poleceń cmdlet konta magazynu trybu zasobu
        * New-AzureRmStorageAccount
        * Set-AzureRmStorageAccount
    * Dodanie obsługi kluczy klientów do poleceń cmdlet konta magazynu trybu zasobu
        * Set-AzureRmStorageAccount
        * New-AzureRmStorageAccountEncryptionKeySource
* TrafficManager

    * Nowe ustawienia monitora „MonitorIntervalInSeconds”, „MonitorTimeoutInSeconds” i „MonitorToleratedNumberOfFailures”
    * Nowy protokół monitora „TCP”
* ServiceManagement
    * Add-AzureVhd: zwiększono limit rozmiaru wirtualnego dysku twardego do 4 TB.
    * New-AzureBGPPeering: obsługa elementu LegacyMode
* Azure.Storage
    * Aktualizacja pomocy dotyczącej parametrów, które akceptują symbole wieloznaczne i aktualizacja typu StorageContext

## <a name="20170523---version-402"></a>2017.05.23 — wersja 4.0.2
* Profil
    * Add-AzureRmAccount
      * Dodano alias parametru `-EnvironmentName` na potrzeby zachowania zgodności z poprzednimi wersjami 2.x elementu AzureRM.profile

## <a name="20170512---version-401"></a>2017.05.12 — wersja 4.0.1
 * Rozwiązano problem z poleceniem New-AzureStorageContext w scenariuszach w trybie offline: https://github.com/Azure/azure-powershell/issues/3939

## <a name="20170510---version-400"></a>2017.05.10 — wersja 4.0.0


* Niniejsza wersja zawiera istotne zmiany. Aby uzyskać szczegółowe informacje o zmianach i ich wpływie na istniejące skrypty, zobacz [przewodnik po migracji](https://aka.ms/azps-migration-guide).
* ApiManagement
  - Dodano obsługę konfigurowania grup zewnętrznych w poleceniu New-AzureRmApiManagementGroup.
* Rozliczenia
  - Nowe polecenie cmdlet Get-AzureRmBillingPeriod
    + Polecenie cmdlet do pobierania okresów rozliczeniowych subskrypcji platformy Azure.
  - Aktualizacja polecenia cmdlet Get-AzureRmBillingInvoice
  - Nowa właściwość BillingPeriodNames
  - Dane wyjściowe w widoku listy
* Wystąpienia obliczeniowe
  - Zaktualizowano polecenia cmdlet Set-AzureRmVMAEMExtension i Test-AzureRmVMAEMExtension o obsługę dysków zarządzanych w warstwie Premium
  - Ustawienia szyfrowania kopii zapasowych maszyn wirtualnych IaaS oraz przywracanie po awarii
  - Zmieniono nazwę opcji ChefServiceInterval na ChefDaemonInterval. Stara opcja będzie jednak nadal działać.
  - Usunięto zduplikowane właściwości DataDiskNames i NetworkInterfaceIDs z obiektu maszyny wirtualnej w programie PowerShell.
  - Zmieniono parametry DataDiskNames i NetworkInterfaceIDs odpowiednio w poleceniach Remove-AzureRmVMDataDisk i Remove-AzureRmVMNetworkInterface na opcjonalne.
  - Naprawiono problem z potokami poleceń cmdlet zawierających wartość Get, który występował, gdy polecenia cmdlet zwracały obiekt listy.
  - Zmieniono nazwy poleceń cmdlet powodujących konflikt z poleceniami cmdlet frontonu RedDog. Aby uzyskać więcej informacji, zobacz problem https://github.com/Azure/azure-powershell/issues/2917
    + Zmieniono nazwę polecenia `New-AzureVMSqlServerAutoBackupConfig` na `New-AzureRmVMSqlServerAutoBackupConfig`
    + Zmieniono nazwę polecenia `New-AzureVMSqlServerAutoPatchingConfig` na `New-AzureRmVMSqlServerAutoPatchingConfig`
    + Zmieniono nazwę polecenia `New-AzureVMSqlServerKeyVaultCredentialConfig` na `New-AzureRmVMSqlServerKeyVaultCredentialConfig`
* Zużycie
  - Dodano nowe polecenie cmdlet Get-AzureRmConsumptionUsageDetail
    + Polecenie cmdlet do pobierania szczegółów użycia w ramach subskrypcji.
* ContainerRegistry
  - Dodano polecenia cmdlet programu PowerShell dla usługi Azure Container Registry
    + New-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistry
    + Update-AzureRmContainerRegistry
    + Remove-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistryCredential
    + Update-AzureRmContainerRegistryCredential
    + Test-AzureRmContainerRegistryNameAvailability
* DataLakeAnalytics
  - Dodano obsługę pobierania i wyświetlania listy pakietu wykazu
  - Dodano obsługę wyświetlania listy poniższych elementów wykazu z głębszych elementów nadrzędnych:
    + Tabela
    + Funkcja TVF
    + Widok
    + Statystyki
* DataLakeStore
  - Dla poleceń `Import-AzureRMDataLakeStoreItem` i `Export-AzureRMDataLakeStoreItem` domyślnie wyłączono rejestrowanie śledzenia, aby poprawić wydajność. Aby włączyć rejestrowanie śledzenia, należy użyć parametrów `-DiagnosticLogLevel` i `-DiagnosticLogPath`
  - Naprawiono usterkę, która czasami powodowała awarię programu PowerShell podczas przekazywania wielu małych plików do usługi ADLS.
* EventHub
  - Poprawka usterki:
    + Poprawka błędu dotyczącego polecenia cmdlet Set-AzureRmEventHubNamespace: element „Tier” nie może mieć wartości null, gdy powinien mieć wartość „SkuName”
    + Set-AzureRmEventHub: poprawka dla błędu „Odwołanie do obiektu nie zostało ustawione na wystąpienie obiektu” wyświetlanego podczas aktualizowania usługi EventHub
* Insights
  - Add-AzureRm*AlertRule
    + Zwraca pojedynczy obiekt: newResource, statusCode, requestId
  - Get-AzureRmAlertRule
    + Dane wyjściowe są teraz wyliczane, a nie traktowane jako pojedynczy obiekt. Ich typ nie uległ zmianie. Nadal jest to lista.
  - Remove-AzureRmAlertRule
    + Po kodzie stanu zwróconym przez żądanie jest wyświetlana wartość „statusCode”. Wcześniej był to zawsze ciąg „OK”.
  - Add-AzureRmAutoscaleSetting
    + Zwraca teraz pojedynczy obiekt (a nie listę, jak wcześniej) zawierający wartości statusCode, requestId oraz nowo utworzony/zaktualizowany zasób.
    + Po stanie zwróconym przez żądanie jest wyświetlany kod stanu. Wcześniej był to zawsze ciąg „OK”.
  - New-AzureRmAutoscaleRule
    + Parametr ScaleActionType został rozszerzony. Otrzymuje teraz następujące wartości: ChangeCount, PercentChangeCount, ExactCount.
  - Remove-AzureRmAutoscaleSetting
    + W danych wyjściowych po wartości statusCode zwróconej przez żądanie jest wyświetlany ciąg statusCode. Wcześniej był to zawsze ciąg OK.
  - Get-AzureRMLogProfile
    + Dane wyjściowe są teraz wyliczane. Wcześniej były traktowane jako pojedynczy obiekt. Typ danych wyjściowych to nadal lista, tak jak wcześniej.
  - Remove-AzureRmLogProfile
    + Zaimplementowano parametr PassThru.
  - Interfejs API metryk
    + Zestaw SDK pobiera teraz metryki z usługi MDM.
  - Get-AzureRmMetricDefinition
    + Dane wyjściowe to nadal lista, ale struktura tej listy uległa zmianie.
  - Get-AzureRmMetric
    + Wywołanie uległo zmianie. Oto nowa składnia: Get-AzureRmMetric ResourceId [Nazwy_metryk [Ziarno_czasu] [Typ_agregacji] [Czas_rozpoczęcia] [Czas_zakończenia]] [Szczegółowe_dane_wyjściowe]
    + Dane wyjściowe to lista, a struktura jej elementów uległa zmianie.
* KeyVault
  - Dodano obsługę tworzenia/przywracania kopii zapasowych wpisów tajnych usługi KeyVault
    + Kopie zapasowe wpisów tajnych można tworzyć i przywracać, co zapewnia zgodność z funkcjami obecnie obsługiwanymi w przypadku kluczy

  - Polecenia cmdlet kopii zapasowych dla kluczy i wpisów tajnych akceptują teraz odpowiedni obiekt jako parametr wejściowy
    + Obiekt wywołujący może tworzyć łańcuchy operacji pobierania i tworzenia kopii zapasowych: Get-AzureKeyVaultKey -VaultName mójMagazyn -Name mójKlucz | Backup-AzureKeyVaultKey

  - Polecenia cmdlet kopii zapasowych obsługują teraz przełącznik -Force umożliwiający zastąpienie istniejącego pliku
    + Pamiętaj, że próba zastąpienia istniejącego pliku nie będzie już powodować zgłoszenia błędu. Zamiast tego będzie wyświetlany monit o wybranie działania.
* LogicApp
  - Nowe parametry poleceń cmdlet odzyskiwania po awarii numeru kontrolnego wymiany:
    + Opcjonalny parametr -AgreementType („X12” lub „Edifact”) umożliwiający określenie odpowiednich numerów kontrolnych
* MachineLearning
  - Korzystanie z nowej wersji zestawu .NET SDK usługi Azure Machine Learning i dodanie nowego polecenia cmdlet
    + Add-AzureRmMlWebServiceRegionalProperty
  - Niewielkie poprawki tekstu pomocy.
* Sieć
  - Dodano polecenie cmdlet Test-AzureRmNetworkWatcherConnectivity
    + Zwraca informacje o łączności dla określonej źródłowej maszyny wirtualnej i określonego miejsca docelowego
    + Jeśli nie można ustanowić łączności między miejscem źródłowym i docelowym, polecenie cmdlet zwraca szczegółowe informacje dotyczące problemu
* Profil
  - Dodano polecenie cmdlet „Send-Feedback”, które pozwala użytkownikowi na zainicjowanie zestawu monitów w celu wysłania opinii do zespołu programu Azure PowerShell.
  - Następujące aliasy zostały usunięte, ponieważ powodowały konflikty z istniejącymi nazwami poleceń cmdlet w module platformy Azure:
    + `Enable-AzureDataCollection` (obsługiwany przez `Enable-AzureRmDataCollection`)
    + `Disable-AzureDataCollection` (obsługiwany przez `Disable-AzureRmDataCollection`)
* Usługa Relay
  - Dodano polecenia cmdlet dla usługi Azure Relay umożliwiające użytkownikom tworzenie wszystkich zasobów usługi Azure Relay i zarządzanie nimi.
    + `New-AzureRmRelayNamespace`
    + `Get-AzureRmRelayNamespace`
    + `Set-AzureRmRelayNamespace`
    + `Remove-AzureRmRelayNamespace`
    + `New-AzureRmWcfRelay`
    + `Get-AzureRmWcfRelay`
    + `Set-AzureRmWcfRelay`
    + `Remove-AzureRmWcfRelay`
    + `New-AzureRmRelayHybridConnection`
    + `Get-AzureRmRelayHybridConnection`
    + `Set-AzureRmRelayHybridConnection`
    + `Remove-AzureRmRelayHybridConnection`
    + `Test-AzureRmRelayName`
    + `Get-AzureRmRelayOperation`
    + `New-AzureRmRelayKey`
    + `Get-AzureRmRelayKey`
    + `New-AzureRmRelayAuthorizationRule`
    + `Get-AzureRmRelayAuthorizationRule`
    + `Set-AzureRmRelayAuthorizationRule`
    + `Remove-AzureRmRelayAuthorizationRule`
* Zasoby
  - Obsługa wdrożeń między grupami zasobów w poleceniu cmdlet New-AzureRmResourceGroupDeployment
    + Użytkownicy mogą teraz używać zagnieżdżonych wdrożeń w celu wdrażania w różnych grupach zasobów.
* ServiceBus

  - Poprawka usterki: wartości właściwości obiektu kolejki ServiceBus zostały ustawione na null, obiekt jest używany jako parametr wejściowy w poleceniu cmdlet Set-AzureRmServiceBusQueue w celu zaktualizowania kolejki.
    - Właściwości, których to dotyczy, to: LockDuration, EntityAvailabilityStatus, DuplicateDetectionHistoryTimeWindow, MaxDeliveryCount i MessageCount
* ServiceFabric

  - Dodano polecenia cmdlet dla usługi Service Fabric
    + Add-AzureRmServiceFabricApplicationCertificate       Dodaj certyfikat, który będzie używany jako certyfikat aplikacji
    + Add-AzureRmServiceFabricClientCertificate       Dodaj nazwę pospolitą lub odcisk palca do ustawień klastra na potrzeby uwierzytelniania klienta
    + Add-AzureRmServiceFabricClusterCertificate       Dodaj pomocniczy certyfikat do klastra na potrzeby wymiany istniejącego certyfikatu
    + Add-AzureRmServiceFabricNodes       Dodaj węzły/maszyny wirtualne o określonym typie węzła do klastra
    + Add-AzureRmServiceFabricNodeType       Dodaj maszyny wirtualne/typ węzła do istniejącego klastra
    + Get-AzureRmServiceFabricCluster       Pobierz szczegóły zasobu klastra
    + New-AzureRmServiceFabricCluster Utwórz nowy klaster ServiceFabric. To polecenie ma wiele przeciążeń, aby obsłużyć różne scenariusze
    + Remove-AzureRmServiceFabricClientCertificate       Usuń certyfikat klienta, aby nie był już używany w celu uzyskiwania dostępu do klastra
    + Remove-AzureRmServiceFabricClusterCertificate       Usuń certyfikat klastra, aby nie był już używany do zabezpieczania klastra
    + Remove-AzureRmServiceFabricNodes       Usuń z klastra węzły o określonym typie
    + Remove-AzureRmServiceFabricNodeType       Usuń z klastra typ węzła
    + Remove-AzureRmServiceFabricSettings       Usuń z klastra co najmniej jedno ustawienie ServiceFabric
    + Set-AzureRmServiceFabricSettings       Dodaj lub zaktualizuj co najmniej jedno ustawienie ServiceFabric klastra
    + Set-AzureRmServiceFabricUpgradeType       Zmień typ uaktualnienia ServiceFabric klastra
    + Update-AzureRmServiceFabricDurability       Zmień warstwę trwałości klastra
    + Update-AzureRmServiceFabricReliability       Zmień warstwę niezawodności klastra
* Sql
  - Dodano parametr -SampleName do polecenia New-AzureRmSqlDatabase
  - Aktualizacje poleceń cmdlet grupy trybu failover
  - Usunięto parametry „Tag”
  - Usunięto parametry „PartnerResourceGroupName” i „PartnerServerName” z polecenia cmdlet Remove-AzureRmSqlDatabaseFailoverGroup
  - Dodano parametr „GracePeriodWithDataLossHours” do poleceń cmdlet New- i Set-, który w przyszłości zastąpi parametr „GracePeriodWithDataLossHour”
  - Dopracowano i zaktualizowano dokumentację
  - Zmieniono formatowanie zwracanych obiektów i usunięto usterki, z powodu których pola nie zawsze były wypełniane
  - Dodano właściwości „DatabaseNames” i „PartnerLocation” do obiektu grupy trybu failover
  - Naprawiono usterkę, z powodu której następował natychmiastowy powrót z polecenia cmdlet Switch-, zamiast poczekania na zakończenie operacji
  - Naprawiono usterkę powodującą przekroczenie zakresu liczb całkowitych w przypadku użycia dużych wartości okresu prolongaty
  - Okres prolongaty będzie zmieniany na wartość minimalną (1 godzina), jeśli podano krótszy
  - Usunięto wartość „Usage_Anomaly” z listy akceptowanych wartości parametru „ExcludedDetectionType” poleceń cmdlet Set-AzureRmSqlDatabaseThreatDetectionPolicy i Set-AzureRmSqlServerThreatDetectionPolicy.
* Magazyn
  - Uaktualniono zestaw SRP SDK do wersji 6.3.0
  - New/Set-AzureRmStorageAccount: dodano nowy parametr w celu obsługi atrybutu EnableHttpsTrafficOnly
  - New/Set/Get-AzureRmStorageAccount: zwracane konto magazynu zawiera nowy atrybut EnableHttpsTrafficOnly
* Azure.Storage
  - Uaktualniono bibliotekę klienta usługi Azure Storage do wersji 8.1.1 i bibliotekę przenoszenia danych usługi Azure Storage do wersji 0.5.1
  - Dodano nowe polecenie cmdlet w celu obsługi funkcji przyrostowej kopii obiektu blob
