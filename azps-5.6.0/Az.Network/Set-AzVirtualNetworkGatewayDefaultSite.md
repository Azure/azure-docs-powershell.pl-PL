---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 8e35347813849badfa50100cc4cac418e2d66332
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979441"
---
# Set-AzVirtualNetworkGatewayDefaultSite

## SYNOPSIS
Ustawia domyślną witrynę dla bramy sieci wirtualnej.

## SKŁADNIA

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzVirtualNetworkGatewayDefaultSite** przypisuje do bramy sieci wirtualnej wymuszone wydyskokianie domyślnej witryny.
Wymuszone podkoszowe zapewnia możliwość przekierowywania ruchu związanego z Internetem z maszyn wirtualnych platformy Azure do Twojej sieci lokalnej. umożliwia to inspekcję i inspekcję ruchu przed jego zwolnieniem.
Wymuszone podkołowy są wykonywane przy użyciu podkołowego wirtualnej sieci prywatnej (VPN); ten kork wymaga witryny domyślnej, bramy lokalnej, do której jest przekierowywany cały ruch internetowy platformy Azure.
**Set-AzVirtualNetworkGatewayDefaultSite** umożliwia zmianę domyślnej witryny przypisanej do bramy.

## PRZYKŁADY

### Przykład 1. Przypisywanie witryny domyślnej do bramy sieci wirtualnej
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

W tym przykładzie do bramy sieci wirtualnej jest przypisywana witryna domyślna o nazwie ContosoVirtualGateway.
Pierwsze polecenie tworzy odwołanie do obiektu do bramy lokalnej o nazwie ContosoLocalGateway.
To odwołanie do obiektu przechowywane w zmiennej o nazwie $LocalGateway reprezentuje bramę, która ma zostać skonfigurowana jako witryna domyślna.
Drugie polecenie tworzy wówczas odwołanie do obiektu do bramy sieci wirtualnej i zapisuje wynik w zmiennej o nazwie $VirtualGateway.
Trzecie polecenie używa polecenia cmdlet **Set-AzVirtualNetworkGatewayDefaultSite** w celu przypisania witryny domyślnej do obiektu ContosoVirtualGateway.

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

### -GatewayDefaultSite
Określa odwołanie do obiektu do lokalnej bramy sieciowej, które ma zostać przypisane jako witryna domyślna dla określonej sieci wirtualnej.
Polecenie cmdlet Get-AzLocalNetworkGateway umożliwia utworzenie odwołania do obiektu do bramy lokalnej.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — VirtualNetworkGateway
Określa odwołanie do obiektu do bramy sieci wirtualnej, do której zostanie przypisana witryna domyślna.
Możesz utworzyć odwołanie do obiektu do bramy sieci wirtualnej, używając narzędzia **Get-AzVirtualNetworkGateway** i określając nazwę bramy.
Wartość zmiennej $VirtualGateway następnie może być używana jako wartość parametru dla parametru *VirtualNetworkGateway:*

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

### Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## NOTATKI

## LINKI POKREWNE

[Get-AzLocalNetworkGateway](./Get-AzLocalNetworkGateway.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGatewayDefaultSite](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


