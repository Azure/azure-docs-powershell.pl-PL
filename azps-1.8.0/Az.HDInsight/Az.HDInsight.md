---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: 78153558764d12a63d6c1b599da2067338969628
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93704366"
---
# AZ. moduł HDInsight
## Opis
W tematach w tej sekcji opisano polecenia cmdlet programu Azure PowerShell dla usługi HDInsight platformy Microsoft Azure w ramach usługi Azure Resource Manager (ARM). Te polecenia cmdlet służą do zarządzania klastrami usługi HDInsight i zadaniami, które są na nich uruchomione. Polecenia cmdlet istnieją w przestrzeni nazw Microsoft. Azure. Commands. HDInsight.

## AZ.
### [Dodaj-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
Dodaje tożsamość klastra do obiektu konfiguracji klastra.

### [Dodaj-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
Dodaje wersję usługi działającej w klastrze do obiektu konfiguracji klastra.

### [Dodaj-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
Umożliwia dodanie dostosowania wartości konfiguracji usługi Hadoop i/lub dostosowania biblioteki udostępnionej do obiektu konfiguracji klastra.

### [Dodaj-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
Dodaje bazę danych SQL do obiektu konfiguracji klastra jako gałąź lub Oozie datastore.

### [Dodaj-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
Umożliwia dodanie akcji skryptu do obiektu konfiguracji klastra.

### [Dodaj-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
Dodaje profileto zabezpieczeń do obiektu konfiguracji klastra.

### [Dodaj-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Dodaje klucz usługi Azure Storage do obiektu konfiguracji klastra.

### [Disable-AzHDInsightOperationsManagementSuite](Disable-AzHDInsightOperationsManagementSuite.md)
Wyłącza Pakiet Operations Management Suite (OMS) w klastrze usługi HDInsight i odpowiednie dzienniki przestaną przepływ na obszar roboczy OMS określony podczas włączania.

### [Enable-AzHDInsightOperationsManagementSuite](Enable-AzHDInsightOperationsManagementSuite.md)
Włącza Pakiet Operations Management Suite (OMS) w klastrze usługi HDInsight i odpowiednie dzienniki zostaną wysłane do obszaru roboczego OMS określonego podczas włączania.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
Pobiera i wyświetla listę wszystkich klastrów usługi Azure HDInsight skojarzonych z bieżącą subskrypcją lub określoną grupą zasobów albo pobiera określony klaster.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Pobiera listę zadań z klastra i wyświetla listę w odwrotnym porządku chronologicznym lub pobiera określone zadanie.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
Pobiera dane wyjściowe dziennika dla zadania z konta magazynu skojarzonego z określonym klastrem.

### [Get-AzHDInsightOperationsManagementSuite](Get-AzHDInsightOperationsManagementSuite.md)
Pobiera stan instalacji usługi Operations Management Suite (OMS) w klastrze.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Pobiera akcje trwałego skryptu dla klastra i umieszcza je na liście w kolejności chronologicznej lub pobiera szczegóły określonego działania skryptu trwałego.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Pobiera właściwości usługi HDInsight, takie jak dostępne lokalizacje i pojemność.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Pobiera historię akcji skryptów dla klastra i wyświetla ją w odwrotnej kolejności chronologicznej lub zawiera szczegółowe informacje o wykonanej akcji skryptu.

### [Grant-AzHDInsightHttpServicesAccess](Grant-AzHDInsightHttpServicesAccess.md)
Przyznaje dostęp HTTP do klastra.

### [Grant-AzHDInsightRdpServicesAccess](Grant-AzHDInsightRdpServicesAccess.md)
Udziela dostępu RDP do klastra systemu Windows.

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
Przesyła zapytanie o aplikację Hive do klastra usługi HDInsight i pobiera wyniki zapytania w ramach jednej operacji.

### [Nowe — AzHDInsightCluster](New-AzHDInsightCluster.md)
Tworzy klaster usługi Azure HDInsight w określonej grupie zasobów dla bieżącej subskrypcji.

### [Nowe — AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Tworzy nieutrwalony obiekt konfiguracji klastra opisujący konfigurację klastra usługi Azure HDInsight.

### [Nowe — AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
Tworzy obiekt zadania w usłudze Hive.

### [Nowe — AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
Tworzy obiekt zadania programu MapReduce.

### [Nowe — AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
Tworzy obiekt zadania świni.

### [Nowe — AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
Tworzy obiekt zadania programu Sqoop.

### [Nowe — AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
Tworzy obiekt zadania przesyłania strumieniowego MapReduce.

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
Umożliwia usunięcie określonego klastra usługi HDInsight z bieżącej subskrypcji.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Usuwa akcję trwałego skryptu z klastra usługi HDInsight.

### [REVOKE-AzHDInsightHttpServicesAccess](Revoke-AzHDInsightHttpServicesAccess.md)
Wyłącza dostęp HTTP do klastra.

### [REVOKE-AzHDInsightRdpServicesAccess](Revoke-AzHDInsightRdpServicesAccess.md)
Wyłącza dostęp RDP do klastra systemu Windows.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
Ustawia liczbę węzłów procesu roboczego w określonym klastrze.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Ustawia domyślne ustawienie konta magazynu w obiekcie konfiguracji klastra.

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
Ustawia poprzednio wykonaną akcję skryptu, która będzie akcją utrwalonego skryptu.

### [Start — AzHDInsightJob](Start-AzHDInsightJob.md)
Rozpoczynanie zdefiniowanego zadania usługi Azure HDInsight w określonym klastrze.

### [Zatrzymaj — AzHDInsightJob](Stop-AzHDInsightJob.md)
Zatrzymuje określone uruchomione zadanie w klastrze.

### [Prześlij — AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
Wysyła nową akcję skryptu do klastra usługi Azure HDInsight.

### [Użyj — AzHDInsightCluster](Use-AzHDInsightCluster.md)
Umożliwia wybranie klastra do użycia z poleceniem cmdlet Invoke-RmAzureHDInsightHiveJob.

### [Wait-AzHDInsightJob](Wait-AzHDInsightJob.md)
Oczekuje na zakończenie lub niepowodzenie określonego zadania.

