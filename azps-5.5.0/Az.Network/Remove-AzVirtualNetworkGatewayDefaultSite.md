---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 288812137887e4fc22308bba56a3fbdbeeb28c85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179474"
---
# Remove-AzVirtualNetworkGatewayDefaultSite

## SYNOPSIS
Usuwa witrynę domyślną z bramy sieci wirtualnej.

## SKŁADNIA

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Remove-AzVirtualNetworkGatewayDefaultSite** usuwa z bramy sieci wirtualnej witrynę sieci wirtualnej, która jest wymuszana przez wydychanie z sieci wirtualnej.
Wymuszone podkoszowe zapewnia możliwość przekierowywania ruchu związanego z Internetem z maszyn wirtualnych platformy Azure do Twojej sieci lokalnej. umożliwia to inspekcję i inspekcję ruchu przed jego zwolnieniem.
Wymuszone podkołowy są wykonywane przy użyciu podkołowego wirtualnej sieci prywatnej (VPN); ten kork wymaga witryny domyślnej, bramy lokalnej, do której jest przekierowywany cały ruch internetowy platformy Azure.
**Remove-AzVirtualNetworkGatewayDefaultSite** usuwa domyślną witrynę przypisaną do bramy.
W takim przypadku konieczne będzie użycie programu Set-AzVirtualNetworkGatewayDefaultSite do przypisania nowej witryny domyślnej, aby brama była używana do wymuszania wydychania bram.

## PRZYKŁADY

### Przykład 1. Usuwanie witryny domyślnej przypisanej do bramy sieci wirtualnej
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

W tym przykładzie jest usuwana witryna domyślna obecnie przypisana do wirtualnej bramy sieciowej o nazwie ContosoVirtualGateway.
Pierwsze polecenie tworzy odwołanie do obiektu bramy za pomocą polecenia **Get-AzVirtualNetworkGateway;** to odwołanie do obiektu jest przechowywane w zmiennej o nazwie $Gateway.
Drugie polecenie używa następnie **polecenia Remove-AzVirtualNetworkGatewayDefaultSite** w celu usunięcia witryny domyślnej przypisanej do tej bramy.

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

### — VirtualNetworkGateway
Określa odwołanie do obiektu do bramy sieci wirtualnej zawierającej witrynę domyślną do usunięcia.
Możesz utworzyć odwołanie do obiektu do bramy sieci wirtualnej, używając Get-AzVirtualNetworkGateway i określając nazwę bramy.

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

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## NOTATKI

## LINKI POKREWNE

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayDefaultSite](./Set-AzVirtualNetworkGatewayDefaultSite.md)


