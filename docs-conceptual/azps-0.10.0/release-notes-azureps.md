---
title: Informacje o wersji programu Azure PowerShell
description: Uzyskaj informacje na temat wszystkich najnowszych aktualizacji modułów programu Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ab367ed41c77629122d6a4a9a79b96c7c66d09cb
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427585"
---
# <a name="azure-powershell-release-notes"></a>Informacje o wersji programu Azure PowerShell
## <a name="0100-preview---april-2020"></a>0.10.0-preview — kwiecień 2020 r.
### <a name="general"></a>Ogólne
* Moduły Az są teraz dostępne w wersji zapoznawczej w usłudze Azure Stack Hub. Pozwala to na uzyskanie zgodności między wieloma platformami w przypadku systemów Linux i macOS. Usługa Azure Stack Hub obsługuje teraz program PowerShell Core z modułami Az; więcej informacji znajduje się [tutaj](/azure-stack/operator/powershell-install-az-module)
* Moduły Az obsługują profil 2019-03-01-hybrid:
  - Az.Billing
  - Az.Compute
  - Az.DataBoxEdge
  - Az.EventHub
  - Az.IotHub
  - Az.KeyVault
  - Az.Monitor
  - Az.Network
  - Az.Resources
  - Az.Storage
  - Az.Websites
* Wprowadzono trzy nowe moduły programu PowerShell dla modułu Az, które działają w usłudze Azure Stack Hub: Az.Databox, Az.IotHub i Az.EventHub
* Polecenia pozostają w zasadzie takie same, wprowadzono tylko niewielkie zmiany, np. zmieniono ciąg AzureRM na Az
* Zaktualizowany link do dokumentacji programu PowerShell dla usługi Azure Stack Hub można znaleźć [tutaj](/azure-stack/operator/powershell-install-az-module)

#### <a name="azaccounts"></a>Az.Accounts
* Uaktualnienie z biblioteki ADAL do MSAL


## <a name="370---march-2020"></a>3.7.0 — marzec 2020 r.
#### <a name="azaccounts"></a>Az.Accounts
* Rozwiązano problem powodujący zgłaszanie wyjątku NullReferenceException przez polecenia „Get-AzTenant”, „Get-AzDefault” i „Set-AzDefault”, gdy użytkownik nie jest zalogowany [nr 10292]

#### <a name="azcompute"></a>Az.Compute
* Dodano następujące parametry do polecenia cmdlet „New-AzDiskConfig”:
    - DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference
* Zezwolono na właściwość Encryption parametru Target polecenia cmdlet „New-AzGalleryImageVersion”.
* Rozwiązano problem tempDisk w przypadku poleceń cmdlet „Set-AzVmss” z parametrem -Reimage i „Invoke-AzVMReimage”. [nr 11354]
* Do poniższych poleceń cmdlet dodano obsługę nowego rozszerzenia SAP
    - „Set-AzVMAEMExtension”
    - „Get-AzVMAEMExtension”
    - „Remove-AzVMAEMExtension”
    - „Update-AzVMAEMExtension”
* Usunięto błędy w przykładach dokumentu pomocy
* Pokazano dokładną wartość ciągu dla parametru PowerState maszyny wirtualnej w formacie tabeli.
* „New-AzVmssConfig”: poprawiono serializację właściwości AutomaticRepairs, gdy właściwość SinglePlacementGroup jest wyłączona. [nr 11257]

#### <a name="azdatafactory"></a>Az.DataFactory
* Zaktualizowano wersję zestawu ADF .Net SDK do 4.8.0
* Dodano opcjonalne parametry do polecenia „Invoke-AzDataFactoryV2Pipeline” w celu obsługi ponownego uruchamiania

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Dodano opis zmiany powodującej niezgodność dla poleceń „Export-AzDataLakeStoreItem” i „Import-AzDataLakeStoreItem”
* Dodano opcję kodowania bajtów dla poleceń „New-AzDataLakeStoreItem”, „Add-AzDAtaLakeStoreItemContent” i „Get-AzDAtaLakeStoreItemContent”

#### <a name="azhdinsight"></a>Az.HDInsight
* Dodano obsługę określania minimalnej obsługiwanej wersji protokołu TLS podczas tworzenia klastra.

#### <a name="aziothub"></a>Az.IotHub
* Dodano obsługę zarządzania ustawieniami rozproszonymi dla poszczególnych urządzeń. Nowe polecenia cmdlet:
    - „Get-AzIotHubDistributedTracing”
    - „Set-AzIotHubDistributedTracing”

#### <a name="azkeyvault"></a>Az.KeyVault
* Dodano atrybuty zmian powodujących niezgodność do polecenia „New-AzKeyVault”

#### <a name="azmonitor"></a>Az.Monitor
* Zaktualizowano dokumentację polecenia „New-AzScheduledQueryRuleLogMetricTrigger”

#### <a name="aznetwork"></a>Az.Network
* Zaktualizowano polecenia cmdlet, aby zezwolić na połączenia VirtualHubVnetConnections między dzierżawami
    - „New-AzVirtualHubVnetConnection”
    - „Update-AzVirtualHubVnetConnection”
    - „New-AzVirtualHub”
    - „Update-AzVirtualHub”
* Usunięto zależność od zestawu SDK zarządzania SQL

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Ulepszono komunikaty o błędach

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* W usłudze Azure Site Recovery dodano obsługę ponownego włączania ochrony oraz zaktualizowano właściwości maszyn wirtualnych w przypadku maszyn wirtualnych zaszyfrowanych za pomocą usługi Azure Disk Encryption.
* Dodano monitorowanie odzyskiwania po awarii właściwości VmwareToAzure usługi Azure Site Recovery
* W usłudze Azure Backup dodano obsługę ponawiania aktualizacji zasad w przypadku elementów, dla których zakończyła się ona niepowodzeniem.
* W usłudze Azure Backup dodano obsługę ustawień wykluczania dysków podczas tworzenia i przywracania kopii zapasowych.
* W usłudze Azure Backup dodano obsługę przywracania wielu plików/folderów w elemencie AzureFileShare
* W usłudze Azure Backup dodano obsługę dla określonej przez użytkownika obsługi grupy zasobów w trakcie aktualizowania zasad IaasVM

#### <a name="azresources"></a>Az.Resources
* Poprawiono polecenie „Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType”, aby używało rzeczywistej wersji apiVersion zasobów, a nie domyślnej wersji apiVersion [nr 11267]
* Dodano rejestrowanie identyfikatorów correlationId dla scenariuszy błędów
* Niewielka zmiana dokumentacji polecenia „Get-AzResourceLock”. Dodano przykład.
* Dodano znak ucieczki przed pojedynczym cudzysłowem w wartości parametru „Get-AzADUser” [nr 11317]
* Dodano nowe polecenia cmdlet dla skryptów wdrażania („Get-AzDeploymentScript”, „Get-AzDeploymentScriptLog”, „Save-AzDeploymentScriptLog”, „Remove-AzDeploymentScript”)

#### <a name="azsql"></a>Az.Sql
* Dodano możliwy do odczytu parametr pomocniczy do polecenia „Invoke-AzSqlDatabaseFailover”
* Dodano polecenie cmdlet „Disable-AzSqlServerActiveDirectoryOnlyAuthentication”
* Zapisywanie stopnia czułości podczas klasyfikowania kolumn w bazie danych.

#### <a name="azsupport"></a>Az.Support
* Ogólna dostępność modułu „Az.Support”

#### <a name="azwebsites"></a>Az.Websites
* Dodano obsługę pracy z regułami routingu ruchu aplikacji internetowej za pośrednictwem poniższych nowych poleceń cmdlet
    - „Get-AzWebAppTrafficRouting”
    - „Update-AzWebAppTrafficRouting”
    - „Add-AzWebAppTrafficRouting”
    - „Remove-AzWebAppTrafficRouting”

## <a name="361---march-2020"></a>3.6.1 — marzec 2020 r.
#### <a name="azaccounts"></a>Az.Accounts
* Otwarcie strony ankiety Azure PowerShell w poleceniu „Send-Feedback” [#11020]
* Wyświetlanie adresu URL ankiety Azure PowerShell w poleceniu „Resolve-Error” [#11021]
* Dodano wersję Az w agencie UserAgent

#### <a name="azapimanagement"></a>Az.ApiManagement
* Dodano obsługę pobierania i konfigurowania domeny niestandardowej w punkcie końcowym DeveloperPortal [#11007]
* Dodano obsługę elementu „Export-AzApiManagementApi” do pobierania definicji interfejsu API w formacie JSON [#9987]
* Dla polecenia „Import-AzApiManagementApi” dodano obsługę importowania definicji OpenApi 3.0 z dokumentu JSON
* Dla poleceń „New-AzApiManagementIdentityProvider” i „Set-AzApiManagementIdentityProvider” dodano obsługę konfigurowania „dzierżawy podpisującej” dla dostawcy AAD B2C [#9784]

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Dodano odwołanie do elementu System.Buffers jawnie w plikach csproj i psd1.

#### <a name="aziothub"></a>Az.IotHub
* Dodano obsługę zarządzania urządzeniami w centrum IoT. Nowe polecenia cmdlet:
    - „Add-AzIotHubDevice”
    - „Get-AzIotHubDevice”
    - „Remove-AzIotHubDevice”
    - „Set-AzIotHubDevice”
* Dodano obsługę zarządzania modułami na docelowym urządzeniu IoT w centrum IoT. Nowe polecenia cmdlet:
    - „Add-AzIotHubModule”
    - „Get-AzIotHubModule”
    - „Remove-AzIotHubModule”
    - „Set-AzIotHubModule”
* Dodano polecenie cmdlet do pobierania parametrów połączenia docelowego urządzenia IoT w centrum IoT.
* Dodano polecenie cmdlet do pobierania parametrów połączenia modułu na docelowym urządzeniu IoT w centrum IoT.
* Dodano obsługę pobierania/ustawiania urządzenia nadrzędnego urządzenia IoT. Nowe polecenia cmdlet:
    - „Get-AzIotHubDeviceParent”
    - „Set-AzIotHubDeviceParent”
* Dodano obsługę zarządzania relacją nadrzędny-podrzędny urządzenia.

#### <a name="azmonitor"></a>Az.Monitor
* Stała wartość wyjściowa polecenia „Get-AzMetricDefinition” [#9714]

#### <a name="aznetwork"></a>Az.Network
* Zaktualizowano zestaw SDK zarządzania SQL.
* Rozwiązano problem z różnicą nazewnictwa w klasie PrivateLinkServiceConnectionState.
    - Mapowanie pola ActionsRequired na pole ActionRequired.
* Dodano parametr PublicNetworkAccess do poleceń „New-AzSqlServer” i „Set-AzSqlServer”

#### <a name="azresources"></a>Az.Resources
* Usunięto błąd odwołania o wartości null w elemencie „Get-AzRoleAssignment”
* Opcje „-Force” i „-PassThru” oznaczono jako opcjonalny w poleceniu „Remove-AzADGroup” [#10849]
* Rozwiązano problem polegający na tym, że element „MailNickname” nie jest zwracany przez polecenie „Remove-AzADGroup” [#11167]
* Rozwiązano problem polegający na tym, że operacja potoku „Remove-AzADGroup” nie działa [#11171]
* Naprawiono błąd odwołania o wartości null w poleceniu GetAzureRoleAssignmentCommand
* Dodano atrybuty zmiany powodującej niezgodność dla nadchodzących zmian w poleceniach cmdlet zasad
* Zaktualizowano polecenie „Get-AzResourceGroup”, aby można było wykonać filtrowanie tagów grup zasobów po stronie serwera
* Rozszerzone polecenia cmdlet dotyczące tagów do akceptowania parametru -ResourceId
    - Get-AzTag -ResourceId
    - New-AzTag -ResourceId
    - Remove-AzTag -ResourceId
* Dodano nowe polecenie cmdlet dotyczące tagów
    - Update-AzTag -ResourceId
* Dodano element ScopedDeployment z zestawu SDK 3.3.0

#### <a name="azsql"></a>Az.Sql
* Dodano parametr PublicNetworkAccess do poleceń „New-AzSqlServer” i „Set-AzSqlServer”
* Dodano obsługę konfiguracji długoterminowego przechowywania kopii zapasowych dla zarządzanych baz danych
    - Pobieranie/ustawianie zasad LTR w zarządzanej bazie danych
    - Pobieranie kopii zapasowych LTR według zarządzanej bazy danych, wystąpienia zarządzanego lub lokalizacji
    - Usuwanie kopii zapasowej LTR
    - Przywracanie kopii zapasowej LTR, aby utworzyć nową zarządzaną bazę danych
* Dodano parametr MinimalTlsVersion do polecenia New-AzSqlServer i Set-AzSqlServer
* Dodano parametr MinimalTlsVersion do poleceń New-AzSqlInstance i Set-AzSqlInstance
* Niestandardowa wersja zestawu SQL SDK dla elementu Az.Network

#### <a name="azstorage"></a>Az.Storage
* Obsługiwane polecenie AllowProtectedAppendWrite w zasadach ImmutabilityPolicy
    - „Set-AzRmStorageContainerImmutabilityPolicy”
* Dodano komunikat ostrzegawczy na temat zmiany powodującej niezgodność dla zmiany elementu AzureStorageTable w przyszłej wersji
    - „New-AzStorageTable”
    - „Get-AzStorageTable”

#### <a name="azwebsites"></a>Az.Websites
* Dodano parametr tagu dla opcji „New-AzAppServicePlan” i „Set-AzAppServicePlan”
* Zatrzymaj wykonywanie polecenia cmdlet, jeśli podczas dodawania domeny niestandardowej do witryny internetowej zostanie zgłoszony wyjątek
* Dodano obsługę wykonywania operacji dla usługi App Services nieznajdujących się w tej samej grupie zasobów co plan usługi App Service
* Zastosowano ograniczenie dostępu do aplikacji internetowych/funkcji w różnych grupach zasobów
* Rozwiązano problem w celu ustawienia niestandardowych nazw hostów dla miejsc aplikacji internetowych

## <a name="350---february-2020"></a>3.5.0 — luty 2020 r.
### <a name="highlights-since-the-last-major-release"></a>Najważniejsze zmiany od ostatniej wersji głównej
* Zaktualizowano telemetrię po stronie klienta.
* W module Az.IotHub dodano polecenia cmdlet do obsługi zarządzania urządzeniami.
* W module Az.SqlVirtualMachine dodano polecenia cmdlet na potrzeby odbiornika grupy dostępności.

#### <a name="azaccounts"></a>Az.Accounts
* Dodano identyfikatory SubscriptionId i TenantId oraz czas wykonywania do danych telemetrii po stronie klienta

#### <a name="azautomation"></a>Az.Automation
* Poprawiono literówkę w 1. przykładzie w dokumentacji referencyjnej polecenia „New-AzAutomationSoftwareUpdateConfiguration”

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Zaktualizowano zestaw SDK do wersji 7.0
* Ulepszono komunikat o błędzie, gdy odpowiedź serwera ma pustą treść

#### <a name="azcompute"></a>Az.Compute
* Dozwolono pustą wartość identyfikatora ProximityPlacementGroupId podczas aktualizacji

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Dodano polecenie cmdlet służące do pobierania definicji reguł zarządzanych, które mogą być używane w zaporze aplikacji internetowej

#### <a name="aziothub"></a>Az.IotHub
* Dodano obsługę zarządzania urządzeniami w centrum IoT. Nowe polecenia cmdlet:
    - „Add-AzIotHubDevice”
    - „Get-AzIotHubDevice”
    - „Remove-AzIotHubDevice”
    - „Set-AzIotHubDevice”

#### <a name="azkeyvault"></a>Az.KeyVault
* Poprawiono zduplikowany tekst pliku Add-AzKeyVaultKey.md

#### <a name="azmonitor"></a>Az.Monitor
* Poprawiono opis polecenia cmdlet Get-AzLog.
* Do polecenia „New-AzMetricAlertRuleV2” dodano nowy parametr o nazwie ActionGroupId.
    - Użytkownik może podać wartość ActionGroupId(ciąg) lub ActionGorup(ActivityLogAlertActionGroup).

#### <a name="aznetwork"></a>Az.Network
* Dodano jedną dodatkową uwagę dla parametru „-EnableProxyProtocol” polecenia cmdlet „New-AzPrivateLinkService”.
* Poprawiono przykład opcji FilterData w plikach Start-AzVirtualNetworkGatewayConnectionPacketCapture.md i Start-AzVirtualnetworkGatewayPacketCapture.md.
* Dodano przykład przechwytywania pakietów przedstawiający przechwytywanie wszystkich pakietów wewnętrznych i zewnętrznych w plikach Start-AzVirtualNetworkGatewayConnectionPacketCapture.md i Start-AzVirtualnetworkGatewayPacketCapture.md.
* Obsługa zasad usługi Azure Firewall w przypadku zapór sieci wirtualnych
    - Nie dodano żadnych nowych poleceń cmdlet. Złagodzono ograniczenie dotyczące zasad zapór sieci wirtualnych

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Dodano obsługę funkcji przywracania jako plików dla baz danych SQL.

#### <a name="azresources"></a>Az.Resources
* Refaktoryzowano polecenia cmdlet wdrażania szablonów
    - Dodano nowe polecenia cmdlet do zarządzania wdrożeniami w grupie zarządzania: *-AzManagementGroupDeployment
    - Dodano nowe polecenia cmdlet do zarządzania wdrożeniami w zakresie dzierżawy: *-AzTenantDeployment
    - Refaktoryzowano polecenia cmdlet *-AzDeployment tak, aby działały konkretnie w zakresie subskrypcji
    - Utworzono aliasy *-AzSubscriptionDeployment dla poleceń cmdlet *-AzDeployment
* Poprawiono polecenie „Update-AzADApplication”, gdy parametr „AvailableToOtherTenants” nie jest ustawiony
* Usunięto zestaw parametrów ApplicationObjectWithoutCredentialParameterSet, aby uniknąć wyjątku AmbiguousParameterSetException.
* Ponownie wygenerowano pliki pomocy

#### <a name="azsql"></a>Az.Sql
* Dodano obsługę przywracania do punktu w czasie w wystąpieniach zarządzanych między subskrypcjami.
* Dodano obsługę zmiany obecnej generacji sprzętu wystąpienia zarządzanego SQL
* Poprawiono przykłady w pomocy polecenia „Update-AzSqlServerVulnerabilityAssessmentSetting”: dane wyjściowe parametru/właściwości — EmailAdmins

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* Dodano polecenia cmdlet na potrzeby odbiornika grupy dostępności

#### <a name="azstoragesync"></a>Az.StorageSync
* Zaktualizowano obsługiwane zestawy znaków w poleceniu „Invoke-AzStorageSyncCompatibilityCheck”.

## <a name="340---february-2020"></a>3.4.0 — luty 2020 r.
### <a name="highlights-since-the-last-major-release"></a>Najważniejsze zmiany od ostatniej wersji głównej
* Wydano początkową wersję 0.1.0 funkcji Az.CosmosDB
* Dodano obsługę funkcji Az.Network ConnectionMonitor w wersji 2

#### <a name="azaccounts"></a>Az.Accounts
* Wyłączono automatyczne zapisywanie kontekstu, gdy plik AzureRmContext.json jest niedostępny
* Zaktualizowano odwołania do programu Azure PowerShell Common do wersji 1.3.5-preview

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Get-AzApiManagementApiSchema** Naprawiono pobieranie schematu Open-Api skojarzonego z interfejsem API   https://github.com/Azure/azure-powershell/issues/10626
* **New-AzApiManagementProduct** _ i _ *Set-AzApiManagementProduct**
  - Poprawiono dokumentację dotycząca funkcji https://github.com/Azure/azure-powershell/issues/10472
* **Set-AzApiManagementApi** Dodano przykład pokazujący, jak zaktualizować wartość ServiceUrl przy użyciu polecenia cmdlet

#### <a name="azcompute"></a>Az.Compute
* Ograniczono liczbę stanów maszyn wirtualnych do 100, aby uniknąć ograniczania w przypadku wykonywania operacji Get-AzVM -Status bez nazwy maszyny wirtualnej.
* Dodano polecenie cmdlet Update-AzDiskEncryptionSet
* Dodano parametry EncryptionType i DiskEncryptionSetId do następujących poleceń cmdlet:
    - New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig
* Dodano parametr ColocationStatus do polecenia cmdlet Get-AzProximityPlacementGroup.

#### <a name="azdatafactory"></a>Az.DataFactory
* Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.7.0

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* Dodano operacje LIST dla zasobów
* Dodano możliwość wykonywania operacji na krokach kontroli kondycji

#### <a name="azhdinsight"></a>Az.HDInsight
* Naprawiono błąd w dokumentacji funkcji New-AzHDInsightCluster.

#### <a name="azkeyvault"></a>Az.KeyVault
* Dodano alias Name do atrybutu VaultName, aby uspójnić polecenie Remove-AzureKeyVault z poleceniem New-AzureKeyVault.

#### <a name="aznetwork"></a>Az.Network
* Dodano nowy przykład do polecenia Set-AzNetworkWatcherConfigFlowLog.md w celu zademonstrowania scenariusza wyłączenia analizy ruchu.
* Dodano obsługę przypisywania konfiguracji protokołu IP zarządzania do zapory Azure Firewall — dedykowanej podsieci i publicznego adresu IP, których zapora będzie używać dla swojego ruchu związanego z zarządzaniem
    - Zaktualizowano polecenie cmdlet New-AzFirewall:
        - Dodano parametr -ManagementPublicIpAddress (nieobowiązkowy), który akceptuje obiekt publicznego adresu IP
        - Dodano metodę SetManagementIpConfiguration w obiekcie zapory — wymaga jako danych wejściowych podsieci i publicznego adresu IP — nazwa podsieci musi mieć wartość „AzureFirewallManagementSubnet”
* Poprawiono przykłady polecenia Get-AzNetworkSecurityGroup, aby pokazać przykłady dla sieciowej grupy zabezpieczeń zamiast interfejsów sieciowych.
* Poprawiono literówkę w poleceniu New-AzVpnSite, która uniemożliwiała modułowi wypełniania identyfikatora wypełnienie parametru.
* Dodano obsługę konfiguracji adresu URL w akcji reguł ponownego zapisywania ustawionej w usłudze Application Gateway
    - Dodano nowe polecenia cmdlet:
        - New-AzApplicationGatewayRewriteRuleUrlConfiguration
    - Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -UrlConfiguration
        - New-AzApplicationGatewayRewriteRuleActionSet
* Dodano obsługę dla zasobów NetworkWatcher ConnectionMonitor w wersji 2

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Obsługa oceny zgodności przed ustaleniem, który zasób należy skorygować
    - Dodano parametr „-ResourceDiscoverMode” do polecenia Start-AzPolicyRemediation
* Dodano polecenie cmdlet Get-AzPolicyMetadata na potrzeby pobierania zasobów metadanych zasad
* Zaktualizowano polecenia Get-AzPolicyState i Get-AzPolicyStateSummary dla interfejsu API w wersji 2019-10-01

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Usługa Azure Site Recovery obsługuje usuwanie zreplikowanego dysku.
* W usłudze Azure Backup dodano obsługę dodawania tagów podczas tworzenia magazynu usługi Recovery Services.

#### <a name="azresources"></a>Az.Resources
* Parametr -Scope ustawiono jako opcjonalny w poleceniach cmdlet *-AzPolicyAssignment z domyślną wartością subskrypcji kontekstu
* Dodano przykłady tworzenia obiektu ADServicePrincipal z hasłem i kluczowym poświadczeniem

#### <a name="azsql"></a>Az.Sql
Naprawiono polecenie cmdlet New-AzSqlDatabaseSecondary, aby sprawdzało istnienie elementu PartnerDatabaseName zamiast istnienia elementu DatabaseName.

#### <a name="azstorage"></a>Az.Storage
* Włączono obsługę typu klucza szyfrowania tabeli/kolejki w tworzeniu konta magazynu
    - New-AzStorageAccount
* Pokazywana jest wartość RequestId, gdy właściwość StorageException nie ma wartości ExtendedErrorInformation
* Poprawiono przykład 6 polecenia cmdlet Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* Polecenia Set-AzWebapp i Set-AzWebappSlot obsługują właściwości AlwaysOn, MinTls i FtpsState
* Rozwiązywanie problemu polegającego na tym, że zmienianie ustawienia HttpsOnly jednocześnie ze zmienianiem ustawienia AppservicePlan za pomocą jednego polecenia Set-AzWebApp powodowało resetowanie ustawienia HttpsOnly do wartości domyślnej

## <a name="330---january-2020"></a>3.3.0 — styczeń 2020 r.
#### <a name="azaccounts"></a>Az.Accounts
* Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametry AzureAttestationServiceEndpointResourceId i AzureAttestationServiceEndpointSuffix

#### <a name="azcdn"></a>Az.Cdn
* Wyświetlanie szczegółów odpowiedzi błędu w poleceniu cmdlet New-AzCdnEndpoint

#### <a name="azcompute"></a>Az.Compute
* Poprawiono polecenie cmdlet Set-AzVMCustomScriptExtension dla maszyny wirtualnej z zarządzanym dyskiem systemu operacyjnego, który nie ma profilu systemu operacyjnego.

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Naprawiono nazwy parametrów używanych na przykład przez polecenie New-AzContainerGroup

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* Dodano polecenie cmdlet „Get-AzDataBoxEdgeStorageContainer”
  - Pobieranie kontenera magazynu usługi Edge
* Dodano polecenie cmdlet „New-AzDataBoxEdgeStorageContainer”
  - Tworzenie nowego kontenera magazynu usługi Edge
* Dodano polecenie cmdlet „Remove-AzDataBoxEdgeStorageContainer”
  - Usuwanie kontenera magazynu usługi Edge
* Dodano polecenie cmdlet „Invoke-AzDataBoxEdgeStorageContainer”
  - Wywoływanie akcji odświeżania danych w kontenerze magazynu usługi Edge
* Dodano polecenie cmdlet „Get-AzDataBoxEdgeStorageAccount”
  - Pobieranie konta magazynu usługi Edge
* Dodano polecenie cmdlet „New-AzDataBoxEdgeStorageAccount”
  - Tworzenie nowego konta magazynu usługi Edge
* Dodano polecenie cmdlet „Remove-AzDataBoxEdgeStorageAccount”
  - Usuwanie konta magazynu usługi Edge
* Wywołanie polecenia cmdlet „Invoke-AzDataBoxEdgeShare”
  - Wywołanie akcji odświeżania danych w udziale
* Dodano polecenie cmdlet „Set-AzDataBoxEdgeStorageAccountCredential”
  - Ustawienie poświadczenia konta magazynu az databoxedge

#### <a name="azdatafactory"></a>Az.DataFactory
* Dodano właściwości AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId i VersionStatus do polecenia Get-AzDataFactoryV2IntegrationRuntime
* Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.6.0
* Dodano parametr „PublicIPs” do polecenia „Set-AzureRmDataFactoryV2IntegrationRuntime” w celu umożliwienia tworzenia środowisk IR Azure-SSIS ze statycznymi publicznymi adresami IP.

#### <a name="azdevtestlabs"></a>Az.DevTestLabs
* Usunięto niedziałający link w pliku Get-AzDtlAllowedVMSizesPolicy.md

#### <a name="azeventhub"></a>Az.EventHub
* Rozwiązano problem nr 10634: Naprawiono odwołanie do obiektu null podczas usuwania elementu eventhubnamespace

#### <a name="azhdinsight"></a>Az.HDInsight
* Poprawiono błąd w pliku Invoke-AzHDInsightHiveJob.md.

#### <a name="azmachinelearning"></a>Az.MachineLearning
* Usunięto poniższe polecenia cmdlet, ponieważ funkcja MachineLearningCompute nie jest już dostępna
  - Get-AzMlOpCluster
  - Get-AzMlOpClusterKey
  - New-AzMlOpCluster
  - Remove-AzMlOpCluster
  - Set-AzMlOpCluster
  - Test-AzMlOpClusterSystemServicesUpdateAvailability
  - Update-AzMlOpClusterSystemService

#### <a name="aznetwork"></a>Az.Network
* Uaktualniono zależność Microsoft.Azure.Management.Sql z wersji 1.36-preview do 1.37-preview

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* W usłudze Azure Site Recovery zmieniono obsługę maszyn wirtualnych z dyskiem zarządzanym szyfrowanych podczas magazynowania za pomocą kluczy zarządzanych przez klienta dla platformy Azure na dostawcę platformy Azure.
* Usługa Azure Site Recovery obsługuje wprowadzanie identyfikatora zestawu szyfrowania dysków jako opcjonalnego elementu wejściowego podczas włączania ochrony dla narzędzia VMware na platformie Azure.
* Usługa Azure Site Recovery obsługuje wprowadzanie identyfikatora zestawu szyfrowania dysków jako opcjonalnego elementu wejściowego na poziomie dysku w celu włączenia ochrony dla narzędzia VMware na platformie Azure.
* Usługa Azure Site Recovery obsługuje aktualizację elementu chronionego przez replikację z zestawem szyfrowania dysków mapowanym dla funkcji HyperV na platformie Azure.

#### <a name="azresources"></a>Az.Resources
* Naprawiono błąd w dokumencie pomocy „Remove-AzTag”.

#### <a name="azsql"></a>Az.Sql
* Naprawiono błąd oceny luk w zabezpieczeniach dotyczący funkcji poleceń cmdlet do ustawiania punktu odniesienia w celu działania na bazie danych master dla usługi Azure Database i ograniczenia go w systemowych bazach danych wystąpienia zarządzanego.
* Naprawiono błąd podczas tworzenia grupy trybu failover wystąpienia SQL

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* Dodano nowy prawidłowy typ licencji DR

#### <a name="azstorage"></a>Az.Storage
* Dodano komunikat ostrzegawczy na temat zmiany powodującej niezgodność dla zmiany elementu DefaultAction w przyszłej wersji
    - Update-AzStorageAccountNetworkRuleSet
* Obsługa uzyskiwania ostatniego czasu synchronizacji kont usługi Storage poprzez uruchomienie polecenia get-AzureRMStorageAccount z parametrem -IncludeGeoReplicationStats
    - Get-AzureRMStorageAccount

## <a name="320---december-2019"></a>3.2.0 — grudzień 2019 r.

### <a name="general"></a>Ogólne
* Zaktualizowano odwołania w pliku psd1 tak, aby dla wszystkich modułów były używane ścieżki względne

#### <a name="azaccounts"></a>Az.Accounts
* Ustawiono prawidłowego agenta użytkownika dla telemetrii po stronie klienta dla modułu Az 4.0 (wersja zapoznawcza)
* Wyświetlanie przyjaznego dla użytkownika komunikatu o błędzie, gdy kontekst ma wartość null, w module Az 4.0 (wersja zapoznawcza)

#### <a name="azbatch"></a>Az.Batch
* Rozwiązano problem [nr 10602](https://github.com/Azure/azure-powershell/issues/10602) uniemożliwiający poleceniu **New-AzBatchPool** prawidłowe wysyłanie elementów „VirtualMachineConfiguration.ContainerConfiguration” i „VirtualMachineConfiguration.DataDisks” do serwera.

#### <a name="azdatafactory"></a>Az.DataFactory
* Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.5.0

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Dodano obsługę wykluczania reguł zarządzanych przez zaporę aplikacji internetowej
* Dodano element SocketAddr do autouzupełniania

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Obsługa wyjątków

#### <a name="azkeyvault"></a>Az.KeyVault
* Usunięto błąd podczas uzyskiwania dostępu do wartości, która potencjalnie nie jest ustawiona
* Zarządzanie certyfikatami kryptografii opartej na krzywej eliptycznej
    - Dodano obsługę określania krzywej dla zasad certyfikatów

#### <a name="azmonitor"></a>Az.Monitor
* Dodanie opcjonalnego argumentu do polecenia dodania ustawień diagnostycznych. Argument przełącznika, który, jeśli zostanie podany, wskazuje, że eksportowanie do usługi Log Analytics musi być przeprowadzane do ustalonego schematu (tzn. typu danych, dedykowanego)

#### <a name="aznetwork"></a>Az.Network
* Obsługa grup adresów IP w regułach sieci, translatorze adresów sieciowych i aplikacji usługi Azure Firewall.

#### <a name="azresources"></a>Az.Resources
* Usunięto problem polegający na tym, że wdrożenie szablonu nie może odczytać parametru szablonu, jeśli jego nazwa powoduje konflikt z nazwą wbudowanego parametru.
* Zaktualizowano polecenia cmdlet zasad w celu używania nowej wersji interfejsu API 2019-09-01, która wprowadza obsługę grupowania w definicjach zestawów zasad.

#### <a name="azsql"></a>Az.Sql
* Uaktualniono tworzenie magazynu w automatycznym włączaniu oceny luk w zabezpieczeniach do wersji StorageV2

#### <a name="azstorage"></a>Az.Storage
* Obsługa generowania tokenów SAS opartych na tożsamości kontenera / obiektu blob z kontekstem magazynu w oparciu o uwierzytelnianie OAuth
    - New-AzStorageContainerSASToken
    - New-AzStorageBlobSASToken
* Obsługa odwoływania kluczy delegowania użytkowników dla konta magazynu w celu odwołania wszystkich tokenów SAS tożsamości
    - Revoke-AzStorageAccountUserDelegationKeys
* Uaktualnienie do wersji Microsoft.Azure.Management.Storage 14.2.0 w celu obsługi nowego interfejsu API w wersji 2019-06-01.
* Obsługa funkcji QuotaGiB (udostępnianie limitu przydziału w GiB) dla wartości powyżej 5120 w poleceniach cmdlet płaszczyzny zarządzania udziałem plików i dodano alias parametru „Quota” do parametru „QuotaGiB”.
    - New-AzRmStorageShare
    - Update-AzRmStorageShare
* Dodano alias parametru „QuotaGiB” do parametru „Quota”
    - Set-AzStorageShareQuota
* Rozwiązano problem z czyszczeniem zapisanych zasad dostępu przez polecenie Set-AzStorageContainerAcl
    - Set-AzStorageContainerAcl

## <a name="310---november-2019"></a>3.1.0 — listopad 2019 r.
### <a name="highlights-since-the-last-major-release"></a>Najważniejsze zmiany od ostatniej wersji głównej
* Wydano pakiet Az.DataBoxEdge 1.0.0
* Wydano pakiet Az.SqlVirtualMachine 1.0.0

#### <a name="azcompute"></a>Az.Compute
* Funkcja ponownego stosowania maszyny wirtualnej
    - Dodano parametr Reapply do polecenia cmdlet Set-AzVM
* Funkcja AutomaticRepairs zestawu skalowania maszyn wirtualnych:
    - Dodano parametry EnableAutomaticRepair, AutomaticRepairGracePeriod i AutomaticRepairMaxInstanceRepairsPercent do następujących poleceń cmdlet:   New-AzVmssConfig   Update-AzVmss
* Obsługa obrazów z galerii pomiędzy dzierżawami dla polecenia New-AzVM
* Dodano element „Spot” do modułu wypełniania argumentów parametru Priority w poleceniach cmdlet New-AzVM, New-AzVMConfig i New-AzVmss
* Dodano parametry DiskIOPSReadWrite i DiskMBpsReadWrite do polecenia cmdlet Add-AzVmssDataDisk
* Zmieniono parametr SourceImageId polecenia cmdlet New-AzGalleryImageVersion na opcjonalny
* Dodano parametry OSDiskImage i DataDiskImage do polecenia cmdlet New-AzGalleryImageVersion
* Dodano parametr HyperVGeneration do polecenia cmdlet New-AzGalleryImageDefinition
* Dodano parametry SkipExtensionsOnOverprovisionedVMs do poleceń cmdlet New-AzVmss, New-AzVmssConfig i Update-AzVmss

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* Dodano polecenie cmdlet `Get-AzDataBoxEdgeOrder`
    - Pobieranie zamówienia
* Dodano polecenie cmdlet `New-AzDataBoxEdgeOrder`
    - Utworzono nowe zamówienie
* Dodano polecenie cmdlet `Remove-AzDataBoxEdgeOrder`
    - Usunięto zamówienie
* Zmiana w poleceniu cmdlet `New-AzDataBoxEdgeShare`
    - Teraz tworzy lokalny udział plików
* Dodano polecenie cmdlet `Set-AzDataBoxEdgeRole`
    - Teraz można zamapować wartość IotRole na udział plików
* Dodano polecenie cmdlet `Invoke-AzDataBoxEdgeDevice`
    - Wywoływanie skanowania aktualizacji, pobierania aktualizacji, instalowania aktualizacji na urządzeniu
* Dodano polecenie cmdlet `Get-AzDataBoxEdgeTrigger`
    - Pobiera informacje o wyzwalaczach
* Dodano polecenie cmdlet `New-AzDataBoxEdgeTrigger`
    - Utworzono nowe wyzwalacze
* Dodano polecenie cmdlet `Remove-AzDataBoxEdgeTrigger`
    - Usunięto wyzwalacze

#### <a name="azdatafactory"></a>Az.DataFactory
* Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.4.0
* Dodano parametr „ExpressCustomSetup” do polecenia „Set-AzureRmDataFactoryV2IntegrationRuntime” w celu włączenia konfiguracji i składników innych firm bez niestandardowego skryptu konfiguracji.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Zaktualizowano dokumentację poleceń Get-AzDataLakeStoreDeletedItem i Restore-AzDataLakeStoreDeletedItem

#### <a name="azeventhub"></a>Az.EventHub
* Rozwiązano problem nr 10301: Poprawiono format daty tokenu SAS

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Dodano parametr MinimumTlsVersion do poleceń Enable-AzFrontDoorCustomDomainHttps i New-AzFrontDoorFrontendEndpointObject
* Dodano parametry HealthProbeMethod i EnabledState do polecenia New-AzFrontDoorHealthProbeSettingObject
* Dodano nowe polecenie cmdlet do tworzenia obiektu BackendPoolsSettings w celu przejścia do tworzenia/aktualizacji usługi Front Door
    - New-AzFrontDoorBackendPoolsSettingObject

#### <a name="aznetwork"></a>Az.Network
* Zmieniono przykłady opcji FilterData dla plików „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md” i „Start-AzVirtualnetworkGatewayPacketCapture.md”.

#### <a name="azprivatedns"></a>Az.PrivateDns
* Zaktualizowano zestaw .Net SDK usługi PrivateDns do wersji 1.0.0

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Obsługa usługi Azure Site Recovery w celu wybrania typu dysku przy włączaniu ochrony.
* Poprawka edycji akcji planu odzyskiwania usługi Azure Site Recovery.
* Obsługa przywracania SQL usługi Azure Backup w celu akceptowania baz danych strumienia pliku.

#### <a name="azrediscache"></a>Az.RedisCache
* Dodano parametr „MinimumTlsVersion” w poleceniach cmdlet „New-AzRedisCache” i „Set-AzRedisCache”. Ponadto dodano parametr „MinimumTlsVersion” do danych wyjściowych polecenia cmdlet „Get-AzRedisCache”.
* Dodano weryfikację parametru „-Size” dla poleceń cmdlet „Set-AzRedisCache” i „New-AzRedisCache”

#### <a name="azresources"></a>Az.Resources
- Zaktualizowano polecenia cmdlet zasad, aby używały nowego interfejsu API w wersji 2019-06-01, który ma nową właściwość EnforcementMode w przypisaniu zasad.
- Zaktualizowano przykład pomocy definicji zasad tworzenia
- Usunięto usterkę polegającą na tym, że polecenie Remove-AZADServicePrincipal -ServicePrincipalName zwracało pustą referencję, gdy nie znajdowano głównej nazwy usługi.
- Usunięto usterkę polegającą na tym, że polecenie New-AZADServicePrincipal zwracało pustą referencję, gdy dzierżawa nie miała żadnej subskrypcji.
- Zmieniono polecenie New-AzAdServicePrincipal w celu dodania poświadczeń tylko do skojarzonej aplikacji.

#### <a name="azsql"></a>Az.Sql
* Dodano obsługę bazy danych ReadReplicaCount.
* Naprawiono polecenie Set-AzSqlDatabase w przypadku, gdy nie ustawiono nadmiarowości strefy

## <a name="300---november-2019"></a>3.0.0 — listopad 2019 r.
### <a name="general"></a>Ogólne
* Wydano pakiet Az.PrivateDns 1.0.0

#### <a name="azaccounts"></a>Az.Accounts
* Dodano komunikat o zakończeniu obsługi aliasu „Resolve-Error”.

#### <a name="azadvisor"></a>Az.Advisor
* Dodano nową kategorię „Operational Excellence” do polecenia cmdlet Get-AzAdvisorRecommendation.

#### <a name="azbatch"></a>Az.Batch
* Nazwę elementu `CoreQuota` dla klasy `BatchAccountContext` zmieniono na `DedicatedCoreQuota`. Jest również nowa właściwość `LowPriorityCoreQuota`.
  - Ma to wpływ na polecenie **Get-AzBatchAccount**.
* Parametr polecenia cmdlet **New-AzBatchTask** `-ResourceFile` teraz przyjmuje kolekcję obiektów `PSResourceFile`, którą można utworzyć przy użyciu nowego polecenia cmdlet **New-AzBatchResourceFile**.
* Nowe polecenie cmdlet **New-AzBatchResourceFile** w celu ułatwienia tworzenia obiektów `PSResourceFile`. Można je dostarczyć do polecenia cmdlet **New-AzBatchTask** w parametrze `-ResourceFile`.
  - Obsługuje ono dwa nowe rodzaje plików zasobów oprócz istniejącego sposobu `HttpUrl`:
    - Pliki zasobów oparte na elemencie `AutoStorageContainerName` pobierają cały kontener automatycznego magazynu do węzła usługi Batch.
    - Pliki zasobów oparte na elemencie `StorageContainerUrl` pobierają kontener określony w adresie URL do węzła usługi Batch.
* Usunięto właściwość `ApplicationPackages` elementu `PSApplication` zwracaną przez polecenie cmdlet **Get-AzBatchApplication**.
  - Określone pakiety wewnątrz aplikacji można teraz pobrać przy użyciu polecenia cmdlet **Get-AzBatchApplicationPackage**. Na przykład: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.
* Zmieniono nazwę właściwości `ApplicationId` na `ApplicationName` w poleceniach cmdlet **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** i **Set-AzBatchApplication**.
  - `ApplicationId` teraz jest aliasem `ApplicationName`.
* Dodano nową właściwość `PSWindowsUserConfiguration` do klasy `PSUserAccount`.
* Zmieniono nazwę właściwości `Version` na `Name` w klasie `PSApplicationPackage`.
* Zmieniono nazwę właściwości `BlobSource` na `HttpUrl` w klasie `PSResourceFile`.
* Usunięto właściwość `OSDisk` z klasy `PSVirtualMachineConfiguration`.
* Usunięto polecenie cmdlet **Set-AzBatchPoolOSVersion**. Ta operacja nie jest już obsługiwana.
* Usunięto właściwość `TargetOSVersion` z klasy `PSCloudServiceConfiguration`.
* Zmieniono nazwę właściwości `CurrentOSVersion` na `OSVersion` w klasie `PSCloudServiceConfiguration`.
* Usunięto właściwości `DataEgressGiB` i `DataIngressGiB` z klasy `PSPoolUsageMetrics`.
* Usunięto polecenie cmdlet **Get-AzBatchNodeAgentSku** i zastąpiono je poleceniem cmdlet **Get-AzBatchSupportedImage**.
  - Polecenie cmdlet **Get-AzBatchSupportedImage** zwraca te same dane co polecenie cmdlet **Get-AzBatchNodeAgentSku**, ale w bardziej przyjaznym formacie.
  - Teraz są również zwracane nowe obrazy niezweryfikowane. Uwzględniono również dodatkowe informacje na temat właściwości `Capabilities` i `BatchSupportEndOfLife` dla każdego obrazu.
* Dodano możliwość instalowania zdalnych systemów plików na każdym węźle puli za pośrednictwem nowego parametru `MountConfiguration` polecenia cmdlet **New-AzBatchPool**.
* Teraz obsługiwane są reguły zabezpieczeń sieciowych blokujące dostęp sieciowy do puli na podstawie portu źródłowego ruchu. Jest to realizowane za pomocą właściwości `SourcePortRanges` w klasie `PSNetworkSecurityGroupRule`.
* Podczas uruchamiania kontenera usługa Batch obsługuje teraz wykonywanie zadania w katalogu roboczym kontenera lub w katalogu roboczym zadania usługi Batch. Jest to kontrolowane przez właściwość `WorkingDirectory` w klasie `PSTaskContainerSettings`.
* Dodano możliwość określania kolekcji publicznych adresów IP w klasie `PSNetworkConfiguration` za pośrednictwem nowej właściwości `PublicIPs`. To gwarantuje, że węzły w puli będą miały adres IP z listy adresów IP dostarczonych przez użytkownika.
* Gdy nie zostanie określona, wartością domyślną opcji `WaitForSuccess` w klasie `PSSTartTask` jest teraz `$True` (była wartość `$False`).
* Gdy nie zostanie określona, wartością domyślną opcji `Scope` w klasie `PSAutoUserSpecification` jest teraz `Pool` (była wartość `Task` w systemie Windows i `Pool` w systemie Linux).

#### <a name="azcdn"></a>Az.Cdn
* Wprowadzono akcje UrlRewriteAction i CacheKeyQueryStringAction do aparatu RulesEngine.
* Usunięto kilka usterek, takich jak brakujące dane wejściowe „Selector” w poleceniu cmdlet New-AzDeliveryRuleCondition.

#### <a name="azcompute"></a>Az.Compute
* Funkcja zestawu szyfrowania dysków
    - Nowe polecenia cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet
    - Dodano parametr DiskEncryptionSetId do następujących poleceń cmdlet:   Set-AzImageOSDisk, Set-AzVMOSDisk, Set-AzVmssStorageProfile, Add-AzImageDataDisk, New-AzVMDataDisk, Set-AzVMDataDisk, Add-AzVMDataDisk, Add-AzVmssDataDisk i Add-AzVmssVMDataDisk
    - Dodano parametry DiskEncryptionSetId i EncryptionType do następujących poleceń cmdlet:   New-AzDiskConfig   New-AzSnapshotConfig
* Dodano parametr Add PublicIPAddressVersion do polecenia cmdlet New-AzVmssIPConfig
* Właściwość FileUris rozszerzenia niestandardowego skryptu przeniesiono z ustawienia publicznego do ustawienia chronionego
* Dodano parametr ScaleInPolicy do poleceń cmdlet New-AzVmss, New-AzVmssConfig i Update-AzVmss
* Zmiany powodujące niezgodność
    - Parametr UploadSizeInBytes jest używany zamiast parametru DiskSizeGB dla polecenia cmdlet New-AzDiskConfig, gdy opcja CreateOption ma wartość Upload
    - Element PublishingProfile.Source.ManagedImage.Id został zastąpiony elementem StorageProfile.Source.Id w obiekcie GalleryImageVersion

#### <a name="azdatafactory"></a>Az.DataFactory
* Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.3.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Aktualizacja wersji zestawu SDK ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), wprowadza następujące poprawki
* Unikanie zgłaszania wyjątku, gdy nie można zdeserializować elementu creationtime wpisu kosza lub katalogu.
* Uwidacznianie ustawienia dla limitu czasu żądania w obiekcie adlsclient
* Naprawiono przekazywanie oryginalnej flagi syncflag na potrzeby odzyskiwania badoffset
* Naprawiono klasę EnumerateDirectory, aby pobierała token kontynuacji po sprawdzeniu odpowiedzi
* Usunięto usterkę metody Concat

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Poprawiono różne literówki w module

#### <a name="azhdinsight"></a>Az.HDInsight
* Usunięto usterkę polegającą na tym, że klient otrzymywał błąd „Nieprawidłowy ciąg Base-64” podczas używania polecenia cmdlet Get-AzHDInsightCluster do pobrania klastra za pomocą magazynu usługi ADLSGen1.
* Dodano parametr o nazwie „ApplicationId” do trzech poleceń cmdlet: Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig i New-AzHDInsightCluster, aby klient mógł podać identyfikator aplikacji jednostki usługi na potrzeby uzyskiwania dostępu do usługi Azure Data Lake.
* Zmieniono ustawienie Microsoft.Azure.Management.HDInsight z 2.1.0 na 5.1.0
* Usunięto pięć poleceń cmdlet:
    - Get-AzHDInsightOMS
    - Enable-AzHDInsightOMS
    - Disable-AzHDInsightOMS
    - Grant-AzHDInsightRdpServicesAccess
    - Revoke-AzHDInsightRdpServicesAccess
* Dodano trzy polecenia cmdlet:
    - Get-AzHDInsightMonitoring w celu zastąpienia polecenia cmdlet Get-AzHDInsightOMS.
    - Enable-AzHDInsightMonitoring w celu zastąpienia polecenia cmdlet Enable-AzHDInsightOMS.
    - Disable-AzHDInsightMonitoring w celu zastąpienia polecenia cmdlet Disable-AzHDInsightOMS.
* Naprawiono polecenie cmdlet Get-AzHDInsightProperties w celu obsługi pobierania informacji o możliwościach z określonej lokalizacji.
* Usunięto zestawy parametrów („Spark1”, „Spark2”) z polecenia cmdlet Add-AzHDInsightConfigValue.
* Dodano przykłady do dokumentów pomocy polecenia cmdlet Add-AzHDInsightSecurityProfile.
* Zmieniono typ danych wyjściowych następujących poleceń cmdlet:
*  - Typ danych wyjściowych polecenia cmdlet Get-AzHDInsightProperties zmieniono z CapabilitiesResponse na AzureHDInsightCapabilities.
*  - Typ danych wyjściowych polecenia cmdlet Remove-AzHDInsightCluster zmieniono z ClusterGetResponse na bool.
*  - Typ danych wyjściowych polecenia cmdlet Set-AzHDInsightGatewaySettings zmieniono z HttpConnectivitySettings na GatewaySettings.
* Dodano kilka przypadków testowych scenariuszy.
* Usunięto alias: „Add-AzHDInsightConfigValues”, „Get-AzHDInsightProperties”.

#### <a name="aziothub"></a>Az.IotHub
* Zmiany powodujące niezgodność:
    - Polecenie cmdlet „Add-AzIotHubEventHubConsumerGroup” nie obsługuje już parametru „EventHubEndpointName”, a alias nazwy oryginalnego parametru nie został znaleziony.
    - Zestaw parametrów „__AllParameterSets” dla polecenia cmdlet Add-AzIotHubEventHubConsumerGroup został usunięty.
    - Polecenie cmdlet „Get-AzIotHubEventHubConsumerGroup” nie obsługuje już parametru „EventHubEndpointName”, a alias nazwy oryginalnego parametru nie został znaleziony.
    - Zestaw parametrów „__AllParameterSets” dla polecenia cmdlet „Get-AzIotHubEventHubConsumerGroup” został usunięty.
    - Właściwość „OperationsMonitoringProperties” typu „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties” została usunięta.
    - Właściwość „OperationsMonitoringProperties” typu „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties” została usunięta.
    - Polecenie cmdlet „New-AzIotHubExportDevice” nie obsługuje już aliasu „New-AzIotHubExportDevices”.
    - Polecenie cmdlet „New-AzIotHubImportDevice” nie obsługuje już aliasu „New-AzIotHubImportDevices”.
    - Polecenie cmdlet „Remove-AzIotHubEventHubConsumerGroup” nie obsługuje już parametru „EventHubEndpointName”, a alias nazwy oryginalnego parametru nie został znaleziony.
    - Zestaw parametrów „__AllParameterSets” dla polecenia cmdlet „Remove-AzIotHubEventHubConsumerGroup” został usunięty.
    - Polecenie cmdlet „Set-AzIotHub” nie obsługuje już parametru „OperationsMonitoringProperties”, a alias nazwy oryginalnego parametru nie został znaleziony.
    - Zestaw parametrów „UpdateOperationsMonitoringProperties” dla polecenia cmdlet „Set-AzIotHub” został usunięty.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Obsługa przez usługę Azure Site Recovery konfigurowania zasobów sieciowych, takich jak sieciowa grupa zabezpieczeń, publiczny adres IP i wewnętrzne moduły równoważenia obciążenia, dla odzyskiwania z platformy Azure na platformę Azure.
* Obsługa przez usługę Azure Site Recovery zapisu na dysku zarządzanym dla odzyskiwania z programu vMWare na platformę Azure.
* Obsługa przez usługę Azure Site Recovery redukcji karty interfejsu sieciowego dla odzyskiwania z programu vMWare na platformę Azure.
* Obsługa przez usługę Azure Site Recovery przyspieszonej sieci dla odzyskiwania z platformy Azure na platformę Azure.
* Obsługa przez usługę Azure Site Recovery automatycznej aktualizacji agenta dla odzyskiwania z platformy Azure na platformę Azure.
* Obsługa przez usługę Azure Site Recovery dysku SSD w warstwie Standardowa dla odzyskiwania z platformy Azure na platformę Azure.
* Obsługa przez usługę Azure Site Recovery scenariusza dwuprzebiegowego usługi Azure Disk Encryption dla odzyskiwania z platformy Azure na platformę Azure.
* Obsługa przez usługę Azure Site Recovery ochrony nowo dodanych dysków dla odzyskiwania z platformy Azure na platformę Azure.
* Dodano funkcję SoftDelete dla maszyny wirtualnej i dodano testy dla funkcji softdelete

#### <a name="azresources"></a>Az.Resources
* Aktualizacja zestawu zależnego Microsoft.Extensions.Caching.Memory z 1.1.1 do 2.2

#### <a name="aznetwork"></a>Az.Network
* Zmieniono wszystkie polecenia cmdlet dla klasy PrivateEndpointConnection w celu obsługi ogólnego dostawcy usług.
    - Zaktualizowano polecenie cmdlet:
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Set-AzPrivateEndpointConnection
* Dodano nowe polecenie cmdlet dla klasy PrivateLinkResource, które również obsługuje ogólnego dostawcę usług.
    - Nowe polecenie cmdlet:
        - Get-AzPrivateLinkResource
* Dodano nowe pola i parametr dla funkcji protokołu proxy w wersji 2.
    - Dodano właściwość EnableProxyProtocol w klasie PrivateLinkService
    - Dodano właściwość LinkIdentifier w klasie PrivateEndpointConnection
    - Zaktualizowano polecenie cmdlet New-AzPrivateLinkService w celu dodania nowego opcjonalnego parametru EnableProxyProtocol.
* Poprawiono nieprawidłowy opis parametru w dokumentacji referencyjnej polecenia „New-AzApplicationGatewaySku”
* Nowe polecenia cmdlet do obsługi zasad usługi Azure Firewall
* Dodano obsługę zasobu podrzędnego RouteTables klasy VirtualHub
    - Dodano nowe polecenia cmdlet:
        - Add-AzVirtualHubRoute
        - Add-AzVirtualHubRouteTable
        - Get-AzVirtualHubRouteTable
        - Remove-AzVirtualHubRouteTable
        - Set-AzVirtualHub
* Dodano obsługę nowych właściwości Sku klasy VirtualHub i VirtualWANType klasy VirtualWan
    - Zaktualizowano polecenia cmdlet, dodając parametry opcjonalne:
        - New-AzVirtualHub: dodano parametr Sku
        - Update-AzVirtualHub: dodano parametr Sku
        - New-AzVirtualWan: dodano parametr VirtualWANType
        - Update-AzVirtualWan: dodano parametr VirtualWANType
* Dodano obsługę właściwości EnableInternetSecurity dla klas HubVnetConnection, VpnConnection i ExpressRouteConnection
    - Dodano nowe polecenia cmdlet:
        - Update-AzureRmVirtualHubVnetConnection
    - Zaktualizowano polecenia cmdlet, dodając parametry opcjonalne:
        - New-AzureRmVirtualHubVnetConnection: dodano parametr EnableInternetSecurity
        - New-AzureRmVpnConnection: dodano parametr EnableInternetSecurity
        - Update-AzureRmVpnConnection: dodano parametr EnableInternetSecurity
        - New-AzureRmExpressRouteConnection: dodano parametr EnableInternetSecurity
        - Set-AzureRmExpressRouteConnection: dodano parametr EnableInternetSecurity
* Dodano obsługę konfigurowania zasad TopLevel WebApplicationFirewall
    - Dodano nowe polecenia cmdlet:
        - New-AzApplicationGatewayFirewallPolicySetting
        - New-AzApplicationGatewayFirewallPolicyExclusion
        - New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRuleOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRule
        - New-AzApplicationGatewayFirewallPolicyManagedRuleSet
    - Zaktualizowano polecenia cmdlet, dodając parametry opcjonalne:
        - New-AzApplicationGatewayFirewallPolicy: dodano parametr PolicySetting, ManagedRule
* Dodano obsługę operatora dopasowania geograficznego w obiekcie CustomRule
    - Dodano element GeoMatch do operatora w klasie FirewallCondition
* Dodano obsługę zasad zapory perListener i perSite
    - Zaktualizowano polecenia cmdlet, dodając parametry opcjonalne:
        - New-AzApplicationGatewayHttpListener: dodano parametr FirewallPolicy, FirewallPolicyId
        - New-AzApplicationGatewayPathRuleConfig: dodano parametr FirewallPolicy, FirewallPolicyId
* Poprawka wymaganej podsieci o nazwie AzureBastionSubnet w elemencie „PSBastion” może ignorować wielkość liter
* Obsługa docelowych nazw FQDN w regułach sieci i przetłumaczonej nazwy FQDN w regułach translatora adresów sieciowych dla usługi Azure Firewall
* Dodano obsługę zasobu najwyższego poziomu RouteTables klasy IpGroup
    - Dodano nowe polecenia cmdlet:
        - New-AzIpGroup
        - Remove-AzIpGroup
        - Get-AzIpGroup
        - Set-AzIpGroup

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Usunięto polecenie cmdlet Add-AzServiceFabricApplicationCertificate, ponieważ ten scenariusz jest objęty poleceniem Add-AzVmssSecret.

#### <a name="azsql"></a>Az.Sql
* Dodano obsługę przywracania porzuconych baz danych w wystąpieniach zarządzanych.
* Oznaczono jako przestarzałe w kodzie stare polecenia cmdlet inspekcji.
* Usunięto przestarzałe aliasy:
* Get-AzSqlDatabaseIndexRecommendations (zamiast tego użyj Get-AzSqlDatabaseIndexRecommendation)
* Get-AzSqlDatabaseRestorePoints (zamiast tego użyj Get-AzSqlDatabaseRestorePoint)
* Usunięto polecenie cmdlet Get-AzSqlDatabaseSecureConnectionPolicy
* Usunięto aliasy dla przestarzałych poleceń cmdlet ustawień oceny luk w zabezpieczeniach
* Oznaczono jako przestarzałe polecenia cmdlet ustawień zaawansowanego wykrywania zagrożeń
* Dodawanie poleceń cmdlet do wyłączania i włączania zaleceń dotyczących czułości dla kolumn w bazie danych.

#### <a name="azstorage"></a>Az.Storage
* Obsługa włączania dużego udziału plików podczas tworzenia lub aktualizowania konta magazynu
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Podczas zamykania/uzyskiwania dojścia do pliku pomiń sprawdzanie, czy ścieżka danych wejściowych jest ścieżką pliku, czy plikiem, aby uniknąć błędu obiektu w stanie DeletePending
    -  Get-AzStorageFileHandle
    -  Close-AzStorageFileHandle

## <a name="280---october-2019"></a>2.8.0 — październik 2019 r.
### <a name="general"></a>Ogólne
* Wydanie Az.HealthcareApis 1.0.0

#### <a name="azaccounts"></a>Az.Accounts
* Aktualizacja telemetrii i ponowne zapisywanie adresów URL dla wygenerowanych modułów oraz naprawa testów jednostkowych systemu Windows.

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Set-AzApiManagementApi** — Dodano obsługę aktualizowania interfejsu API do właściwości ApiVersionSet
    - Rozwiązano problem https://github.com/Azure/azure-powershell/issues/10068

#### <a name="azautomation"></a>Az.Automation
* Naprawiono parametr ponownego uruchamiania polecenia cmdlet New-AzureAutomationSoftwareUpdateConfiguration dla systemu Linux.

#### <a name="azbatch"></a>Az.Batch
* Polecenie **Get-AzBatchNodeAgentSku** jest przestarzałe i zostanie zastąpione poleceniem **Get-AzBatchSupportImage** w wersji 2.0.0.

#### <a name="azcompute"></a>Az.Compute
* Dodano parametry Priority, EvictionPolicy i MaxPrice do poleceń cmdlet New-AzVM i New-AzVmss
* Naprawiono komunikat ostrzegawczy i dokumentację pomocy dla poleceń Add-AzVMAdditionalUnattendContent i Add-AzVMSshPublicKey
* Naprawiono wyjątek -skipVmBackup dla maszyn wirtualnych z systemem Linux z dyskami zarządzanymi dla polecenia Set-AzVMDiskEncryptionExtension.
* Naprawiono usterkę w ustawieniach szyfrowania aktualizacji w scenariuszu dwuprzebiegowym polecenia Set-AzVMDiskEncryptionExtension.

#### <a name="azdatafactory"></a>Az.DataFactory
* Dodano polecenia CRUD dla przepływu danych usługi ADF w wersji 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow i Get-AzDataFactoryV2DataFlow.
* Dodano polecenia akcji dla sesji debugowania przepływu danych usługi ADF w wersji 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand i Stop-AzDataFactoryV2DataFlowDebugSession.
* Zaktualizowano zestaw .Net SDK usługi ADF do wersji 4.2.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Naprawiono weryfikację kont, aby umożliwić przekazywanie kont ze znakiem „-” bez domeny

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Zaktualizowano program PowerShell do wersji 1.0.0
* Zaktualizowano zestaw SDK do wersji 1.0.2
* Zaktualizowano testy, aby odwoływały się do nowej wersji zestawu SDK
* Zaktualizowano strukturę wyjściową z zagnieżdżonej do spłaszczonej.

#### <a name="aziothub"></a>Az.IotHub
* Dodano nowe źródło routingu: DigitalTwinChangeEvents
* Drobna poprawka usterki: Polecenie Get-AzIothub nie zwraca wartości subscriptionId

#### <a name="azmonitor"></a>Az.Monitor
* Dodano nowe odbiorniki grupy akcji dla grupy akcji -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver
* Włączono korzystanie z typowych schematów alertów dla odbiorników. Nie dotyczy to odbiorników wiadomości SMS, powiadomień push usługi Azure App , narzędzia ITSM i połączeń głosowych
* Elementy webhook obsługują teraz również uwierzytelnianie za pomocą usługi Azure Active Directory.

#### <a name="aznetwork"></a>Az.Network
* Dodano nowe polecenie cmdlet Get-AzAvailableServiceAlias, które można wywołać, aby pobrać aliasy do użytku z zasadami punktu końcowego dostawcy.
* Dodano obsługę dodawania selektorów ruchu do połączeń bramy sieci wirtualnej
    - Dodano nowe polecenia cmdlet:
        - New-AzureRmTrafficSelectorPolicy
    - Polecenia cmdlet zostały zaktualizowane o opcjonalny parametr -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection
* Dodano obsługę protokołów ESP i AH do konfiguracji reguł zabezpieczeń sieci
    - Zaktualizowano następujące polecenia cmdlet:
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* Poprawiono obsługę wyjątków w poleceniach cmdlet usługi Cortex
* Dodano nowe generacje i jednostki SKU dla elementów VirtualNetworkGateway
  - Wprowadzono nowe generacje dla elementów VirtualNetworkGateway.
  - Wprowadzono nowe jednostki SKU o wysokiej przepływności dla elementów VirtualNetworkGateway.

#### <a name="azrediscache"></a>Az.RedisCache
* Zaktualizowano dokumentację referencyjną polecenia „Set-AzRedisCache” w celu uwzględnienia brakujących wartości parametru „-Size”

#### <a name="azsql"></a>Az.Sql
* Dodano obsługę ustawiania administratora usługi Active Directory w wystąpieniu zarządzanym

#### <a name="azstorage"></a>Az.Storage
* Uaktualniono bibliotekę klienta usługi Azure Storage do wersji 11.1.0
* Utworzenie listy kontenerów przy użyciu interfejsu API płaszczyzny zarządzania spowoduje wyświetlenie listy przy użyciu właściwości NextPageLink
    -  Get-AzRmStorageContainer
* Utworzenie listy kont magazynu z subskrypcji spowoduje wyświetlenie listy przy użyciu właściwości NextPageLink
    -  Get-AzStorageAccount

#### <a name="azstoragesync"></a>Az.StorageSync
* Naprawiono problem 9810 w poleceniu Reset-AzStorageSyncServerCertificate.

#### <a name="azwebsites"></a>Az.Websites
* Aktualizowanie elementu ASP aplikacji przy użyciu polecenia Set-AzWebApp kończyło się niepowodzeniem

## <a name="270---september-2019"></a>2.7.0 — wrzesień 2019 r.
#### <a name="azapimanagement"></a>Az.ApiManagement
* Aktualizacja opisu parametru „-Format” w dokumentacji referencyjnej polecenia „Set-AzApiManagementPolicy”
* Usunięto z dokumentacji referencyjnej odwołania do przestarzałego polecenia cmdlet „Update-AzApiManagementDeployment”. Zamiast niego należy używać polecenia „Set-AzApiManagement”.

#### <a name="azautomation"></a>Az.Automation
* Poprawiono literówkę w przykładzie w dokumentacji referencyjnej polecenia „Register-AzAutomationDscNode”
* Dodano wyjaśnienie dotyczące ograniczeń systemu operacyjnego dla polecenia Register-AzAutomationDSCNode
* Naprawiono wyjątek odwołania o wartości null dla opcji -Wait polecenia cmdlet Start-AzAutomationRunbook.

#### <a name="azcompute"></a>Az.Compute
* Dodanie parametru UploadSizeInBytes do polecenia New-AzDiskConfig
* Dodanie parametru Incremental do polecenia New-AzSnapshotConfig
* Dodanie funkcji maszyny wirtualnej o niskim priorytecie:
    - do polecenia New-AzVMConfig dodano parametry MaxPrice, EvictionPolicy i Priority.
    - Parametr MaxPrice został dodany do poleceń cmdlet New-AzVmssConfig, Update-AzVM i Update-AzVmss.
* Rozwiązanie problemu z odwołaniem do maszyny wirtualnej dla polecenia cmdlet Get-AzAvailabilitySet, gdy wyświetla listę wszystkich zestawów dostępności w subskrypcji.
* Naprawienie wyjątku o wartości null dla polecenia Get-AzRemoteDesktopFile.
* Naprawienie metody przeszukiwania wirtualnego dysku twardego dla pozycji względem końca.
* Rozwiązanie problemu z dyskami UltraSSD dla poleceń New-AzVM i Update-AzVM.

#### <a name="azdatafactory"></a>Az.DataFactory
* Dodanie 3 nowych poleceń do usługi ADF w wersji 2 — Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription i Get-AzDataFactoryV2TriggerSubscriptionStatus
* Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.3

#### <a name="azhdinsight"></a>Az.HDInsight
* Wywołanie zmian powodujących niezgodność

#### <a name="aziothub"></a>Az.IotHub
* Dodanie obsługi w celu wywołania trybu failover dla usługi IotHub do sparowanego geograficznie regionu odzyskiwania po awarii.
* Dodanie obsługi do zarządzania wzbogacaniem komunikatów dla usługi IotHub. Nowe polecenia cmdlet:
    - Add-AzIotHubMessageEnrichment
    - Get-AzIotHubMessageEnrichment
    - Remove-AzIotHubMessageEnrichment
    - Set-AzIotHubMessageEnrichment

#### <a name="azmonitor"></a>Az.Monitor
* Wskazanie najnowszego zestawu Monitor SDK, tj. 0.24.1-preview
   - Dodaje zmiany niepowodujące niezgodności do poleceń cmdlet metryk, tj. wyliczenie Unit obsługuje kilka nowych wartości. Są to polecenia cmdlet tylko do odczytu, więc nie będzie żadnych zmian w danych wejściowych tych poleceń cmdlet.
   - Wartość api-version żądań **ActionGroups** to teraz **2019-06-01**, wcześniej było to **2018-03-01**. Testy scenariusza zostały zaktualizowane w celu dostosowania do tej zmiany.
   - Konstruktory dla klas **EmailReceiver** i **WebhookReceiver** dodały jeden nowy argument obowiązkowy, tj. wartość logiczną o nazwie **useCommonAlertSchema**. Obecnie wartość ta jest stała i równa **false**, aby ukryć tę zmianę powodującą niezgodność przed poleceniami cmdlet. **UWAGA**: Jest to tymczasowa zmiana, która musi być zweryfikowana przez zespół ds. alertów.
   - Kolejność argumentów konstruktora klasy **Source** (powiązanej z klasą **ScheduledQueryRuleSource**) zmieniła się od poprzedniego zestawu SDK. Ta zmiana wymaga naprawienia dwóch testów jednostkowych: kompilowały się, ale nie przechodziły testów.
   - Kolejność argumentów konstruktora klasy **AlertingAction** (powiązanej z klasą **ScheduledQueryRuleSource**) została zmieniona od poprzedniego zestawu SDK. Ta zmiana wymaga naprawienia dwóch testów jednostkowych: kompilowały się, ale nie przechodziły testów.
* Obsługa kryteriów progu dynamicznego dla alertu metryki w wersji 2
    - New-AzMetricAlertRuleV2Criteria: teraz tworzy kryteria progów dynamicznych
    - Add-AzMetricAlertRuleV2: teraz akceptuje kryteria progów dynamicznych
* Ulepszenia poleceń cmdlet reguły zaplanowanego zapytania (SQR)
 - Polecenia cmdlet będą akceptować parametr „Location” w obu formatach: jako lokalizację (np. eastus) i jako nazwę wyświetlaną lokalizacji (np. East US)
 - Poprawnie zilustrowano parametr „Enabled” w plikach pomocy
 - Dodano przykłady dla opcjonalnego parametru „ActionGroup”
 - Ogólnie ulepszono pliki pomocy
* Naprawienie usterki dotyczącej określania typu zakresu dla polecenia „Set-AzActionRule”

#### <a name="aznetwork"></a>Az.Network
* Naprawienie nieprawidłowego przykładu w dokumentacji referencyjnej polecenia „New-AzApplicationGateway”
* Dodanie w dokumentacji referencyjnej polecenia „Get-AzNetworkWatcherPacketCapture” uwagi dotyczącej pobierania wszystkich właściwości na potrzeby przechwytywania pakietów
* Naprawiono przykład w dokumentacji referencyjnej polecenia „Test-AzNetworkWatcherIPFlow”, aby poprawnie wyliczał karty sieciowe
* Ulepszono analizę wyjątku w chmurze, aby wyświetlane były dodatkowe szczegóły, jeśli są obecne
* Ulepszono analizę wyjątku w chmurze, aby był obsługiwany dodatkowy typ wyjątku zestawu SDK
* Naprawiono niepoprawne mapowanie modeli reguł zabezpieczeń
* Dodano właściwości interfejsu sieciowego dla funkcji prywatnego adresu IP
    - Dodano właściwość „PrivateEndpoint” jako typ PSResourceId do elementu PSNetworkInterface
    - Dodano właściwość „PrivateLinkConnectionProperties” jako typ PSIpConfigurationConnectivityInformation do elementu PSNetworkInterfaceIPConfiguration
    - Dodano nową klasę modelu PSIpConfigurationConnectivityInformation
* Dodano nowy typ ApplicationRuleProtocolType „mssql” dla zasobu usługi Azure Firewall
* Obsługa linku wielokrotnego w wirtualnej sieci WAN
    - Nowe polecenia cmdlet
        - New-AzVpnSiteLink
        - New-AzVpnSiteLinkConnection
    - Zaktualizowano polecenie cmdlet:
        - New-VpnSite
        - Update-VpnSite
        - New-VpnConnection
        - Update-VpnConnection
* Niektóre dokumenty dla przykładów programu PowerShell naprawiono w taki sposób, aby były w nich używane polecenia cmdlet Az zamiast poleceń cmdlet AzureRM

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Aktualizacja obiektu AzureVMpolicy o atrybut ProtectedItemsCount
* Dodano testy dotyczące zasad maszyny wirtualnej i przywracania oryginalnego konta magazynu

#### <a name="azresources"></a>Az.Resources
* Naprawienie usterki polegającej na tym, że nie można było wywołać polecenia New-AzRoleAssignment bez parametru Scope.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Poprawiono literówkę w przykładzie w dokumentacji referencyjnej polecenia „Update-AzServiceFabricReliability”
* Dodanie nowych poleceń cmdlet do zarządzania aplikacją i usługami:
    - New-AzServiceFabricApplication
    - New-AzServiceFabricApplicationType
    - New-AzServiceFabricApplicationTypeVersion
    - New-AzServiceFabricService
    - Update-AzServiceFabricApplication
    - Get-AzServiceFabricApplication
    - Get-AzServiceFabricApplicationType
    - Get-AzServiceFabricApplicationTypeVersion
    - Get-AzServiceFabricService
    - Remove-AzServiceFabricApplication
    - Remove-AzServiceFabricApplicationType
    - Remove-AzServiceFabricApplicationTypeVersion
    - Remove-AzServiceFabricServic
* Uaktualniono zestaw Service Fabric SDK do wersji 1.2.0, która korzysta z dostawcy zasobów usługi Service Fabric o wersji interfejsu API 2019-03-01.

#### <a name="azsignalr"></a>Az.SignalR
* Dodanie poleceń cmdlet Update, Restart, CheckNameAvailability i GetUsage

#### <a name="azsql"></a>Az.Sql
* Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzSqlElasticPool”
* Dodano przykład dla rdzenia wirtualnego do tworzenia elastycznej puli (New-AzSqlElasticPool).
* Usunięcie weryfikacji parametru EmailAddresses i sprawdzania, czy parametr EmailAdmins nie ma wartości false w przypadku, gdy parametr EmailAddresses jest pusty w poleceniach Set-AzSqlServerAdvancedThreatProtectionPolicy i Set-AzSqlDatabaseAdvancedThreatProtectionPolicy
* Włączono usuwanie ustawień inspekcji serwera/bazy danych, gdy istnieje wiele ustawień diagnostycznych włączających kategorię inspekcji.
* Naprawa weryfikacji adresów e-mail w wielu poleceniach cmdlet do oceny luk w zabezpieczeniach SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting i Update-AzSqlInstanceVulnerabilityAssessmentSetting).

#### <a name="azstorage"></a>Az.Storage
* Zaktualizowano przykład w dokumentacji referencyjnej dla polecenia „Get-AzStorageAccountKey”
* Obsługa zachowywania w pliku docelowym właściwości SMB pliku źródłowego przy przekazywaniu/pobieraniu pliku platformy Azure (atrybuty pliku, czas utworzenia pliku, czas ostatniego zapisu pliku)
    -  Set-AzStorageFileContent
    -  Get-AzStorageFileContent
* Naprawa awarii przekazywania blokowego obiektu blob z właściwościami/metadanymi dla elementu ImmutabilityPolicy z obsługą kontenerów.
    -  Set-AzStorageBlobContent
* Obsługa zarządzania udziałami plików platformy Azure za pomocą interfejsu API płaszczyzny zarządzania
    -  New-AzRmStorageShare
    -  Get-AzRmStorageShare
    -  Update-AzRmStorageShare
    -  Remove-AzRmStorageShare

#### <a name="azwebsites"></a>Az.Websites
* Naprawa problemu polegającego na tym, że tagi webapp były usuwane podczas migracji aplikacji do nowej platformy ASP
* Naprawa polecenia Publish-AzureWebapp w taki sposób, aby działało w systemach Linux i Windows
* Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzWebAppPublishingProfile”

## <a name="260---august-2019"></a>2.6.0 — sierpień 2019 r.
#### <a name="general"></a>Ogólne
* Naprawiono różne literówki w wielu modułach

#### <a name="azaccounts"></a>Az.Accounts
* Obsługa pliku MSI przypisanego przez użytkownika w ramach uwierzytelniania usługi Azure Functions (nr 9479)

#### <a name="azaks"></a>Az.Aks
* Rozwiązano problem z danymi wyjściowymi polecenia „Get-AzAks”
    * Więcej informacji: https://github.com/Azure/azure-powershell/issues/9847

#### <a name="azapimanagement"></a>Az.ApiManagement
* Rozwiązano problem https://github.com/Azure/azure-powershell/issues/9351
    - Zaktualizowano wersję nuget .net, która nie wymusza ograniczeń dotyczących identyfikatorów productId, apiId, groupId i userId
* **Get-AzApiManagementProduct** — dodano obsługę wysyłania zapytań dotyczących produktów przy użyciu interfejsu API.
  https://github.com/Azure/azure-powershell/issues/9482
* **New-AzApiManagementApiRevision** — poprawka rozwiązująca problem polegający na tym, że wartość ApiRevisionDescription nie była ustawiana podczas tworzenia nowej wersji pomocniczej interfejsu API https://github.com/Azure/azure-powershell/issues/9752
* Poprawiono literówkę w modelu „PsApiManagementOAuth2AuthrozationServer” na „PsApiManagementOAuth2AuthorizationServer”

#### <a name="azbatch"></a>Az.Batch
* Poprawiono literówkę w komunikacie pomocy i dokumentacji, zmieniając literę w nazwie systemu Windows na wielką

#### <a name="azcdn"></a>Az.Cdn
* Poprawiono literówkę w pomocniku konwersji modułu CDN

#### <a name="azcompute"></a>Az.Compute
* Dodanie polecenia VmssId to New-AzVMConfig
* Dodanie parametrów TerminateScheduledEvents i TerminateScheduledEventNotBeforeTimeoutInMinutes do polecenia New-AzVmssConfig and Update-AzVmss
* Dodanie właściwości HyperVGeneration do obiektu obrazu maszyny wirtualnej
* Dodanie funkcji Host i HostGroup
    - Nowe polecenia cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost
    - Dodano parametr HostId do poleceń New-AzVMConfig i New-AzVM
* Aktualizacja przykładu w dokumentacji polecenia „Invoke-AzVMRunCommand” w celu użycia poprawnej nazwy parametru
* Aktualizacja opisu parametru „-VolumeType” w dokumentacji referencyjnej poleceń „Set-AzVMDiskEncryptionExtension” i „Set-AzVmssDiskEncryptionExtension”

#### <a name="azdatafactory"></a>Az.DataFactory
* Poprawiono literówkę w poleceniu „New-AzDataFactoryEncryptValue”, zmieniając literę w nazwie systemu Windows na wielką
* Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.2
* Dodanie parametrów „DataProxyIntegrationRuntimeName”, „DataProxyStagingLinkedServiceName” i „DataProxyStagingPath” dla polecenia „Set-AzureRmDataFactoryV2IntegrationRuntime”, aby umożliwić konfigurowanie własnego środowiska Integration Runtime jako serwera proxy dla środowiska SSIS Integration Runtime
* Zaktualizowano PSTriggerRun na potrzeby wyświetlania wyzwalanych potoków, komunikatów i właściwości, a także PSActivityRun na potrzeby wyświetlania typu działania

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Poprawiono wysunięcie polecenia Get-DataLakeStoreDeletedItem pod kątem obsługi błędów lub wyjątków zdalnych.

#### <a name="azeventhub"></a>Az.EventHub
* Rozwiązano problem nr 9658: Literówka VirtualNteworkRule w poleceniu Set-AzEventHubNetworkRuleSet
* Rozwiązano problem nr 9558: Polecenie Set-AzEventHubNamespace używa elementu PATCH zamiast PUT
* dodano parametr EnableKafka do polecenia cmdlet Set-AzEventHubNamespace
* Rozwiązano problem nr 9786: nie można utworzyć reguły z prawami tylko do nasłuchiwania

#### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* Poprawiono literówkę w dokumentacji: „Azure” rozpoczynające się małą literą

#### <a name="azmonitor"></a>Az.Monitor
* Poprawiono niepoprawną nazwę parametru w dokumentacji pomocy

#### <a name="aznetwork"></a>Az.Network
* Zaktualizowano polecenie New-AzPrivateLinkServiceIpConfig
    - Sklasyfikowano parametr „PublicIpAddress” jako przestarzały, ponieważ nie jest on nigdy używany po stronie serwera.
    - Dodano jeden opcjonalny parametr „Primary” wskazujący, czy bieżąca konfiguracja IP jest podstawowa, czy nie.
* Ulepszono obsługę wyjątku błędu żądania z zestawu SDK — rozwiązuje to problem polegający na tym, że poprzednio wyjątki zestawu SDK nie były poprawnie obsługiwane, wskutek czego nie były wyświetlane kluczowe szczegóły błędu
* Skorygowano logikę weryfikacji prefiksu IP w wersji IPv6 w celu sprawdzania, czy długość prefiksu IPv6 jest poprawna.
* Zaktualizowano polecenie Get-AzVirtualNetworkSubnetConfig: Dodano parametr ustawiany w celu pobrania identyfikatora zasobu podsieci.
* Zaktualizowano opis parametru Location dla AzNetworkServiceTag

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Zaktualizowano dokumentację polecenia „New-AzOperationalInsightsLinuxSyslogDataSource”
    - Dodano przykład
    - Zaktualizowano opis parametru „-Name”
* Dodano przykład dla polecenia New-AzOperationalInsightsWindowsEventDataSource
* Zaktualizowano opis parametru „-Name” dla polecenia New-AzOperationalInsightsWindowsEventDataSource

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Aktualizacja polecenia „Get-AzRecoveryServicesBackupJobDetail.md”

#### <a name="azresources"></a>Az.Resources
* Dodano obsługę nowej wersji interfejsu API (2019-05-10) dla Microsoft.Resource
    - Dodano obsługę „copy.count = 0” dla zmiennych, zasobów i właściwości
    - Zasoby z ustawieniami „condition = false” lub „copy.count = 0” będą usuwane w trybie ukończenia
* Dodanie do dokumentu pomocy przykładu przypisywania zasad na poziomie subskrypcji

#### <a name="azservicebus"></a>Az.ServiceBus
* Rozwiązano problem nr 9658: Literówka VirtualNetworkRule w poleceniu Set-AzServiceBusNetworkRuleSet
* Rozwiązano problem nr 9786: nie można utworzyć reguły z prawami tylko do nasłuchiwania
* Dodano nowe polecenie „Test-AzServiceBusNameAvailability” do sprawdzania dostępności nazwy dla kolejki i tematu

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Usunięcie usterek poleceń cmdlet dodawania typu węzła:
    - Usterka NullReferenceException, gdy grupa zasobów ma inny zestaw VMSS niezwiązany z klastrem usługi Service Fabric. Rozwiązanie problemu: https://github.com/Azure/azure-powershell/issues/8681
    - Usunięcie usterki powodującej niepowodzenie polecenia cmdlet, gdy sieć wirtualna znajdowała się w innej grupie zasobów niż klaster. rozwiązanie problemu: https://github.com/Azure/azure-powershell/issues/8407
    - Sklasyfikowanie polecenia cmdlet Add-AzServiceFabricApplicationCertificate jako przestarzałego

#### <a name="azsql"></a>Az.Sql
* Aktualizacja dokumentacji starych poleceń cmdlet inspekcji.

#### <a name="azstorage"></a>Az.Storage
* Aktualizacja pomocy dotyczącej poleceń Get/Close-AzStorageFileHandle, przez dodanie kolejnych scenariuszy do przykładów dotyczących poleceń cmdlet i zaktualizowanie opisów parametrów
* Obsługa StandardBlobTier w ramach przekazywania i kopiowania obiektów blob
    -  Set-AzStorageBlobContent
    -  Start-AzStorageBlobCopy
* Obsługa priorytetu ponownego wypełniania w ramach kopiowania obiektów blob
    -  Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* Dodanie wyjaśnienia do parametru -AppSettings w poleceniach Set-AzWebApp i Set-AzWebAppSlot

## <a name="250---july-2019"></a>2.5.0 — lipiec 2019
#### <a name="azaccounts"></a>Az.Accounts
* Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta

#### <a name="azapplicationinsights"></a>Az.ApplicationInsights
* Poprawienie pisowni w przykładzie w dokumentacji polecenia „Remove-AzApplicationInsightsApiKey”

#### <a name="azautomation"></a>Az.Automation
* Poprawienie pisowni w ciągu zasobu

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Dodano obsługę właściwości NetworkRuleSet.

#### <a name="azcompute"></a>Az.Compute
* Dodanie brakujących właściwości (ComputerName, OsName, OsVersion i HyperVGeneration) obiektu widoku wystąpienia maszyny wirtualnej.

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Poprawienie pisowni parametru Replication w opisie polecenia Remove-AzContainerRegistryReplication
    - Więcej informacji można znaleźć tutaj: https://github.com/Azure/azure-powershell/issues/9633

#### <a name="azdatafactory"></a>Az.DataFactory
* Zaktualizowano wersję zestawu ADF .Net SDK do 4.1.0
* Poprawienie pisowni w dokumentacji dla polecenia „Get-AzDataFactoryV2PipelineRun”

#### <a name="azeventhub"></a>Az.EventHub
* Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzEventHubAuthorizationRuleSASToken
* Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”

#### <a name="azkeyvault"></a>Az.KeyVault
* Dodano obsługę określania rozmiaru klucza dla zasad certyfikatów

#### <a name="azlogicapp"></a>Az.LogicApp
* Poprawienie polecenia Get-AzIntegrationAccountMap tak, aby wyświetlało listę wszystkich typów map
    - Dodano nowy parametr MapType na potrzeby filtrowania

#### <a name="azmanagedservices"></a>Az.ManagedServices
* Dodano obsługę interfejsu API w wersji 2019-06-01 (ogólna dostępność)

#### <a name="aznetwork"></a>Az.Network
* Dodanie obsługi prywatnego punktu końcowego i prywatnej usługi łączenia
    - Nowe polecenia cmdlet
        - Set-AzPrivateEndpoint
        - Set-AzPrivateLinkService
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Test-AzPrivateLinkServiceVisibility
        - Get-AzAutoApprovedPrivateLinkService
* Zaktualizowano poniższe polecenia dla funkcji: Flaga PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies w podsieci w sieci wirtualnej
    - Zaktualizowano polecenia New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig
        - Dodano opcjonalny parametr -PrivateEndpointNetworkPoliciesFlag, który konfiguruje, czy stosować zasady sieciowe w prywatnym punkcie końcowym w tej podsieci.
        - Dodano opcjonalny parametr -PrivateLinkServiceNetworkPoliciesFlag, który konfiguruje, czy stosować zasady sieciowe w usłudze łącza prywatnego w tej podsieci.
* Nazwa parametru „ServiceName” polecenia cmdlet AzPrivateLinkService została zmieniona na „Name” z aliasem „ServiceName” w celu zachowania zgodności z poprzednimi wersjami
* Włączenie protokołu ICMP dla konfiguracji reguł zabezpieczeń sieci
    - Zaktualizowano następujące polecenia cmdlet
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* Dodanie wartości ConnectionProtocolType (Ikev1/Ikev2) jako konfigurowalnego parametru dla polecenia New-AzVirtualNetworkGatewayConnection
* Dodanie parametru PrivateIpAddressVersion w elemencie LoadBalancerFrontendIpConfiguration
    - Zaktualizowano polecenie cmdlet:
        - New-AzLoadBalancerFrontendIpConfig
        - Add-AzLoadBalancerFrontendIpConfig
        - Set-AzLoadBalancerFrontendIpConfig
* Aktualizacja polecenia New-AzApplicationGatewayProbeConfig usługi Application Gateway o obsługę portu niestandardowego w sondzie
    - Aktualizacja polecenia New-AzApplicationGatewayProbeConfig: Dodano opcjonalny parametr Port, który służy do sondowania serwera zaplecza. Ten parametr ma zastosowanie w przypadku jednostek SKU Standard_V2 i WAF_V2.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Zaktualizowano domyślną wersję zapisywanych wyszukiwań na 1.
* Poprawiono obsługę wyrażeń regularnych o wartości null dla dzienników niestandardowych

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Aktualizacja pliku „Get-AzRecoveryServicesBackupJob.md”
* Aktualizacja pliku „Get-AzRecoveryServicesBackupContainer.md”
* Aktualizacja pliku „Get-AzRecoveryServicesVault.md”
* Aktualizacja pliku „Wait-AzRecoveryServicesBackupJob.md”
* Aktualizacja pliku „Set-AzRecoveryServicesVaultContext.md”
* Aktualizacja pliku „Get-AzRecoveryServicesBackupItem.md”
* Aktualizacja pliku „Get-AzRecoveryServicesBackupRecoveryPoint.md”
* Aktualizacja pliku „Restore-AzRecoveryServicesBackupItem.md”
* Zaktualizowano wywołanie usługi do wyrejestrowywania kontenera dla udziału plików platformy Azure
* Aktualizacja pliku „Set-AzRecoveryServicesAsrAlertSetting.md”

#### <a name="azresources"></a>Az.Resources
- Usunięcie brakującego polecenia cmdlet przywoływanego w dokumentacji polecenia „New-AzResourceGroupDeployment”
- Zaktualizowano polecenia cmdlet zasad w celu używania nowego interfejsu API w wersji 2019-01-01

#### <a name="azservicebus"></a>Az.ServiceBus
* Dodano nowe polecenie cmdlet do generowania tokenu SAS: New-AzServiceBusAuthorizationRuleSASToken
* Dodano weryfikację i komunikat o błędzie dla praw reguł autoryzacji, jeśli przypisane jest tylko prawo „Manage”

#### <a name="azsql"></a>Az.Sql
* Poprawienie brakujących przykładów dla polecenia cmdlet Set-AzSqlDatabaseSecondary
* Poprawienie ustawiania cyklicznego skanowania przez rozszerzenie Ocena luk w zabezpieczeniach bez podawania żadnego adresu e-mail
* Poprawienie pisowni w komunikacie ostrzegawczym.

#### <a name="azstorage"></a>Az.Storage
* Aktualizacja przykładu w dokumentacji referencyjnej polecenia „Get-AzStorageAccount” w celu użycia poprawnej nazwy parametru

#### <a name="azstoragesync"></a>Az.StorageSync
* Dodanie polecenia cmdlet Invoke-AzStorageSyncChangeDetection.
* Rozwiązanie problemu 9551 dotyczącego respektowania wartości TierFilesOlderThanDays

#### <a name="azwebsites"></a>Az.Websites
* Usunięcie usterki polegającej na tym, że niektóre właściwości SiteConfig nie były zwracane przez polecenia Get-AzWebApp i Set-AzWebApp
* Dodanie nowego parametru Location dla poleceń Get-AzDeletedWebApp i Restore-AzDeletedWebApp
* Usunięcie usterki związanej z klonowaniem miejsc aplikacji internetowych przy użyciu polecenia New-AzWebApp -IncludeSourceWebAppSlots

## <a name="240---july-2019"></a>2.4.0 — czerwiec 2019 r.
#### <a name="azaccounts"></a>Az.Accounts
* Dodano obsługę poleceń cmdlet profilu
* Dodano obsługę środowisk i płaszczyzn danych w generowanych poleceniach cmdlet
* Naprawiono błąd polegający na tym, że w niektórych przypadkach dla poleceń cmdlet płaszczyzny danych w programie Windows PowerShell był używany nieprawidłowy punkt końcowy

#### <a name="azadvisor"></a>Az.Advisor
* Wersja ogólnodostępna modułu Az.Advisor
* Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`

#### <a name="azapimanagement"></a>Az.ApiManagement
* Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8671
    - **Get-AzApiManagementSubscription**
        - Dodano obsługę wykonywania zapytań dotyczących subskrypcji według użytkownika i produktu
        - Dodano obsługę wykonywania zapytań przy użyciu zakresu „/”, „/apis”, „/apis/echo-api”
* Rozwiązano problemy https://github.com/Azure/azure-powershell/issues/9307 i https://github.com/Azure/azure-powershell/issues/8432
    - **Import-AzApiManagementApi**
        - Dodano obsługę określania właściwości „ApiVersion” i „ApiVersionSetId” podczas importowania interfejsów API

#### <a name="azautomation"></a>Az.Automation
* Usunięto usterkę polecenia cmdlet Set-AzAutomationConnectionFieldValue w celu obsługi wartości ciągu.

#### <a name="azcompute"></a>Az.Compute
* Dodano parametr HyperVGeneration do polecenia New-AzImageConfig

#### <a name="azdatafactory"></a>Az.DataFactory
* Aktualizowanie danych wyjściowych poleceń cmdlet pobierania uruchomień działań, pobierania uruchomień potoków i pobierania uruchomień wyzwalaczy usługi ADF w celu obsługi potoku Select-Object.

#### <a name="azeventgrid"></a>Az.EventGrid
* Poprawiono literówkę w dokumentacji polecenia New-AzEventGridSubscription

#### <a name="aziothub"></a>Az.IotHub
* Dodano obsługę ponownego generowania kluczy zasad autoryzacji.

#### <a name="aznetwork"></a>Az.Network
* Dodano właściwość „RoutingPreference” do tagów publicznych adresów IP
* Poprawiono przykłady dla dokumentacji referencyjnej polecenia „Get-AzNetworkServiceTag”

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Rozwiązano problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyState
    - Więcej informacji: https://github.com/Azure/azure-powershell/issues/9446

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Naprawiono model źródła danych CustomLog zwracany w poleceniu Get-AzOperationalInsightsDataSource

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Poprawka dotycząca polecenia get-policy dla maszyn wirtualnych IaaS

#### <a name="azresources"></a>Az.Resources
    - Poprawiono tekst pomocy dotyczącej parametru -Top polecenia Get-AzPolicyState
    - Dodano obsługę stronicowania po stronie klienta dla polecenia Get-AzPolicyAlias
    - Dodano nowe parametry dla polecenia Set-AzPolicyAssignment: -PolicyParameters i -PolicyParametersObject
    - Aktualizacje dokumentacji i przykładów dla poleceń cmdlet zasad

#### <a name="azservicebus"></a>Az.ServiceBus
* Poprawka rozwiązująca problem #4938 — polecenie New-AzureRmServiceBusQueue zwraca wynik BadRequest w przypadku ustawienia właściwości MaxSizeInMegabytes

#### <a name="azsql"></a>Az.Sql
* Dodano polecenia cmdlet grupy trybu failover wystąpienia z wersji zapoznawczej do wersji publicznej
* Obsługa inspekcji w usłudze Azure SQL Server/Database za pomocą nowych poleceń cmdlet.
    - Set-AzSqlServerAudit
    - Get-AzSqlServerAudit
    - Remove-AzSqlServerAudit
    - Set-AzSqlDatabaseAudit
    - Get-AzSqlDatabaseAudit
    - Remove-AzSqlDatabaseAudit
* Usunięto ograniczenia wiadomości e-mail z ustawień oceny luk w zabezpieczeniach

#### <a name="azstorage"></a>Az.Storage
* Zmieniono dwa parametry: „-IndexDocument” i „-ErrorDocument404Path” z wymaganych na opcjonalne w poleceniu cmdlet:
    -  Enable-AzStorageStaticWebsite
* Zaktualizowano pomoc dotyczącą polecenia Get-AzStorageBlobContent przez dodanie przykładu
* Wyświetlanie dodatkowych informacji o błędzie w przypadku niepowodzenia polecenia cmdlet z powodu wyjątku StorageException
* Obsługa tworzenia i aktualizowania konta magazynu przy użyciu uwierzytelniania usługi AAD DS w usłudze Azure Files
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Obsługa wyświetlania listy lub zamykania dojść do plików udziału plików, katalogu plików lub pliku
    - Get-AzStorageFileHandle
    - Close-AzStorageFileHandle

#### <a name="azstoragesync"></a>Az.StorageSync
* Ten moduł jest teraz dołączony jako część modułu zbiorczego `Az`

## <a name="232---june-2019"></a>2.3.2 — czerwiec 2019 r.
#### <a name="azaccounts"></a>Az.Accounts
* Usunięto usterkę polegającą na używaniu w niektórych przypadkach niepoprawnego adresu URL w wywołaniach funkcji
    - Więcej informacji: https://github.com/Azure/azure-powershell/issues/8983
* Rozwiązano problem z aliasami w poleceniach cmdlet z modułu AzureRM do modułu Az
  - Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic
  - Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest

#### <a name="azcompute"></a>Az.Compute
* Proste zestawy parametrów New-AzVm i New-AzVmss akceptują teraz parametr „ProximityPlacementGroup”.
* Poprawiono literówkę w dokumentacji referencyjnej polecenia „New-AzVM”

#### <a name="azdns"></a>Az.Dns
* Poprawiono literówkę w przykładach pomocy polecenia „Set-AzDnsZone”.

#### <a name="azeventgrid"></a>Az.EventGrid
* Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-06-01.
* Nowe polecenia cmdlet:
    - New-AzureRmEventGridDomain
        - Tworzy nową domenę usługi Azure Event Grid.
    - Get-AzureRmEventGridDomain
        - Pobiera szczegóły domeny usługi Event Grid lub pobiera listę wszystkich domen usługi Event Grid w bieżącej subskrypcji platformy Azure.
    - Remove-AzureRmEventGridDomain
        - Usuwa domenę usługi Azure Event Grid.
    - New-AzureRmEventGridDomainKey
        - Ponownie generuje klucz dostępu współdzielonego dla domeny usługi Azure Event Grid.
    - Get-AzureRmEventGridDomainKey
        - Pobiera klucze dostępu współdzielonego używane do publikowania zdarzeń w domenie usługi Event Grid.
    - New-AzureRmEventGridDomainTopic:
        - Tworzy nowy temat domeny usługi Azure Event Grid.
    - Get-AzureRmEventGridDomainTopic
        - Pobiera szczegóły tematu domeny usługi Event Grid lub pobiera listę wszystkich tematów domeny usługi Event Grid w bieżącej subskrypcji platformy Azure.
    - Remove-AzureRmEventGridDomainTopic:
        - Usuwa istniejący temat domeny usługi Azure Event Grid.
* Zaktualizowano następujące polecenia cmdlet:
    - New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:
        - Dodano nowe wymagane parametry do obsługi przesyłania potokowego nowej domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.
        - Dodano nowe wymagane parametry w celu określenia nowej nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić utworzenie nowej subskrypcji zdarzeń w tych zasobach.
        - Dodano nowe zestawy parametrów dla domen i tematów domen, aby umożliwić ponowne używanie istniejących parametrów (np. EndPointType, SubjectBeginsWith itp.).
        - Dodano nowe parametry opcjonalne do określania następujących elementów:
            - Data wygaśnięcia subskrypcji zdarzeń,
            - Zaawansowane parametry filtrowania.
        - Dodano nowe wyliczenie dla elementu servicebusqueue jako miejsca docelowego.
        - Uniemożliwiono użycie elementu „Wszystkie” w opcji -IncludedEventType i zamieniono go na
    - Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:
        - Dodano nowe opcjonalne parametry (Top, ODataQuery i NextLink) w celu obsługi filtrowania i stronicowania wyników.
    - Remove-AzureRmEventGridSubscription
        - Dodano nowe wymagane parametry do obsługi przesyłania potokowego domeny usługi Event Grid i tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.
        - Dodano nowe wymagane parametry w celu określenia nazwy domeny usługi Event Grid i/lub nazwy tematu domeny usługi Event Grid, aby umożliwić przeniesienie istniejącej subskrypcji zdarzeń w tych zasobach.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* New-AzFrontDoorWafMatchConditionObject
    - Dodano obsługę przekształceń i nową wartość autouzupełniania operatora (wyrażenie regularne)
* New-AzFrontDoorWafManagedRuleObject
    - Dodano nowe wartości autouzupełniania

#### <a name="aznetwork"></a>Az.Network
* Dodano obsługę zasobu bramy sieci wirtualnej
    - Nowe polecenia cmdlet
        - Get-AzVirtualNetworkGatewayVpnClientConnectionHealth
* Dodano element AvailablePrivateEndpointType
    - Nowe polecenia cmdlet
        - Get-AzAvailablePrivateEndpointType
* Dodano element PrivatePrivateLinkService
    - Nowe polecenia cmdlet
        - Get-AzPrivateLinkService
        - New-AzPrivateLinkService
        - Remove-AzPrivateLinkService
        - New-AzPrivateLinkServiceIpConfig
        - Set-AzPrivateEndpointConnection
* Dodano element PrivateEndpoint
    - Nowe polecenia cmdlet
        - Get-AzPrivateEndpoint
        - New-AzPrivateEndpoint
        - Remove-AzPrivateEndpoint
        - New-AzPrivateLinkServiceConnection
* Zaktualizowano poniższe polecenia dla funkcji: Flaga UseLocalAzureIpAddress w elemencie VpnConnection
    - Zaktualizowano polecenie New-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.
    - Zaktualizowano polecenie Set-AzVpnConnection: Dodano opcjonalny parametr -UseLocalAzureIpAddress, aby wskazać, że podczas inicjowania połączenia jako adres źródłowy powinien zostać użyty lokalny adres IP platformy Azure.
* Dodano pole tylko do odczytu PeeredConnections w komunikacji równorzędnej usługi ExpressRoute.
* Dodano pole tylko do odczytu GlobalReachEnabled w usłudze ExpressRoute.
* Dodano atrybut zmiany wywołujący zakończenie obsługi pola AllowGlobalReach w modelu ExpressRouteCircuit
* Rozwiązano problem 8756 podczas używania elementu TargetListenerID z poleceniami cmdlet AzApplicationGatewayRedirectConfiguration
* Usunięto usterkę w poleceniu New-AzApplicationGatewayPathRuleConfig, która uniemożliwiała ustawienie zestawu reguł regenerowania.
* Rozwiązano problem z wyświetlaniem elementu VirtualNetworkTaps w elemencie NetworkInterfaceIpConfiguration
* Naprawiono polecenia cmdlet pobierania Cortex dla listy wszystkich części
* Naprawiono tworzenie odwołań elementu VirtualHub dla elementu ExpressRouteGateways, VpnGateway
* Dodano obsługę stref dostępności w elementach AzureFirewall i NatGateway
* Dodano polecenie cmdlet Get-AzNetworkServiceTag
* Dodano obsługę wielu publicznych adresów IP usługi Azure Firewall
    - Zaktualizowano polecenie cmdlet New-AzFirewall:
        - Dodano parametr -PublicIpAddress, który akceptuje co najmniej jeden obiekt publicznego adresu IP
        - Dodano parametr -VirtualNetwork, który akceptuje obiekt sieci wirtualnej
        - Dodano do obiektu zapory metody AddPublicIpAddress i RemovePublicIpAddress, które akceptują obiekt publicznego adresu IP jako dane wejściowe
        - Wycofano parametry -PublicIpName i -VirtualNetworkName
* Zaktualizowano poniższe polecenia dla funkcji: Ustawiono w opcjach uwierzytelniania usługi AAD elementu VpnClient zasób bramy sieci wirtualnej.
    - Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.
    - Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano parametry opcjonalne AadTenantUri, AadAudienceId i AadIssuerUri, aby ustawić opcje uwierzytelniania usługi AAD elementu VpnClient w bramie.
    - Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr przełącznika RemoveAadAuthentication w celu usunięcia z bramy opcji uwierzytelniania usługi AAD elementu VpnClient.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Włączono warstwę cenową **pergb2018** w poleceniu „New-AzureRmOperationalInsightsWorkspace”

#### <a name="azresources"></a>Az.Resources
* Obsługa dodatkowych opcji eksportowania szablonu
    - Dodano parametr „-SkipResourceNameParameterization” do polecenia Export-AzResourceGroup
    - Dodano parametr „-SkipAllParameterization” do polecenia Export-AzResourceGroup
    - Dodano parametr „-Resource” do polecenia Export-AzResourceGroup w celu filtrowania wyeksportowanych zasobów

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Usunięto błąd dodawania certyfikatu polegający na pobieraniu przez element ByExistingKeyVault nieprawidłowego odcisku palca w niektórych przypadkach

#### <a name="azsql"></a>Az.Sql
* Naprawiono sufiks punktu końcowego magazynu usługi Advanced Threat Protection
* Rozwiązano problem z usługą Advanced Data Security polegający na przesłanianiu zasad usługi Advanced Threat Protection
* Nowe polecenia cmdlet modułu Management.Sql umożliwiające klientom dodawanie kluczy funkcji TDE i ustawianie funkcji ochrony TDE dla wystąpień zarządzanych
   - Add-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceKeyVaultKey
   - Remove-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceTransparentDataEncryptionProtector
   - Set-AzSqlInstanceTransparentDataEncryptionProtector

#### <a name="azstorage"></a>Az.Storage
* Obsługa rodzajów FileStorage i SkuName Premium_ZRS podczas tworzenia konta magazynu
    - New-AzStorageAccount
* Opis z wyjaśnieniem polecenia cmdlet niezmienności obiektów blob
    -  Remove-AzRmStorageContainerImmutabilityPolicy

#### <a name="azwebsites"></a>Az.Websites
* Optymalizuje polecenie Get-AzWebAppCertificate w celu filtrowania według grupy zasobów na serwerze zamiast na kliencie
* Dodano parametr przełącznika -UseDisasterRecovery do polecenia Get-AzWebAppSnapshot

## <a name="220---june-2019"></a>2.2.0 — czerwiec 2019 r.
#### <a name="azcdn"></a>Az.Cdn
* Zaktualizowano polecenia cmdlet do obsługi funkcji rulesEngine na podstawie interfejsu API w wersji 2019-04-15.

#### <a name="azcompute"></a>Az.Compute
* Dodano parametr `NoWait`, który powoduje rozpoczęcie operacji i natychmiastowy powrót, bez czekania na ukończenie operacji.
    - Zaktualizowano następujące polecenia cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM

#### <a name="azeventhub"></a>Az.EventHub
* Poprawka błędu #9231 — polecenie Get-AzEventHubNamespace nie zwraca tagów
* Poprawka błędu #9230 — polecenie Get-AzEventHubNamespace zwraca wartość ResourceGroup zamiast wartości ResourceGroupName

#### <a name="aznetwork"></a>Az.Network
* Aktualizowanie wartości ResourceId i InputObject dla bramy translatora adresów sieciowych
    - Dodawanie aliasów dla wartości ResourceId i InputObject

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Rozwiązanie problemu z odwołaniem o wartości null w poleceniu Get-AzPolicyEvent

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Minimalny czas przechowywania zasad IaaSVM w dniach zmieniono z 7 na 1

#### <a name="azservicebus"></a>Az.ServiceBus
* Rozwiązanie problemu #9182 — Get-AzServiceBusNamespace zwraca wartość ResourceGroup zamiast ResourceGroupName

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Poprawienie błędu pisowni w komunikacie o błędzie polecenia „Update-AzServiceFabricReliability”
* Poprawienie brakującego znaku w wierszach polecenia usługi Service Fabric

#### <a name="azsql"></a>Az.Sql
* Dodanie parametru DnsZonePartner dla polecenia cmdlet New-AzureSqlInstance w celu obsługi funkcji AutoDr dla wystąpienia zarządzanego.
* Wycofanie polecenia cmdlet Get-AzSqlDatabaseSecureConnectionPolicy
* Zmiana nazwy poleceń cmdlet z Wykrywanie zagrożeń na Advanced Threat Protection
* Parametry New-AzSqlInstance -StorageSizeInGB i -LicenseType są teraz opcjonalne.

#### <a name="azwebsites"></a>Az.Websites
* Rozwiązanie problemu polegającego na tym, że użycie poleceń Set-AzWebApp i Set-AzWebAppSlot z właściwością -WebApp powodowało usunięcie tagów

## <a name="210---may-2019"></a>2.1.0 — maj 2019 r.
#### <a name="azapimanagement"></a>Az.ApiManagement
* Utworzono nowe polecenia cmdlet do zarządzania diagnostyką w zakresie globalnym i interfejsu API
    - **Get-AzApiManagementDiagnostic** — uzyskiwanie diagnostyki skonfigurowanej w zakresie globalnym lub interfejsu API
    - **New-AzApiManagementDiagnostic** — tworzenie nowej diagnostyki w zakresie globalnym lub interfejsu API
    - **New-AzApiManagementHttpMessageDiagnostic** — tworzenie ustawienia diagnostyki określającego nagłówki do rejestrowania i rozmiar treści w bajtach
    - **New-AzApiManagementPipelineDiagnosticSetting** — tworzenie ustawień diagnostyki dla przychodzących/wychodzących komunikatów HTTP do bramy.
    - **New-AzApiManagementSamplingSetting** — tworzenie ustawienia próbkowania dla żądań i odpowiedzi na potrzeby diagnostyki
    - **Remove-AzApiManagementDiagnostic** — usuwanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API
    - **Set-AzApiManagementDiagnostic** — aktualizowanie jednostki diagnostycznej w zakresie globalnym lub interfejsu API
* Utworzono nowe polecenia cmdlet do zarządzania pamięcią podręczną usługi ApiManagement
    - **Get-AzApiManagementCache** — uzyskiwanie szczegółów pamięci podręcznej określonej przez identyfikator lub wszystkich pamięci podręcznych
    - **New-AzApiManagementCache** — tworzenie nowej, „domyślnej” pamięci podręcznej lub pamięci podręcznej w konkretnym „regionie” platformy Azure
    - **Remove-AzApiManagementCache** — usuwanie pamięci podręcznej
    - **Update-AzApiManagementCache** — aktualizacja pamięci podręcznej
* Utworzono nowe polecenia cmdlet do zarządzania schematem interfejsu API
    - **New-AzApiManagementSchema** — tworzenie nowego schematu dla interfejsu API
    - **Get-AzApiManagementSchema** — pobieranie schematów skonfigurowanych w interfejsie API
    - **Remove-AzApiManagementSchema** — usuwanie schematu skonfigurowanego w interfejsie API
    - **Set-AzApiManagementSchema** — aktualizowanie schematu skonfigurowanego w interfejsie API
* Utworzono nowe polecenie cmdlet do generowania tokenu użytkownika.
    - **New-AzApiManagementUserToken** — generowanie nowego tokenu użytkownika ważnego domyślnie przez 8 godzin. Za pomocą tego polecenia cmdlet można wygenerować token dla użytkownika „GIT”.
* Utworzono nowe polecenie cmdlet do pobierania stanu sieci.
    - **Get-AzApiManagementNetworkStatus** — uzyskiwanie stanu sieci dla łączności z zasobami, od których zależy usługa API Management. Jest to przydatne w przypadku wdrażania usługi ApiManagement w sieci wirtualnej i weryfikacji, czy któreś z zależności są uszkodzone.
* Zaktualizowano polecenie cmdlet **New-AzApiManagement** do zarządzania usługą ApiManagement
    - Dodano obsługę nowych jednostek SKU „Zużycie”
    - Dodano obsługę włączania flagi „EnableClientCertificate” dla jednostek SKU „Zużycie”
    - Nowe polecenie cmdlet **New-AzApiManagementSslSetting** umożliwia skonfigurowanie ustawienia „TLS/SSL” na „Zaplecze” i „Fronton”. Za jego pomocą można też skonfigurować szyfrowanie, takie jak „3DES”, i protokoły serwera, takie jak „Http2”we frontonie usługi ApiManagement.
    - Dodano obsługę konfigurowania nazwy hosta „DeveloperPortal” usługi ApiManagement.
* Zaktualizowano polecenia cmdlet **Get-AzApiManagementSsoToken**, aby przyjmowały jako wejście obiekt „PsApiManagement”
* Zaktualizowano polecenie cmdlet, aby wyświetlało komunikaty o błędach śródwierszowo
     > PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Kod błędu: Komunikat o błędzie ValidationError: Co najmniej jedno pole zawiera nieprawidłową wartość: Szczegóły błędu:    [Code=ValidationError, Message=Błąd w elemencie „log-to-eventhub” w wierszu 3, kolumna 10: Nie znaleziono rejestratora, element docelowy=log-to-eventhub]
* Zaktualizowano polecenie cmdlet **Export-AzApiManagementApi** tak, aby eksportowało interfejsy API w formacie „OpenApi 3.0”
* Zaktualizowano polecenie cmdlet **Import-AzApiManagementApi**
    - W celu importowania interfejsu Api z dokumentu ze specyfikacją interfejsu „OpenApi 3.0”.
    - W celu przesłonięcia właściwości „PsApiManagementSchema” określonej w dowolnym dokumencie („Swagger”, „Wadl”, „Wsdl”, „OpenApi”).
    - W celu przesłonięcia właściwości „ServiceUrl” określonej w dowolnym dokumencie.
* Zaktualizowano polecenie cmdlet **Get-AzApiManagementPolicy** tak, aby zwracało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml”
* Zaktualizowano polecenie cmdlet **Set-AzApiManagementPolicy** tak, aby akceptowało zasady w formacie ze zmianą znaczenia inną niż Xml przy użyciu formatu „rawxml” i ze zmianą znaczenia Xml przy użyciu formatu „xml”
* Zaktualizowano polecenie cmdlet **New-AzApiManagementApi**
    - W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.
    - W celu utworzenia interfejsu API we właściwości ApiVersionSet.
    - W celu sklonowania interfejsu API przy użyciu właściwości „SourceApiId” i „SourceApiRevision”.
    - Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.
* Zaktualizowano polecenie cmdlet **Set-AzApiManagementApi**
    - W celu skonfigurowania interfejsu API za pomocą serwera autoryzacji „OpenId”.
    - W celu zaktualizowania interfejsu API we właściwości „ApiVersionSet”.
    - Możliwość skonfigurowania właściwości „SubscriptionRequired” w zakresie interfejsu API.
* Zaktualizowano polecenie cmdlet **New-AzApiManagementRevision**
    - W celu klonowania (kopiowanie tagów, produktów, operacji i zasad) istniejącej wersji przy użyciu właściwości „SourceApiRevision”. Dla nowej wersji przyjmowana jest wartość „ApiId” elementu nadrzędnego.
    - W celu dostarczenia właściwości „ApiRevisionDescription”.
    - W celu przesłonięcia właściwości „ServiceUrl” podczas klonowania interfejsu API.
* Zaktualizowano polecenie cmdlet **New-AzApiManagementIdentityProvider**
    - W celu skonfigurowania właściwości „AAD” lub „AADB2C” za pomocą właściwości „Authority”.
    - W celu skonfigurowania właściwości „SignupPolicy”, „SigninPolicy”, „ProfileEditingPolicy” i „PasswordResetPolicy”.
* Zaktualizowano polecenie cmdlet **New-AzApiManagementSubscription**
    - W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.
    - W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.
    - Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.
* Zaktualizowano polecenie cmdlet **Set-AzApiManagementSubscription**
    - W celu uwzględnienia nowego modelu subskrypcji przy użyciu właściwości „Scope” i „UserId”.
    - W celu uwzględnienia starego modelu subskrypcji przy użyciu właściwości „ProductId” i „UserId”.
    - Dodanie obsługi, aby włączyć właściwość „AllowTracing” na poziomie subskrypcji.
* Zaktualizowano następujące polecenia cmdlet do akceptowania właściwości „ResourceId” jako danych wejściowych
    - „New-AzApiManagementContext”
        > New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso
    - „Get-AzApiManagementApiRelease”
        > Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId
    - „Get-AzApiManagementApiVersionSet”
        > Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset
    - „Get-AzApiManagementAuthorizationServer”
    - „Get-AzApiManagementBackend”
        > Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric
    - „Get-AzApiManagementCertificate”
    - „Remove-AzApiManagementApiVersionSet”
    - „Remove-AzApiManagementSubscription”

#### <a name="azautomation"></a>Az.Automation
* Zaktualizowano polecenie Get-AzAutomationJobOutputRecord tak, aby obsługiwało wartości rekordów w postaci kodu JSON i tekstowej.
    - Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7977
    - Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8600
* Zmieniono działanie polecenia Start-AzAutomationDscCompilationJob tak, aby tylko uruchamiało zadanie zamiast czekać na jego zakończenie.
    * Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8347
* Poprawka dla polecenia Get-AzAutomationDscNode podczas używania opcji -Name zwraca wszystkie węzły. Teraz zwraca tylko pasujące węzły.

#### <a name="azcompute"></a>Az.Compute
* Dodanie parametrów ProtectFromScaleIn i ProtectFromScaleSetAction do polecenia cmdlet Update-AzVmssVM.
* Nowy zestaw parametrów New-AzVM wimple teraz używa domyślnie dostępnej lokalizacji, jeśli region „Wschodnie stany USA” nie jest obsługiwany.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Aktualizacja zestawu ADLS SDK do korzystania z klienta httpclient, integrowanie testowania płaszczyzny danych z platformą Azure

#### <a name="azmonitor"></a>Az.Monitor
* Naprawiono nieprawidłowe nazwy parametrów w przykładach pomocy

#### <a name="aznetwork"></a>Az.Network
* Dodanie flagi DisableBgpRoutePropagation do danych wyjściowych obowiązującej tabeli routingu
    - Zaktualizowano polecenie cmdlet:
        - Get-AzEffectiveRouteTable
* Poprawienie podwójnego łącznika w dokumentacji polecenia New-AzApplicationGatewayTrustedRootCertificate

#### <a name="azresources"></a>Az.Resources
* Dodanie nowego polecenia cmdlet Get-AzureRmDenyAssignment do pobierania przypisań odmowy

#### <a name="azsql"></a>Az.Sql
* Zmiana nazwy poleceń cmdlet usługi Advanced Threat Protection na Advanced Data Security i domyślne włączenie oceny luk w zabezpieczeniach

## <a name="200---may-2019"></a>2.0.0 — maj 2019 r.
#### <a name="azaccounts"></a>Az.Accounts
* Aktualizacja biblioteki uwierzytelniania w celu rozwiązania problemów z usługą ADFS dotyczących uwierzytelniania nazwy użytkownika i hasła

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Dla usług wyszukiwania Bing wyświetlane jest tylko zrzeczenie odpowiedzialności usługi Bing.
* Naprawiono błąd polegający na niepomyślnym tworzeniu konta.

#### <a name="azcompute"></a>Az.Compute
* Funkcja Grupa umieszczania w pobliżu.
    - Dodano następujące nowe polecenia cmdlet:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup
    - Do następujących poleceń cmdlet dodano nowy parametr ProximityPlacementGroupId:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig
* Do polecenia New-AzGalleryImageVersion dodano parametr StorageAccountType.
* Właściwość TargetRegion polecenia New-AzGalleryImageVersion może zawierać parametr StorageAccountType.
* Do poleceń Stop-AzVM i Stop-AzVmss dodano parametr przełącznika SkipShutdown
* Zmiany powodujące niezgodność
    - Polecenie Set-AzVMBootDiagnostics zamieniono na polecenie Set-AzVMBootDiagnostic.
    - Polecenie Export-AzLogAnalyticThrottledRequests zamieniono na polecenie Export-AzLogAnalyticThrottledRequests.

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure Deployment Manager

#### <a name="azdns"></a>Az.Dns
* Automatyczne delegowanie serwera nazw systemu DNS
    - Polecenie cmdlet tworzenia strefy DNS akceptuje nazwę strefy nadrzędnej jako dodatkowy parametr opcjonalny.
    - Dodaje rekordy serwera nazw w strefie nadrzędnej dla nowo utworzonej strefy podrzędnej.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Pierwsze ogólnie dostępne wydanie poleceń cmdlet usługi Azure FrontDoor
* Zmiana nazw poleceń cmdlet zapory aplikacji internetowej w celu dołączenia ciągu „Waf”
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a>Az.HDInsight
* Usunięto dwa polecenia cmdlet:
    - Grant-AzHDInsightHttpServicesAccess
    - Revoke-AzHDInsightHttpServicesAccess
* Dodano nowe polecenie cmdlet Set-AzHDInsightGatewayCredential w celu zastąpienia polecenia Grant-AzHDInsightHttpServicesAccess
* Zaktualizowano polecenie cmdlet Get-AzHDInsightJobOutput, aby rozróżnić rolę czytelnika i rolę operatora usługi HDInsight:
    - Użytkownicy z rolą czytelnika muszą jawnie określić parametr „DefaultStorageAccountKey” — w przeciwnym razie wystąpi błąd.
    - Nie będzie to miało wpływu na użytkowników z rolą operatora usługi HDInsight.

#### <a name="azmonitor"></a>Az.Monitor
* Nowe polecenia cmdlet dla interfejsu API SQR (Scheduled Query Rule, reguła zaplanowanego zapytania)
    - New-AzScheduledQueryRuleAlertingAction
    - New-AzScheduledQueryRuleAznsActionGroup
    - New-AzScheduledQueryRuleLogMetricTrigger
    - New-AzScheduledQueryRuleSchedule
    - New-AzScheduledQueryRuleSource
    - New-AzScheduledQueryRuleTriggerCondition
    - New-AzScheduledQueryRule
    - Get-AzScheduledQueryRule
    - Set-AzScheduledQueryRule
    - Update-AzScheduledQueryRule
    - Remove-AzScheduledQueryRule
    - [Więcej](/rest/api/monitor/scheduledqueryrules) informacji na temat interfejsu API SQR
    - Zaktualizowano plik Az.Monitor.md w celu uwzględnienia poleceń cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)

#### <a name="aznetwork"></a>Az.Network
* Dodano obsługę dla zasobu usługi NAT Gateway
    - Nowe polecenia cmdlet
        - New-AzNatGateway
        - Get-AzNatGateway
        - Set-AzNatGateway
        - Remove-AzNatGateway
   - Zaktualizowano następujące polecenia cmdlet
        - New-AzureVirtualNetworkSubnetConfigCommand
        - Add-AzureVirtualNetworkSubnetConfigCommand
* Zaktualizowano poniższe polecenia dla funkcji: Ustawianie/usuwanie tras niestandardowych dla bramy Brooklyn Gateway.
    - Zaktualizowano polecenie New-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.
    - Zaktualizowano polecenie Set-AzVirtualNetworkGateway: Dodano opcjonalny parametr -CustomRoute w celu ustawienia prefiksów adresów jako tras niestandardowych do ustawienia na bramie.

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Obsługa zapytań dotyczących szczegółów oceny zasad.
    - Dodano parametr „-Expand” do polecenia Get-AzPolicyState. Obsługa polecenia „-Expand PolicyEvaluationDetails”.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Obsługa odzyskiwania lokacji między subskrypcjami z platformy Azure na platformę Azure.
* Oznaczanie nadchodzących zmian powodujących niezgodność dla usługi Azure Site Recovery.
* Poprawka zakończenia planu akcji dla planu odzyskiwania usługi Azure Site Recovery.
* Poprawka aktualizacji mapowania sieci usługi Azure Site Recovery z platformy Azure na platformę Azure.
* Poprawka aktualizacji kierunku ochrony usługi Azure Site Recovery z platformy Azure na platformę Azure dla dysku zarządzanego.
* Inne drobne poprawki.

#### <a name="azrelay"></a>Az.Relay
* Poprawiono błędy pisowni w komunikatach przeznaczonych dla klientów

#### <a name="azservicebus"></a>Az.ServiceBus
* Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw

#### <a name="azstorage"></a>Az.Storage
* Uaktualnienie biblioteki klienta usługi Storage do wersji 10.0.1 (przestrzeń nazw wszystkich obiektów tego zestawu SDK została zmieniona z „Microsoft.WindowsAzure.Storage. *” na „Microsoft.Azure.Storage.* ”)
* Uaktualnienie do wersji Microsoft.Azure.Management.Storage 11.0.0 w celu obsługi nowego interfejsu API w wersji 2019-04-01.
* Domyślny rodzaj konta magazynu w poleceniu Utwórz konto magazynu został zmieniony ze „Storage” na „StorageV2”
    - New-AzStorageAccount
* Zmiana wyjściowego parametru Sku.Name polecenia cmdlet konta magazynu w celu wyrównania z wejściowym parametrem SkuName przez dodanie znaku „-”, na przykład zmiana „StandardLRS” na „Standard_LRS”
    - New-AzStorageAccount
    - Get-AzStorageAccount
    - Set-AzStorageAccount

#### <a name="azwebsites"></a>Az.Websites
* Właściwość „Kind” będzie teraz ustawiona dla obiektów PSSite zwracanych przez polecenie Get-AzWebApp
* Polecenia Get-AzWebApp*Metrics i Get-AzAppServicePlanMetrics oznaczono jako przestarzałe

## <a name="180---april-2019"></a>1.8.0 — kwiecień 2019 r.
### <a name="highlights-since-the-last-major-release"></a>Najważniejsze zmiany od ostatniej wersji głównej
* Ogólna dostępność modułu `Az`
* Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce
* Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network
* Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1
* Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation
* Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji

#### <a name="azaccounts"></a>Az.Accounts
* Aktualizacja polecenia Uninstall-AzureRm w sposób gwarantujący poprawne usuwanie modułów na komputerach Mac

#### <a name="azbatch"></a>Az.Batch
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.

#### <a name="azcdn"></a>Az.Cdn
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.

#### <a name="azcompute"></a>Az.Compute
* Rozwiązanie problemu z instalacją funkcji AEM w sytuacji, gdy identyfikatory zasobów dysków zawierały grupy zasobów napisane małymi literami w identyfikatorze zasobu
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.
* Poprawiono informacje o symbolach wieloznacznych w dokumentacji

#### <a name="azdatafactory"></a>Az.DataFactory
* Dodanie elementu SsisProperties w sytuacji, gdy element NodeCount nie ma wartości null dla zarządzanego środowiska Integration Runtime.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.

#### <a name="azeventgrid"></a>Az.EventGrid
* Zaktualizowano tekst pomocy dla punktu końcowego w celu wskazania, że zasoby powinny zostać utworzone przed rozpoczęciem korzystania z poleceń cmdlet do tworzenia/aktualizacji subskrypcji zdarzenia.

#### <a name="azeventhub"></a>Az.EventHub
* Dodano nowe polecenia cmdlet dla elementu NetworkRuleSet przestrzeni nazw

#### <a name="azhdinsight"></a>Az.HDInsight
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.

#### <a name="aziothub"></a>Az.IotHub
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.

#### <a name="azkeyvault"></a>Az.KeyVault
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.
* Poprawiono informacje o symbolach wieloznacznych w dokumentacji

#### <a name="azmachinelearning"></a>Az.MachineLearning
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.

#### <a name="azmedia"></a>Az.Media
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.

#### <a name="azmonitor"></a>Az.Monitor
  * Nowe polecenia cmdlet dla reguły alertu opartej na metryce GenV2 (nieklasycznej)
      - New-AzMetricAlertRuleV2DimensionSelection
      - New-AzMetricAlertRuleV2Criteria
      - Remove-AzMetricAlertRuleV2
      - Get-AzMetricAlertRuleV2
      - Add-AzMetricAlertRuleV2
  * Zaktualizowano zestaw Monitor SDK do wersji 0.22.0-preview

#### <a name="aznetwork"></a>Az.Network
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.
* Poprawiono informacje o symbolach wieloznacznych w dokumentacji

#### <a name="aznotificationhubs"></a>Az.NotificationHubs
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.

#### <a name="azpowerbiembedded"></a>Az.PowerBIEmbedded
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.
* Zaktualizowano format tabeli dla bazy danych SQL na maszynie wirtualnej platformy Azure
* Dodano alternatywną metodę pobierania lokalizacji w elemencie AzureFileShare
* Zaktualizowano element ScheduleRunDays w elemencie SchedulePolicy zgodnie ze strefą czasową

#### <a name="azrediscache"></a>Az.RedisCache
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.

#### <a name="azresources"></a>Az.Resources
* Poprawiono informacje o symbolach wieloznacznych w dokumentacji

#### <a name="azsql"></a>Az.Sql
* Zamiana zależności od zestawu Monitor SDK na typowy kod
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.
* Rozszerzony proces klasyfikowania wielu kolumn.
* Uwzględnienie właściwości jednostki SKU (nazwa jednostki SKU, rodzina, pojemność) w odpowiedzi od polecenia Get-AzSqlServerServiceObjective i domyślne formatowanie jako tabeli.
* Możliwość używania polecenia Get-AzSqlServerServiceObjective według lokalizacji bez konieczności wcześniejszego istnienia serwera w regionie.
* Obsługa parametru strefy czasowej przy tworzeniu wystąpienia zarządzanego.
* Poprawiono informacje o symbolach wieloznacznych w dokumentacji

#### <a name="azwebsites"></a>Az.Websites
* Poprawki poleceń Set-AzWebApp i Set-AzWebAppSlot, dzięki którym tagi nie są usuwane przy wykonywaniu
* Zaktualizowano polecenia cmdlet z rzeczownikami w liczbie mnogiej do pojedynczej. Nazwy w liczbie mnogiej zostały oznaczone jako przestarzałe.
* Zaktualizowano zestaw WebSites SDK.
* Usunięto właściwość AdminSiteName z elementu PSAppServicePlan.

## <a name="170---april-2019"></a>1.7.0 — kwiecień 2019 r.
### <a name="highlights-since-the-last-major-release"></a>Najważniejsze zmiany od ostatniej wersji głównej
* Ogólna dostępność modułu `Az`
* Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce
* Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network
* Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1
* Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation
* Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji

#### <a name="azaccounts"></a>Az.Accounts
* Zaktualizowano polecenia Add-AzEnvironment i Set-AzEnvironment, aby akceptowały parametr AzureAnalysisServicesEndpointResourceId

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Użyto elementu ServiceClient w poleceniach cmdlet płaszczyzny danych i usunięto oryginalną logikę uwierzytelniania
* Użyto polecenia Add-AzureASAccount jako otoki polecenia Connect-AzAccount, aby uniknąć zmiany powodującej niezgodność

#### <a name="azautomation"></a>Az.Automation
* Usunięto usterkę polecenia cmdlet New-AzAutomationSoftwareUpdateConfiguration dotyczącą uwzględnień. Teraz parametry IncludedKbNumber i IncludedPackageNameMask powinny działać.
* Poprawka usterki dotyczącej dynamicznej grupy zarządzania aktualizacjami usługi Azure Automation

#### <a name="azcompute"></a>Az.Compute
* Dodano parametr HyperVGeneration do poleceń New-AzDiskConfig i New-AzSnapshotConfig
* Umożliwiono tworzenie maszyny wirtualnej za pomocą obrazu galerii z innych dzierżaw.

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Rozwiązano problem w parametrze -Command polecenia New-AzContainerGroup, który polegał na dodawaniu pustego argumentu końcowego

#### <a name="azdatafactory"></a>Az.DataFactory
* Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.2
* Zaktualizowano polecenie cmdlet Set-AzDataFactoryV2 przy użyciu dodatkowych parametrów powiązanych ustawień RepoConfiguration.

#### <a name="azresources"></a>Az.Resources
* Ulepszono obsługę dostawców polecenia „Get-AzResource” w przypadku określenia parametrów „-ResourceId” lub „-ResourceGroupName”, „-Name” i „-ResourceType”
* Ulepszono obsługę błędów poleceń „Test-AzDeployment” i „Test-AzResourceGroupDeployment”
    - Obsługa błędów zgłaszanych poza walidacją wdrożenia i dodanie ich do danych wyjściowych polecenia
    - Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856
* Dodano parametr przełącznika „-IgnoreDynamicParameters” do zestawu poleceń cmdlet wdrażania, aby pominąć monit w scenariuszach skryptów i zadań
    - Więcej informacji: https://github.com/Azure/azure-powershell/issues/6856

#### <a name="azsql"></a>Az.Sql
* Dodano obsługę klasyfikacji danych bazy danych.

#### <a name="azstorage"></a>Az.Storage
* Zgłaszanie szczegółowego błędu podczas tworzenia kontekstu magazynu za pomocą parametru -UseConnectedAccount, ale bez konta logowania platformy Azure
    - New-AzStorageContext
* Dodano obsługę zarządzania właściwościami usługi obiektów blob określonego konta magazynu przy użyciu interfejsu API płaszczyzny zarządzania
    - Update-AzStorageBlobServiceProperty
    - Get-AzStorageBlobServiceProperty
    - Enable-AzStorageBlobDeleteRetentionPolicy
    - Disable-AzStorageBlobDeleteRetentionPolicy
* Obsługa parametru -AsJob w poleceniach cmdlet przekazywania oraz pobierania obiektów blob i plików
    - Get-AzStorageBlobContent
    - Set-AzStorageBlobContent
    - Get-AzStorageFileContent
    - Set-AzStorageFileContent

## <a name="160---march-2019"></a>1.6.0 — marzec 2019
### <a name="highlights-since-the-last-major-release"></a>Najważniejsze zmiany od ostatniej wersji głównej
* Ogólna dostępność modułu `Az`
* Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce
* Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Dodano obsługę symboli wieloznacznych w poleceniach cmdlet pobierania elementów Az.Compute i Az.Network
* Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1
* Dodano obsługę elementów runbook języka Python 2 w elemencie Az.Automation
* Az.LogicApp: Nowe polecenia cmdlet dla konfiguracji zestawów i partii konta integracji

#### <a name="azautomation"></a>Az.Automation
* Zmiana zarządzania aktualizacjami w usłudze Azure Automation w celu obsługi następujących nowych funkcji:
    * Grupowanie dynamiczne
    * Działania przed napisaniem skryptu i po napisaniu skryptu
    * Ustawienie ponownego uruchamiania

#### <a name="azcompute"></a>Az.Compute
* Rozwiązano problem z rozpoznawaniem ścieżek w poleceniu Get-AzVmBootDiagnosticsData
* Zaktualizowano bibliotekę klienta obliczeń do wersji 25.0.0.

#### <a name="azkeyvault"></a>Az.KeyVault
* Dodano obsługę symboli wieloznacznych do poleceń cmdlet usługi KeyVault

#### <a name="aznetwork"></a>Az.Network
* Dodano obsługę analizy zagrożeń w usłudze Azure Firewall
* Dodano zasób najwyższego poziomu zasad zapory usługi Application Gateway i reguły niestandardowe

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Dodano element SnapshotRetentionInDays w zasadach maszyny wirtualnej platformy Azure w celu obsługi natychmiastowego elementu RP
* Dodano obsługę potoków do wyrejestrowania kontenera

#### <a name="azresources"></a>Az.Resources
* Zaktualizowano obsługę symboli wieloznacznych w poleceniach Get-AzResource i Get-AzResourceGroup
* Zaktualizowano poświadczenia używane w wywołaniach ogólnych do usługi ARM

#### <a name="azsql"></a>Az.Sql
* Zmieniono parametr polecenia cmdlet wykrywania zagrożeń (ExcludeDetectionType) z DetectionType na string[], aby dostosować go do przyszłych potrzeb po dodaniu nowych elementów DetectionType i zapewnić obsługę autouzupełniania.

#### <a name="azstorage"></a>Az.Storage
* Obsługa pobierania/ustawiania/usuwania zasad zarządzania na koncie magazynu
    - Set-AzStorageAccountManagementPolicy
    - Get-AzStorageAccountManagementPolicy
    - Remove-AzStorageAccountManagementPolicy
    - Add-AzStorageAccountManagementPolicyAction
    - New-AzStorageAccountManagementPolicyFilter
    - New-AzStorageAccountManagementPolicyRule

#### <a name="azwebsites"></a>Az.Websites
* Usunięto usterkę szablonu usługi ARM, która przerywała klonowanie wszystkich miejsc przy użyciu elementu „New-AzWebApp -IncludeSourceWebAppSlots”

## <a name="150---march-2019"></a>1.5.0 — marzec 2019
#### <a name="azaccounts"></a>Az.Accounts
* Dodano polecenie „Register-AzModule” do obsługi poleceń cmdlet generowanych przez narzędzie AutoRest
* Zaktualizowano przykłady polecenia Connect-AzAccount

#### <a name="azautomation"></a>Az.Automation
* Rozwiązano problem polegający na pobieraniu niektórych harmonogramów miesięcznych w kilku poleceniach cmdlet usługi Azure Automation
* Rozwiązano problem polegający na zwracaniu tylko pierwszych 20 węzłów przez polecenie Get-AzAutomationDscNode. Teraz polecenie zwraca wszystkie węzły

#### <a name="azcdn"></a>Az.Cdn
* Dodano nowe polecenia cmdlet programu PowerShell do włączania/wyłączania protokołu HTTPS domeny niestandardowej i wycofano stare polecenia

#### <a name="azcompute"></a>Az.Compute
* Dodano obsługę symboli wieloznacznych do poleceń cmdlet pobierania

#### <a name="azdatafactory"></a>Az.DataFactory
* Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.1

#### <a name="azlogicapp"></a>Az.LogicApp
* Rozwiązano problem polegający na pobieraniu tylko pierwszej strony wyników przez element ListWorkflows

#### <a name="aznetwork"></a>Az.Network
* Dodano obsługę symboli wieloznacznych do poleceń cmdlet sieci

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Dodano obsługę programu SQL Server na maszynie wirtualnej platformy Azure
* Aktualizacja zestawu SDK
* Usunięto sprawdzanie elementu VMappContainer w poleceniu Get-ProtectableItem
* Dodano parametry Name i ServerName dla polecenia Get-ProtectableItem

#### <a name="azresources"></a>Az.Resources
* Dodano parametr `-TemplateObject` do poleceń cmdlet wdrażania
    - Więcej informacji: https://github.com/Azure/azure-powershell/issues/2933
* Rozwiązano problem polegający na potokowaniu wyniku polecenia `Get-AzResource` do polecenia `Set-AzResource`
    - Więcej informacji: https://github.com/Azure/azure-powershell/issues/8240
* Rozwiązano problem ze zmianą typu danych JSON podczas uruchamiania polecenia `Set-AzResource`
    - Więcej informacji: https://github.com/Azure/azure-powershell/issues/7930

#### <a name="azsql"></a>Az.Sql
* Zaktualizowano element AuditingEndpointsCommunicator.
    - Naprawiono zachowanie przypadku brzegowego podczas tworzenia nowych ustawień diagnostycznych.

#### <a name="azstorage"></a>Az.Storage
* Obsługa rodzaju BlockBlobStorage podczas tworzenia konta magazynu — New-AzStorageAccount

## <a name="140---february-2019"></a>1.4.0 — luty 2019 r.
#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Przestarzałe polecenie cmdlet AddAzureASAccount

#### <a name="azautomation"></a>Az.Automation
* Zaktualizowano pomoc dotyczącą polecenia Import-AzAutomationDscNodeConfiguration
* Dodano walidację nazwy konfiguracji do polecenia cmdlet Import-AzAutomationDscConfiguration
* Ulepszono obsługę błędów dla polecenia cmdlet Import-AzAutomationDscConfiguration

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Dodano nazwę CustomSubdomainName jako nowy parametr opcjonalny polecenia New-AzCognitiveServicesAccount, które jest używany do określania poddomeny zasobu.

#### <a name="azcompute"></a>Az.Compute
* Naprawiono błąd z zestawami parametrów identyfikatorów
* Zaktualizowano polecenie Get-AzVMExtension w celu wyświetlania listy wszystkich zainstalowanych rozszerzeń, jeśli nie parametr Name nie został podany
* Dodano parametry Tag i ResourceId do polecenia cmdlet Update-AzImage
* Polecenie Get-AzVmssVM bez identyfikatora wystąpienia i z elementem InstanceView może wyświetlać maszyny wirtualne usługi Virtual Machine Scale Sets z widokiem wystąpienia.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Dodano polecenia cmdlet na potrzeby wyliczania i przywracania usuniętego elementu usługi ADL

#### <a name="azeventhub"></a>Az.EventHub
* Dodano nową właściwość typu wartość logiczna SkipEmptyArchives w celu pomijania pustych archiwów w klasie CaptureDescription usługi Eventhub

#### <a name="azkeyvault"></a>Az.KeyVault
* Naprawiono tagowanie w poleceniu Set-AzKeyVaultSecret

#### <a name="azlogicapp"></a>Az.LogicApp
* Dodano podstawową jednostkę SKU na potrzeby kont integracji
* Dodano typy XSLT 2.0, XSLT 3.0 i mapę Liquid
* Nowe polecenia cmdlet dla zestawów kont integracji
    - Get-AzIntegrationAccountAssembly
    - New-AzIntegrationAccountAssembly
    - Remove-AzIntegrationAccountAssembly
    - Set-AzIntegrationAccountAssembly
* Nowe polecenia cmdlet dla konfiguracji partii konta integracji
    - Get-AzIntegrationAccountBatchConfiguration
    - New-AzIntegrationAccountBatchConfiguration
    - Remove-AzIntegrationAccountBatchConfiguration
    - Set-AzIntegrationAccountBatchConfiguration
* Zaktualizowano zestaw SDK aplikacji logiki do wersji 4.1.0

#### <a name="azmonitor"></a>Az.Monitor
* Zaktualizowano pomoc dotyczącą polecenia Get-AzMetric

#### <a name="aznetwork"></a>Az.Network
* Zaktualizowano przykładową pomoc dotyczącą polecenia Add-AzApplicationGatewayCustomError

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Dodatkowa obsługa źródła danych New i Get ApplicationInsights.
    - Dodano nowy rodzaj „Application Insights” do obsługi źródeł danych usługi ApplicationInsights typu Pobierz określone i Pobierz wszystkie dla danego obszaru roboczego.
    - Dodano polecenie cmdlet New-AzOperationalInsightsApplicationInsightsDataSource służące do tworzenia źródła danych z użyciem danych parametrów zasobów usługi Application-Insights: identyfikator subskrypcji, resourceGroupName i nazwa.

#### <a name="azresources"></a>Az.Resources
* Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8166
* Rozwiązano problem https://github.com/Azure/azure-powershell/issues/8235
* Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6219
* Rozwiązano problem uniemożliwiający powtórzone tworzenie poświadczeń KeyCredentials

#### <a name="azsql"></a>Az.Sql
* Dodano obsługę warstwy Hiperskala bazy danych SQL
* Rozwiązano problem polegający na tym, że przywracanie może zakończyć się niepowodzeniem z powodu ustawienia niepotrzebnych właściwości w żądaniu przywracania

#### <a name="azwebsites"></a>Az.Websites
* Naprawiono przykład w poleceniu Get-AzWebAppSlotMetrics

## <a name="130---february-2019"></a>1.3.0 — luty 2019 r.
#### <a name="azaccounts"></a>Az.Accounts
* Zaktualizowano do najnowszej wersji środowiska ClientRuntime

#### <a name="azanalysisservices"></a>Az.AnalysisServices
Ogólna dostępność modułu Az.AnalysisServices.

#### <a name="azcompute"></a>Az.Compute
* Rozszerzenie AEM: Dodano obsługę obsługi dysków UltraSSD oraz P60, P70 i P80
* Zaktualizowano opis pomocy dla polecenia Set-AzVMBootDiagnostics
* Zaktualizowano opis pomocy i przykład dla polecenia Update-AzImage

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
Ogólna dostępność modułu Az.RecoveryServices.

#### <a name="azresources"></a>Az.Resources
* Poprawiono tagowanie dla grup zasobów
    - Więcej informacji: https://github.com/Azure/azure-powershell/issues/8166
* Rozwiązano problem polegający na tym, że polecenie `Get-AzureRmRoleAssignment` nie uwzględniało parametru -ErrorAction
    - Więcej informacji: https://github.com/Azure/azure-powershell/issues/8235

#### <a name="azsql"></a>Az.Sql
* Dodano polecenia Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy
* Rozwiązano problem polegający na tym, że niezalogowanie na koncie platformy Azure powodowało wyjątek nullref podczas wykonywania poleceń cmdlet usługi SQL
* Naprawiono wyjątek odwołania o wartości null w poleceniu Get-AzSqlCapability

## <a name="121---january-2019"></a>1.2.1 — styczeń 2019 r.
#### <a name="azaccounts"></a>Az.Accounts
* Wersja z poprawną wersją uwierzytelniania

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Wersja ze zaktualizowaną zależnością uwierzytelniania

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Wersja ze zaktualizowaną zależnością uwierzytelniania

## <a name="120---january-2019"></a>1.2.0 — styczeń 2019 r.
#### <a name="azaccounts"></a>Az.Accounts
* Dodano uwierzytelnianie interakcyjne i uwierzytelnianie nazwy użytkownika/hasła tylko dla programu Windows PowerShell 5.1
* Zaktualizowano nieprawidłowe adresy URL pomocy online
* Dodanie komunikatu ostrzegawczego w programie PS Core dla polecenia Uninstall-AzureRm

#### <a name="azaks"></a>Az.Aks
* Zaktualizowano nieprawidłowe adresy URL pomocy online

#### <a name="azautomation"></a>Az.Automation
* Dodano obsługę elementów runbook języka Python 2
* Zaktualizowano nieprawidłowe adresy URL pomocy online

#### <a name="azcdn"></a>Az.Cdn
* Zaktualizowano nieprawidłowe adresy URL pomocy online

#### <a name="azcompute"></a>Az.Compute
* Dodano polecenie cmdlet Invoke-AzVMReimage
* Dodano parametr TempDisk do polecenia Set-AzVmss
* Poprawiono komunikat ostrzegawczy polecenia New-AzVM

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Zaktualizowano nieprawidłowe adresy URL pomocy online

#### <a name="azdatafactory"></a>Az.DataFactory
* Zaktualizowano zestaw ADF .Net SDK do wersji 3.0.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Rozwiązano problem z punktem końcowym usługi ADLS podczas korzystania z pakietu MSI
    - Więcej informacji: https://github.com/Azure/azure-powershell/issues/7462
* Zaktualizowano nieprawidłowe adresy URL pomocy online

#### <a name="aziothub"></a>Az.IotHub
* Dodano format kodowania do polecenia cmdlet Add-IotHubRoutingEndpoint.

#### <a name="azkeyvault"></a>Az.KeyVault
* Zaktualizowano nieprawidłowe adresy URL pomocy online

#### <a name="aznetwork"></a>Az.Network
* Zaktualizowano nieprawidłowe adresy URL pomocy online

#### <a name="azresources"></a>Az.Resources
* Poprawiono nieprawidłowe przykłady w dokumentacji referencyjnej poleceń New-AzADAppCredential i New-AzADSpCredential
* Rozwiązano problem polegający na tym, że parametr -TemplateFile nie był rozpoznawany przez wykonaniem poleceń cmdlet wdrożenia grupy zasobów
* Az.Resources: Poprawiono dokumentację dla wartości domyślnej parametru -Mode polecenia New-AzureRmPolicyDefinition
* Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7522
* Az.Resources: Rozwiązano problem https://github.com/Azure/azure-powershell/issues/5747
* Rozwiązano problem z formatowaniem obiektu PSResourceGroupDeployment
    - Więcej informacji: https://github.com/Azure/azure-powershell/issues/2123

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Wycofanie, kiedy certyfikat jest dodawany do modelu usługi VMSS, ale zwracany jest wyjątek w celu poprawienia błędu: https://github.com/Azure/service-fabric-issues/issues/932
* Poprawiono niektóre komunikaty o błędach.
* Poprawiono tworzenie klastra za pomocą domyślnego szablonu ARM dla polecenia New-AzServiceFabriCluster, które nie działało w przypadku migracji do platformy Azure.
* Poprawiono dodawanie certyfikatu klastra/aplikacji, aby był on dodawany tylko do zestawów skalowania maszyn wirtualnych odpowiadających klastrowi, przez sprawdzanie identyfikatora klastra w rozszerzeniu.

#### <a name="azsignalr"></a>Az.SignalR
* Zaktualizowano nieprawidłowe adresy URL pomocy online

#### <a name="azsql"></a>Az.Sql
* Zaktualizowano nieprawidłowe adresy URL pomocy online
* Zaktualizowano opis parametru LicenseType przy użyciu możliwych wartości
* Poprawka dotycząca braku działania aktualizowania tożsamości wystąpienia zarządzanego, kiedy jest to jedyna aktualizowana właściwość
* Obsługa niestandardowego sortowania w wystąpieniu zarządzanym

#### <a name="azstorage"></a>Az.Storage
* Zaktualizowano nieprawidłowe adresy URL pomocy online
* Udostępnianie szczegółowych komunikatów o błędzie podczas wykonywania instrukcji get/set dla klasycznego rejestrowania/metryk na koncie usługi Premium Storage, ponieważ konto usługi Premium Storage nie obsługuje klasycznego rejestrowania/metryk.
    - Get/Set-AzStorageServiceLoggingProperty
    - Get/Set-AzStorageServiceMetricsProperty

#### <a name="aztrafficmanager"></a>Az.TrafficManager
* Zaktualizowano nieprawidłowe adresy URL pomocy online

#### <a name="azwebsites"></a>Az.Websites
* Zaktualizowano nieprawidłowe adresy URL pomocy online
* Poprawiono polecenie New-AzWebAppSSLBinding, aby certyfikat był przekazywany do prawidłowej grupy zasobów i lokalizacji, jeśli aplikacja jest hostowana w środowisku ASE.
* Poprawiono polecenie New-AzWebAppSSLBinding, aby nie zastępowało tagów podczas powiązania certyfikatu SSL z aplikacją

## <a name="110---january-2019"></a>1.1.0 — styczeń 2019 r.
#### <a name="azaccounts"></a>Az.Accounts
* Dodano zakres „Local” do polecenia Enable-AzureRmAlias

#### <a name="azcompute"></a>Az.Compute
* Nazwa jest teraz opcjonalna w zestawie parametrów identyfikatora dla poleceń Restart/Start/Stop/Remove/Set-AzVM i Save-AzVMImage
* Zaktualizowano opis identyfikatora w plikach Pomocy
* Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Zaktualizowano wersję zestawu SDK płaszczyzny danych do 1.1.14 w związku z poprawkami zestawu SDK.
    - Poprawiono obsługę ujemnego czasu dostępu i czasu modyfikacji dla pobierania stanu pliku i stanu listy, poprawiono token anulowania asynchronicznego

#### <a name="azeventgrid"></a>Az.EventGrid
* Zaktualizowano na potrzeby korzystania z interfejsu API w wersji 2019-01-01.
* Zaktualizowano następujące polecenia cmdlet w celu obsługi nowego scenariusza w interfejsie API w wersji 2019-01-01
    - New-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:
        - czas wygaśnięcia zdarzenia,
        - maksymalna liczba prób dostarczenia dla zdarzeń,
        - punkt końcowy utraconych wiadomości.
    - Update-AzureRmEventGridSubscription: Dodano nowe parametry opcjonalne do określania następujących elementów:
        - czas wygaśnięcia zdarzenia,
        - maksymalna liczba prób dostarczenia dla zdarzeń,
        - punkt końcowy utraconych wiadomości.
* Dodano nowe wartości wyliczeniowe (storageQueue i hybridConnection) dla opcji EndpointType w poleceniach cmdlet New-AzureRmEventGridSubscription i Update-AzureRmEventGridSubscription.
* Wyświetlany jest komunikat ostrzegawczy, jeśli dla tworzonej lub aktualizowanej subskrypcji zdarzeń oczekiwana jest ręczna akcja użytkownika.

#### <a name="aziothub"></a>Az.IotHub
* Zaktualizowano do najnowszej wersji zestawu SDK usługi IotHub

#### <a name="azlogicapp"></a>Az.LogicApp
* Polecenie Get-AzLogicApp wyświetla wszystkie elementy, jeśli nie określono nazwy

#### <a name="azresources"></a>Az.Resources
* Rozwiązano problem z zestawem parametrów podczas podawania parametrów „-ODataQuery” i „-ResourceId” dla polecenia „Get-AzResource”
    - Więcej informacji: https://github.com/Azure/azure-powershell/issues/7875
* Poprawiono obsługę parametru -Custom w poleceniach New/Set-AzPolicyDefinition
* Poprawiono błąd pisowni w dokumentacji polecenia New-AzDeployment
* Określono parametr „-MailNickname” jako obowiązkowy dla polecenia „New-AzADUser”
    - Więcej informacji: https://github.com/Azure/azure-powershell/issues/8220

#### <a name="azsignalr"></a>Az.SignalR
* Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts

#### <a name="azsql"></a>Az.Sql
* Przekonwertowano zależność klienta zarządzania magazynem na wspólną implementację zestawu SDK.

#### <a name="azstorage"></a>Az.Storage
* Wartość StorageAccountName w kontekście magazynu jest ustawiana jako rzeczywista nazwa konta magazynu, gdy jest tworzona przy użyciu tokenu SAS, protokołu OAuth lub wartości Anonymous
    - New-AzStorageContext
* Podczas tworzenia tokenu SAS dla obiektu migawki obiektu blob z parametrem „-FullUri” poprawiono zwracany identyfikator URI, tak aby był identyfikatorem URI migawki
    - New-AzStorageBlobSASToken

#### <a name="azwebsites"></a>Az.Websites
* Naprawiono usterkę podczas analizowania daty w poleceniu „Get-AzDeletedWebApp”
* Rozwiązano problem dotyczący zgodności z poprzednimi wersjami w module Az.Accounts

## <a name="100---december-2018"></a>1.0.0 — grudzień 2018 r.
### <a name="general"></a>Ogólne

- Ogólna dostępność modułu Az
- Pomoc online dla każdego modułu
- Aby uzyskać więcej informacji i plan, zobacz [stronę z ogłoszeniem modułu Az](https://aka.ms/azps-announce)
- Zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać informacje na temat migracji z modułu AzureRM

### <a name="azaccounts"></a>Az.Accounts
- Zmiana z modułu Az.Profile
- Poprawiono formaty tabel dla typów profili i kontekstu

### <a name="azapimanagement"></a>Az.ApiManagement
- Poprawki dotyczące usterki nr 7002
- Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje

### <a name="azbatch"></a>Az.Batch
- Dodano możliwość sprawdzenia, która wersja agenta węzła usługi Azure Batch działa na każdej maszynie wirtualnej w puli, za pośrednictwem nowej właściwości `NodeAgentInformation` klasy `PSComputeNode`.
- Wartość domyślna właściwości `Caching` dla klasy `PSDataDisk` to teraz `ReadWrite`, a nie `None`.
- Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje

### <a name="azbilling"></a>Az.Billing
- Łączy polecenia cmdlet Billing, Consumption i UsageAggregates; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje

### <a name="azcognitivservices"></a>Az.CognitivServices
- Dodano moduły wypełniania dla parametrów SkuName i Typem dostępnych w operacji New-AzureRmCognitiveServicesAccount
- Usunięto zestaw parametrów GetSkusWithAccountParamSetName z polecenia Get-AzCognitiveServicesAccountSkus

### <a name="azcontainerinstance"></a>Az.ContainerInstance
- Dodano obsługę elementu ManagedIdentity

### <a name="azdatalakeanalytics"></a>Az.DataLakeAnalytics
- Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje

### <a name="azdatalakestore"></a>Az.DataLakeStore
- Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje

### <a name="azmonitor"></a>Az.Monitor
- Zmieniono nazwę modułu Az.Insights na Az.Monitor oraz wprowadzono inne drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje

### <a name="azkeyvault"></a>Az.KeyVault
- Usunięto przestarzałą właściwość „PurgeDisabled” z typów danych wyjściowych

### <a name="azmachinelearning"></a>Az.MachineLearning
- Uwzględniono polecenia cmdlet z modułu Az.MachineLearningCompute

### <a name="azmedia"></a>Az.Media
- Usunięto przestarzały alias -Tags z polecenia New-AzMediaService

### <a name="aznetwork"></a>Az.Network
Dodano obsługę konfigurowania zestawów RewriteRuleSet w usłudze Application Gateway
    - Dodano nowe polecenia cmdlet:
        - Add-AzureRmApplicationGatewayRewriteRuleSet
        - Get-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRuleSet
        - Remove-AzureRmApplicationGatewayRewriteRuleSet
        - Set-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRule
        - New-AzureRmApplicationGatewayRewriteRuleActionSet
        - New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration
    - Zaktualizowano polecenia cmdlet, dodając opcjonalny parametr -RewriteRuleSet
        - New-AzureRmApplicationGateway
        - New-AzureRmApplicationGatewayRequestRoutingRule
        - Add-AzureRmApplicationGatewayRequestRoutingRule
        - New-AzureRmApplicationGatewayPathRuleConfig
        - Add-AzureRmApplicationGatewayUrlPathMapConfig
        - New-AzureRmApplicationGatewayUrlPathMapConfig Dodano obsługę magazynu KeyVault do usługi Application Gateway za pomocą tożsamości.
    - Zaktualizowano polecenia cmdlet, dodając opcjonalne parametry -KeyVaultSecretId i -KeyVaultSecret
        - Add-AzApplicationGatewaySslCertificate
        - New-AzApplicationGatewaySslCertificate
        - Set-AzApplicationGatewaySslCertificate
    - Zaktualizowano polecenie cmdlet New-AzApplicationGateway, dodając opcjonalny parametr -UserAssignedIdentity
- Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje

### <a name="azoperationalinsights"></a>Az.OperationalInsights
- Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje

### <a name="azprofile"></a>Az.Profile
- Zmieniono nazwę modułu na Az.Accounts

### <a name="azrecoveryservices"></a>Az.RecoveryServices
- Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje

### <a name="azresources"></a>Az.Resources
- Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje

### <a name="azservicefabric"></a>Az.ServiceFabric
- Obsługa określania certyfikatu według nazwy pospolitej i odcisku palca
- Niewielkie zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje

### <a name="azsignalr"></a>Az.SIgnalR
- Ogólna dostępność poleceń cmdlet programu PowerShell dla modułu SIgnalR

### <a name="azsql"></a>Az.Sql
- Dodano nowe typy wykrywania, Data_Exfiltration i Unsafe_Action, do poleceń cmdlet wykrywania zagrożeń
- Zaktualizowano przykłady poleceń cmdlet dotyczących inspekcji SQL w dokumentacji
- Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje

### <a name="azstorage"></a>Az.Storage
- Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje

### <a name="azwebsites"></a>Az.Websites
- Drobne zmiany powodujące niezgodność; zobacz [Przewodnik migracji](https://aka.ms/azps-migration-guide), aby uzyskać szczegółowe informacje

## <a name="070---december-2018"></a>0.7.0 — grudzień 2018 r.

### <a name="general"></a>Ogólne

* Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az

### <a name="azcompute"></a>Az.Compute

* Dodano obsługę opcji UltraSSD i Galeria obrazów w prostych zestawach parametrów dla poleceń cmdlet `New-AzVm(ss)`.

### <a name="azdatalakestore"></a>Az.DataLakeStore

* Poprawiono końcowy ukośnik w domenie konta usługi ADLS

### <a name="azfrontdoor"></a>Az.FrontDoor

* Poprawiono kilka przerwanych hiperlinków
    - W artykułach dotyczących poleceń New-AzureRmFrontDoor i Set-AzureRmFrontDoor poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.
    - W artykule dotyczącym polecenia New-AzureRmFrontDoorManagedRuleObject poprawiono link do artykułu dotyczącego polecenia cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.

### <a name="azrecoveryservices"></a>Az.RecoveryServices

* Dodano walidacje po stronie klienta na potrzeby operacji przywracania udziału plików platformy Azure.
* Parametry storageAccountName i storageAccountResourceGroupName są teraz opcjonalne w przypadku przywracania udziału plików platformy Azure.

### <a name="azresources"></a>Az.Resources

* Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7679
    - Aktualizacja polecenia Get-AzureRmRoleAssignment w celu używania zakresu subskrypcji, jeśli został podany, podczas żądania klasycznych administratorów.

### <a name="azsql"></a>Az.Sql

* Drobne zmiany na potrzeby nadchodzącego przejścia z modułu AzureRM do modułu Az
* Rozwiązano problem dotyczący używania polecenia Get-AzureRmSqlDatabaseVulnerabilityAssessment na platformie .NET Core
* Zmodyfikowano dokumentację komunikatów pomocy dotyczących poleceń cmdlet z zakresu inspekcji SQL.

### <a name="azstorage"></a>Az.Storage

* Dodano parametr -EnableHierarchicalNamespace do polecenia New-AzureRmStorageAccount
* Rozwiązano problem polegający na tym, że polecenie cmdlet kopiowania pliku nie może ponownie używać kontekstu źródłowego w miejscu docelowym, jeśli nie podano parametru -DestContext
    - Start-AzureStorageFileCopy
* Obsługa konfiguracji statycznej witryny internetowej
    - Enable-AzureStorageStaticWebsite
    - Disable-AzureStorageStaticWebsite

### <a name="azwebsites"></a>Az.Websites

* Set-AzureRmWebApp i Set-AzureRmWebAppSlot
    - Dodano nowy parametr (-AzureStoragePath) umożliwiający określenie ścieżek usługi Azure Storage, które mają zostać zainstalowane w aplikacjach kontenera systemów Windows i Linux. Użyj danych wyjściowych nowego polecenia cmdlet New-AzureRmWebAppAzureStoragePath jako parametru, aby ustawić ścieżki usługi Azure Storage.

## <a name="061---november-2018"></a>0.6.1 — listopad 2018 r.

### <a name="azapimanagement"></a>Az.ApiManagement
* Aktualizacja zależności w związku z problemem dotyczącym mapowania typów

### <a name="azautomation"></a>Az.Automation
* Polecenia cmdlet usługi Azure Automation oparte na programie Swagger
* Dodano polecenia cmdlet rozwiązania Update Management
* Dodano polecenia cmdlet kontroli kodu źródłowego
* Dodano polecenie cmdlet Remove-AzureRmAutomationHybridWorkerGroup
* Naprawiono polecenie konfiguracji DSC służące do rejestrowania węzła

### <a name="azcompute"></a>Az.Compute
* Rozwiązano problem dotyczący tożsamości SystemAssigned
* Aktualizacja zależności w związku z problemem dotyczącym mapowania typów

### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Aktualizacja zależności w związku z problemem dotyczącym mapowania typów

### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* Aktualizacja opisu przykładów dla poleceń cmdlet witryny Marketplace

### <a name="aznetwork"></a>Az.Network
* Dodano następujące polecenia cmdlet: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError
* Ponownie dodano protokół ICMP do obsługiwanych protokołów sieciowych AzureFirewall
* Aktualizacja polecenia cmdlet Test-AzureRmNetworkWatcherConnectivity — dodanie walidacji identyfikatora, adresu i portu docelowego.
* Rozwiązano problemy z użyciem pamięci w mapie VirtualNetwork

### <a name="azrecoveryservicesbackup"></a>Az.RecoveryServices.Backup
* Poprawka dotycząca modyfikowania zasad dla chronionego udziału plików.
* Przekonwertowano strefę czasową zasad na wielkie litery.

### <a name="azrecoveryservicessiterecovery"></a>Az.RecoveryServices.SiteRecovery
* Poprawiono przykład w poleceniu New-AzureRmRecoveryServicesAsrProtectableItem
* Aktualizacja zależności w związku z problemem dotyczącym mapowania typów

### <a name="azrelay"></a>Az.Relay
* Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmRelayKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.

### <a name="azresources"></a>Az.Resources
* Aktualizacja dokumentacji pomocy dotyczącej parametrów związanych z tożsamością zasobu w poleceniach `New-AzureRmPolicyAssignment` i `Set-AzureRmPolicyAssignment`
* Dodanie przykładu dla polecenia New-AzureRmPolicyDefinition używającego parametru -Metadata
* Poprawka umożliwiająca zachowanie wielkości liter w kluczach tagów w elemencie NetStandard: #7678 #7703

### <a name="azservicefabric"></a>Az.ServiceFabric
* Dodanie komunikatów o zakończeniu obsługi w związku z nadchodzącymi zmianami powodującymi niezgodność

### <a name="azsql"></a>Az.Sql
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

## <a name="050---november-2018"></a>0.5.0 — listopad 2018 r.
#### <a name="general"></a>Ogólne
* Dodano moduły wypełniania zasobów do wielu podstawowych poleceń cmdlet — umożliwiają one przechodzenie między nazwami istniejących zasobów za pomocą klawisza Tab podczas interaktywnego wywoływania poleceń cmdlet

#### <a name="azprofile"></a>Az.Profile
* Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta
* Zmieniono nazwę parametru TenantId w poleceniu cmdlet Connect-AzAccount na Tenant i dodano alias dla parametru TenantId
* Zaktualizowano opis parametru TenantId dla polecenia Connect-AzAccount
* Naprawiono komunikat o błędzie dotyczący nieudanego logowania podczas podawania domeny dzierżawy
    - https://github.com/Azure/azure-powershell/issues/6936
* Rozwiązano problem polegający na konflikcie nazw kontekstu w przypadku kont bez subskrypcji w dzierżawie
    - https://github.com/Azure/azure-powershell/issues/7453
* Rozwiązano problem z punktami końcowymi usługi DataLake w przypadku używania tożsamości usługi zarządzanej
    - https://github.com/Azure/azure-powershell/issues/7462
* Rozwiązano problem polegający na tym, że polecenie „Disconnect-AzAccount” zgłaszało wyjątek w przypadku braku połączenia
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Dodano operację Get-AzCognitiveServicesAccountSkus.

#### <a name="azcompute"></a>Az.Compute
* Dodano polecenia cmdlet Add-AzVmssVMDataDisk i Remove-AzVmssVMDataDisk
* Polecenie Get-AzVMImage wyświetla element AutomaticOSUpgradeProperties
* Rozwiązano problem polegający na tym, że wartości opcji SetAzVMChefExtension -BootstrapOptions i -JsonAttribute nie były ustawiane w formacie JSON.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Zaktualizowano pakiet usługi DataLake do wersji 1.1.10.
* Dodano domyślną współbieżność do operacji wielowątkowych.

#### <a name="azinsights"></a>Az.Insights
* Rozwiązano problem nr 7267 (obszar autoskalowania)
    - Podczas tworzenia nowej reguły autoskalowania występował problem polegający na niepoprawnym ustawieniu parametrów wyliczanych (zawsze była ustawiana wartość domyślna).
* Rozwiązano problem nr 7513 [Insights] polegający na tym, że polecenie Set-AzDiagnosticSetting wymagało jawnego określenia kategorii podczas tworzenia ustawienia
    - Teraz polecenie cmdlet nie wymaga jawnego określenia kategorii do włączenia podczas tworzenia, czyli działa zgodnie z opisem w dokumentacji

#### <a name="aznetwork"></a>Az.Network
* Parametr PeeringType jest teraz obowiązkowym parametrem dla następujących poleceń cmdlet:
    - Get-AzExpressRouteCircuitRouteTable
    - Get-AzExpressRouteCircuitARPTable
    - Get-AzExpressRouteCircuitRouteTableSummary
    - Get-AzExpressRouteCrossConnectionArpTable
    - Get-AzExpressRouteCrossConnectionRouteTable
    - Get-AzExpressRouteCrossConnectionRouteTableSummary

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Dodano polecenia cmdlet korygowania zasad

#### <a name="azresources"></a>Az.Resources
* Rozwiązano problem https://github.com/Azure/azure-powershell/issues/7402
    - Umożliwiono wyświetlanie list zasobów za pomocą parametru „-ResourceId” polecenia „Get-AzResource”

#### <a name="azservicebus"></a>Az.ServiceBus
* Dodano właściwość tylko do odczytu MigrationState do elementu PSServiceBusMigrationConfigurationAttributes, dzięki czemu można łatwiej sprawdzić stan migracji.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Rozwiązano problem z dodawaniem certyfikatu do zestawu skalowania maszyn wirtualnych w systemie Linux.
* Rozwiązano problem z poleceniem „Add-AzServiceFabricClusterCertificate”
    - Jest używany poprawny odcisk palca z nowego certyfikatu (Azure/service-fabric-issues#932).
    - Wyjątek jest wyświetlany poprawnie (Azure/service-fabric-issues#1054).
* Rozwiązano problem z poleceniem „Update-AzServiceFabricDurability” polegający na aktualizowaniu konfiguracji klastra przed rozpoczęciem operacji CreateOrUpdate zestawu skalowania maszyn wirtualnych.

## <a name="040---october-2018"></a>0.4.0 — październik 2018 r.
#### <a name="azprofile"></a>Az.Profile
* Rozwiązano problem z poleceniem Get-AzSubscription w usłudze CloudShell
* Zaktualizowano wspólny kod, aby korzystał z najnowszej wersji środowiska uruchomieniowego klienta

#### <a name="azcompute"></a>Az.Compute
* Dodano nowe rozmiary do listy dozwolonych rozmiarów maszyn wirtualnych, dla których będzie włączona przyspieszona sieć w przypadku użycia prostego zestawu parametrów dla polecenia „New-AzVm”
* Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Dodawanie obsługi dla reguł sieci wirtualnej
    - Get-AzDataLakeStoreVirtualNetworkRule: Pobiera lub wyświetla regułę sieci wirtualnej usługi Azure Data Lake Store.
    - Add-AzDataLakeStoreVirtualNetworkRule: Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.
    - Set-AzDataLakeStoreVirtualNetworkRule: Modyfikuje wskazaną regułę sieci wirtualnej na określonym koncie usługi Data Lake Store.
    - Remove-AzDataLakeStoreVirtualNetworkRule: Usuwa regułę sieci wirtualnej usługi Azure Data Lake Store.

#### <a name="aznetwork"></a>Az.Network
* Aktualizacja polecenia cmdlet Test-AzNetworkWatcherConnectivity: przekazywanie wartości protokołu do zaplecza.
* Dodano moduł uzupełniający argument ResourceName do wszystkich poleceń cmdlet.

#### <a name="azresources"></a>Az.Resources
* Rozwiązano problem polegający na tym, że polecenie Get-AzRoleDefinition zgłaszało niezrozumiały wyjątek (gdy domyślny profil nie zawierał subskrypcji i nie określono zakresu), dodając zrozumiały wyjątek do scenariusza. Oprócz tego ustawiono domyślny zestaw parametrów na wartość „RoleDefinitionNameParameterSet”.

## <a name="030---october-2018"></a>0.3.0 — październik 2018 r.
#### <a name="azurestorage"></a>Azure.Storage
* Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy
* Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.
    - Get-AzStorageUsage

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Obsługa polecenia Get-AzCognitiveServicesAccountSkus bez istniejącego konta.

#### <a name="azcompute"></a>Az.Compute
* Rozwiązano problem z poleceniem Get-AzVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne
* Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzVmss.
* Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption

#### <a name="azdatafactoryv2"></a>Az.DataFactoryV2
* Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.

#### <a name="aznetwork"></a>Az.Network
* Dodano funkcję NetworkProfile. Dodano nowe polecenia cmdlet
    - Get-AzNetworkProfile
    - New-AzNetworkProfile
    - Remove-AzNetworkProfile
    - Set-AzNetworkProfile
    - New-AzContainerNicConfig
    - New-AzContainerNicConfigIpConfig
* Dodano link skojarzenia usługi w modelu podsieci
* Dodano polecenia cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap i Remove-AzVirtualNetworkTap
* Dodano polecenia cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig i Remove-AzNEtworkInterfaceTapConfig

#### <a name="azrediscache"></a>Az.RedisCache
* Jako parametru Size będzie można użyć dowolnego ciągu. Dodano element P5 w menu podręcznym PSArgumentCompleter

#### <a name="azresources"></a>Az.Resources
* Dodano brakujący parametr -Mode do polecenia Set-AzPolicyDefinition
* Usunięto usterkę polecenia cmdlet Get-AzProviderOperation w operacjach ze źródłem zawierającym użytkownika

#### <a name="azsql"></a>Az.Sql
* Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure

#### <a name="azwebsites"></a>Az.Websites
* Nowe polecenie cmdlet Get-AzWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłego wdrażania kontenera
* Nowe polecenia cmdlet New-AzWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows

## <a name="020---september-2018"></a>0.2.0 — Wrzesień 2018 r.
 Wersja początkowa