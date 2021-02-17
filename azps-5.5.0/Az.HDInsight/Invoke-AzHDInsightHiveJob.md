---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/invoke-azhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
ms.openlocfilehash: 737ccdbd742b3c4cc12518262423e846678cf599
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188347"
---
# Invoke-AzHDInsightHiveJob

## SYNOPSIS
Przesyła zapytanie Do klastra HDInsight i pobiera wyniki zapytania w jednej operacji.

## SKŁADNIA

```
Invoke-AzHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Invoke-AzHDInsightHiveJob** przesyła zapytanie w usłudze Azure HDInsight i pobiera wyniki zapytania w ramach jednej operacji.
Użyj Use-AzHDInsightCluster cmdlet przed wywołaniem **invoke-AzHDInsightHiveJob,** aby określić klaster, który będzie używany dla zapytania.

## PRZYKŁADY

### Przykład 1. Przesyłanie zapytania w usłudze Azure HDInsight
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

To polecenie przesyła zapytanie SHOW TABLES do klastra o nazwie Twoja-hadoop-001.

## PARAMETERS

### — Argumenty
Określa tablicę argumentów dla zadania.
Argumenty są przekazywane jako argumenty wiersza polecenia do każdego zadania.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultContainer
Określa nazwę domyślnego kontenera na domyślnym koncie magazynu platformy Azure używanym przez klaster HDInsight.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageAccountKey
Określa klucz konta dla domyślnego konta magazynu używanego przez klaster HDInsight.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageAccountName
Określa nazwę domyślnego konta magazynu używanego przez klaster HDInsight.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — definiuje
Określa wartości konfiguracji usługi Hadoop, które mają być ustawiane podczas pracy zadania.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Plik
Określa ścieżkę do pliku w magazynie platformy Azure zawierającego zapytanie do uruchomienia.
Możesz użyć tego parametru zamiast *parametru Query.*

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Pliki
Określa zbiór plików wymaganych dla zadania Gałąź.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — JobName
Określa nazwę zadania Gałąź.
Jeśli nie określisz tego parametru, to polecenie cmdlet użyje wartości domyślnej: "Gałąź: \<first 100 characters of Query\> ".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — zapytanie
Określa zapytanie Ułana.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunAsFileJob
Wskazuje, że to polecenie cmdlet tworzy plik na domyślnym koncie magazynu platformy Azure, na którym ma być przechowywane zapytanie.
To polecenie cmdlet przesyła zadanie, które odwołuje się do tego pliku jako skrypt do uruchomienia.
Ta funkcja umożliwia obsługę znaków specjalnych, takich jak znak procentu (%) oznaczałoby niepowodzenie przesłania zadania za pośrednictwem Templetona, ponieważ Templeton interpretuje zapytanie z znakiem procentu jako parametr adresu URL.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StatusFolder
Określa lokalizację folderu zawierającego standardowe dane wyjściowe i dane wyjściowe błędów dla zadania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Brak

## DANE WYJŚCIOWE

### System.String

## NOTATKI

## LINKI POKREWNE

[Use-AzHDInsightCluster](./Use-AzHDInsightCluster.md)


