---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 68599a48c4b0e608f629a628968c1918e62ec226
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/21/2020
ms.locfileid: "93554405"
---
# New-AzureRmExpressRouteCircuitAuthorization

## STRESZCZENIe
Umożliwia utworzenie autoryzacji obwodu ExpressRoute.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmExpressRouteCircuitAuthorization** umożliwia utworzenie autoryzacji obwodu, którą można dodać do obwodu ExpressRoute. Obwody ExpressRoute łączą sieć lokalną z chmurą firmy Microsoft, korzystając z dostawcy usług łączności zamiast z publicznego Internetu. Właściciel obwodu ExpressRoute może utworzyć maksymalnie 10 zezwoleń dla każdego obwodu; te pozwolenia generują klucz autoryzacji, który może być wykorzystywany przez właściciela sieci wirtualnej w celu połączenia sieci z obwodem. Istnieje tylko jedna autoryzacja na sieć wirtualną.

Po utworzeniu obwodu ExpressRoute możesz dodać autoryzację do tego obwodu za pomocą **dodatku Add-AzureRmExpressRouteCircuitAuthorization** .
Możesz też użyć **nowych — AzureRmExpressRouteCircuitAuthorization** , aby utworzyć autoryzację, którą można dodać do nowego obwodu w trakcie tworzenia obwodu.

## Przykłady

### Przykład 1. Tworzenie nowego zezwolenia na obwód
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

To polecenie tworzy nowy element autoryzacji obwodu o nazwie ContosoCircuitAuthorization, a następnie zapisuje ten obiekt w zmiennej o nazwie $Authorization. Zapisanie obiektu jako zmiennej jest ważne: Chociaż **nowe-AzureRmExpressRouteCircuitAuthorization** mogą utworzyć autoryzację obwodu, nie może ona dodać tej autoryzacji do trasy obwodu. Zamiast tego zmienna $Authorization jest używana New-AzureRmExpressRouteCircuit podczas tworzenia nowego obwodu ExpressRoute marki.

Aby uzyskać więcej informacji, zobacz dokumentację New-AzureRmExpressRouteCircuit polecenia cmdlet.

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

### -Name (nazwa)
Określa unikatową nazwę dla nowej autoryzacji obwodu ExpressRoute.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje danych wejściowych potoku.

## WYSYŁA

### PSExpressRouteCircuitAuthorization
To polecenie cmdlet tworzy wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitAuthorization** .

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

