---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: b952033bc6f04f2ed1e6d2e257dc68da1a6ec6db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979690"
---
# Add-AzVpnClientRevokedCertificate

## SYNOPSIS
Dodaje certyfikat odwołania klienta sieci VPN.

## SKŁADNIA

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Add-AzVpnClientRevokedCertificate** przypisuje certyfikat odwołania klienta do bramy sieci wirtualnej.
Certyfikaty odwołań klientów uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.
Aby użyć tego polecenia cmdlet, należy zarówno określić nazwę certyfikatu, jak i nazwę usbprint certyfikatu.

## PRZYKŁADY

### Przykład 1. Dodawanie nowego certyfikatu odwołania klienta do bramy sieci wirtualnej
```powershell
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

To polecenie dodaje nowy certyfikat odwołania klienta do bramy sieci wirtualnej o nazwie ContosoVirtualNetwork.
Aby dodać certyfikat, musisz określić zarówno nazwę certyfikatu, jak i usbprint certyfikatu.

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

### -ResourceGroupName
Określa nazwę grupy zasobów, do których przypisano bramę sieci wirtualnej.
Grupy zasobów kategoryzowają elementy, aby uprościć zarządzanie zapasami i ogólną administrację azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - Thumbprint
Określa identyfikator unikatowy dodawana certyfikatu.
Na przykład: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" Możesz uzyskać informacje dotyczące kciuka dla certyfikatów, używając polecenia programu Windows PowerShell podobnego do `Get-ChildItem -Path Cert:\LocalMachine\Root` tego:
Poprzednie polecenie pobiera informacje dotyczące wszystkich certyfikatów komputerów lokalnych znalezionych w głównym magazynie certyfikatów.

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

### -VirtualNetworkGatewayName
Określa nazwę bramy sieci wirtualnej, do której ma zostać dodany certyfikat.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnClientRevokedCertificateName
Określa nazwę certyfikatu klienta sieci VPN do dodania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate

## NOTATKI

## LINKI POKREWNE

[Get-AzVpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[New-AzVpnClientRevokedCertificate](./New-AzVpnClientRevokedCertificate.md)

[Remove-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


