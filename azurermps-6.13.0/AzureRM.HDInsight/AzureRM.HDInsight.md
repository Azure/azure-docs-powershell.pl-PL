---
Module Name: AzureRM.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
ms.openlocfilehash: bbbb418a8e101fa1b806bc910132f44e40158190
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522441"
---
# Moduł AzureRM. HDInsight
## Opis
W tematach w tej sekcji opisano polecenia cmdlet programu Azure PowerShell dla usługi HDInsight platformy Microsoft Azure w ramach usługi Azure Resource Manager (ARM). Te polecenia cmdlet służą do zarządzania klastrami usługi HDInsight i zadaniami, które są na nich uruchomione. Polecenia cmdlet istnieją w przestrzeni nazw Microsoft. Azure. Commands. HDInsight.

## Polecenia cmdlet usługi AzureRM. HDInsight
### [Dodaj-AzureRmHDInsightClusterIdentity](Add-AzureRmHDInsightClusterIdentity.md)
Dodaje tożsamość klastra do obiektu konfiguracji klastra.

### [Dodaj-AzureRmHDInsightComponentVersion](Add-AzureRmHDInsightComponentVersion.md)
Dodaje wersję usługi działającej w klastrze do obiektu konfiguracji klastra.

### [Dodaj-AzureRmHDInsightConfigValues](Add-AzureRmHDInsightConfigValues.md)
Umożliwia dodanie dostosowania wartości konfiguracji usługi Hadoop i/lub dostosowania biblioteki udostępnionej do obiektu konfiguracji klastra.

### [Dodaj-AzureRmHDInsightMetastore](Add-AzureRmHDInsightMetastore.md)
Dodaje bazę danych SQL do obiektu konfiguracji klastra jako gałąź lub Oozie datastore.

### [Dodaj-AzureRmHDInsightScriptAction](Add-AzureRmHDInsightScriptAction.md)
Umożliwia dodanie akcji skryptu do obiektu konfiguracji klastra.

### [Dodaj-AzureRmHDInsightSecurityProfile](Add-AzureRmHDInsightSecurityProfile.md)
Dodaje profileto zabezpieczeń do obiektu konfiguracji klastra.

### [Dodaj-AzureRmHDInsightStorage](Add-AzureRmHDInsightStorage.md)
Dodaje klucz usługi Azure Storage do obiektu konfiguracji klastra.

### [Disable-AzureRmHDInsightOperationsManagementSuite](Disable-AzureRmHDInsightOperationsManagementSuite.md)
Wyłącza Pakiet Operations Management Suite (OMS) w klastrze usługi HDInsight i odpowiednie dzienniki przestaną przepływ na obszar roboczy OMS określony podczas włączania.

### [Enable-AzureRmHDInsightOperationsManagementSuite](Enable-AzureRmHDInsightOperationsManagementSuite.md)
Włącza Pakiet Operations Management Suite (OMS) w klastrze usługi HDInsight i odpowiednie dzienniki zostaną wysłane do obszaru roboczego OMS określonego podczas włączania.

### [Get-AzureRmHDInsightCluster](Get-AzureRmHDInsightCluster.md)
Pobiera i wyświetla listę wszystkich klastrów usługi Azure HDInsight skojarzonych z bieżącą subskrypcją lub określoną grupą zasobów albo pobiera określony klaster.

### [Get-AzureRmHDInsightJob](Get-AzureRmHDInsightJob.md)
Pobiera listę zadań z klastra i wyświetla listę w odwrotnym porządku chronologicznym lub pobiera określone zadanie.

### [Get-AzureRmHDInsightJobOutput](Get-AzureRmHDInsightJobOutput.md)
Pobiera dane wyjściowe dziennika dla zadania z konta magazynu skojarzonego z określonym klastrem.

### [Get-AzureRmHDInsightOperationsManagementSuite](Get-AzureRmHDInsightOperationsManagementSuite.md)
Pobiera stan instalacji usługi Operations Management Suite (OMS) w klastrze.

### [Get-AzureRmHDInsightPersistedScriptAction](Get-AzureRmHDInsightPersistedScriptAction.md)
Pobiera akcje trwałego skryptu dla klastra i umieszcza je na liście w kolejności chronologicznej lub pobiera szczegóły określonego działania skryptu trwałego.

### [Get-AzureRmHDInsightProperties](Get-AzureRmHDInsightProperties.md)
Pobiera właściwości usługi HDInsight, takie jak dostępne lokalizacje i pojemność.

### [Get-AzureRmHDInsightScriptActionHistory](Get-AzureRmHDInsightScriptActionHistory.md)
Pobiera historię akcji skryptów dla klastra i wyświetla ją w odwrotnej kolejności chronologicznej lub zawiera szczegółowe informacje o wykonanej akcji skryptu.

### [Grant-AzureRmHDInsightHttpServicesAccess](Grant-AzureRmHDInsightHttpServicesAccess.md)
Przyznaje dostęp HTTP do klastra.

### [Grant-AzureRmHDInsightRdpServicesAccess](Grant-AzureRmHDInsightRdpServicesAccess.md)
Udziela dostępu RDP do klastra systemu Windows.

### [Invoke-AzureRmHDInsightHiveJob](Invoke-AzureRmHDInsightHiveJob.md)
Przesyła zapytanie o aplikację Hive do klastra usługi HDInsight i pobiera wyniki zapytania w ramach jednej operacji.

### [Nowe — AzureRmHDInsightCluster](New-AzureRmHDInsightCluster.md)
Tworzy klaster usługi Azure HDInsight w określonej grupie zasobów dla bieżącej subskrypcji.

### [Nowe — AzureRmHDInsightClusterConfig](New-AzureRmHDInsightClusterConfig.md)
Tworzy nieutrwalony obiekt konfiguracji klastra opisujący konfigurację klastra usługi Azure HDInsight.

### [Nowe — AzureRmHDInsightHiveJobDefinition](New-AzureRmHDInsightHiveJobDefinition.md)
Tworzy obiekt zadania w usłudze Hive.

### [Nowe — AzureRmHDInsightMapReduceJobDefinition](New-AzureRmHDInsightMapReduceJobDefinition.md)
Tworzy obiekt zadania programu MapReduce.

### [Nowe — AzureRmHDInsightPigJobDefinition](New-AzureRmHDInsightPigJobDefinition.md)
Tworzy obiekt zadania świni.

### [Nowe — AzureRmHDInsightSqoopJobDefinition](New-AzureRmHDInsightSqoopJobDefinition.md)
Tworzy obiekt zadania programu Sqoop.

### [Nowe — AzureRmHDInsightStreamingMapReduceJobDefinition](New-AzureRmHDInsightStreamingMapReduceJobDefinition.md)
Tworzy obiekt zadania przesyłania strumieniowego MapReduce.

### [Remove-AzureRmHDInsightCluster](Remove-AzureRmHDInsightCluster.md)
Umożliwia usunięcie określonego klastra usługi HDInsight z bieżącej subskrypcji.

### [Remove-AzureRmHDInsightPersistedScriptAction](Remove-AzureRmHDInsightPersistedScriptAction.md)
Usuwa akcję trwałego skryptu z klastra usługi HDInsight.

### [REVOKE-AzureRmHDInsightHttpServicesAccess](Revoke-AzureRmHDInsightHttpServicesAccess.md)
Wyłącza dostęp HTTP do klastra.

### [REVOKE-AzureRmHDInsightRdpServicesAccess](Revoke-AzureRmHDInsightRdpServicesAccess.md)
Wyłącza dostęp RDP do klastra systemu Windows.

### [Set-AzureRmHDInsightClusterSize](Set-AzureRmHDInsightClusterSize.md)
Ustawia liczbę węzłów procesu roboczego w określonym klastrze.

### [Set-AzureRmHDInsightDefaultStorage](Set-AzureRmHDInsightDefaultStorage.md)
Ustawia domyślne ustawienie konta magazynu w obiekcie konfiguracji klastra.

### [Set-AzureRmHDInsightPersistedScriptAction](Set-AzureRmHDInsightPersistedScriptAction.md)
Ustawia poprzednio wykonaną akcję skryptu, która będzie akcją utrwalonego skryptu.

### [Start — AzureRmHDInsightJob](Start-AzureRmHDInsightJob.md)
Rozpoczynanie zdefiniowanego zadania usługi Azure HDInsight w określonym klastrze.

### [Zatrzymaj — AzureRmHDInsightJob](Stop-AzureRmHDInsightJob.md)
Zatrzymuje określone uruchomione zadanie w klastrze.

### [Prześlij — AzureRmHDInsightScriptAction](Submit-AzureRmHDInsightScriptAction.md)
Wysyła nową akcję skryptu do klastra usługi Azure HDInsight.

### [Użyj — AzureRmHDInsightCluster](Use-AzureRmHDInsightCluster.md)
Umożliwia wybranie klastra do użycia z poleceniem cmdlet Invoke-RmAzureHDInsightHiveJob.

### [Wait-AzureRmHDInsightJob](Wait-AzureRmHDInsightJob.md)
Oczekuje na zakończenie lub niepowodzenie określonego zadania.

