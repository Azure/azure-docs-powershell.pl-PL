---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: d7665d490979ca15189650572c083a94efb6c123
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003553"
---
# Remove-AzVpnClientRevokedCertificate

## SYNOPSIS
Usuwa certyfikat odwołania klienta sieci VPN.

## SKŁADNIA

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Remove-AzVpnClientRevokedCertificate** usuwa certyfikat odwołania klienta z bramy sieci wirtualnej.
Certyfikaty odwołań klientów uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.
Jeśli usuniesz klientów klientów z certyfikatem odwołania klienta, mogą użyć poprzednio zablokowanego certyfikatu w celu nawiązaniu połączenia z wirtualną siecią prywatną (VPN).

## PRZYKŁADY

### Przykład 1. Usuwanie certyfikatu odwołania klienta z bramy sieci wirtualnej
```powershell
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

To polecenie usuwa certyfikat odwołania klienta z wirtualnej bramy sieciowej o nazwie ContosoVirtualNetwork.
Aby usunąć certyfikat odwołania klienta, należy określić zarówno nazwę certyfikatu, jak i certyfikat thumbprint.

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
Określa identyfikator unikatowy usunięcia certyfikatu.
Możesz zwrócić informacje dotyczące kciuka w certyfikatach za pomocą polecenia programu Windows PowerShell podobnego do tego: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`
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

### -VirtualNetworkGatewayName
Określa nazwę bramy sieci wirtualnej, do których jest przypisany certyfikat.

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
Określa nazwę usuwanego certyfikatu klienta sieci VPN.

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

### System.Boolean

## NOTATKI

## LINKI POKREWNE

[Add-AzVpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[Get-AzVpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[New-AzVpnClientRevokedCertificate](./New-AzVpnClientRevokedCertificate.md)


