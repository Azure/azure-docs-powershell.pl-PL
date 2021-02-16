---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 4cf45d237d5611d5d9fb0fb1eb178d2c85807354
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200258"
---
# New-AzHDInsightHiveJobDefinition

## SYNOPSIS
Tworzy obiekt zadania Gałąź.

## SKŁADNIA

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzHDInsightHiveJobDefinition** definiuje obiekt zadania Gałąź do użytku z klastrem usługi Azure HDInsight.

## PRZYKŁADY

### Przykład 1. Tworzenie definicji stanowiska
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

To polecenie tworzy definicję stanowiska Gałąź.

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
Określa ścieżkę do pliku zawierającego zapytanie do uruchomienia.
Plik musi być dostępny na koncie magazynu skojarzonym z klastrem.
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
Określa zbiór plików skojarzonych z zadaniem Gałąź.

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
Określa nazwę zadania.

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

### Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition

## NOTATKI

## LINKI POKREWNE

[Start-AzHDInsightJob](./Start-AzHDInsightJob.md)


