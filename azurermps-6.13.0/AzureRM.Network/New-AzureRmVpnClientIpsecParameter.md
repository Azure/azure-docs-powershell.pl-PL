---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 89106b6474e52863514c65614d334cf5d8382f3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719395"
---
# New-AzureRmVpnClientIpsecParameter

## STRESZCZENIe
To polecenie umożliwia użytkownikom tworzenie obiektu parametry protokołu IPsec sieci VPN z podaniem jednej lub wszystkich wartości, takich jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia istniejącej bramy sieci VPN.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
To polecenie umożliwia użytkownikom tworzenie obiektu parametry protokołu IPsec sieci VPN z podaniem jednej lub wszystkich wartości, takich jak IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup do ustawienia istniejącej bramy sieci VPN.

## Przykłady

### Przykład 1
```
PS C:\> $vpnclientipsecparams1 = New-AzureRmVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

Polecenie cmdlet New-AzureRmVpnClientIpsecParameter służy do tworzenia obiektu parametry IPsec sieci VPN z użyciem wartości przekazanych jeden lub wszystkie parametry, które użytkownik może ustawić dla dowolnej istniejącej bramy sieci wirtualnej w obszarze zasobów.
Ten obiekt VpnClientIPsecParameters został przekazany do polecenia Set-AzureRmVpnClientIpsecParameter w celu ustawienia określonych zasad niestandardowych IPSec VPN w bramie sieci wirtualnej, jak pokazano na przykładzie powyżej. To polecenie zwraca obiekt VpnClientIPsecParameters, w którym pokazano parametry Set.

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
Grupy Vpnclient DH używane w usłudze IKE phase 1 w przypadku początkowego skojarzenia zabezpieczeń.

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

### Microsoft. Azure. Commands. Network. models. PSVpnClientIPsecParameters

## INFORMACYJN

## LINKI POKREWNE
