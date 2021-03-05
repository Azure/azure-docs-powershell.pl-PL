---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2c58549ee79cd24d29c1e3549d729995313c5748
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967850"
---
# Get-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Pobiera informacje o autoryzacjach obwodów w układzie ExpressRoute.

## SKŁADNIA

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzExpressRouteCircuitAuthorization** pobiera informacje o autoryzacjach przypisanych do obwodu expressroute. Obwody usługi ExpressRoute łączą Twoją sieć lokalną z chmurą firmy Microsoft przy użyciu dostawcy łączności zamiast publicznego Internetu. Właściciel obwodu expressRoute może utworzyć aż 10 autoryzacji dla każdego obwodu. te autoryzacje generują klucz autoryzacji, za pomocą których właściciel sieci wirtualnej może połączyć swoją sieć z obwodem (jedna autoryzacja na sieć wirtualną). Klucze autoryzacji, a także inne informacje o autoryzacji, można wyświetlić w dowolnym momencie, uruchamiając program **Get-AzExpressRouteCircuitAuthorization.**

## PRZYKŁADY

### Przykład 1. Uzyskiwanie wszystkich autoryzacji w uroute
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

Te polecenia zwracają informacje o wszystkich autoryzacjach w układzie ExpressRoute skojarzonych z obwodem expressRoute. Pierwsze polecenie tworzy odwołanie do obiektu w obwodzie o nazwie ContosoCircuit za pomocą polecenia cmdlet **Get-AzExpressRouteCircuit.** to odwołanie do obiektu jest przechowywane w zmiennej $Circuit. Drugie polecenie używa następnie tego odwołania do obiektu i polecenia **cmdlet Get-AzExpressRouteCircuitAuthorization** w celu zwrócenia informacji o autoryzacjach skojarzonych z ContosoCircuit.

### Przykład 2. Uzyskiwanie wszystkich autoryzacji usługi ExpressRoute przy użyciu Where-Object cmdlet
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

Te polecenia reprezentują odmianę poleceń użytych w przykładzie 1. W tym przypadku jednak informacje są zwracane tylko dla tych autoryzacji, które są dostępne do użycia (czyli dla autoryzacji, które nie zostały przypisane do sieci wirtualnej). W tym celu informacje autoryzacji obwodu są zwracane w poleceniu 2 i są przekierowywane do polecenia cmdlet **Where-Object.**
**Następnie obiekt Where-Object** wybiera tylko te autoryzacje, dla których właściwość *AuthorizationUseStatus* ma wartość Dostępny. Aby wyświetlić listę tylko tych uprawnień, które nie są dostępne, należy użyć tej składni dla klauzuli Where: `{$_.AuthorizationUseStatus -ne "Available"}`

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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
Określa autoryzację obwodu w układzie ExpressRoute.

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

### — Nazwa
Określa nazwę autoryzacji obwodu expressRoute, która otrzymuje to polecenie cmdlet.
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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization

## NOTATKI

## LINKI POKREWNE

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)
