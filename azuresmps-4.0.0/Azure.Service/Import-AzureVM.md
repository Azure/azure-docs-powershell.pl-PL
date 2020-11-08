---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7180CAC6-BFC1-4A18-A754-83D5F05C5BEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: c62c30558147bccd9cdecc73925b7e1a379d1c5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055221"
---
# Import-AzureVM

## STRESZCZENIe
Importuje stan maszyny wirtualnej platformy Azure z pliku.

## POLECENIA

```
Import-AzureVM [-Path] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Import-AzureVM** importuje wcześniej zapisany stan maszyny wirtualnej z pliku XML.
To polecenie cmdlet jest przydatne, gdy chcesz później utworzyć maszynę wirtualną na podstawie zaimportowanych danych.

Uruchomienie programu **Export-AzureVM** , a następnie polecenie **Remove-AzureVM** , a następnie polecenie **Import-AzureVM** w celu ponownego utworzenia maszyny wirtualnej może spowodować, że wynikowy komputer wirtualny będzie miał inny adres IP niż oryginalny.

## Przykłady

### Przykład 1: Importowanie stanu maszyny wirtualnej
```
PS C:\> Import-AzureVM -Path "C:\VMstate.xml" | New-AzureVM -ServiceName "ContosoService02"
```

To polecenie umożliwia zaimportowanie stanu maszyny wirtualnej z pliku VMstate.xml, a następnie utworzenie maszyny wirtualnej w określonej usłudze chmury.

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

### -Path
Określa ścieżkę pliku z wcześniej zapisanym stanem maszyny wirtualnej.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

[Eksportowanie — AzureVM](./Export-AzureVM.md)

[Nowe — AzureVM](./New-AzureVM.md)


