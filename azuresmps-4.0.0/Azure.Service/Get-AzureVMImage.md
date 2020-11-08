---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055498"
---
# Get-AzureVMImage

## STRESZCZENIe
Pobiera właściwości jednej lub listy systemów operacyjnych lub obrazów maszyny wirtualnej w repozytorium obrazów.

## POLECENIA

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureVMImage** pobiera właściwości jednej lub listy systemów operacyjnych lub obrazów maszyny wirtualnej w repozytorium obrazów.
Polecenie cmdlet zwraca informacje dotyczące wszystkich obrazów w repozytorium lub informacje o określonym obrazie, jeśli jego nazwa obrazu jest podana.

## Przykłady

### Przykład 1: uzyskiwanie określonego obiektu obrazu z bieżącego repozytorium obrazów.
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

To polecenie pobiera obiekt obrazu o nazwie Image001 z bieżącego repozytorium obrazów.

### Przykład 2: pobieranie wszystkich obrazów z bieżącego repozytorium obrazów
```
PS C:\> Get-AzureVMImage
```

To polecenie pobiera wszystkie obrazy z bieżącego repozytorium obrazów.

### Przykład 3: Ustawianie kontekstu subskrypcji, a następnie uzyskiwanie wszystkich obrazów
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

To polecenie ustawia kontekst abonamentu, a następnie pobiera wszystkie obrazy z repozytorium obrazów.

## PARAMETRÓW

### -ImageName
Określa nazwę obrazu systemu operacyjnego lub maszyny wirtualnej w repozytorium obrazów.
Jeśli nie podano tego parametru, zostaną zwrócone wszystkie obrazy.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureVMImage](./Add-AzureVMImage.md)

[Remove-AzureVMImage](./Remove-AzureVMImage.md)

[Zapisz — AzureVMImage](./Save-AzureVMImage.md)

[Update-AzureVMImage](./Update-AzureVMImage.md)


