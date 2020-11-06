---
external help file: Microsoft.Azure.Commands.ResourceGraph.dll-Help.xml
Module Name: AzureRM.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resourcegraph/search-azurermgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ResourceGraph/Commands.ResourceGraph/help/Search-AzureRmGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ResourceGraph/Commands.ResourceGraph/help/Search-AzureRmGraph.md
ms.openlocfilehash: 900722c15d1c7a6560ba1f498b9dd0d3981f899a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549296"
---
# Search-AzureRmGraph

## STRESZCZENIe
Wysyła zapytanie dotyczące zasobów zarządzanych przez Menedżera zasobów Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Search-AzureRmGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Dowiedz się więcej na temat składni kwerendy: https://aka.ms/resource-graph/learntoquery

## Przykłady

### Przykład 1
```powershell
PS C:\> Search-AzureRmGraph "project id, name, type, location, tags" -First 3


id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.Compute/virtualMachineScaleSets/nt
name       : nt
type       : microsoft.compute/virtualmachinescalesets
location   : eastus
tags       : @{resourceType=Service Fabric; clusterName=gov-art-int-nt-a}

id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.EventGrid/topics/egtopic-1
name       : egtopic-1
type       : microsoft.eventgrid/topics
location   : westus2
tags       :
```

Zapytanie zasobów prostych żądających podzestawu pól zasobów.

### Przykład 2
```powershell
PS C:\> Search-AzureRmGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

Złożona kwerenda w zasobach, która zawiera zaznaczenie pól, filtrowanie i podsumowywanie.

## PARAMETRÓW

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

### -Query
Kwerenda wykresu zasobów.

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

### -Subscription
Abonamentów, dla których ma zostać uruchomiony program Query.

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

### -Skip
Ignoruje pierwsze N obiektów, a następnie pobiera pozostałe obiekty.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -First
Maksymalna liczba obiektów do zwrócenia. Dozwolone wartości: 1-5000.
Wartość domyślna to 100.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.
Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### System. Management. Automation. PSObject

## INFORMACYJN

## LINKI POKREWNE
