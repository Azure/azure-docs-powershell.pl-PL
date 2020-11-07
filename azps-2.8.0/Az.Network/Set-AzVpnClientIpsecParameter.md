---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 248e932bfc2c9148122ecad924ae10b3e480fd3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872120"
---
# Set-AzVpnClientIpsecParameter

## STRESZCZENIe
Ustawia parametry protokołu IPsec sieci VPN dla istniejącej bramy sieci wirtualnej.

## POLECENIA

### ByFactoryName (domyślny)
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

## Opis
Polecenie cmdlet **Set-AzVpnClientIpsecParameter** ustawia parametry protokołu IPsec sieci VPN dla istniejącej bramy sieci wirtualnej.
Po utworzeniu bramy sieci wirtualnej ustawia ona zestaw domyślnych zasad IPSec sieci VPN w bramie. W przypadku wskazywania, że użytkownik witryny chce użyć pewnych niestandardowych zasad IPSec do łączenia się z bramą VPN, użytkownik musi najpierw ustawić zasady IPSec w bramie VPN. **Set-AzVpnClientIpsecParameter** umożliwia wykonanie tej czynności.

## Przykłady

### Przykład 1: ustawia niestandardową zasadę IPSec sieci VPN na istniejącą bramę sieci wirtualnej.
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

W tym przykładzie ustawiono niestandardowe zasady IPSec sieci VPN do istniejącej bramy sieci wirtualnej o nazwie ContosoVirtualGateway z grupy zasobów o nazwie ContosoResourceGroup.
Polecenie cmdlet New-AzVpnClientIpsecParameter służy do tworzenia obiektu parametry IPsec sieci VPN z użyciem wartości przekazanych jeden lub wszystkie parametry, które użytkownik może ustawić dla dowolnej istniejącej bramy sieci wirtualnej w obszarze zasobów.
Ten obiekt VpnClientIPsecParameters został przekazany do polecenia Set-AzVpnClientIpsecParameter w celu ustawienia określonych zasad niestandardowych IPSec VPN w bramie sieci wirtualnej, jak pokazano na przykładzie powyżej. To polecenie zwraca obiekt VpnClientIPsecParameters, w którym pokazano parametry Set.

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

### -Inputobject
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
Identyfikator zasobu platformy Azure.

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

### -VpnClientIPsecParameter
Parametry protokołu IPSec klienta sieci VPN. Ta wartość parametru może być konstruowana za pomocą polecenia PS Let: New-AzVpnClientIpsecParameter

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Network. models. PSVpnClientIPsecParameters

### Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSVpnClientIPsecParameters

## INFORMACYJN

## LINKI POKREWNE

[Get-AzVpnClientIpsecParameter](./Get-AzVpnClientIpsecParameter.md)

[Nowe — AzVpnClientIpsecParameter](./New-AzVpnClientIpsecParameter.md)

[Remove-AzVpnClientIpsecParameter](./Remove-AzVpnClientIpsecParameter.md)
