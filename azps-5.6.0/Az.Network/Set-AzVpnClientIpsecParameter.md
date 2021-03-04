---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 55a4f3c143355bf40672a1c3151d509b69062490
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952010"
---
# Set-AzVpnClientIpsecParameter

## SYNOPSIS
Ustawia parametry ipsec połączenia vpn dla istniejącej bramy sieci wirtualnej.

## SKŁADNIA

### ByFactoryName (Default)
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceId
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzVpnClientIpsecParameters** ustawia parametry ipsec połączenia vpn dla istniejącej bramy sieci wirtualnej.
Podczas tworzenia wirtualnej bramy sieciowej ustawia ona zestaw domyślnych zasad ipsec sieci vpn dla bramy. W przypadku, gdy użytkownik wskaż witrynę chce używać pewnych niestandardowych zasad ipsec do łączenia się z bramą VPN, użytkownik musi najpierw ustawić te zasady ipsec dla bramy VPN. **Set-AzVpnClientIpsecParameters** umożliwia to.

## PRZYKŁADY

### Przykład 1. Ustawia niestandardowe zasady ipsec sieci vpn na istniejącą bramę sieci wirtualnej.
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

W tym przykładzie niestandardowa zasada ipsec połączenia vpn jest ustawiana na istniejącą wirtualną bramę sieciową o nazwie ContosoVirtualGateway z grupy Zasobów o nazwie ContosoResourceGroup.
New-AzVpnClientIpsecParameter cmdlet służy do tworzenia obiektu parametrów ipsec sieci vpn w celu użycia wartości przekazywanego jednego lub wszystkich parametrów, które użytkownik może ustawić dla dowolnej istniejącej bramy sieci wirtualnej w grupie Zasobów.
Ten utworzony obiekt VpnClientIPsecParameters jest przekazywany do polecenia Set-AzVpnClientIpsecParameter w celu ustawienia określonych niestandardowych zasad ipsec sieci vpn dla wirtualnej bramy sieciowej, jak pokazano w powyższym przykładzie. To polecenie zwraca obiekt VpnClientIPsecParameters, który pokazuje ustawione parametry.

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

### -InputObject
Obiekt bramy sieci wirtualnej

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

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

### -ResourceId
Identyfikator zasobu Azure.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Nazwa bramy sieci wirtualnej.

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

### -VpnClientIPsecParameters
Parametry ipsec klienta sieci VPN. Tę wartość parametru można utworzyć przy użyciu polecenia PS let:New-AzVpnClientIpsecParameters

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters

## NOTATKI

## LINKI POKREWNE

[Get-AzVpnClientIpsecParameters](./Get-AzVpnClientIpsecParameter.md)

[New-AzVpnClientIpsecParameters](./New-AzVpnClientIpsecParameter.md)

[Remove-AzVpnClientIpsecParameters](./Remove-AzVpnClientIpsecParameter.md)
