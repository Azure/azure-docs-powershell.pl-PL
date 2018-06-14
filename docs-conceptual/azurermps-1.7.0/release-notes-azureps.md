---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 9a40eae86b60afb5e04dd6a6074b60e82731578f
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/08/2018
ms.locfileid: "34854634"
---
# <a name="release-notes"></a>Informacje o wersji

To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.

## <a name="version-170"></a>Wersja 1.7.0

* **Zmiana działania parametrów -Force, -Confirm i $ConfirmPreference dla wszystkich poleceń cmdlet. Zmieniamy tę implementację, aby była zgodna z wytycznymi programu PowerShell. W przypadku większości poleceń cmdlet oznacza to usunięcie parametru Force, zaś aby pominąć monit ShouldProcess, użytkownicy będą musieli dodać parametr: „-Confirm:$false” w swoich skryptach programu PowerShell.** Te zmiany rozwiązują następujące problemy:
  - Poprawnej implementacji funkcjonalności -WhatIf, pozwalając użytkownikom na ustalenie efektów polecenia cmdlet lub skryptu bez wprowadzania żadnych rzeczywistych zmian
  - Kontroli nad monitowaniem przy użyciu obejmującego całą sesję parametru $ConfirmPreference, dzięki czemu użytkownik jest monitowany na podstawie wpływu potencjalnej zmiany (zgłoszonej w ustawieniu ConfirmImpact w poleceniu cmdlet)
  - Specyficznej dla polecenia cmdlet kontroli nad monitami o potwierdzenie przy użyciu parametru –Confirm
  - Spójnego używania parametru ShouldContinue i -Force w poleceniach cmdlet tylko dla tych akcji, które wymagałyby monitowania użytkownika z powodu specjalnego rodzaju zmian (na przykład usuwania plików ukrytych)
  - Spójności z innymi poleceniami cmdlet programu PowerShell, dzięki czemu wiedza o pisaniu skryptów programu PowerShell z innych poleceń cmdlet natychmiast jest stosowana do poleceń cmdlet programu Azure PowerShell.

**Pamiętaj, że teraz, aby *automatycznie pominąć wszystkie monity w każdych okolicznościach*, polecenia cmdlet programu Azure PowerShell wymagają podania przez użytkownika dwóch parametrów:**
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* Azure Compute
  - Set-AzureRmVMADDomainExtension
  - Get-AzureRmVMADDomainExtension
  - Parametr -Redeploy dla polecenia Restart-AzureVM
  - Parametr -Validate dla poleceń Move-AzureService, Move-AzureStorageAccount i Move-AzureVirtualNetwork
  - Nazwa i wersja parametrów poleceń cmdlet rozszerzenia są opcjonalne jak przedtem.
  - Polecenie New-AzureVM może uzyskać typ licencji z obiektu maszyny wirtualnej.
* Azure Storage
  - Zmieniono parametr Tags na Tag oraz dodano alias parametru Tags
    + New-AzureRmStorageAccount
    + Set-AzureRmStorageAccount
* Azure Network
  - Dodano nowe polecenie cmdlet dla równorzędnych sieci wirtualnych
* Azure Redis Cache
  - Dodano nowe polecenie cmdlet dla polecenia Reset-AzureRmRedisCache
  - Dodano nowe polecenie cmdlet dla polecenia Export-AzureRmRedisCache
  - Dodano nowe polecenie cmdlet dla polecenia Import-AzureRmRedisCache
  - Zmodyfikowano polecenie cmdlet New-AzureRmRedisCache, aby uwzględnić zmianę parametru dla sieci wirtualnej
* Przywracanie/tworzenie kopii zapasowej bazy danych Azure SQL
  - Polecenia cmdlet dla funkcji kopii zapasowej dla długiego okresu przechowywania
  - Get-AzureRmSqlServerBackupLongTermRetentionVault
  - Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - Set-AzureRmSqlServerBackupLongTermRetentionVault
  - Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - Polecenie Restore-AzureRmSqlDatabase obsługuje teraz przywracanie do określonego momentu usuniętej bazy danych
  - Polecenie Restore-AzureRmSqlDatabase obsługuje teraz przywracanie z kopii zapasowej dla długiego okresu przechowywania
* Azure LogicApp
  - Dodano polecenia cmdlet kont integracji programu LogicApp.
  - Get-AzureRmIntegrationAccountAgreement
  - Get-AzureRmIntegrationAccountCallbackUrl
  - Get-AzureRmIntegrationAccountCertificate
  - Get-AzureRmIntegrationAccount
  - Get-AzureRmIntegrationAccountMap
  - Get-AzureRmIntegrationAccountPartner
  - Get-AzureRmIntegrationAccountSchema
  - New-AzureRmIntegrationAccountAgreement
  - New-AzureRmIntegrationAccountCertificate
  - New-AzureRmIntegrationAccount
  - New-AzureRmIntegrationAccountMap
  - New-AzureRmIntegrationAccountPartner
  - New-AzureRmIntegrationAccountSchema
  - Remove-AzureRmIntegrationAccountAgreement
  - Remove-AzureRmIntegrationAccountCertificate
  - Remove-AzureRmIntegrationAccount
  - Remove-AzureRmIntegrationAccountMap
  - Remove-AzureRmIntegrationAccountPartner
  - Remove-AzureRmIntegrationAccountSchema
  - Set-AzureRmIntegrationAccountAgreement
  - Set-AzureRmIntegrationAccountCertificate
  - Set-AzureRmIntegrationAccount
  - Set-AzureRmIntegrationAccountMap
  - Set-AzureRmIntegrationAccountPartner
  - Set-AzureRmIntegrationAccountSchema
* Azure Data Lake Store
  - Znacząco zwiększono wydajność przekazywania i pobierania plików oraz folderów.
  - Obejmuje to niewielkie zmiany nazw parametrów dla pobierania i włączenie dwóch nowych parametrów dla przekazywania:
    + NumThreads -> PerFileThreadCount, który służy do wskazywania liczby wątków do użycia w jednym pliku
    + ConcurrentFileCount, który służy do wskazywania liczby plików do równoległego przekazania/pobrania dla przekazywania/pobierania folderu.
  - Domyślne wartości wątkowości służą obecnie do zapewnienia lepszej ogólnej przepływności dla większości rozmiarów plików. Jeśli wydajność nie jest taka, jak wymagana, powyższe wartości można modyfikować, aby spełnić wymagania.
* Azure Data Lake Analytics
  - Polecenie Get-AzureRMDataLakeAnalyticsDataSource teraz zwraca wszystkie źródła danych, gdy zostanie wywołane bez argumentów.
  - Ta zmiana spowoduje również usunięcie parametru typu źródła danych z polecenia cmdlet.
  - Ta zmiana powoduje zwracanie nowego obiektu dla operacji listy z następującymi właściwościami:
    + Type, typ źródła danych
    + Name, nazwa źródła danych
    + IsDefault, ma wartość true, jeśli jest to domyślne źródło danych dla konta
  - Polecenie Get-AzureRMDataLakeAnalyticsJob jest stałe dla pewnych wartości przesunięcia daty i godziny podczas filtrowania według parametru submittedBefore i submittedAfter.
* Web Apps
  - Dodano polecenie cmdlet Swap-AzureRmWebAppSlot dla zwykłej wymiany i wymiany z podglądem
  - Rozszerzono polecenie cmdlet Set-AzureRmWebAppSlot w celu obsługi wymiany automatycznej
* Usługa Azure API Management
  - Poprawiono polecenia cmdlet wdrażania usługi Azure API Management dla polecenia AzureChinaCloud.
  - Usunięto polecenie cmdlet Set-AzureRmApiManagementTenantGitAccess, ponieważ właściwość Git Access jest domyślnie włączona.
* Tworzenie kopii zapasowej usług Azure Recovery Services
  - Dodano obsługę obciążenia Azure SQL
  - Dodano obsługę tworzenia kopii zapasowych i przywracania zaszyfrowanych maszyn wirtualnych platformy Azure
  - Backup-AzureRmRecoveryServicesBackupItem — dodano opcjonalny czas przechowywania punktów odzyskiwania
  - Poprawiono niewielkie błędy związane z filtrem w poleceniach cmdlet Get-AzureRmRecoveryServicesBackupContainer i Get-AzureRmRecoveryServicesBackupItem
* Azure Automation
  - Dodano polecenie Get-AzureRmAutomationHybridWorkerGroup
