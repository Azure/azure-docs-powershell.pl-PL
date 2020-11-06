---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: a6a5b9ed5dbf1faa4a2be345039e53bb3daae291
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525913"
---
# Set-AzureRmTrafficManagerEndpoint

## STRESZCZENIe
Aktualizowanie punktu końcowego w usłudze Traffic Manager.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmTrafficManagerEndpoint** umożliwia zaktualizowanie punktu końcowego w usłudze Azure Traffic Manager.
To polecenie cmdlet spowoduje zaktualizowanie ustawień na podstawie obiektu lokalnego punktu końcowego.
Obiekt Endpoint można określić za pomocą parametru *TrafficManagerEndpoint* lub za pomocą potoku.

Obiekt lokalny reprezentujący punkt końcowy można uzyskać przy użyciu Get-AzureRmTrafficManagerEndpoint polecenia cmdlet.
Zmodyfikuj obiekt lokalnie, a następnie użyj **Ustawienia Set-AzureRmTrafficManagerEndpoint** w celu zatwierdzenia zmian.

## Przykłady

### Przykład 1: aktualizowanie punktu końcowego
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Pierwsze polecenie pobiera punkt końcowy usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzureRmTrafficManagerEndpoint** .
Polecenie zapisuje punkt końcowy lokalnie w zmiennej $TrafficManagerEndpoint.

Drugie polecenie powoduje zmianę lokalnego punktu końcowego.
To polecenie powoduje zmianę wagi punktu końcowego na 20.

W trzecim poleceniu jest aktualizowany punkt końcowy w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerEndpoint.

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

### -TrafficManagerEndpoint
Określa lokalny obiekt **TrafficManagerEndpoint** .
To polecenie cmdlet umożliwia zaktualizowanie Menedżera ruchu w celu dopasowania go do tego obiektu lokalnego.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
To polecenie cmdlet akceptuje obiekt **TrafficManagerEndpoint** .

## WYSYŁA

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
To polecenie cmdlet zwraca obiekt **TrafficManagerEndpoint** .

## INFORMACYJN

## LINKI POKREWNE
