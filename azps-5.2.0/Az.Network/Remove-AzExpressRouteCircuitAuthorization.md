---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360754"
---
# Remove-AzExpressRouteCircuitAuthorization

## STRESZCZENIe
Usuwa istniejącą autoryzację konfiguracji ExpressRoute.

## POLECENIA

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzExpressRouteCircuitAuthorization** usuwa autoryzację przypisaną do obwodu ExpressRoute. ExpressRoute obwodów łączy się z siecią lokalną na platformie Azure, korzystając z dostawcy usług łączności zamiast z publicznego Internetu. Właściciel obwodu ExpressRoute może utworzyć maksymalnie 10 zezwoleń dla każdego obwodu; te pozwolenia generują klucz autoryzacji, który może być wykorzystywany przez właściciela sieci wirtualnej w celu podłączenia sieci do obwodu. Może istnieć tylko jedna autoryzacja na sieć wirtualną. Jednak w dowolnym momencie właściciel obwodu może użyć narzędzia **Remove-AzExpressRouteCircuitAuthorization** w celu usunięcia autoryzacji przypisanej do sieci wirtualnej. Gdy to nastąpi, odpowiednia sieć wirtualna nie może już używać obwodu ExpressRoute do łączenia się z platformą Azure.

## Przykłady

### Przykład 1: usuwanie autoryzacji obwodu z obwodu ExpressRoute
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

W tym przykładzie jest usuwana autoryzacja obwodu ze obwodu ExpressRoute. W pierwszym poleceniu użyto polecenia cmdlet **Get-AzExpressRouteCircuit** w celu utworzenia odwołania do obiektu dla obwodu ExpressRoute o nazwie ContosoCircuit i zapisanie wyniku w zmiennej o nazwie $Circuit.
Drugie polecenie oznacza ContosoCircuitAuthorization autoryzacji obwodu do usunięcia.
W trzecim poleceniu użyto polecenia cmdlet Set-AzExpressRouteCircuit w celu potwierdzenia usunięcia obwodu ExpressRoute przechowywanego w zmiennej $Circuit.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -ExpressRouteCircuit
Określa obiekt ExpressRouteCircuit, który jest usuwany przez to polecenie cmdlet.

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
Określa nazwę autoryzacji obwodu usuniętego przez to polecenie cmdlet.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[Nowe — AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
