---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 768eff2dda32c6dfa0bad14f028338d3c5fa1abd
ms.sourcegitcommit: 87730c7ea4f98f628d3fe1b40aa4a9d2885e1c75
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/12/2021
ms.locfileid: "98110482"
---
# New-AzureWebsite

## STRESZCZENIe
Utwórz nową witrynę sieci Web do uruchamiania na platformie Azure.

## POLECENIA

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GitHubCredentials <PSCredential>] [-GitHubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet tworzy nową witrynę sieci Web do uruchamiania na platformie Azure i przygotowywanie jej do wdrożenia za pośrednictwem usługi GitHub.

## Przykłady

### Przykład 1. Tworzenie nowej witryny sieci Web przy użyciu narzędzia Git
```
PS C:\> New-AzureWebsite mySite -Git
```

W tym przykładzie jest tworzona nowa witryna sieci Web na platformie Azure oraz lokalne repozytorium git używane do wdrażania plików w nowej witrynie sieci Web.

### Przykład 2: Tworzenie witryny sieci Web zintegrowanej z usługą GitHub
```
PS C:\> New-AzureWebsite mysite -GitHub -GitHubRepository myaccount/myrepo
```

W tym przykładzie jest tworzona nowa witryna sieci Web połączona z repozytorium GitHub o nazwie Moje konto/moje repozytorium.
Zatwierdzanie repozytorium GitHub jest przekazywane do witryny sieci Web na platformie Azure.

## PARAMETRÓW

### -Git
Konfiguruje lokalne repozytorium git i łączy je z witryną internetową.
W przypadku określenia tego parametru ten parametr konfiguruje repozytorium Git w katalogu lokalnym i dodanie repozytorium zdalnego o nazwie "Azure" połączonego z witryną internetową na platformie Azure.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHub
Wskazuje, że to polecenie cmdlet łączy nową witrynę sieci Web z istniejącym repozytorium GitHub.
Zatwierdzanie repozytorium Giuthub jest przekazywane do witryny sieci Web na platformie Azure.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHubCredentials
Określa poświadczenia nazwy użytkownika i hasła w celu nawiązania połączenia z usługą GitHub.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHubRepository
Określa pełną nazwę repozytorium GitHub, które ma zostać połączone z tą witryną internetową.
Na przykład `myaccount/myrepo` .

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

### -Hostname
Określa alternatywną nazwę hosta dla nowej witryny sieci Web.

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

### — Lokalizacja
Określa lokalizację centrum danych, w którym ma zostać wdrożona witryna sieci Web.

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

### -Name (nazwa)
Określa nazwę witryny sieci Web.

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

### -PublishingUsername
Określa nazwę użytkownika określoną w portalu Azure dla wdrożenia git.

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

### -Slot
Określa nazwę gniazda witryny sieci Web.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Set-AzureWebsite](./Set-AzureWebsite.md)


