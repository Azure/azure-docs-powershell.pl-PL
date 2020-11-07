---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: b4ab525623dd6bcb5aee57aeecf70ae36bdac380
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890929"
---
# Add-AzVpnClientRootCertificate

## STRESZCZENIe
Dodaje certyfikat główny klienta VPN.

## POLECENIA

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzVpnClientRootCertificate** dodaje certyfikat główny do bramy sieci wirtualnej.
Certyfikaty główne to certyfikaty X. 509, które identyfikują główny urząd certyfikacji.
Według projektu wszystkie certyfikaty używane w bramie ufają certyfikatowi głównemu.

To polecenie cmdlet przypisuje istniejący certyfikat jako certyfikat główny bramy.
Jeśli nie masz dostępnego certyfikatu X. 509, możesz wygenerować go za pośrednictwem infrastruktury klucza publicznego lub użyć generatora certyfikatów, takiego jak makecert.exe.

Aby dodać certyfikat główny, należy określić nazwę certyfikatu i przekazać reprezentację tylko tekstową certyfikatu (Aby uzyskać więcej informacji, zobacz parametr *PublicCertData* ).
Azure umożliwia przypisywanie więcej niż jednego certyfikatu głównego do bramy.
Wiele certyfikatów głównych jest często wdrażanych przez organizacje, które zawierają użytkowników z więcej niż jednej firmy.

## Przykłady

### Przykład 1: Dodawanie głównego certyfikatu klienta do bramy wirtualnej
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

W tym przykładzie jest dodawany certyfikat główny klienta do bramy wirtualnej o nazwie ContosoVirtualGateway.

W pierwszym poleceniu jest używane polecenie **Get-Content** , które pozwala uzyskać uprzednio wyeksportowaną reprezentację głównego certyfikatu głównego i przechowywać w nim dane tekstowe o zmiennej nazwie $Text.

Drugie polecenie używa pętli for w celu wyodrębnienia całego tekstu z wyjątkiem pierwszego wiersza i ostatniego wiersza.
Wyodrębniony tekst jest przechowywany w zmiennej o nazwie $CertificateText.

Trzecia komenda korzysta z tekstu przechowywanego w $CertificateText za pomocą polecenia cmdlet **Add-AzVpnClientRootCertificate** w celu dodania głównego certyfikatu do bramy.

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

### -PublicCertData
Określa tekstową reprezentację głównego certyfikatu do dodania.
Aby otrzymać reprezentację tekstową, wyeksportuj certyfikat w formacie CER (przy użyciu kodowania base64), a następnie otwórz wynikowy plik w edytorze tekstów.
Po wykonaniu tej czynności zostanie wyświetlony wynik podobny do następującego (Zauważ, że rzeczywista produkcja zawiera więcej niż jeden wiersz tekstu niż w skróconym przykładzie pokazany poniżej):

-----ROZPOCZYNAć certyfikat-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----koniec certyfikatu-----

PublicCertData składa się ze wszystkich linii między pierwszym wierszem (-----ROZPOCZYNAć certyfikat-----) oraz ostatniego wiersza (-----końcowy certyfikat-----) w pliku.
Możesz pobrać te dane za pomocą poleceń programu Windows PowerShell podobnych do tego: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do której przypisano certyfikat główny.

Grupy zasobów umożliwiają Kategoryzowanie elementów w celu uproszczenia zarządzania zapasami i ogólnego administrowania usługą Azure.

```yaml
Type: String
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
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnClientRootCertificateName
Określa nazwę certyfikatu głównego klienta, który jest dodawany przez to polecenie cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSVpnClientRootCertificate

## INFORMACYJN

## LINKI POKREWNE

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Nowe — AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


