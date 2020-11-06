---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 5b277ca35071c3639a3c7b341451cea78c024901
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553523"
---
# Get-AzureRmExpressRouteCircuitAuthorization

## STRESZCZENIe
Pobiera informacje na temat autoryzacji obwodu ExpressRoute.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmExpressRouteCircuitAuthorization** pobiera informacje o autoryzacjach przypisanych do obwodu ExpressRoute. Obwody ExpressRoute łączą sieć lokalną z chmurą firmy Microsoft, korzystając z dostawcy usług łączności zamiast z publicznego Internetu. Właściciel obwodu ExpressRoute może utworzyć maksymalnie 10 zezwoleń dla każdego obwodu; te autoryzacje generują klucz autoryzacji, który może być wykorzystywany przez właściciela sieci wirtualnej w celu podłączenia sieci do obwodu (jednej autoryzacji na sieć wirtualną). Klucze autoryzacji, a także inne informacje o autoryzacji można wyświetlać w dowolnym momencie, uruchamiając polecenie **Get-AzureRmExpressRouteCircuitAuthorization**.

## Przykłady

### Przykład 1: pobieranie wszystkich autoryzacji ExpressRoute
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit
```

Te polecenia zwracają informacje dotyczące wszystkich autoryzacji ExpressRoute skojarzonych z obwodem ExpressRoute. W pierwszym poleceniu użyto polecenia cmdlet **Get-AzureRmExpressRouteCircuit** w celu utworzenia odwołania do obiektu o obwodzie o nazwie ContosoCircuit; odwołanie do tego obiektu jest przechowywane w zmiennej $Circuit. Drugie polecenie korzysta z tego odwołania do obiektu i polecenia cmdlet **Get-AzureRmExpressRouteCircuitAuthorization** w celu zwrócenia informacji o autoryzacjach skojarzonych z ContosoCircuit.

### Przykład 2: uzyskiwanie wszystkich autoryzacji ExpressRoute za pomocą polecenia cmdlet Where-Object
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

Te polecenia reprezentują odmianę poleceń używanych w przykładzie 1. Jednak w tym przypadku informacje są zwracane tylko w przypadku tych autoryzacji, które są dostępne do użytku (czyli dla autoryzacji, które nie zostały przypisane do sieci wirtualnej). W tym celu informacje o autoryzacji obwodu są zwracane w poleceniu 2 i są przełączane do polecenia cmdlet **WHERE-Object** .
**Gdzie-Object** wybiera tylko te pozwolenia, w których właściwość *AuthorizationUseStatus* jest ustawiona jako dostępna. Aby wyświetlić listę tylko tych autoryzacji, które są niedostępne, użyj następującej składni dla klauzuli WHERE: `{$_.AuthorizationUseStatus -ne "Available"}`

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

### -ExpressRouteCircuit
Określa autoryzację obwodu ExpressRoute.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę autoryzacji obwodu ExpressRoute, która jest pobierana przez to polecenie cmdlet.
-Name "ContosoCircuitAuthorization"

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit
Parametry: ExpressRouteCircuit (ByValue)

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitAuthorization

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[Nowe — AzureRmExpressRouteCircuitAuthorization](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)
