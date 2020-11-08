---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BFB57100-93F6-4FD2-8ECA-7F54BEB0D6B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7114f39ee2b105c80429151df8347b5c17dcfea0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055472"
---
# Get-AzureWebsiteLog

## STRESZCZENIe
Pobiera dzienniki określonej witryny sieci Web.

## POLECENIA

### Ogonkiem
```
Get-AzureWebsiteLog [-Path <String>] [-Message <String>] [-Tail] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ListPath
```
Get-AzureWebsiteLog [-ListPath] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Pobiera dziennik dla określonej witryny sieci Web.

## Przykłady

### Przykład 1: Rozpoczynanie przesyłania strumieniowego dziennika
```
PS C:\> Get-AzureWebsiteLog -Tail
```

W tym przykładzie rozpoczęto przesyłanie strumieniowe dziennika dla wszystkich dzienników aplikacji.

### Przykład 2: Rozpoczynanie przesyłania strumieniowego dziennika dla dzienników http
```
PS C:\> Get-AzureWebsiteLog -Tail -Path http
```

W tym przykładzie Rozpoczynanie przesyłania strumieniowego dziennika dla dzienników http.

### Przykład 3: Rozpoczynanie przesyłania strumieniowego dziennika dla dzienników błędów
```
PS C:\> Get-AzureWebsiteLog -Tail -Message Error
```

W tym przykładzie Rozpoczynanie przesyłania strumieniowego dziennika i wyświetlanie tylko dzienników błędów.

### Przykład 4: Wyświetlanie dzienników avaiable
```
PS C:\> Get-AzureWebsiteLog -Name MyWebsite -ListPath
```

W tym przykładzie są wyświetlane wszystkie dostępne ścieżki dziennika w witrynie sieci Web.

## PARAMETRÓW

### -ListPath
Wskazuje, czy mają być wystawiane ścieżki dziennika.

```yaml
Type: SwitchParameter
Parameter Sets: ListPath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Message
Określa ciąg znaków, który zostanie zastosowany do filtrowania komunikatu dziennika.
Zostaną pobrane tylko dzienniki zawierające ten ciąg.

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa witryny sieci Web.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Ścieżka, z której ma zostać pobrany dziennik.
Domyślnie jest to element główny, co oznacza, że obejmuje wszystkie ścieżki.

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Slot
Określa nazwę gniazda.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Koniec
Określa, czy mają być przesyłane strumieniowo dzienniki.

```yaml
Type: SwitchParameter
Parameter Sets: Tail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureWebsite](./Get-AzureWebsite.md)

[Nowe — AzureWebsite](./New-AzureWebsite.md)

[Remove-AzureWebsite](./Remove-AzureWebsite.md)

[Start — AzureWebsite](./Start-AzureWebsite.md)


