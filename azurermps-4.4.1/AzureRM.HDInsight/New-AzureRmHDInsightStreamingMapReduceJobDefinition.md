---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 526f2005f1c6594128af7e259e2ccb0aa296a71b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553319"
---
# New-AzureRmHDInsightStreamingMapReduceJobDefinition

## STRESZCZENIe
Tworzy obiekt zadania przesyłania strumieniowego MapReduce.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>]
 [-Files <String[]>] [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>]
 -InputPath <String> [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmHDInsightStreamingMapReduceJobDefinition** definiuje strumień strumieniowy obiektu zadania MapReduce, który ma być używany w klastrze usługi Azure HDInsight.

## Przykłady

### Przykład 1: Tworzenie definicji zadania MapReduce strumieniowego
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

To polecenie tworzy definicję zadania MapReduce strumieniowego.

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

### -CommandEnvironment
Określa tablicę zmiennych środowiskowych wiersza polecenia do ustawiania czasu uruchamiania zadania w węzłach procesu roboczego.

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

### -Definiuje
Określa wartości konfiguracji usługi Hadoop, które mają być ustawiane podczas uruchamiania zadania.

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
Określa ścieżkę do pliku zawierającego zapytanie, które ma zostać uruchomione.
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
Określa zbiór plików skojarzonych z zadaniem w ramach usługi Hive.

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

### -InputPath
Określa ścieżkę do plików wejściowych.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Maper
Określa nazwę pliku mapera.

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

### -OutputPath
Określa ścieżkę dla wyników zadania.

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

### -Zmniejszenie
Określa nazwę pliku z ograniczeniami.

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

### Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightStreamingMapReduceJobDefinition

## INFORMACYJN

## LINKI POKREWNE

[Start — AzureRmHDInsightJob](./Start-AzureRmHDInsightJob.md)


