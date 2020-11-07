---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcomputeresourcesku
schema: 2.0.0
ms.openlocfilehash: e7ebc6a8e6b59679757f559ff2d09ebaa8c5475f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899388"
---
# Get-AzureRmComputeResourceSku

## STRESZCZENIe
Lista wszystkich jednostek SKU zasobu COMPUTE

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Lista wszystkich jednostek SKU zasobu COMPUTE

## Przykłady

### Przykład 1
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

Lista wszystkich jednostek obliczeniowych zasobów w regionie zachód Stanów Zjednoczonych

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
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

### Znaleziono

## WYSYŁA

### System. Object

## INFORMACYJN

## LINKI POKREWNE

