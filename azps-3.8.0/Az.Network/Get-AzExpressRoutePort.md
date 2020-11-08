---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: 670880a9fa82e4845f37cdb5f0d108533a2b72c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052327"
---
# Get-AzExpressRoutePort

## STRESZCZENIe
Pobiera zasób usługi Azure ExpressRoutePort.

## POLECENIA

### ResourceNameParameterSet (domyślny)
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzExpressRoutePort** służy do pobierania obiektu ExpressRoutePort z subskrypcji. Zwrócony obiekt expressrouteport może być wykorzystywany jako dane wejściowe dla innych poleceń cmdlet, które działają na ExpressRoutePort.

## Przykłady

### Przykład 1
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

Pobiera obiekt ExpressRoutePort o nazwie $PortName w grupie zasobów $rg w subskrypcji.

### Przykład 2
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

Pobiera wszystkie obiekty ExpressRoutePort, których nazwa zaczyna się od tekstu "test".

### Przykład 3
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

Pobiera obiekt ExpressRoutePort o identyfikatorze ResourceId $id. 

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

### -Name (nazwa)
Nazwa ExpressRoutePort.

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceGroupName
Nazwa grupy zasobów ExpressRoutePort.

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceId
Identyfikator zasobu Express Route port.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSExpressRoutePort

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzExpressRoutePort](./New-AzExpressRoutePort.md)

[Remove-AzExpressRoutePort](./Remove-AzExpressRoutePort.md)

[Set-AzExpressRoutePort](./Set-AzExpressRoutePort.md)
