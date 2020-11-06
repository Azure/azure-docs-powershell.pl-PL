---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
ms.openlocfilehash: 127e949bfaa9d54644f7f690cfefbf095d477374
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553886"
---
# Invoke-AzureRmHDInsightHiveJob

## STRESZCZENIe
Przesyła zapytanie o aplikację Hive do klastra usługi HDInsight i pobiera wyniki zapytania w ramach jednej operacji.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Invoke-AzureRmHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Invoke-AzureRmHDInsightHiveJob** przesyła zapytanie o aplikację Hive do klastra usługi Azure HDInsight i pobiera wyniki zapytania w jednej operacji.
Przed wywołaniem funkcji **Invoke-AzureRmHDInsightHiveJob** Użyj polecenia cmdlet Use-AzureRmHDInsightCluster, aby określić klaster, który będzie używany dla kwerendy.

## Przykłady

### Przykład 1: przesyłanie zapytania Hive do klastra usługi Azure HDInsight
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzureRmHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzureRmHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageAccountContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

To polecenie przesyła kwerendy do klastra o nazwie Your-Hadoop-001.

## PARAMETRÓW

### -Argumenty
Określa tablicę argumentów dla zadania.
Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.

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
Określa nazwę kontenera domyślnego w domyślnym koncie magazynu platformy Azure używanym przez klaster usługi HDInsight.

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

### -DefaultStorageAccountKey
Określa klucz konta dla domyślnego konta magazynu używanego przez klaster usługi HDInsight.

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
Określa nazwę domyślnego konta magazynu używanego przez klaster usługi HDInsight.

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

### -Definiuje
Określa wartości konfiguracji usługi Hadoop, które mają zostać ustawione podczas uruchamiania zadania.

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

### -File (plik)
Określa ścieżkę do pliku w usłudze Azure Storage, który zawiera zapytanie do uruchomienia.
Tego parametru można użyć zamiast parametru *zapytania* .

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

### -Files
Określa zbiór plików wymaganych dla zadania w ramach usługi Hive.

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

### -JobName
Określa nazwę zadania w ramach usługi Hive.
Jeśli ten parametr nie jest określony, w tym poleceniu cmdlet jest używana wartość domyślna: "gałąź: \<first 100 characters of Query\> ".

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

### -Query
Określa zapytanie dotyczące gałęzi.

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
Wskazuje, że to polecenie cmdlet tworzy plik na domyślnym koncie usługi Azure Storage, w którym ma być przechowywane zapytanie.
To polecenie cmdlet przesyła zadanie odwołujące się do tego pliku jako skrypt do uruchomienia.

Za pomocą tej funkcji można obsługiwać znaki specjalne, takie jak znak procentu (%). to nie powiodło się w przypadku przesyłania zadania za pośrednictwem Templeton, ponieważ Templeton interpretuje zapytanie z znakiem procentu jako parametr adresu URL.

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
Określa lokalizację folderu, który zawiera standardowe wyjścia i wyjścia z błędów dla zadania.

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

### System. String

## INFORMACYJN

## LINKI POKREWNE

[Użyj — AzureRmHDInsightCluster](./Use-AzureRmHDInsightCluster.md)


