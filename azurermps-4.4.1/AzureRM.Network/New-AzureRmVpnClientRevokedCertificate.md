---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e1f85cbb90e1318c6eab595ef00929ceb1a5b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527430"
---
# New-AzureRmVpnClientRevokedCertificate

## STRESZCZENIe
Tworzy nowy certyfikat odwołania klienta sieci VPN.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmVpnClientRevokedCertificate** tworzy nowy certyfikat odwołania klienta wirtualnej sieci prywatnej (VPN) do użycia w wirtualnej bramie sieci.
Certyfikaty odwołań klienta uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.

To polecenie cmdlet tworzy autonomiczny certyfikat, który nie jest przypisany do bramy wirtualnej.
Zamiast tego certyfikat utworzony za pomocą polecenia **New-AzureRmVpnClientRevokedCertificate** jest wykorzystywany w połączeniu z poleceniem cmdlet New-AzureRmVirtualNetworkGateway podczas tworzenia nowej bramy.
Załóżmy na przykład, że tworzysz nowy certyfikat i zapisujesz go w zmiennej o nazwie $Certificate.
Po utworzeniu nowej bramy wirtualnej można użyć tego obiektu certyfikatu.
Na przykład

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`

Aby uzyskać więcej informacji, zobacz dokumentację New-AzureRmVirtualNetworkGateway polecenia cmdlet.

## Przykłady

### Przykład 1. Tworzenie nowego certyfikatu odwołanego przez klienta
```
PS C:\>$Certificate = New-AzureRmVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

To polecenie tworzy nowy certyfikat odwołany przez klienta i zapisuje obiekt Certificate w zmiennej o nazwie $Certificate.
Ta zmienna może być następnie używana przez polecenie cmdlet **New-AzureRmVirtualNetworkGateway** , aby dodać certyfikat do nowej bramy sieci wirtualnej.

## PARAMETRÓW

### -Name (nazwa)
Określa unikatową nazwę nowego certyfikatu odwołania klienta.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Odcisk palca
Określa unikatowy identyfikator dodawanego certyfikatu.

Możesz zwrócić informacje o odcisku palca dotyczące certyfikatów przy użyciu polecenia programu Windows PowerShell podobnej do następującego:

`Get-ChildItem -Path Cert:\LocalMachine\Root`

Powyższe polecenie zwraca informacje dotyczące wszystkich certyfikatów komputerów lokalnych znajdujących się w głównym magazynie certyfikatów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
To polecenie cmdlet nie akceptuje danych wejściowych potoku.

## WYSYŁA

###  
To polecenie cmdlet tworzy nowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVpnClientRevokedCertificate** .

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureRmVpnClientRevokedCertificate](./Add-AzureRmVpnClientRevokedCertificate.md)

[Get-AzureRmVpnClientRevokedCertificate](./Get-AzureRmVpnClientRevokedCertificate.md)

[Remove-AzureRmVpnClientRevokedCertificate](./Remove-AzureRmVpnClientRevokedCertificate.md)


