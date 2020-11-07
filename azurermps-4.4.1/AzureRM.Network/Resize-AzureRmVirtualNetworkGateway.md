---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 9f7b85ed3c8f7c1c64ec89f8575975dde81fed7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719617"
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
Type: System.String
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
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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


