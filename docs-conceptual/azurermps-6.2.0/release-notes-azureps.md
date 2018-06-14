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
ms.openlocfilehash: 5bc3c9079cb4019bdb2255ab1f947e8ad35ae4cc
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853461"
---
# <a name="release-notes"></a>Informacje o wersji

To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.

---
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