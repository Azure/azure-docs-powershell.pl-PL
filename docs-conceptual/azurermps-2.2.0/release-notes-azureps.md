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
ms.openlocfilehash: ca25f3c66f8e8f4c64fc04275da2bd28e32d2f6c
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/08/2018
ms.locfileid: "34854617"
---
# <a name="release-notes"></a>Informacje o wersji

To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.

## <a name="version-220"></a>Wersja 2.2.0
* Compute
  - Dodano obsługę pytania o stan szyfrowania z rozszerzenia AzureDiskEncryptionForLinux
* DataFactory
  - Dodano nowe polecenie cmdlet do wyświetlania listy okien działania
    + Get-AzureRmDataFactoryActivityWindow
* DataLake
  - Zmieniono parametr `Host` na `DatabaseHost` i dodano alias do `Host`
    + New-AzureRmDataLakeAnalyticsCatalogSecret
    + Set-AzureRmDataLakeAnalyticsCatalogSecret
  - Dodano obsługę usuwania listy ACL i domyślnej listy ACL
  - Dodano obsługę pobierania i ustawiania nienazwanych uprawnień do plików i folderów
* KeyVault
  - Dodano obsługę certyfikatów
    + Add-AzureKeyVaultCertificate
    + Add-AzureKeyVaultCertificateContact
    + Get-AzureKeyVaultCertificate
    + Get-AzureKeyVaultCertificateContact
    + Get-AzureKeyVaultCertificateIssuer
    + Get-AzureKeyVaultCertificateOperation
    + Get-AzureKeyVaultCertificatePolicy
    + Import-AzureKeyVaultCertificate
    + New-AzureKeyVaultCertificateAdministratorDetails
    + New-AzureKeyVaultCertificateOrganizationDetails
    + New-AzureKeyVaultCertificatePolicy
    + Remove-AzureKeyVaultCertificate
    + Remove-AzureKeyVaultCertificateContact
    + Remove-AzureKeyVaultCertificateIssuer
    + Remove-AzureKeyVaultCertificateOperation
    + Set-AzureKeyVaultCertificateAttribute
    + Set-AzureKeyVaultCertificateIssuer
    + Set-AzureKeyVaultCertificatePolicy
    + Stop-AzureKeyVaultCertificateOperation
* Sieć

  - Dodano nowy parametr przełącznika interfejsu sieciowego, aby włączyć/wyłączyć wydajniejsze sieci +New-AzureRmNetworkInterface -EnableAcceleratedNetworking
  - Włączono polecenia cmdlet programu PowerShell funkcji bramy Active-Active
    + Add-AzureRmVirtualNetworkGatewayIpConfig
    + Remove-AzureRmVirtualNetworkGatewayIpConfig
  - Dodano nowe polecenie cmdlet
    + Test-AzureRmPrivateIpAddressAvailability
* Zasoby
  - Obsługa stref w poleceniach cmdlet dostawcy i zasobów
    + Get-AzureRmProvider
    + New-AzureRmResource
    + Set-AzureRmResource
* Sql
  - Dodano nowe polecenia cmdlet do zarządzania zasadami wykrywania zagrożeń usług Azure SQL na poziomie serwera
    + Get-AzureRmSqlServerThreatDetectionPolicy
    + Remove-AzureRmSqlServerThreatDetectionPolicy
    + Set-AzureRmSqlServerThreatDetectionPolicy
  - Dodano nowe polecenia cmdlet do obsługi włączania/wyłączania zasad GeoBackupPolicy dla usług Azure SQL DataWarehouse
    + Get-AzureRmSqlDatabaseGeoBackupPolicy
    + Set-AzureRmSqlDatabaseGeoBackupPolicy
  - Dodano nowe polecenia cmdlet dla interfejsów API usług Azure SQL Advisor i zalecanych akcji
    + Get-AzureRmSqlDatabaseAdvisor
    + Get-AzureRmSqlElasticPoolAdvisor
    + Get-AzureRmSqlServerAdvisor
    + Get-AzureRmSqlDatabaseRecommendedActions
    + Get-AzureRmSqlElasticPoolRecommendedActions
    + Get-AzureRmSqlServerRecommendedActions
    + Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus
    + Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus
    + Set-AzureRmSqlServerAdvisorAutoExecuteStatus
    + Set-AzureRmSqlDatabaseRecommendedActionState
    + Set-AzureRmSqlElasticPoolRecommendedActionState
    + Set-AzureRmSqlServerRecommendedActionState
