---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 0a3dea2b706f7efcdc76b48175df225e2974728c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899215"
---
# Resize-AzureRmVirtualNetworkGateway

## STRESZCZENIe
Zmienia rozmiar istniejącej bramy sieci wirtualnej.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet Change **-AzureRmVirtualNetworkGateway** umożliwia zmianę jednostki składowania zapasu (SKU) dla bramy sieci wirtualnej.
Wersje SKU określają możliwości bramy, w tym takie jak przepływność i Maksymalna liczba dozwolonych tuneli IP.
Platforma Azure obsługuje podstawowe, standardowe, wysoko wydajne, VpnGw1, VpnGw2 i VpnGw3 SKU (czasami nazywane małymi, średnimi i dużymi wersjami SKU).
Aby uzyskać szczegółowe informacje o możliwościach poszczególnych typów SKU, zobacz temat https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .

Pamiętaj, że jednostki SKU są różne w kalkulacji cen, a także możliwości.
Aby uzyskać więcej informacji, zobacz https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## Przykłady

### Przykład 1. Zmienianie rozmiaru bramy sieci wirtualnej
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

W tym przykładzie jest zmieniany rozmiar bramy sieci wirtualnej o nazwie ContosoVirtualGateway.

Pierwsze polecenie tworzy odwołanie do obiektu ContosoVirtualGateway; odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $Gateway.

Drugie polecenie używa polecenia cmdlet **zmiany rozmiaru AzureRmVirtualNetworkGateway** , aby ustawić właściwość *GatewaySku* na podstawową.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GatewaySku
Określa nowy typ jednostki SKU bramy.
Dopuszczalne wartości tego parametru to:

- Podstawowym
- Standard
- Wysoka wydajność
- VpnGw1
- VpnGw2
- VpnGw3

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Określa odwołanie do obiektu bramy sieci wirtualnej, którego rozmiar ma zostać zmieniony.
To odwołanie do obiektu można utworzyć przy użyciu Get-AzureRmVirtualNetworkGateway i określając nazwę bramy.

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

###  
To polecenie cmdlet akceptuje potokowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .

## WYSYŁA

###  
To polecenie cmdlet modyfikuje istniejące wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .

## INFORMACYJN
Nie można zmienić rozmiaru podstawowego/standardowego/HighPerformance SKU na nowy VpnGw1/VpnGw2/VpnGw3 SKU. Zobacz https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways instrukcje.

## LINKI POKREWNE

[Get-AzureRmVpnClientPackage](./Get-AzureRmVpnClientPackage.md)

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGatewayVpnClientConfig](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


