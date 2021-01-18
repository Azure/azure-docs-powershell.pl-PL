---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: e3c3bb9d4d8225823ec84750c8292288ce25c15b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500998"
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
Dodaje profil zabezpieczeń do obiektu konfiguracji klastra.

### [Dodaj-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Dodaje klucz usługi Azure Storage do obiektu konfiguracji klastra.

### [Disable-AzHDInsightMonitoring](Disable-AzHDInsightMonitoring.md)
Wyłącza monitorowanie w klastrze usługi HDInsight, a odpowiednie dzienniki będą przelewane do obszaru roboczego monitorowania określonego podczas włączania.

### [Enable-AzHDInsightMonitoring](Enable-AzHDInsightMonitoring.md)
Umożliwia monitorowanie w klastrze usługi HDInsight i odpowiednie dzienniki zostaną wysłane do obszaru roboczego monitorowania określonego podczas włączania.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
Pobiera i wyświetla listę wszystkich klastrów usługi Azure HDInsight skojarzonych z bieżącą subskrypcją lub określoną grupą zasobów albo pobiera określony klaster.

### [Get-AzHDInsightClusterAutoscaleConfiguration](Get-AzHDInsightClusterAutoscaleConfiguration.md)
Pobiera konfigurację autoskalowania klastra usługi HDInsight.

### [Get-AzHDInsightHost](Get-AzHDInsightHost.md)
Wyświetla listę hostów klastra usługi HDInsight.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Pobiera listę zadań z klastra i wyświetla listę w odwrotnym porządku chronologicznym lub pobiera określone zadanie.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
Pobiera dane wyjściowe dziennika dla zadania z konta magazynu skojarzonego z określonym klastrem.

### [Get-AzHDInsightMonitoring](Get-AzHDInsightMonitoring.md)
Pobiera stan instalacji monitorowania w klastrze.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Pobiera akcje trwałego skryptu dla klastra i umieszcza je na liście w kolejności chronologicznej lub pobiera szczegóły określonego działania skryptu trwałego.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Pobiera właściwości usługi HDInsight, takie jak dostępne lokalizacje i pojemność.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Pobiera historię akcji skryptów dla klastra i wyświetla ją w odwrotnej kolejności chronologicznej lub zawiera szczegółowe informacje o wykonanej akcji skryptu.

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
Przesyła zapytanie o aplikację Hive do klastra usługi HDInsight i pobiera wyniki zapytania w ramach jednej operacji.

### [Nowe — AzHDInsightCluster](New-AzHDInsightCluster.md)
Tworzy klaster usługi Azure HDInsight w określonej grupie zasobów dla bieżącej subskrypcji.

### [Nowe — AzHDInsightClusterAutoscaleConfiguration](New-AzHDInsightClusterAutoscaleConfiguration.md)
Tworzy nieutrwalony obiekt, który opisuje konfigurację autoskalowania klastra usługi Azure HDInsight.

### [Nowe — AzHDInsightClusterAutoscaleScheduleCondition](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
Tworzy warunek autoskalowania na podstawie harmonogramu.

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

### [Remove-AzHDInsightClusterAutoscaleConfiguration](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
Usuwa konfigurację autoskalowania klastra usługi HDInsight.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Usuwa akcję trwałego skryptu z klastra usługi HDInsight.

### [Restart-AzHDInsightHost](Restart-AzHDInsightHost.md)
Ponownie uruchamia określone hosty klastra usługi HDInsight.

### [Set-AzHDInsightClusterAutoscaleConfiguration](Set-AzHDInsightClusterAutoscaleConfiguration.md)
Ustawia konfigurację autoskalowania klastra usługi Azure HDInsight.

### [Set-AzHDInsightClusterDiskEncryptionKey](Set-AzHDInsightClusterDiskEncryptionKey.md)
Obraca klucz szyfrowania dysku określonego klastra usługi HDInsight.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
Ustawia liczbę węzłów procesu roboczego w określonym klastrze.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Ustawia domyślne ustawienie konta magazynu w obiekcie konfiguracji klastra.

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
Ustawia poświadczenia HTTP bramy klastra usługi Azure HDInsight.

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

