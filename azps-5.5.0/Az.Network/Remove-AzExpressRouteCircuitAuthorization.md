---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191778"
---
# Remove-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Usuwa istniejącą autoryzację konfiguracji usługi ExpressRoute.

## SKŁADNIA

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Remove-AzExpressRouteCircuitAuthorization** usuwa autoryzację przypisaną do obwodu expressRoute. Obwody usługi ExpressRoute łączą Twoją sieć lokalną z platformą Azure przy użyciu dostawcy łączności zamiast publicznego Internetu. Właściciel obwodu expressRoute może utworzyć aż 10 autoryzacji dla każdego obwodu. te autoryzacje generują klucz autoryzacji, za pomocą których właściciel sieci wirtualnej może połączyć swoją sieć z obwodem. W przypadku jednej sieci wirtualnej może być tylko jedna autoryzacja. Jednak w dowolnym momencie właściciel obwodu może użyć funkcji **Remove-AzExpressRouteCircuitAuthorization** w celu usunięcia autoryzacji przypisanej do sieci wirtualnej. W takim przypadku odpowiednia sieć wirtualna nie może już łączyć się z platformą Azure za pomocą obwodu usługi ExpressRoute.

## PRZYKŁADY

### Przykład 1. Usuwanie autoryzacji obwodu z obwodu w układzie ExpressRoute
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

W tym przykładzie autoryzacja obwodu jest usuwana z obwodu w układzie ExpressRoute. Pierwsze polecenie używa polecenia cmdlet **Get-AzExpressRouteCircuit** w celu utworzenia odwołania do obiektu obwodu usługi ExpressRoute o nazwie ContosoCircuit i przechowuje wynik w zmiennej o nazwie $Circuit.
Drugie polecenie oznacza autoryzację obwodu ContosoCircuitAuthorization do usunięcia.
Trzecie polecenie używa Set-AzExpressRouteCircuit cmdlet w celu potwierdzenia usunięcia obwodu usługi ExpressRoute przechowywanego w $Circuit danych.

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
Określa obiekt ExpressRouteCircuit, który usuwa to polecenie cmdlet.

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
Określa nazwę autoryzacji obwodu, które usuwa to polecenie cmdlet.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## NOTATKI

## LINKI POKREWNE

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
