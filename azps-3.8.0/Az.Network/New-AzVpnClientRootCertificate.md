---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052176"
---
# New-AzVpnClientRootCertificate

## STRESZCZENIe
Tworzy nowy certyfikat główny klienta sieci VPN.

## POLECENIA

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzVpnClientRootCertificate** tworzy nowy certyfikat główny sieci VPN do użytku w bramie sieci wirtualnej.
Certyfikaty główne to certyfikaty X. 509, które identyfikują główny urząd certyfikacji: wszystkie inne certyfikaty używane w bramie ufają certyfikatowi głównemu.
To polecenie cmdlet tworzy autonomiczny certyfikat, który nie jest przypisany do bramy wirtualnej.
Zamiast tego certyfikat utworzony za pomocą polecenia **New-AzVpnClientRootCertificate** jest wykorzystywany w połączeniu z poleceniem cmdlet New-AzVirtualNetworkGateway podczas tworzenia nowej bramy.
Załóżmy na przykład, że tworzysz nowy certyfikat i zapisujesz go w zmiennej o nazwie $Certificate.
Po utworzeniu nowej bramy wirtualnej można użyć tego obiektu certyfikatu.
Na przykład `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`
Aby uzyskać więcej informacji, zobacz dokumentację New-AzVirtualNetworkGateway polecenia cmdlet.

## Przykłady

### Przykład 1. Tworzenie głównego certyfikatu klienta
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

W tym przykładzie przedstawiono Tworzenie certyfikatu głównego klienta i przechowywanie obiektu Certificate w zmiennej o nazwie $Certificate.
Ta zmienna może być następnie używana przez polecenie cmdlet **New-AzVirtualNetworkGateway** w celu dodania certyfikatu głównego do nowej bramy sieci wirtualnej.
W pierwszym poleceniu jest używane polecenie **Get-Content** , aby uzyskać uprzednio wyeksportowany tekst reprezentujący certyfikat główny. dane tekstowe są przechowywane w zmiennej o nazwie $Text.
Drugie polecenie używa pętli for w celu wyodrębnienia całego tekstu z wyjątkiem pierwszego wiersza i ostatniego wiersza, przechowując wyodrębniony tekst w zmiennej o nazwie $CertificateText.
W trzecim poleceniu użyto polecenia cmdlet **New-AzVpnClientRootCertificate** , aby utworzyć certyfikat, przechowując utworzony obiekt w zmiennej o nazwie $Certificate.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Name (nazwa)
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
Określa tekstową reprezentację głównego certyfikatu do dodania.
Aby otrzymać reprezentację tekstową, wyeksportuj certyfikat w formacie CER (przy użyciu kodowania base64), a następnie otwórz wynikowy plik w edytorze tekstów.
Powinno być wyświetlane dane wyjściowe podobne do tego (Zauważ, że rzeczywista produkcja zawiera więcej niż jeden wiersz tekstu niż skrót skrócony):-----ROZPOCZYNAć certyfikat-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----Kończenie certyfikatu-----PublicCertData składa się ze wszystkich wierszy między pierwszym wierszem (-----Rozpocznij certyfikat-----) i ostatnim wierszem (----------końcowego certyfikatu) w pliku.
Możesz pobrać PublicCertData, używając poleceń środowiska Windows PowerShell podobnych do tego: $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSVpnClientRootCertificate

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


