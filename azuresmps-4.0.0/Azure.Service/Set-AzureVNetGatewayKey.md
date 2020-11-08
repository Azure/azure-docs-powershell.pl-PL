---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1AB168AA-F466-4C7C-9AD7-0BC7AEEBC932
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8daca2a335f063264fb2e6734948cc1353946e8a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054776"
---
# Set-AzureVNetGatewayKey

## STRESZCZENIe
Ustawia klucz wstępny dla połączenia między bramą sieci VPN platformy Azure a lokacją sieci lokalnej.

## POLECENIA

```
Set-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureVNetGatewayKey** ustawia klucz wstępny dla połączenia między bramą wirtualnej sieci prywatnej (VPN) a lokalną lokacją sieci lokalnej.
Klucz musi być równy kluczowi skonfigurowanemu w bramie lokalnej sieci.
Jeśli te klucze nie pasują do siebie, połączenie nie może nawiązać połączenia.

## Przykłady

## PARAMETRÓW

### -LocalNetworkSiteName
Określa nazwę lokacji sieci lokalnej łączącej się z bramą sieci wirtualnej.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet. Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharedKey
Określa klucz udostępniony, który ma zostać przypisany do bramy sieci VPN.
Wartość musi być ciągiem numerycznym o wartości alfanumerycznej, który nie przekracza 128 znaków.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
Określa sieć wirtualną, za pomocą której to polecenie cmdlet ustawia klucz udostępniony dla połączenia.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureVNetGatewayKey](./Get-AzureVNetGatewayKey.md)


