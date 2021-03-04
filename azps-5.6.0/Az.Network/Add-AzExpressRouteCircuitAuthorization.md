---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9812316b20db927dea9bfe999cad54fe002bfc93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952305"
---
# Add-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Dodaje autoryzację obwodu w układzie ExpressRoute.

## SKŁADNIA

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Add-AzExpressRouteCircuitAuthorization** dodaje autoryzację do obwodu expressRoute. Obwody usługi ExpressRoute łączą Twoją sieć lokalną z chmurą firmy Microsoft przy użyciu dostawcy łączności zamiast publicznego Internetu. Właściciel obwodu expressRoute może utworzyć aż 10 autoryzacji dla każdego obwodu. te autoryzacje generują klucz autoryzacji, za pomocą których właściciel sieci wirtualnej może połączyć swoją sieć z obwodem (jedna autoryzacja na sieć wirtualną). **Dodatek AzExpressRouteCircuitAuthorization** dodaje nową autoryzację do obwodu, a jednocześnie generuje odpowiedni klucz autoryzacji. Te klucze można wyświetlić w dowolnym momencie, uruchamiając polecenie cmdlet Get-AzExpressRouteCircuitAuthorization, a następnie, w razie potrzeby, można je skopiować i przesyłać dalej do odpowiedniego właściciela sieci.
Zwróć uwagę, że po uruchomieniu dodatku **AzExpressRouteCircuitAuthorization** musisz wywołać Set-AzExpressRouteCircuit cmdlet, aby aktywować klucz. Jeśli nie wywołasz **set-azExpressRouteCircuit,** autoryzacja zostanie dodana do obwodu, ale nie będzie włączona do użycia.

## PRZYKŁADY

### Przykład 1. Dodawanie autoryzacji do określonego obwodu usług ExpressRoute
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Polecenia w tym przykładzie dodają nową autoryzację do istniejącego obwodu expressRoute. Pierwsze polecenie tworzy odwołanie do obiektu o nazwie ContosoCircuit za pomocą polecenia **Get-AzExpressRouteCircuit.** To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $Circuit.
W drugim poleceniu polecenie cmdlet **Add-AzExpressRouteCircuitAuthorization** służy do dodawania nowej autoryzacji (ContosoCircuitAuthorization) do obwodu expressRoute. To polecenie dodaje autoryzację, ale nie aktywuje tej autoryzacji. Aktywacja autoryzacji wymaga **ustawienia Set-AzExpressRouteCircuit** pokazanego w ostatnim poleceniu w przykładzie.

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
Określa obwód expressRoute, do który to polecenie cmdlet dodaje autoryzację.

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
Określa nazwę autoryzacji obwodu do dodania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## NOTATKI

## LINKI POKREWNE

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
