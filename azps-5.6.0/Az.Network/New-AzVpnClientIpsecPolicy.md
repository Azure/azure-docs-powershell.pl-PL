---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 7556a2d23d4c4969c3037d6b49dbd482bcdea207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964113"
---
# New-AzVpnClientIpsecPolicy

## SYNOPSIS
To polecenie umożliwia użytkownikom utworzenie obiektu zasad vpn ipsec określającego jedną lub wszystkie wartości, takie jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia dla bramy VPN. To polecenie pozwala obiektowi wyjścioweowi na ustawianie zasad ipsec sieci vpn zarówno dla nowej/ istniejącej bramy, jak i dla istniejącej bramy.

## SKŁADNIA

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
To polecenie umożliwia użytkownikom utworzenie obiektu zasad vpn ipsec określającego jedną lub wszystkie wartości, takie jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia dla bramy VPN. To polecenie pozwala obiektowi wyjścioweowi na ustawianie zasad ipsec sieci vpn zarówno dla nowej/ istniejącej bramy, jak i dla istniejącej bramy.

## PRZYKŁADY

### Przykład 1. Definiowanie obiektu zasad vpn ipsec:
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

To polecenie cmdlet służy do tworzenia obiektu zasad vpn ipsec przy użyciu wartości przekazywanego jednego lub wszystkich parametrów, które użytkownik może przekazać do parametru:VpnClientIpsecPolicy z polecenia PS let: New-AzVirtualNetworkGateway (Tworzenie nowej bramy VPN) / Set-AzVirtualNetworkGateway (istniejąca aktualizacja bramy VPN) w grupie Zasobów:

### Przykład 2. Tworzenie nowej bramy sieci wirtualnej z ustawieniem niestandardowych zasad ipsec sieci vpn:
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

To polecenie cmdlet zwraca obiekt wirtualnej bramy sieciowej po utworzeniu. 

### Przykład 3. Ustawianie niestandardowych zasad ipsec sieci vpn dla istniejącej bramy sieci wirtualnej:
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

To polecenie cmdlet zwraca obiekt bramy sieci wirtualnej po ustawieniu niestandardowych zasad ipsec sieci vpn.

### Przykład 4. Uzyskaj wirtualną bramę sieciową, aby sprawdzić, czy niestandardowe zasady sieci vpn są poprawnie ustawione:
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

To polecenie cmdlet zwraca obiekt bramy sieci wirtualnej.

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
Grupy VPNClient DH używane w IKE Phase 1 dla początkowego SA

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

### Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy

## NOTATKI

## LINKI POKREWNE
