---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: ab97162fb2651bce8e242ca0cef7b497ffcf1bef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489597"
---
# Remove-AzHDInsightCluster

## STRESZCZENIe
Umożliwia usunięcie określonego klastra usługi HDInsight z bieżącej subskrypcji.

## POLECENIA

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzHDInsightCluster** umożliwia usunięcie określonego klastra usługi HDInsight z subskrypcji.
Ta operacja usuwa również wszystkie dane przechowywane w systemie plików HDFS (Distributed File System) usługi Hadoop w klastrze.
Dane przechowywane na skojarzonym koncie usługi Azure Storage nie są usuwane.
Dane przechowywane w zewnętrznych magazynach strumieniowych nie są usuwane.

## Przykłady

### Przykład 1: usuwanie klastra usługi Azure HDInsight
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

To polecenie powoduje usunięcie klastra o nazwie Your-Hadoop-001.

## PARAMETRÓW

### -Nazwaklastraname
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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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
Jeśli PassThru jest obecny, wynik

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Znaleziono
## WYSYŁA

### System. Boolean
## INFORMACYJN

## LINKI POKREWNE

[Get-AzHDInsightCluster](./Get-AzHDInsightCluster.md)

[Użyj — AzHDInsightCluster](./Use-AzHDInsightCluster.md)


