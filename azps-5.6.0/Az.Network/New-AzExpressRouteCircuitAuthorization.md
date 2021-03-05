---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9c247784a9f890d97aee301383656f97ef9c7dd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995359"
---
# New-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Tworzy autoryzację obwodu w układzie ExpressRoute.

## SKŁADNIA

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzExpressRouteCircuitAuthorization** tworzy autoryzację obwodu, która może zostać dodana do obwodu expressRoute. Obwody usługi ExpressRoute łączą Twoją sieć lokalną z chmurą firmy Microsoft przy użyciu dostawcy łączności zamiast publicznego Internetu. Właściciel obwodu expressRoute może utworzyć aż 10 autoryzacji dla każdego obwodu. te autoryzacje generują klucz autoryzacji, za pomocą których właściciel sieci wirtualnej może połączyć sieć z obwodem. W przypadku jednej sieci wirtualnej może być dostępna tylko jedna autoryzacja.
Po utworzeniu obwodu expressRoute możesz użyć funkcji **Add-AzExpressRouteCircuitAuthorization** w celu dodania autoryzacji do tego obwodu.
Możesz również użyć funkcji **New-AzExpressRouteCircuitAuthorization,** aby utworzyć autoryzację, która może zostać dodana do nowego obwodu jednocześnie z utworzeniem obwodu.

## PRZYKŁADY

### Przykład 1. Tworzenie nowej autoryzacji obwodu
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

To polecenie tworzy nową autoryzację obwodu o nazwie ContosoCircuitAuthorization, a następnie przechowuje ten obiekt w zmiennej o nazwie $Authorization. Zapisywanie obiektu w zmiennej jest ważne: chociaż **new-AzExpressRouteCircuitAuthorization** może utworzyć autoryzację obwodu, nie może dodać tej autoryzacji do trasy obwodu. Zamiast tego zmienna $Authorization używana New-AzExpressRouteCircuit podczas tworzenia zupełnie nowego obwodu expressRoute.
Aby uzyskać więcej informacji, zapoznaj się z dokumentacją tego New-AzExpressRouteCircuit cmdlet.

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

### — Nazwa
Określa unikatową nazwę dla nowej autoryzacji obwodu w układzie ExpressRoute.

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

### Brak

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization

## NOTATKI

## LINKI POKREWNE

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

