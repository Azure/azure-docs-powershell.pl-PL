---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522685"
---
# Save-AzureRmContext

## STRESZCZENIe
Zapisuje bieżące informacje o uwierzytelnianiu do użycia w innych sesjach programu PowerShell.

## POLECENIA

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## Opis
Polecenie cmdlet Save-AzureRmContext zapisuje bieżące informacje o uwierzytelnianiu do użycia w innych sesjach programu PowerShell.

## Przykłady

### Przykład 1. zapisywanie kontekstu bieżącej sesji
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

W tym przykładzie zapisywany jest kontekst platformy Azure bieżącej sesji w udostępnionym pliku JSON.

### Przykład 2: zapisanie określonego kontekstu
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

W tym przykładzie zapisywany jest kontekst platformy Azure przekazany do polecenia cmdlet do dostarczonego pliku JSON.

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
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa kontekst platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie określisz kontekstu, to polecenie cmdlet odczytuje dane z lokalnego kontekstu domyślnego.

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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

## WEJŚCIOWE

### Microsoft. Azure. Commands. Common. Authentication. models. AzureRMProfile

## WYSYŁA

### Microsoft. Azure. Commands. profile. PSAzureProfile

## INFORMACYJN

## LINKI POKREWNE

