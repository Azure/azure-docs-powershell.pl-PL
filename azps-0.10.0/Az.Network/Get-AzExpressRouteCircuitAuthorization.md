---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 3b51a16d6ff2de8292b1bbb66f7f5ab24cc17b93
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890805"
---
# Get-AzExpressRouteCircuitAuthorization

## STRESZCZENIe
Pobiera informacje na temat autoryzacji obwodu ExpressRoute.

## POLECENIA

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzExpressRouteCircuitAuthorization** pobiera informacje o autoryzacjach przypisanych do obwodu ExpressRoute. Obwody ExpressRoute łączą sieć lokalną z chmurą firmy Microsoft, korzystając z dostawcy usług łączności zamiast z publicznego Internetu. Właściciel obwodu ExpressRoute może utworzyć maksymalnie 10 zezwoleń dla każdego obwodu; te autoryzacje generują klucz autoryzacji, który może być wykorzystywany przez właściciela sieci wirtualnej w celu podłączenia sieci do obwodu (jednej autoryzacji na sieć wirtualną). Klucze autoryzacji, a także inne informacje o autoryzacji można wyświetlać w dowolnym momencie, uruchamiając polecenie **Get-AzExpressRouteCircuitAuthorization**.

## Przykłady

### Przykład 1: pobieranie wszystkich autoryzacji ExpressRoute
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

Te polecenia zwracają informacje dotyczące wszystkich autoryzacji ExpressRoute skojarzonych z obwodem ExpressRoute. W pierwszym poleceniu użyto polecenia cmdlet **Get-AzExpressRouteCircuit** w celu utworzenia odwołania do obiektu o obwodzie o nazwie ContosoCircuit; odwołanie do tego obiektu jest przechowywane w zmiennej $Circuit. Drugie polecenie korzysta z tego odwołania do obiektu i polecenia cmdlet **Get-AzExpressRouteCircuitAuthorization** w celu zwrócenia informacji o autoryzacjach skojarzonych z ContosoCircuit.

### Przykład 2: uzyskiwanie wszystkich autoryzacji ExpressRoute za pomocą polecenia cmdlet Where-Object
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

Te polecenia reprezentują odmianę poleceń używanych w przykładzie 1. Jednak w tym przypadku informacje są zwracane tylko w przypadku tych autoryzacji, które są dostępne do użytku (czyli dla autoryzacji, które nie zostały przypisane do sieci wirtualnej). W tym celu informacje o autoryzacji obwodu są zwracane w poleceniu 2 i są przełączane do polecenia cmdlet **WHERE-Object** .
**Gdzie-Object** wybiera tylko te pozwolenia, w których właściwość *AuthorizationUseStatus* jest ustawiona jako dostępna. Aby wyświetlić listę tylko tych autoryzacji, które są niedostępne, użyj następującej składni dla klauzuli WHERE:

`{$_.AuthorizationUseStatus -ne "Available"}`

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

### -ExpressRouteCircuit
Określa autoryzację obwodu ExpressRoute.

```yaml
Type: PSExpressRouteCircuit
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
Type: String
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

### PSExpressRouteCircuit
Polecenie **Get-AzExpressRouteCircuitAuthorization** akceptuje potokowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit** .

## WYSYŁA

### PSExpressRouteCircuitAuthorization
Polecenie **Get-AzExpressRouteCircuitAuthorization** zwraca wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitAuthorization** .

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Nowe — AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)
