---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a>Informacje o wersji

To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.

---

## <a name="600---may-2018"></a>6.0.0 — maj 2018 r.

### <a name="general"></a>Ogólne
* Ustawianie zależności minimalnej modułów na program PowerShell 5.0

### <a name="azurestorage"></a>Azure.Storage
* Obsługa jako nazwa kontenera magazynu usługi Storage Blob
    - New-AzureStorageBlobContainer
    - Remove-AzureStorageBlobContainer
    - Set-AzureStorageBlobContent
    - Get-AzureStorageBlobContent
* Rozwiązano problem polegający na tym, że niektóre dane wyjściowe dotyczące błędów nie zawierają szczegółowych informacji o błędzie

### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Wprowadzenie wielu zmian powodujących niezgodność
    - Więcej informacji można znaleźć w przewodniku po migracji

### <a name="azurermautomation"></a>AzureRM.Automation
* Usunięto przestarzałe aliasy „Tags” z poleceń cmdlet
    - „Set-AzureRmAutomationRunbook”

### <a name="azurermbatch"></a>AzureRM.Batch
* Zaktualizowano dokumentację polecenia New-AzureBatchPool w celu usunięcia przestarzałego przykładu

### <a name="azurermcdn"></a>AzureRM.Cdn
* Wprowadzenie wielu zmian powodujących niezgodność
    - Więcej informacji można znaleźć w przewodniku po migracji

### <a name="azurermcompute"></a>AzureRM.Compute
* Polecenia „New-AzureRmVm” i „New-AzureRmVmss” obsługują pełne dane wyjściowe parametrów
* Polecenia „New-AzureRmVm” i „New-AzureRmVmss” (prosty zestaw parametrów) obsługują przypisywanie maszynom wirtualnych tożsamości zdefiniowanych przez użytkownika i/lub system.
* Ponowne wdrażanie zestawu skalowania maszyn wirtualnych i funkcja PerformMaintenance
    -  Dodano nowy parametr przełącznika -Redeploy and -PerformMaintenance do poleceń „New-AzureRmVm” i „New-AzureRmVmss”
* Dodano parametr przełącznika DisableVMAgent do polecenia cmdlet „Set-AzureRmVMOperatingSystem”
* Polecenia „New-AzureRmVm” i „New-AzureRmVmss” (prosty zestaw parametrów) obsługują obraz „Win10”.
* Dodano polecenie cmdlet „Repair-AzureRmVmssServiceFabricUpdateDomain”.
* Wprowadzenie wielu zmian powodujących niezgodność
    - Więcej informacji można znaleźć w przewodniku po migracji
* Polecenie „Set-AzureRmVmDiskEncryptionExtension” umożliwia opcjonalne użycie parametrów usługi AAD

### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Usunięto przestarzałe aliasy „Tags” z poleceń cmdlet
    - New-AzureRmDataFactory

### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Zaktualizowano zestaw ADF .Net SDK do wersji 0.7.0-preview zawierającej następujące zmiany:
    - Dodano parametry wykonywania i właściwość menedżerów połączenia w działaniu ExecuteSSISPackage
    - Zaktualizowano połączoną usługę baz danych PostgreSql i MySql w celu używania pełnych parametrów połączenia zamiast serwera, bazy danych, schematu, nazwy użytkownika i hasła
    - Wyłączono schemat z połączonej usługi bazy danych DB2
    - Usunięto właściwość schematu z połączonej usługi programu Teradata
    - Dodano elementy LinkedService, Dataset i CopySource do rozwiązania Responsys

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Usunięto przestarzałe aliasy „Tags” z poleceń cmdlet
    - „New-AzureRmDataLakeAnalyticsAccount”
    - „Set-AzureRmDataLakeAnalyticsAccount”

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Dodano nową funkcję służącą do cyklicznej zmiany listy ACL do poleceń Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry i Set-AzureRmDataLakeStoreItemAcl
* Dodano nowe polecenie cmdlet służące do pobierania podsumowania zawartości w ramach katalogu
* Dodano nowe polecenie cmdlet służące do pobierania użycia dysku i zrzutu listy ACL
* Poprawiono typ zwracany wartości logicznej polecenia Set-AzureRmDataLakeStoreItemAcl na interfejs IEnumerable<DataLakeStoreItemAce>
* Poprawiono typ zwracany wartości logicznej polecenia Set-AzureRmDataLakeStoreItemAclEntry na interfejs IEnumerable<DataLakeStoreItemAce>
* Zmiany powodujące niezgodność dotyczące poleceń Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem i Remove-AzureRmDataLakeStoreItem

### <a name="azurermdns"></a>AzureRM.Dns
* Wprowadzenie wielu zmian powodujących niezgodność
    - Więcej informacji można znaleźć w przewodniku po migracji

### <a name="azurermeventhub"></a>AzureRM.EventHub
* Zaktualizowano informacje pomocy dotyczącą poleceń cmdlet brakującymi przykładami

### <a name="azurerminsights"></a>AzureRM.Insights
* Wprowadzono wiele zmian powodujących niezgodność
    - Więcej informacji można znaleźć w przewodniku po migracji

### <a name="azurermiothub"></a>AzureRM.IotHub
* Włączono tagi i podstawową jednostkę SKU w usłudze IotHub

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Zmiany powodujące niezgodność dotyczące obsługi scenariuszy z potokami
* Dodano nowe polecenia cmdlet: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval i Undo-AzureKeyVaultManagedStorageAccountRemoval

### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Usunięto przestarzałe aliasy „Tags” z poleceń cmdlet
    - Update-AzureRmMlCommitmentPlan

### <a name="azurermmedia"></a>AzureRM.Media
* Usunięto przestarzałe aliasy „Tags” z poleceń cmdlet
    - „Set-AzureRmMediaService”

### <a name="azurermnetwork"></a>AzureRM.Network
* Dodano obsługę zasobów planu ochrony przed atakami DDoS
* Wprowadzono wiele zmian powodujących niezgodność
    - Więcej informacji można znaleźć w przewodniku po migracji

### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Wprowadzenie wielu zmian powodujących niezgodność
    - Więcej informacji można znaleźć w przewodniku po migracji

### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Wprowadzenie wielu zmian powodujących niezgodność
    - Więcej informacji można znaleźć w przewodniku po migracji

### <a name="azurermprofile"></a>AzureRM.Profile
* Domyślnie włączono automatyczne zapisywanie kontekstu
* Dodano właściwości USGovernmentOperationalInsightsEndpoint i USGovernmentOperationalInsightsEndpointResourceId do środowiska platformy Azure dla instytucji rządowych USA.

### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Naprawiono nagłówek uwierzytelnienia w scenariuszach usługi SiteRecovery

### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Wprowadzono wiele zmian powodujących niezgodność
    - Więcej informacji można znaleźć w przewodniku po migracji

### <a name="azurermresources"></a>AzureRM.Resources
* Usunięto przestarzały parametr -AtScopeAndBelow z wywołania Get-AzureRmRoledefinition
* Dołączono przypisania do usuniętych użytkowników/grup/jednostek usługi w wynikach polecenia Get-AzureRmRoleAssignment
* Dodano moduły wypełniania kart dla zakresu i typu zasobu
* Dodano wygodne polecenie cmdlet służące do tworzenia wygody tworzenia jednostek usługi
* Scalono funkcje Get- i Find w poleceniu Get-AzureRmResource
* Dodawano polecenia cmdlet usługi AD:
  - Remove-AzureRmADGroupMember
  - Get-AzureRmADGroup
  - New-AzureRmADGroup
  - Remove-AzureRmADGroup
  - Remove-AzureRmADUser
  - Update-AzureRmADApplication
  - Update-AzureRmADServicePrincipal
  - Update-AzureRmADUser

### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Zaktualizowano domyślną jednostkę SKU wersji obrazu systemu Linux
  - Domyślna aktualizacja jednostki SKU serwera UbuntuServer1604 (plik NewAzureServiceFabricCluster.cs)

### <a name="azurermstorage"></a>AzureRM.Storage
* Wprowadzono wiele zmian powodujących niezgodność
    - Więcej informacji można znaleźć w przewodniku po migracji

### <a name="azurermwebsites"></a>AzureRM.Websites
* Przeprowadzono uaktualnienie do najnowszej wersji zestawu SDK witryn internetowych
* Dodane właściwości -AssignIdentity i -Httpsonly do poleceń Set-AzureRmWebApp i Set-AzureRmWebAppSlot
* Dodano dwa nowe polecenia cmdlet: Get-AzureRmWebAppSnapshots i Restore-AzureRmWebAppSnapshot
