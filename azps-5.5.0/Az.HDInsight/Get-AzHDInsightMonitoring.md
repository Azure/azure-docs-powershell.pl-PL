---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: 2d91c96d20797988a7def2d11d633f36b08cb8cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237760"
---
# Get-AzHDInsightMonitoring

## SYNOPSIS
Pobiera stan instalacji monitorowania w klastrze.

## SKŁADNIA

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzHDInsightMonitoring** otrzymuje stan instalacji monitorowania w klastrze usługi Azure HDInsight. Jeśli monitorowanie jest włączone, zwracany jest również identyfikator obszaru roboczego analizy dziennika.

## PRZYKŁADY

### Przykład 1
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

Monitorowanie jest włączone w klastrze, ponieważ właściwość ClusterMonitoringEnabled jest prawdziwa. Identyfikator obszaru roboczego monitorowania, w którym przepływają dzienniki, to 1d364e89-bb71-4503-aa3d-a23535aea7bd

### Przykład 2
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

Monitorowanie jest włączone w klastrze, ponieważ właściwość ClusterMonitoringEnabled jest prawdziwa. Identyfikator obszaru roboczego monitorowania, w którym przepływają dzienniki, to 1d364e89-bb71-4503-aa3d-a23535aea7bd

### Przykład 3
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

Monitorowanie jest wyłączone w klastrze, ponieważ właściwość ClusterMonitoringEnabled ma wartość fałszywą.

### Przykład 4
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

Monitorowanie jest wyłączone w klastrze, ponieważ właściwość ClusterMonitoringEnabled ma wartość fałszywą.

## PARAMETERS

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

### — Nazwa
Nazwa klastra, który ma być w stanie monitorowania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Grupa zasobów klastrów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring

## NOTATKI

## LINKI POKREWNE
