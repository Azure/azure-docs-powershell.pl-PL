---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: e3c3bb9d4d8225823ec84750c8292288ce25c15b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241435"
---
# Moduł Az.HDInsight
## Opis
Tematy w tej sekcji dokumentu zawierają polecenia cmdlet programu Azure PowerShell dla usługi HdInsight platformy Microsoft Azure w ramach usługi Azure Resource Manager (ARM). Te polecenia cmdlet są używane do zarządzania klastrami HDInsight i uruchomionymi na nich zadaniami. Polecenia cmdlet istnieją w przestrzeni nazw Microsoft.Azure.Commands.HDInsight.

## Az.HDInsight Cmdlet
### [Add-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
Dodaje tożsamość klastrów do obiektu konfiguracji klastrów.

### [Add-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
Dodaje wersję dla usługi uruchomionej w klastrze do obiektu konfiguracji klastrów.

### [Add-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
Powoduje dodanie dostosowania wartości konfiguracji usługi Hadoop i/lub dostosowania biblioteki udostępnionej w użytku w obiekcie konfiguracji klastrów.

### [Add-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
Dodaje bazę danych SQL, która będzie pełnić funkcję metastore Oozie lub Gałąź do obiektu konfiguracji klastrów.

### [Add-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
Dodaje akcję skryptu do obiektu konfiguracji klastrów.

### [Add-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
Dodaje profil zabezpieczeń do obiektu konfiguracji klastrów.

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Dodaje klucz magazynu platformy Azure do obiektu konfiguracji klastrów.

### [Disable-AzHDInsightMonitoring](Disable-AzHDInsightMonitoring.md)
Wyłącza monitorowanie w klastrze HDInsight i odpowiednie dzienniki przestaną przepływać do obszaru roboczego monitorowania określonego podczas włączania.

### [Enable-AzHDInsightMonitoring](Enable-AzHDInsightMonitoring.md)
Umożliwia monitorowanie w klastrze HDInsight, a odpowiednie dzienniki będą wysyłane do obszaru roboczego monitorowania określonego podczas włączania.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
Pobiera i wyświetla wszystkie klastry usługi Azure HDInsight skojarzone z bieżącą subskrypcją lub określoną grupą zasobów albo pobiera określony klaster.

### [Get-AzHDInsightClusterAutoscaleConfiguration](Get-AzHDInsightClusterAutoscaleConfiguration.md)
Pobiera konfigurację automatycznego skalowania klastrów HDInsight.

### [Get-AzHDInsightHost](Get-AzHDInsightHost.md)
Wyświetla listę hostów klastrów HDInsight.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Pobiera listę zadań z klastra i wyświetla je w odwrotnej kolejności chronologicznej lub pobiera określone zadanie.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
Pobiera dane wyjściowe dziennika dla zadania z konta magazynu skojarzonego z określonym klastrem.

### [Get-AzHDInsightMonitoring](Get-AzHDInsightMonitoring.md)
Pobiera stan instalacji monitorowania w klastrze.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Pobiera utrwalone akcje skryptu dla klastra i wyświetla je w porządku chronologicznym lub pobiera szczegółowe informacje dotyczące określonej, utrwalonej akcji skryptu.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Pobiera właściwości usługi HDInsight, takie jak dostępne lokalizacje i pojemność.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Pobiera historię akcji skryptu dla klastra i wyświetla ją w odwrotnej kolejności chronologicznej lub zawiera szczegóły wcześniej wykonanej akcji skryptu.

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
Przesyła zapytanie Do klastra HDInsight i pobiera wyniki zapytania w jednej operacji.

### [New-AzHDInsightCluster](New-AzHDInsightCluster.md)
Tworzy klaster usługi Azure HDInsight w określonej grupie zasobów dla bieżącej subskrypcji.

### [New-AzHDInsightClusterAutoscaleConfiguration](New-AzHDInsightClusterAutoscaleConfiguration.md)
Tworzy nietrwale obiekt opisujący konfigurację skalowania automatycznego klastrów usługi Azure HDInsight.

### [New-AzHDInsightClusterAutoscaleScheduleCondition](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
Tworzy warunek autoskalowania oparty na harmonogramie.

### [New-AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Tworzy nietrwale obiekt konfiguracji klastrów opisujący konfigurację klastrów HDInsight platformy Azure.

### [New-AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
Tworzy obiekt zadania Gałąź.

### [New-AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
Tworzy obiekt zadania MapReduce.

### [New-AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
Tworzy obiekt zadania Świnka.

### [New-AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
Tworzy obiekt zadania Sqoop.

### [New-AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
Tworzy obiekt zadania MapReduce przesyłania strumieniowego.

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
Usuwa określony klaster USŁUGI HDInsight z bieżącej subskrypcji.

### [Remove-AzHDInsightClusterAutoscaleConfiguration](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
Usuwa konfigurację automatycznego skalowania klastrów HDInsight.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Usuwa trwałą akcję skryptu z klastra HDInsight.

### [Restart-AzHDInsightHost](Restart-AzHDInsightHost.md)
Powoduje ponowne uruchomienie określonych hostów klastrów HDInsight.

### [Set-AzHDInsightClusterAutoscaleConfiguration](Set-AzHDInsightClusterAutoscaleConfiguration.md)
Ustawia konfigurację automatycznego skalowania klastra usługi Azure HDInsight.

### [Set-AzHDInsightClusterCryptEncryptionKey](Set-AzHDInsightClusterDiskEncryptionKey.md)
Obraca klucz szyfrowania dysku określonego klastra usługi HDInsight.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
Ustawia liczbę węzłów pracownik w określonym klastrze.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Ustawia domyślne ustawienie konta magazynu w obiekcie konfiguracji klastrów.

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
Ustawia poświadczenia HTTP bramy klastrów HDInsight platformy Azure.

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
Ustawia wcześniej wykonaną akcję skryptu jako trwałą akcję skryptu.

### [Start-AzHDInsightJob](Start-AzHDInsightJob.md)
Uruchamia zdefiniowane zadanie usługi Azure HDInsight w określonym klastrze.

### [Stop-AzHDInsightJob](Stop-AzHDInsightJob.md)
Zatrzymuje określone zadanie uruchomione w klastrze.

### [Submit-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
Przesyła nową akcję skryptu do klastrów usługi Azure HDInsight.

### [Use-AzHDInsightCluster](Use-AzHDInsightCluster.md)
Wybiera klaster, który ma być używany z Invoke-RmAzureHDInsightHiveJob cmdlet.

### [Wait-AzHDInsightJob](Wait-AzHDInsightJob.md)
Czeka na ukończenie lub niepowodzenie określonego zadania.

