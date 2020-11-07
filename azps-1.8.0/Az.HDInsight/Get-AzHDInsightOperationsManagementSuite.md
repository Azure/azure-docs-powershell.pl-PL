---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: fa19e7817d9d9be5e0c941db6d814500bad33509
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868284"
---
# Get-AzHDInsightOperationsManagementSuite

## STRESZCZENIe
Pobiera stan instalacji usługi Operations Management Suite (OMS) w klastrze.

## POLECENIA

```
Get-AzHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzHDInsightOperationsManagementSuite** Pobiera stan instalacji OMS w klastrze usługi Azure HDInsight. Jeśli funkcja OMS jest włączona, zostanie również zwrócony identyfikator obszaru roboczego OMS.

## Przykłady

### Przykład 1
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

Pakiet Operations Management Suite (OMS) jest włączony w klastrze, ponieważ właściwość ClusterMonitoringEnabled ma wartość PRAWDA. Identyfikator obszaru roboczego OMS, w którym są nalewane dzienniki, to 1d364e89-bb71-4503-aa3d-a23535aea7bd

### Przykład 2
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

Pakiet Operations Management Suite (OMS) jest włączony w klastrze, ponieważ właściwość ClusterMonitoringEnabled ma wartość PRAWDA. Identyfikator obszaru roboczego OMS, w którym są nalewane dzienniki, to 1d364e89-bb71-4503-aa3d-a23535aea7bd

### Przykład 3
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

Pakiet Operations Management Suite (OMS) jest wyłączony w klastrze, ponieważ właściwość ClusterMonitoringEnabled ma wartość false.

### Przykład 4
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

Pakiet Operations Management Suite (OMS) jest wyłączony w klastrze, ponieważ właściwość ClusterMonitoringEnabled ma wartość false.

## PARAMETRÓW

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

### -Name (nazwa)
Nazwa klastra, aby uzyskać stan pakietu Operations Management Suite (OMS).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Grupa zasobów klastra.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. HDInsight. models. Management. AzureHDInsightOMS

## INFORMACYJN

## LINKI POKREWNE
