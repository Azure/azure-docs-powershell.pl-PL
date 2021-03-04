---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: 38a6abb631a77d41e38026edd3bef5abe9c70c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979658"
---
# Add-AzVpnClientRootCertificate

## SYNOPSIS
Dodaje certyfikat główny klienta sieci VPN.

## SKŁADNIA

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Add-AzVpnClientRootCertificate** dodaje certyfikat główny do bramy sieci wirtualnej.
Certyfikaty główne to certyfikaty X.509, które identyfikują główny urząd certyfikacji.
Domyślnie wszystkie certyfikaty używane w bramie są zaufane dla certyfikatu głównego.
To polecenie cmdlet przypisuje istniejący certyfikat jako certyfikat główny bramy.
Jeśli certyfikat X.509 nie jest dostępny, można go wygenerować za pośrednictwem infrastruktury kluczy publicznych lub użyć generatora certyfikatów, takiego jak makecert.exe.
Aby dodać certyfikat główny, musisz określić nazwę certyfikatu i podać tylko tekstową reprezentację certyfikatu (aby uzyskać więcej informacji, zobacz parametr *PublicCertData).*
Platforma Azure umożliwia przypisanie więcej niż jednego certyfikatu głównego do bramy.
Wiele certyfikatów głównych jest często wdrażanych przez organizacje, które zawierają użytkowników z więcej niż jednej firmy.

## PRZYKŁADY

### Przykład 1. Dodawanie certyfikatu głównego klienta do bramy wirtualnej
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

W tym przykładzie do bramy wirtualnej jest dodano certyfikat główny klienta o nazwie ContosoVirtualGateway.
Pierwsze polecenie używa polecenia cmdlet **Get-Content** w celu uzyskania poprzednio wyeksportowanej reprezentacji tekstowej certyfikatu głównego i przechowuje te dane tekstowe zmiennej o nazwie $Text.
Drugie polecenie używa pętli w celu wyodrębnienia całego tekstu z wyjątkiem pierwszego i ostatniego wiersza.
Wyodrębniony tekst jest przechowywany w zmiennej o nazwie $CertificateText.
Trzecie polecenie użyje następnie tekstu przechowywanego w programie $CertificateText z poleceniem cmdlet **Add-AzVpnClientRootCertificate** w celu dodania certyfikatu głównego do bramy.

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

### -PublicCertData
Określa tekstową reprezentację certyfikatu głównego do dodania.
Aby uzyskać reprezentację tekstową, wyeksportuj certyfikat w formacie cer (przy użyciu kodowania Base64), a następnie otwórz wynikowy plik w edytorze tekstów.
W tym przypadku dane wyjściowe będą podobne do poniższych (zwróć uwagę, że rzeczywiste dane wyjściowe będą zawierać o wiele więcej wierszy tekstu niż przedstawiono w przykładzie skróconym): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHGUNEW8343NM Certyfikat KOŃCOWY ----- PublicCertData Jklo09982CVVFAw8w ----- -----. Dane PublicCertData składa się ze wszystkich wierszy między pierwszym wierszem (----- BEGIN CERTIFICATE -----) ----- ostatnim wierszem (----- END CERTIFICATE -----) w pliku.
Te dane można pobrać przy użyciu poleceń programu Windows PowerShell podobnych do tych: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`

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

### -ResourceGroupName
Określa nazwę grupy zasobów, do których jest przypisany certyfikat główny.
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
Określa nazwę bramy sieci wirtualnej, do której został dodany certyfikat.

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
Określa nazwę certyfikatu głównego klienta, który dodaje to polecenie cmdlet.

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

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## NOTATKI

## LINKI POKREWNE

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


