---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: 6211b422e9dfc16358303d766edecf437b44240d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016202"
---
# Get-AzVpnClientRootCertificate

## SYNOPSIS
Pobiera informacje o certyfikatach głównych sieci VPN.

## SKŁADNIA

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>] -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzVpnClientRootCertificate** zwraca informacje o certyfikatach głównych przypisanych do bramy sieci wirtualnej.
Certyfikaty główne to certyfikaty X.509 identyfikujące główny urząd certyfikacji: wszystkie pozostałe certyfikaty używane w bramie są zaufanymi certyfikatami głównymi.
Domyślnie **get-AzVpnClientRootCertificate** zwraca informacje o wszystkich certyfikatach głównych przypisanych do bramy.
Bramy mogą mieć więcej niż jeden certyfikat główny. Jednak uwzględniając parametr **VpnClientRootCertificateName,** możesz ograniczyć zwracane dane do określonego certyfikatu.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie informacji o wszystkich certyfikatach głównych
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

To polecenie pobiera informacje o wszystkich certyfikatach głównych przypisanych do bramy sieci wirtualnej o nazwie ContosoVirtualNetwork.

### Przykład 2. Uzyskiwanie informacji o konkretnych certyfikatach głównych
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

To polecenie jest odmianą polecenia pokazaną w przykładzie 1.
Jednak w tym przypadku parametr *VpnClientRootCertificateName* jest uwzględniany w celu ograniczenia zwracanych danych do określonego certyfikatu głównego: ContosoRootClientCertificate.

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

### -VirtualNetworkGatewayName
Określa nazwę bramy sieci wirtualnej, do której jest przypisany certyfikat główny.

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

### -VpnClientRootCertificateName
Określa nazwę certyfikatu głównego klienta, który otrzymuje to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## NOTATKI

## LINKI POKREWNE

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


