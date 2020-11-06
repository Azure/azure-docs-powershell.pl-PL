---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: fc89ff40c36fc444eec23089288849aa5ffe592c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553838"
---
# Update-AzureRmMlOpClusterSystemService

## STRESZCZENIe
Rozpoczyna aktualizację usług systemowych klastra operationalization.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Uruchom aktualizację usług systemowych z parametrów wejściowych polecenia cmdlet.
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### Uruchom aktualizację usług systemowych z definicji wystąpienia PSOperationalizationCluster.
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### Uruchom aktualizację usług systemowych na podstawie identyfikatora usługi Azure Resouce.
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-WhatIf] [-Confirm]
```

## Opis
Usługi systemowe można aktualizować niezależnie od klastra programu operationalization. Aby rozpocząć aktualizację usług systemowych, użyj tego polecenia cmdlet. Jeśli żadna aktualizacja nie jest dostępna, aktualizacja będzie nadal uruchamiana i zostanie pomyślnie przywrócona. Po zakończeniu aktualizacji raporty są zgłaszane po jej uruchomieniu, zakończeniu i po poprawnym utworzeniu.

## Przykłady

### Przykład 1
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

Rozpoczyna aktualizację usług systemowych w określonym klastrze. 

## PARAMETRÓW

### -Inputobject
Obiekt klastra operationalization.

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Start a system services update from an PSOperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa klastra usługi operationalization.

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów dla klastra usługi operationalization.

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu platformy Azure dla klastra usługi operationalization.

```yaml
Type: String
Parameter Sets: Start a system services update from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## WEJŚCIOWE

### Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster
### System. String


## WYSYŁA

### Microsoft. Azure. Commands. MachineLearningCompute. models. PSUpdateSystemServicesResponse


## INFORMACYJN

## LINKI POKREWNE

