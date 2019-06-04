---
ms.openlocfilehash: 10d8d50131b3c55ae19c5142c42cb47f37c68c92
ms.sourcegitcommit: 6171bab74aec6785938cad54d584f425ddbb850e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/21/2019
ms.locfileid: "65971907"
---
## <a name="180---april-2019"></a>1.8.0 — kwiecień 2019 r.
### <a name="highlights-since-the-last-major-release"></a>Najważniejsze zmiany od ostatniej wersji głównej
* Ogólna dostępność modułu `Az`
* Aby uzyskać więcej informacji na temat modułu `Az`, odwiedź następujące strony: https://aka.ms/azps-announce
* Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/
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
* Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/
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
* Dodano moduły wypełniania elementów Location, ResourceGroup i ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/
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