---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 560053ca6b5e49ffcef8dbb6ee4b0ba32f3ed276
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892721"
---
# Set-AzVirtualNetworkGatewayDefaultSite

## STRESZCZENIe
Ustawia domyślną witrynę bramy sieci wirtualnej.

## POLECENIA

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzVirtualNetworkGatewayDefaultSite** przypisuje domyślną witrynę tunelowania wymuszonego do bramy sieci wirtualnej.
Wymuszone tunelowanie zapewnia sposób na przekierowanie ruchu związanego z Internetem z maszyn wirtualnych platformy Azure do sieci lokalnej. Dzięki temu można sprawdzać ruch i prowadzić inspekcję ruchu przed jego zwolnieniem.
Tunelowanie wymuszone jest realizowane przy użyciu tunelu wirtualnej sieci prywatnej (VPN); ten tunel wymaga witryny domyślnej, bramy lokalnej, w której jest przekierowywany cały ruch związany z Internetem usługi Azure.
**Set-AzVirtualNetworkGatewayDefaultSite** umożliwia zmianę domyślnej witryny przypisanej do bramy.

## Przykłady

### Przykład 1: przypisywanie domyślnej witryny do bramy sieci wirtualnej
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

W tym przykładzie przypiszesz witrynę domyślną do bramy sieci wirtualnej o nazwie ContosoVirtualGateway.

Pierwsze polecenie tworzy odwołanie do obiektu do bramy lokalnej o nazwie ContosoLocalGateway.
Odwołanie do obiektu przechowywane w zmiennej o nazwie $LocalGateway reprezentuje bramę, która ma zostać skonfigurowana jako witryna domyślna

.
Drugie polecenie tworzy następnie odwołanie do obiektu bramy sieci wirtualnej i zapisuje wynik w zmiennej o nazwie $VirtualGateway.

W trzecim poleceniu przypiszesz domyślną witrynę do ContosoVirtualGateway przy użyciu polecenia cmdlet **Set-AzVirtualNetworkGatewayDefaultSite** .

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

### -GatewayDefaultSite
Określa odwołanie do obiektu bramy sieci lokalnej, które ma zostać przypisane jako witryna domyślna dla określonej sieci wirtualnej.
Za pomocą polecenia cmdlet Get-AzLocalNetworkGateway można utworzyć odwołanie do obiektu do bramy lokalnej.

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Określa odwołanie do obiektu bramy sieci wirtualnej, w której zostanie przypisana domyślna witryna.
Odwołanie do obiektu bramy sieci wirtualnej można utworzyć, korzystając z funkcji **Get-AzVirtualNetworkGateway** i określając nazwę bramy.

Zmienna $VirtualGateway może być następnie używana jako wartość parametru parametru *VirtualNetworkGateway* :

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

## LINKI POKREWNE

[Get-AzLocalNetworkGateway](./Get-AzLocalNetworkGateway.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGatewayDefaultSite](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


