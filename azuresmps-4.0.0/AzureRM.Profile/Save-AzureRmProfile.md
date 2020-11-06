---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06a78584437021df570bc5ff2b6ec19e332bffd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523553"
---
# Save-AzureRmProfile

## STRESZCZENIe
Zapisuje bieżące informacje o uwierzytelnianiu do użycia w innych sesjach programu PowerShell.

## POLECENIA

```
Save-AzureRmProfile [[-Profile] <AzureRMProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet Save-AzureRmProfile zapisuje bieżące informacje o uwierzytelnianiu do użycia w innych sesjach programu PowerShell.

## Przykłady

### Przykład 1. zapisywanie bieżącego profilu sesji
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmProfile -Path C:\test.json
```

W tym przykładzie zapisywany jest profil platformy Azure bieżącej sesji w udostępnionym pliku JSON.

### Przykład 2: zapisanie określonego profilu
```
PS C:\> Save-AzureRmProfile -Profile (Add-AzureRmAccount) -Path C:\test.json
```

W tym przykładzie zapisywany jest profil platformy Azure przekazany do polecenia cmdlet do podanego pliku JSON.

## PARAMETRÓW

### -Force
Zastąpienie danego pliku, jeśli istnieje

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Określa ścieżkę pliku, do którego mają zostać zapisane informacje uwierzytelniające.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureRMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### PSAzureProfile

## INFORMACYJN

## LINKI POKREWNE

[Wybierz — AzureRMProfile]()

