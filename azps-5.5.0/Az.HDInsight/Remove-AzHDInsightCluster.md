---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: ab97162fb2651bce8e242ca0cef7b497ffcf1bef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200210"
---
# Remove-AzHDInsightCluster

## SYNOPSIS
Usuwa określony klaster USŁUGI HDInsight z bieżącej subskrypcji.

## SKŁADNIA

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Remove-AzHDInsightCluster** usuwa określony klaster usługi HDInsight z subskrypcji.
Ta operacja powoduje również usunięcie wszystkich danych przechowywanych w systemie plików HDFS (Hadoop Distributed File System) w klastrze.
Dane przechowywane na skojarzonym koncie magazynu platformy Azure nie są usuwane.
Dane przechowywane w zewnętrznych metastorech nie są usuwane.

## PRZYKŁADY

### Przykład 1. Usuwanie klastrów usługi Azure HDInsight
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

To polecenie usuwa klaster o nazwie Twoja-hadoop-001.

## PARAMETERS

### -ClusterName
Określa nazwę klastra.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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

### -PassThru
Jeśli passthru jest obecne, wyeksymuj wynik

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

### -ResourceGroupName
Określa nazwę grupy zasobów.

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
## OUTPUTS

### System.Boolean
## NOTATKI

## LINKI POKREWNE

[Get-AzHDInsightCluster](./Get-AzHDInsightCluster.md)

[Use-AzHDInsightCluster](./Use-AzHDInsightCluster.md)


