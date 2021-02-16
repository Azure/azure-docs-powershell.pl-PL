---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191834"
---
# New-AzVpnClientRootCertificate

## SYNOPSIS
Tworzy nowy certyfikat główny klienta sieci VPN.

## SKŁADNIA

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzVpnClientRootCertificate** tworzy nowy certyfikat główny VPN do użycia w wirtualnej bramie sieciowej.
Certyfikaty główne to certyfikaty X.509 identyfikujące główny urząd certyfikacji: wszystkie pozostałe certyfikaty używane w bramie są zaufanymi certyfikatami głównymi.
To polecenie cmdlet tworzy autonomiczny certyfikat, który nie jest przypisany do bramy wirtualnej.
Zamiast tego certyfikat utworzony przez **new-AzVpnClientRootCertificate** jest używany w połączeniu z poleceniem cmdlet New-AzVirtualNetworkGateway podczas tworzenia nowej bramy.
Załóżmy na przykład, że tworzysz nowy certyfikat i przechowujesz go w zmiennej o nazwie $Certificate.
Następnie można użyć tego obiektu certyfikatu podczas tworzenia nowej bramy wirtualnej.
Na przykład: `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`
Aby uzyskać więcej informacji, zapoznaj się z dokumentacją New-AzVirtualNetworkGateway cmdlet.

## PRZYKŁADY

### Przykład 1. Tworzenie certyfikatu głównego klienta
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

W tym przykładzie jest tworzenie certyfikatu głównego klienta i przechowywanie obiektu certyfikatu w zmiennej o nazwie $Certificate.
Ta zmienna może być następnie używana przez polecenie cmdlet **New-AzVirtualNetworkGateway** w celu dodania certyfikatu głównego do nowej bramy sieci wirtualnej.
Pierwsze polecenie używa polecenia cmdlet **Get-Content** w celu uzyskania poprzednio wyeksportowanej tekstowej reprezentacji certyfikatu głównego. że dane tekstowe są przechowywane w zmiennej o nazwie $Text.
Drugie polecenie używa pętli w celu wyodrębnienia całego tekstu z wyjątkiem pierwszego i ostatniego wiersza, zapisując wyodrębniony tekst w zmiennej o nazwie $CertificateText.
Trzecie polecenie tworzy certyfikat za pomocą polecenia cmdlet **New-AzVpnClientRootCertificate,** przechowując utworzony obiekt w zmiennej o nazwie $Certificate.

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
Określa nazwę nowego certyfikatu głównego klienta.

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

### -PublicCertData
Określa tekstową reprezentację certyfikatu głównego do dodania.
Aby uzyskać reprezentację tekstową, wyeksportuj certyfikat w formacie cer (przy użyciu kodowania Base64), a następnie otwórz wynikowy plik w edytorze tekstów.
Dane wyjściowe powinny być podobne do przedstawionego (należy zauważyć, że rzeczywiste dane wyjściowe będą zawierać o wiele więcej wierszy tekstu niż przedstawiono w przykładzie skróconym): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHGUNEW8343NMJk Certyfikat końcowy -----CVVFAw8w ----- ----- Dane PublicCertData składa się ze wszystkich wierszy między pierwszym wierszem (----- BEGIN CERTIFICATE -----) a ostatnim wierszem (----- END CERTIFICATE -----) w pliku.
Można pobrać dane PublicCertData, używając poleceń programu Windows PowerShell podobnych do tych: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## NOTATKI

## LINKI POKREWNE

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


