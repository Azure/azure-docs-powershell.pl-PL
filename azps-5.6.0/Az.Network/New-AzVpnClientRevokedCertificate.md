---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 85a35fe4c6b988ce6f5320d308582fb722cc5791
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964097"
---
# New-AzVpnClientRevokedCertificate

## SYNOPSIS
Tworzy nowy certyfikat odwołania klienta sieci VPN.

## SKŁADNIA

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **New-AzVpnClientRevokedCertificate** tworzy nowy certyfikat odwołania klienta wirtualnej sieci prywatnej (VPN) do użytku w bramie sieci wirtualnej.
Certyfikaty odwołań klientów uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.
To polecenie cmdlet tworzy autonomiczny certyfikat, który nie jest przypisany do bramy wirtualnej.
Zamiast tego certyfikat utworzony przez **new-AzVpnClientRevokedCertificate** jest używany w połączeniu z poleceniem cmdlet New-AzVirtualNetworkGateway podczas tworzenia nowej bramy.
Załóżmy na przykład, że tworzysz nowy certyfikat i przechowujesz go w zmiennej o nazwie $Certificate.
Następnie można użyć tego obiektu certyfikatu podczas tworzenia nowej bramy wirtualnej.
Na przykład: `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`
Aby uzyskać więcej informacji, zapoznaj się z dokumentacją tego New-AzVirtualNetworkGateway cmdlet.

## PRZYKŁADY

### Przykład 1. Tworzenie nowego certyfikatu z odwołaniem klienta
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

To polecenie tworzy nowy certyfikat odwołany przez klienta i przechowuje obiekt certyfikatu w zmiennej o nazwie $Certificate.
Ta zmienna może być następnie używana przez polecenie cmdlet **New-AzVirtualNetworkGateway** w celu dodania certyfikatu do nowej bramy sieci wirtualnej.

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

### — Nazwa
Określa unikatową nazwę dla nowego certyfikatu odwołania klienta.

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

### - Thumbprint
Określa identyfikator unikatowy dodawana certyfikatu.
Możesz zwrócić informacje dotyczące kciuka w certyfikatach za pomocą polecenia programu Windows PowerShell podobnego do tego: `Get-ChildItem -Path Cert:\LocalMachine\Root`
Poprzednie polecenie zwraca informacje dotyczące wszystkich certyfikatów Komputer lokalny znalezionych w magazynie certyfikatów głównych.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Brak

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate

## NOTATKI

## LINKI POKREWNE

[Add-AzVpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[Get-AzVpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[Remove-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


