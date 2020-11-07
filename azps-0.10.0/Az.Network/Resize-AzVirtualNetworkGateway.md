---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: bd42d7cec30b7d42dcb1cdb3657f6681bf2cb6b0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892877"
---
# Resize-AzVirtualNetworkGateway

## STRESZCZENIe
Zmienia rozmiar istniejącej bramy sieci wirtualnej.

## POLECENIA

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet Change **-AzVirtualNetworkGateway** umożliwia zmianę jednostki składowania zapasu (SKU) dla bramy sieci wirtualnej.
Wersje SKU określają możliwości bramy, w tym takie jak przepływność i Maksymalna liczba dozwolonych tuneli IP.
Platforma Azure obsługuje podstawowe, standardowe, wysoko wydajne, VpnGw1, VpnGw2 i VpnGw3 SKU (czasami nazywane małymi, średnimi i dużymi wersjami SKU).
Aby uzyskać szczegółowe informacje o możliwościach poszczególnych typów SKU, zobacz temat https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .

Pamiętaj, że jednostki SKU są różne w kalkulacji cen, a także możliwości.
Aby uzyskać więcej informacji, zobacz https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## Przykłady

### Przykład 1. Zmienianie rozmiaru bramy sieci wirtualnej
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

W tym przykładzie jest zmieniany rozmiar bramy sieci wirtualnej o nazwie ContosoVirtualGateway.

Pierwsze polecenie tworzy odwołanie do obiektu ContosoVirtualGateway; odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $Gateway.

Drugie polecenie używa polecenia cmdlet **zmiany rozmiaru AzVirtualNetworkGateway** , aby ustawić właściwość *GatewaySku* na podstawową.

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
To odwołanie do obiektu można utworzyć przy użyciu Get-AzVirtualNetworkGateway i określając nazwę bramy.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

###  
To polecenie cmdlet akceptuje potokowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .

## WYSYŁA

###  
To polecenie cmdlet modyfikuje istniejące wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .

## INFORMACYJN
Nie można zmienić rozmiaru podstawowego/standardowego/HighPerformance SKU na nowy VpnGw1/VpnGw2/VpnGw3 SKU. Zobacz https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways instrukcje.

## LINKI POKREWNE

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


