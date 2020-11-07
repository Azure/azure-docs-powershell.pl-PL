---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: af8490ab242919d44b0b1b47c9cab92674e9df9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719620"
---
# Remove-AzureRmExpressRouteCircuitAuthorization

## STRESZCZENIe
Usuwa istniejącą autoryzację konfiguracji ExpressRoute.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureRmExpressRouteCircuitAuthorization** usuwa autoryzację przypisaną do obwodu ExpressRoute. ExpressRoute obwodów łączy się z siecią lokalną na platformie Azure, korzystając z dostawcy usług łączności zamiast z publicznego Internetu. Właściciel obwodu ExpressRoute może utworzyć maksymalnie 10 zezwoleń dla każdego obwodu; te pozwolenia generują klucz autoryzacji, który może być wykorzystywany przez właściciela sieci wirtualnej w celu podłączenia sieci do obwodu. Może istnieć tylko jedna autoryzacja na sieć wirtualną. Jednak w dowolnym momencie właściciel obwodu może użyć narzędzia **Remove-AzureRmExpressRouteCircuitAuthorization** w celu usunięcia autoryzacji przypisanej do sieci wirtualnej. Gdy to nastąpi, odpowiednia sieć wirtualna nie może już używać obwodu ExpressRoute do łączenia się z platformą Azure.

## Przykłady

### Przykład 1: usuwanie autoryzacji obwodu z obwodu ExpressRoute
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

W tym przykładzie jest usuwana autoryzacja obwodu ze obwodu ExpressRoute. W pierwszym poleceniu użyto polecenia cmdlet **Get-AzureRmExpressRouteCircuit** w celu utworzenia odwołania do obiektu dla obwodu ExpressRoute o nazwie ContosoCircuit i zapisanie wyniku w zmiennej o nazwie $Circuit.

Drugie polecenie oznacza ContosoCircuitAuthorization autoryzacji obwodu do usunięcia.

W trzecim poleceniu użyto polecenia cmdlet Set-AzureRmExpressRouteCircuit w celu potwierdzenia usunięcia obwodu ExpressRoute przechowywanego w zmiennej $Circuit.

## PARAMETRÓW

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### PSExpressRouteCircuit
To polecenie cmdlet akceptuje potokowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit** .

## WYSYŁA

### PSExpressRouteCircuit
To polecenie cmdlet modyfikuje istniejące wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit** .

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[Nowe — AzureRmExpressRouteCircuitAuthorization](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Set-AzureRmExpressRouteCircuit](./Set-AzureRmExpressRouteCircuit.md)
