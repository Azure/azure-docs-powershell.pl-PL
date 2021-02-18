---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: e345d64a921d598e610f297a0508df58b45c99a6
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410551"
---
# Resize-AzVirtualNetworkGateway

## SYNOPSIS
Zmienia rozmiar istniejącej bramy sieci wirtualnej.

## SKŁADNIA

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Resize-AzVirtualNetworkGateway** umożliwia zmianę jednostki magazynowej (SKU) dla bramy sieci wirtualnej.
Jednostki SKU określają możliwości bramy, w tym przepływność i maksymalną dozwoloną liczbę adresów IP.
Platforma Azure obsługuje jednostki SKU Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ (czasami określane mianem małych, średnich i dużych jednostki SKU).
Aby uzyskać szczegółowe informacje na temat możliwości poszczególnych typów sKU, https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ zobacz.
Pamiętaj, że ceny i możliwości aplikacji różnią się w poszczególnych cenach.
Aby uzyskać więcej informacji, zobacz https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## PRZYKŁADY

### Przykład 1. Zmienianie rozmiaru bramy sieci wirtualnej
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

W tym przykładzie zmienia się rozmiar bramy sieci wirtualnej o nazwie ContosoVirtualGateway.
Pierwsze polecenie tworzy odwołanie do obiektu ContosoVirtualGateway. to odwołanie do obiektu jest przechowywane w zmiennej o nazwie $Gateway.
Drugie polecenie użyje polecenia cmdlet **Resize-AzVirtualNetworkGateway** w celu ustawienia właściwości *GatewaySku* na Wartość Podstawowa.

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

### -GatewaySku
Określa nowy typ sKU bramy.
Dopuszczalne wartości dla tego parametru to:
- Podstawowe
- Standardowe
- Wysoka wydajność
- VpnGw1
- VpnGw2
- VpnGw3
- VpnGw1AZ 
- VpnGw2AZ 
- VpnGw3AZ 
- ErGw1AZ 
- ErGw2AZ 
- ErGw3AZ 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — VirtualNetworkGateway
Określa odwołanie do obiektu do bramy sieci wirtualnej, których rozmiar ma zostać zmieniony.
To odwołanie do obiektu można utworzyć, używając Get-AzVirtualNetworkGateway i określając nazwę bramy.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## NOTATKI
Nie można zmienić rozmiaru z wersji Basic/Standard/HighPerformance na nowe jednostki SKU VpnGw1/VpnGw2/VpnGw3. Dalsze zmienianie rozmiaru nie jest dozwolone z/do VpnGw1AZ/VpnGw2AZ/VpnGw3AZ lub ErGw1AZ/ErGw2AZ/ErGw3AZ. Zmiana rozmiaru jest dozwolona tylko w "serii" SKU, np. VpnGw1AZ można zmienić na/z VpnGw2AZ/VpnGw3AZ i ErGw1AZ można zmienić na/z ErGw2AZ/ErGw3AZ. Zobacz https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways instrukcje.

## LINKI POKREWNE

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[New-AzVirtualNetworkGateway](./New-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGateway](./Remove-AzVirtualNetworkGateway.md)

[Reset-AzVirtualNetworkGateway](./Reset-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGateway](./Set-AzVirtualNetworkGateway.md)

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

