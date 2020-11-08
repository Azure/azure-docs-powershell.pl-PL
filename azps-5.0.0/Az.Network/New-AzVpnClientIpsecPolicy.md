---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 028c33db36df5debb6f951f11e27f0586e7a21dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234119"
---
# New-AzVpnClientIpsecPolicy

## STRESZCZENIe
To polecenie umożliwia użytkownikom tworzenie obiektu zasad IPSec sieci VPN określającego jedno lub wszystkie wartości, takie jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia bramy sieci VPN. To polecenie umożliwia obiektowi Output określenie zasad IPSec sieci VPN zarówno dla nowej, jak i istniejącej bramy.

## POLECENIA

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
To polecenie umożliwia użytkownikom tworzenie obiektu zasad IPSec sieci VPN określającego jedno lub wszystkie wartości, takie jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia bramy sieci VPN. To polecenie umożliwia obiektowi Output określenie zasad IPSec sieci VPN zarówno dla nowej, jak i istniejącej bramy.

## Przykłady

### Przykład 1: Definiowanie obiektu zasad IPSec sieci VPN:
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

To polecenie cmdlet służy do tworzenia obiektu zasad IPSec sieci VPN przy użyciu wartości przekazana jedna lub wszystkie parametry ', które użytkownik może przekazać do parametru PARAM: VpnClientIpsecPolicy z polecenia PS: New-AzVirtualNetworkGateway (Tworzenie nowego bramy sieci VPN)/Set-AzVirtualNetworkGateway (istniejąca aktualizacja bramy sieci VPN) w obszarze zasobów.

### Przykład 2: Utwórz nową bramę sieci wirtualnej z ustawieniem niestandardowych zasad IPSec sieci VPN:
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

To polecenie cmdlet zwraca obiekt bramy sieci wirtualnej po utworzeniu. 

### Przykład 3: Ustawianie niestandardowych zasad IPSec sieci VPN w istniejącej bramie sieci wirtualnej:
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

To polecenie cmdlet zwraca obiekt bramy sieci wirtualnej po ustawieniu niestandardowych zasad IPSec sieci VPN.

### Przykład 4: Uzyskaj wirtualną bramę sieciową, aby sprawdzić, czy zasady niestandardowe sieci VPN są ustawione poprawnie:
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

To polecenie cmdlet zwraca obiekt bramy sieci wirtualnej.

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

### -DhGroup
Grupy VpnClient DH używane w usłudze IKE phase 1 dla początkowego skojarzenia zabezpieczeń

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

### -IkeEncryption
Algorytm szyfrowania VpnClient IKE (Usługa IKE Phase 2)

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
Algorytm integralności usługi IKE VpnClient (Usługa IKE Phase 2)

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
Algorytm szyfrowania IPSec VpnClient (faza IKE 1)

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
Algorytm integralności protokołu IPSec VpnClient (faza IKE 1)

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

### -PfsGroup
Grupy PFS VpnClient używane w usłudze IKE Phase 2 dla nowego podrzędnego pakietu SA

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
Rozmiar ładunku skojarzenia zabezpieczeń IPSec VpnClient (nazywanego także trybem szybkim lub fazą 2 SA) w KB

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
W sekundach skojarzenie zabezpieczeń IPSec VpnClient (nazywane także trybem szybkim lub fazą 2 SA)

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSIpsecPolicy

## INFORMACYJN

## LINKI POKREWNE
