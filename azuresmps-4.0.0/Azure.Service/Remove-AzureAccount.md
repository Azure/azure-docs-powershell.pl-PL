---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054836"
---
# Remove-AzureAccount

## STRESZCZENIe
Usuwa konto platformy Azure z programu Windows PowerShell.

## POLECENIA

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureAccount** usuwa konto platformy Azure i jego subskrypcje z pliku danych subskrypcji w profilu użytkownika mobilnego.
Nie powoduje usunięcia konta z platformy Microsoft Azure ani zmiany rzeczywistego konta w jakikolwiek sposób.

Korzystanie z tego polecenia cmdlet jest bardzo podobne do logowania się z konta platformy Azure.
Aby ponownie zalogować się do konta, użyj apletu **Add-AzureAccount** lub **Import-AzurePublishSettingsFile** w celu ponownego dodania konta do programu Windows PowerShell.

Możesz również użyć polecenia cmdlet **Remove-AzureAccount** , aby zmienić sposób, w jaki polecenia cmdlet programu Azure PowerShell będą się podpisywać do konta platformy Azure.
Jeśli konto ma certyfikat administracyjny z **Import-AzurePublishSettingsFile** i token dostępu z **dodatku Add-AzureAccount** , polecenia cmdlet programu Azure PowerShell używają tylko tokena dostępu. zignorują one certyfikat zarządzania.
Aby użyć certyfikatu zarządzania, uruchom polecenie **Remove-AzureAccount**.
Gdy element **Remove-AzureAccount** odnajdzie certyfikat zarządzania i token dostępu, usuwa tylko token dostępu, zamiast usuwać konto.
Certyfikat zarządzania jest nadal dostępny, więc konto jest nadal dostępne dla programu Windows PowerShell.

W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

## Przykłady

### Przykład 1. Usuń konto
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

To polecenie usuwa admin@contoso.com z pliku danych subskrypcji.
Po zakończeniu polecenia konto nie jest już dostępne w programie Windows PowerShell.

## PARAMETRÓW

### -Force
Pomija monit o potwierdzenie.
Domyślnie polecenie **Remove-AzureAccount** wyświetla monit przed usunięciem konta z programu Windows PowerShell.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę konta, które ma zostać usunięte.
W wartości parametru jest uwzględniana wielkość liter.
Symbole wieloznaczne nie są obsługiwane.

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

### -PassThru
Zwraca wartość $True, jeśli wykonanie polecenia powiedzie się i $False, jeśli nie powiodło się.
Domyślnie to polecenie cmdlet nie zwraca żadnych danych wyjściowych.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.

## WYSYŁA

### Brak lub system. Boolean
W przypadku użycia parametru *PassThru* to polecenie cmdlet zwraca wartość logiczną.
W przeciwnym razie nie zwróci żadnych danych wyjściowych.

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureAccount](./Add-AzureAccount.md)

[Get-AzureAccount](./Get-AzureAccount.md)


