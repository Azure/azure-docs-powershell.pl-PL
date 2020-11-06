---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecPolicy.md
ms.openlocfilehash: 98ea39141614c800b7b71d2f0c75519762bb87b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553483"
---
# New-AzureRmVpnClientIpsecPolicy

## STRESZCZENIe
To polecenie umożliwia użytkownikom tworzenie obiektu zasad IPSec sieci VPN określającego jedno lub wszystkie wartości, takie jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia bramy sieci VPN. To polecenie umożliwia obiektowi Output określenie zasad IPSec dla sieci VPN zarówno dla bramy New/dopełnienie.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
To polecenie umożliwia użytkownikom tworzenie obiektu zasad IPSec sieci VPN określającego jedno lub wszystkie wartości, takie jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia bramy sieci VPN. To polecenie umożliwia obiektowi Output określenie zasad IPSec dla sieci VPN zarówno dla bramy New/dopełnienie.

## Przykłady

### Definiowanie obiektu zasad IPSec sieci VPN:
```
PS C:\>$vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

To polecenie cmdlet służy do tworzenia obiektu zasad IPSec sieci VPN przy użyciu wartości przekazana jedna lub wszystkie parametry ', które użytkownik może przekazać do parametru PARAM: VpnClientIpsecPolicy z polecenia PS: New-AzureRmVirtualNetworkGateway (Tworzenie nowego bramy sieci VPN)/Set-AzureRmVirtualNetworkGateway (istniejąca aktualizacja bramy sieci VPN) w obszarze zasobów.

### Utwórz nową bramę sieci wirtualnej z ustawieniem niestandardowych zasad IPSec sieci VPN:
```
PS C:\> $vnetGateway = New-AzureRmVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

To polecenie cmdlet zwraca obiekt bramy sieci wirtualnej po utworzeniu. 

### Ustawianie niestandardowych zasad IPSec sieci VPN w istniejącej bramie sieci wirtualnej:
```
PS C:\> $vnetGateway = Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

To polecenie cmdlet zwraca obiekt bramy sieci wirtualnej po ustawieniu niestandardowych zasad IPSec sieci VPN.

### Uzyskaj bramę sieci wirtualnej, aby sprawdzić, czy zasady niestandardowe sieci VPN są ustawione poprawnie:
```
PS C:\> $gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

To polecenie cmdlet zwraca obiekt bramy sieci wirtualnej.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DhGroup
Grupy Vpnclient DH używane w usłudze IKE phase 1 dla początkowego skojarzenia zabezpieczeń

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
Algorytm szyfrowania Vpnclient IKE (Usługa IKE Phase 2)

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
Algorytm integralności usługi IKE Vpnclient (Usługa IKE Phase 2)

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
Algorytm szyfrowania IPSec Vpnclient (faza IKE 1)

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
Algorytm integralności protokołu IPSec Vpnclient (faza IKE 1)

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
Grupy PFS Vpnclient używane w usłudze IKE Phase 2 dla nowego podrzędnego pakietu SA

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
Rozmiar ładunku skojarzenia zabezpieczeń IPSec Vpnclient (nazywanego także trybem szybkim lub fazą 2 SA) w KB

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
W sekundach skojarzenie zabezpieczeń IPSec Vpnclient (nazywane także trybem szybkim lub fazą 2 SA)

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSIpsecPolicy

## INFORMACYJN

## LINKI POKREWNE
