---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D866554F-78B0-4691-BA06-F625F9B0DFC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 366941504c020910735015e3d8b282af376d54d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054843"
---
# Publish-AzureWebsiteProject

## STRESZCZENIe
Publikowanie projektu programu Visual Studio w sieci Web w witrynie usługi Microsoft Azure w sieci Web za pomocą aplikacji webdeploy.

## POLECENIA

### ProjectFile
```
Publish-AzureWebsiteProject -ProjectFile <String> [-Configuration <String>] [-ConnectionString <Hashtable>]
 [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Pakietu
```
Publish-AzureWebsiteProject -Package <String> [-ConnectionString <Hashtable>] [-Tokens <String>]
 [-SetParametersFile <String>] [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Publikowanie projektu programu Visual Studio w sieci Web w witrynie usługi Microsoft Azure w sieci Web za pomocą aplikacji webdeploy.
Może wykonać pakiet webdeploy i opublikować go bezpośrednio albo utworzyć projekt w sieci Web programu Visual Studio, zbudować projekt i publikować.
Może także zastąpić parametry połączenia w Web.config podczas publikowania.

## Przykłady

### Przykład 1
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -Configuration Debug
```

Tworzenie projektu programu Visual Studio w sieci Web z konfiguracją "Debugowanie" (oznacza używanie Web.Debug.config) i publikowanie w witrynie Microsoft Azure w sieci Web za pomocą aplikacji webdeploy.

### Przykład 2
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1.zip
```

Publikowanie pliku. zip pakietu webdeploy w witrynie sieci Web platformy Microsoft Azure za pomocą aplikacji webdeploy.

### Przykład 3
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1
```

Publikowanie folderu pakietu webdeploy w witrynie sieci Web platformy Microsoft Azure za pomocą aplikacji webdeploy.

### Przykład 4
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -ConnectionString @{ DefaultConnection = "my connection string" }
```

Utwórz projekt programu Visual Studio w sieci Web, Zastąp ciąg połączenia "DefaultConnection" w Web.config i opublikuj go w witrynie sieci Web platformy Microsoft Azure za pomocą narzędzia webdeploy.

### Przykład 5
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -DefaultConnection "my connection string"
```

Utwórz projekt programu Visual Studio w sieci Web, Zastąp ciąg połączenia "DefaultConnection" w Web.config i opublikuj go w witrynie sieci Web platformy Microsoft Azure za pomocą narzędzia webdeploy.
Zwróć uwagę, że DefaultConnection jest parametrem dynamicznym, który zostanie dodany przez przeanalizowanie Web.config.

## PARAMETRÓW

### — Konfiguracja
Konfiguracja używana do konstruowania projektu aplikacji sieci Web programu Visual Studio.

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConnectionString
Parametry połączenia używane do wdrożenia.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DoNotDelete
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

### -Package
Folder pakietu webdeploy na potrzeby publikowania pliku zip projektu aplikacji sieci Web programu Visual Studio.

```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: True
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

### -ProjectFile
Projekt aplikacji sieci Web Visual Studio, który ma zostać opublikowany.

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SetParametersFile
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipAppData
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

### -Slot
Nazwa miejsca w witrynie sieci Web.

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

### -Tokens
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
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

[Set-AzureWebsite](./Set-AzureWebsite.md)


