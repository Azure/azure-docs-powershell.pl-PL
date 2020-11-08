---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E3D405D-69FB-42C2-8A5B-BDBD27B63088
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503c2e0a076be3f31b6435a30dc658af9b45835a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055133"
---
# Remove-AzureCertificate

## STRESZCZENIe
Usuwa certyfikat z usługi platformy Azure.

## POLECENIA

```
Remove-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureCertificate** usuwa certyfikat z usługi platformy Azure.

## Przykłady

### Przykład 1: Usuwanie certyfikatu z usługi
```
PS C:\> Remove-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

To polecenie umożliwia usunięcie obiektu certyfikatu z określonym odciskiem palca z usługi w chmurze.

### Przykład 2: Usuwanie wszystkich certyfikatów z usługi
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" | Remove-AzureCertificate
```

To polecenie pobiera wszystkie certyfikaty z usługi o nazwie ContosoService przy użyciu polecenia cmdlet **Get-AzureCertificate** .
Polecenie przekazuje poszczególne certyfikaty do bieżącego polecenia cmdlet za pomocą operatora potoku.
Polecenie cmdlet powoduje usunięcie każdego certyfikatu z usługi w chmurze.

### Przykład 3: Usuwanie wszystkich certyfikatów z usługi, która używa konkretnego algorytmu odcisku palca
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" -ThumbprintAlgorithm "sha1" | Remove-AzureCertificate
```

To polecenie pobiera wszystkie certyfikaty z usługi o nazwie ContosoService, które używają algorytmu odcisku palca SHA1.
Polecenie przekazuje poszczególne certyfikaty do bieżącego polecenia cmdlet, które usuwa każdy certyfikat.

## PARAMETRÓW

### -InformationAction
Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.

Dopuszczalne wartości tego parametru to:

- Kontynuacj
- Ignorować
- Inquire
- SilentlyContinue
- Przestaw
- Wykonywanie

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Określa zmienną informacyjną.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

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

### -ServiceName
Określa nazwę usługi platformy Azure, z której to polecenie cmdlet usuwa certyfikat.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Odcisk palca
Określa odcisk palca certyfikatu usuniętego przez ten aplet polecenia.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ThumbprintAlgorithm
Określa algorytm używany do tworzenia odcisku palca certyfikatu.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### ManagementOperationContext

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureCertificate](./Add-AzureCertificate.md)

[Get-AzureCertificate](./Get-AzureCertificate.md)

[Nowe — AzureCertificateSetting](./New-AzureCertificateSetting.md)


