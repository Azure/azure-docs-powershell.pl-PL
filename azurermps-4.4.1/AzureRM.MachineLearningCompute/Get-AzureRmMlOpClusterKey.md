---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550931"
---
# Get-AzureRmMlOpClusterKey

## STRESZCZENIe
Pobiera klucze dostępu skojarzone z klastrem usługi operationalization.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Pobierz klucze klastra operationalization z parametrów wejściowych polecenia cmdlet.
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### Pobierz klucze klastra operationalization z definicji wystąpienia OperationalizationCluster.
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### Pobierz klucze klastra operationalization z identyfikatora zasobu platformy Azure.
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## Opis
Klucze dla konta magazynu, rejestru kontenera i innych usług skojarzonych z klastrem operationalization nie są zwracane podczas uzyskiwania właściwości klastra. Należy wprowadzić określone połączenie, aby pobrać klucze, ponieważ są to informacje poufne.

## Przykłady

### Przykład 1
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

Zwraca klucze tajne dla usług skojarzonych z klastrem operationalization.

## PARAMETRÓW

### -Inputobject
Obiekt klastra operationalization.

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa klastra usługi operationalization.

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
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
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
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
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## WEJŚCIOWE

### Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster
System. String


## WYSYŁA

### Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationClusterCredentials


## INFORMACYJN

## LINKI POKREWNE

