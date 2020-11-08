---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0809415ea5dfff687c69089e1aeda60c9f3b00ee
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054686"
---
# Add-AzureHDInsightScriptAction

## STRESZCZENIe
Dodaje akcję skryptu usługi HDInsight.

## POLECENIA

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.
Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.
Użyj nowszej wersji usługi HDInsight Azure PowerShell.

Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

Polecenie cmdlet **Add-AzureHDInsightScriptAction** oferuje funkcję HDInsight Azure, która służy do instalowania dodatkowego oprogramowania lub zmieniania konfiguracji aplikacji uruchomionych w klastrze usługi Hadoop za pomocą skryptów programu Windows PowerShell.

Akcja skryptu uruchamia się w węzłach klastra, gdy są wdrożone klastry usługi HDInsight i są uruchamiane po zakończeniu konfigurowania usługi HDInsight w klastrze.
Akcja skryptu jest uruchamiana w obszarze uprawnienia konta administratora systemu i zapewnia pełne prawa dostępu do węzłów klastra.
Możesz udostępnić każdemu klastrowi listę akcji skryptów do uruchomienia w określonej kolejności.

## Przykłady

### Przykład 1: Dodawanie akcji skryptu do klastra
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

W pierwszym poleceniu użyto polecenia cmdlet **New-AzureHDInsightClusterConfig** w celu utworzenia konfiguracji klastra usługi HDInsight, a następnie zapisu w zmiennej $config.

W drugim poleceniu użyto polecenia cmdlet **Add-AzureHDInsightScriptAction** w celu dodania akcji skryptu o nazwie TestScriptAction do $config.

W poleceniu ostatnim użyto polecenia cmdlet **New-AzureHDInsightCluster** w celu utworzenia nowego klastra usługi HDInsight, który uruchamia akcję skryptu przechowywaną w $config.

### Przykład 2: Dodawanie akcji wielu skryptów do klastra
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

W pierwszym poleceniu użyto polecenia cmdlet **New-AzureHDInsightClusterConfig** w celu utworzenia konfiguracji klastra usługi HDInsight, a następnie zapisu w zmiennej $config.

W drugim poleceniu użyto polecenia cmdlet **Add-AzureHDInsightScriptAction** , aby dodać określoną akcję skryptu do $config, a następnie użyć operatora potoku w celu przejścia $config do polecenia **Dodaj-AzureHDInsightScriptAction** po raz drugi w celu dodania drugiego skryptu do $config.

W poleceniu ostatnim użyto polecenia cmdlet **New-AzureHDInsightCluster** w celu utworzenia klastra uruchamiającego akcje skryptu w $config.

## PARAMETRÓW

### -ClusterRoleCollection
Określa węzły, dla których ma zostać uruchomiony skrypt.
Dopuszczalne wartości tego parametru to: HeadNode lub datanode.

Możesz określić pojedynczą wartość lub obie wartości.

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
Określa obiekt konfiguracji.
To polecenie cmdlet umożliwia dodanie informacji o akcji skryptu do obiektu, który ten parametr określa.

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę akcji skryptu.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Parametry
Określa parametry, które są wymagane przez akcję skryptu.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -URI
Określa lokalizację URI skryptu, który ma być uruchomiony.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[Nowe — AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)


