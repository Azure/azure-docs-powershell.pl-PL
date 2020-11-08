---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6F89C297-4D3D-4DAD-A63A-FCC51A86BF43
online version: ''
schema: 2.0.0
ms.openlocfilehash: 542b2fb83b69fe5eb63ac6b8b979df6cc8051ed2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054694"
---
# Add-AzureHDInsightConfigValues

## STRESZCZENIe
Umożliwia dodanie dostosowania wartości konfiguracji usługi Hadoop lub dostosowania udostępnionej biblioteki gałęzi do konfiguracji klastra usługi HDInsight.

## POLECENIA

```
Add-AzureHDInsightConfigValues -Config <AzureHDInsightConfig> [-Core <Hashtable>] [-Yarn <Hashtable>]
 [-Hdfs <Hashtable>] [-Hive <AzureHDInsightHiveConfiguration>]
 [-MapReduce <AzureHDInsightMapReduceConfiguration>] [-Oozie <AzureHDInsightOozieConfiguration>]
 [-Storm <Hashtable>] [-Spark <Hashtable>] [-HBase <AzureHDInsightHBaseConfiguration>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.
Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.
Użyj nowszej wersji usługi HDInsight Azure PowerShell.

Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).
Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).
Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx).

Polecenie cmdlet **Add-AzureHDInsightConfigValues** umożliwia dodanie dostosowania wartości konfiguracji usługi Hadoop, takiego jak Core-site.xml lub Hive-site.xml, lub dostosowania biblioteki udostępnionej w usłudze Azure do konfiguracji klastra usługi Azure HDInsight.

Polecenie cmdlet umożliwia dodanie niestandardowych wartości konfiguracji do określonego obiektu konfiguracji.
Ustawienia niestandardowe są dodawane do plików konfiguracji odpowiednich usług Hadoop po wdrożeniu klastra.

## Przykłady

### Przykład 1: Konfigurowanie klastra
```
PS C:\>$HiveConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightHiveConfiguration'
PS C:\> $HiveConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $HiveConfigValues.AdditionalLibraries = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightDefaultStorageAccount'
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountName = "MyStorageAccount.blob.core.windows.net"
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountKey = (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageContainerName = "MySharedLibContainer"
PS C:\> $OozieConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightOozieConfiguration'
PS C:\> $OozieConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $MapredConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightMapReduceConfiguration'
PS C:\> $MapredConfigValues.Configuration = @{ mapred.map.max.attempts = 2 }
PS C:\> $MapredConfigValues.CapacitySchedulerConfiguration = @{ mapred.capacity-scheduler.init-poll-interval = 1000 }
PS C:\> $Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyStorageAccount.blob.core.windows.net -StorageAccountKey (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary -StorageContainerName "MyStorageContainer"
    | Add-AzureHDInsightConfigValues -Core @{ io.file.buffer.size = 300000 } -MapReduce $MapredConfigValues -Hive $HiveConfigValues -Oozie $OozieConfigValues
PS C:\> $Config | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds -Name "MyCluster" -Location "North Europe"
```

Pierwsze polecenie tworzy nowy obiekt **AzureHDInsightHiveConfiguration** , a następnie zapisuje go w zmiennej $HiveConfigValues.

Kolejne pięć poleceń umożliwia utworzenie wartości konfiguracji gałęzi i zapisanie tych wartości jako członków $HiveConfigValues.

Polecenie siódme powoduje utworzenie obiektu **AzureHDInsightOozieConfiguration** , a następnie zapisanie go w zmiennej $OozieConfigValues.
Ósmej polecenie tworzy wartość konfiguracji dla Oozie, a następnie przechowuje te wartości jako członka $OozieConfigValues.

Dziewiąte polecenie tworzy obiekt **AzureHDInsightMapReduceConfiguration** , a następnie zapisuje go w zmiennej $MapredConfigValues.
Następne dwa polecenia tworzą wartości konfiguracji dla MapReduce i przechowuj te wartości jako członkowie $MapredConfigValues.

W poleceniu dwunaste użyto polecenia cmdlet **New-AzureHDInsightClusterConfig** w celu utworzenia konfiguracji klastra usługi HDInsight, a następnie zapisu w zmiennej $config.
W poleceniu użyto operatora potoku w celu przekazania $Config do polecenia cmdlet **Set-AzureHDInsightDefaultStorage** w celu zaktualizowania domyślnego ustawienia przechowywania i polecenia cmdlet **Add-AzureHDInsightConfigValues** w celu dodania nowych wartości konfiguracji do konfiguracji klastra.

W poleceniu ostatnim jest używany operator potoku umożliwiający przekazanie $Config do polecenia cmdlet **New-AzureHDInsightCluster** w celu utworzenia nowego klastra usługi HDInsight z dostosowanymi ustawieniami.

## PARAMETRÓW

### -Config
Określa obiekt konfiguracji, do którego ma zostać dodana konfiguracja usługi Hadoop.

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

### -Core
Określa zestaw wartości konfiguracji usługi Hadoop dla Core-site.xml.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HBase
Określa zestaw HBaseych wartości konfiguracji dla Hbase-site.xml.

```yaml
Type: AzureHDInsightHBaseConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HDFS
Określa zestaw wartości konfiguracji usługi Hadoop dla Hdfs-site.xml.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Gałąź rejestru
Określa obiekt Customization dla usługi uli usługi Hadoop, w tym zestaw wartości konfiguracji usługi Hadoop dla Hive-site.xml i udostępnionych bibliotek gałęzi.

```yaml
Type: AzureHDInsightHiveConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MapReduce
Określa obiekt dostosowania dla MapReduce i harmonogramu pojemności.

```yaml
Type: AzureHDInsightMapReduceConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Oozie
Określa obiekt dostosowywania dla usługi Oozie usługi Hadoop, w tym zestaw wartości konfiguracji usługi Hadoop dla Oozie-site.xml.

```yaml
Type: AzureHDInsightOozieConfiguration
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

### -Spark
Określa obiekt dostosowania dla programu Apache Spark.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Burza
Określa obiekt Customization (Dostosowywanie) dla programu Apache.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Przędza
Określa obiekt dostosowania dla PRZĘDZy usługi Hadoop, określając zestaw dostosowanych wartości konfiguracji PRZĘDZy dla Yarn-site.xml.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
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

[Set-AzureHDInsightDefaultStorage](./Set-AzureHDInsightDefaultStorage.md)
