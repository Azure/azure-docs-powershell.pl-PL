---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 1c85bc5e2a935378630728083b19544ace8670b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892693"
---
# Set-AzVirtualNetworkGatewayVpnClientConfig

## STRESZCZENIe
Ustawia pulę adresów klienta sieci VPN dla bramy sieci wirtualnej.

## POLECENIA

### Domyślne (domyślnie)
```
Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RadiusServerConfiguration
```
Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzVirtualNetworkVpnClientConfig** konfiguruje pulę adresów klienta dla bramy sieci wirtualnej.
Klientom wirtualnej sieci prywatnej (VPN) łączącym się z tą bramą będzie przypisywany adres IP z tej puli adresów.

## Przykłady

### Przykład 1: przypisywanie puli adresów klienta sieci VPN do bramy sieci wirtualnej
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

W tym przykładzie przypiszesz pulę adresów klienta sieci VPN do bramy sieci wirtualnej o nazwie ContosoVirtualGateway.

Pierwsze polecenie tworzy odwołanie do obiektu do bramy, a obiekt jest przechowywany w zmiennej o nazwie $Gateway.

Drugie polecenie w przykładzie używa polecenia cmdlet **Set-AzVirtualNetworkGatewayVpnClientConfig** w celu przypisania puli adresów 10.0.0.0/16 do ContosoVirtualGateway.

### Przykład 2: Konfigurowanie uwierzytelniania zewnętrznego opartego na usłudze RADIUS w istniejącej bramie
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

W tym przykładzie przypiszesz pulę adresów klienta sieci VPN do bramy sieci wirtualnej o nazwie ContosoVirtualGateway.

Pierwsze polecenie tworzy odwołanie do obiektu do bramy, a obiekt jest przechowywany w zmiennej o nazwie $Gateway.

Drugie polecenie w przykładzie używa polecenia cmdlet **Set-AzVirtualNetworkGatewayVpnClientConfig** w celu przypisania puli adresów 10.0.0.0/16 do ContosoVirtualGateway. Ponadto konfiguruje zewnętrzny serwer RADIUS "TestRadiusServer", który ma być wykorzystywany do uwierzytelniania klientów VPN.

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

### -RadiusServerAddress
P2S zewnętrzny adres serwera RADIUS.

```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RadiusServerSecret
P2S zewnętrznych kluczy tajnych serwera RADIUS.

```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Określa odwołanie do obiektu bramy sieci wirtualnej, które zawiera ustawienia konfiguracji klienta sieci VPN, które to polecenie cmdlet modyfikuje.
Odwołanie do obiektu bramy sieci wirtualnej można utworzyć przy użyciu Get-AzVirtualNetworkGateway i określając nazwę bramy.

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

### -VpnClientAddressPool
Określa adresy IP, które mają być przypisywane klientom łączącym się z tą bramą.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Zmienianie rozmiaru — AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)


