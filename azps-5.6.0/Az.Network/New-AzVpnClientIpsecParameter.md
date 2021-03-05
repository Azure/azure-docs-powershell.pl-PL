---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 3b34fb1de6b661a622690f93808eaf0660da461b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995324"
---
# New-AzVpnClientIpsecParameter

## SYNOPSIS
To polecenie umożliwia użytkownikom utworzenie obiektu parametrów ipsec połączenia vpn, który określa jedną lub wszystkie wartości, takie jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia dla istniejącej bramy VPN.

## SKŁADNIA

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
To polecenie umożliwia użytkownikom utworzenie obiektu parametrów ipsec połączenia vpn, który określa jedną lub wszystkie wartości, takie jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia dla istniejącej bramy VPN.

## PRZYKŁADY

### Przykład 1
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

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

### - DhGroup
Grupy VPNClient DH używane w IKE Phase 1 dla początkowego SA.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - IkeEncryption
Algorytm szyfrowania IKE vpnClient (etap 2 usługi IKE)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IkeIntegrity
Algorytm integralności IKE vpnClient (etap 2 usługi IKE)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpsecEncryption
Algorytm szyfrowania IPSec usługi VpnClient (etap IKE 1)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpsecIntegrity
Algorytm integralności IPSec usługi VpnClient (etap IKE 1)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - PfsGroup
Grupy VPNClient PFS używane w fazie 2 IKE dla nowego dziecka SA

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SADataSize
Rozmiar ładowania vpnClient IPSec Security Association (nazywany również szybkim trybem lub etapem 2 SA) w KB

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SALifeTime
Okres istnienia skojarzenia zabezpieczeń IPSec usługi VpnClient (nazywanego również trybem szybkim lub etapem 2 SA) w ciągu kilku sekund

```yaml
Type: System.Int32
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

### Brak

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters

## NOTATKI

## LINKI POKREWNE

[Get-AzVpnClientIpsecParameters](./Get-AzVpnClientIpsecParameter.md)

[Remove-AzVpnClientIpsecParameters](./Remove-AzVpnClientIpsecParameter.md)

[Set-AzVpnClientIpsecParameters](./Set-AzVpnClientIpsecParameter.md)
