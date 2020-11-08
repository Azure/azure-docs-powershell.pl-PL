---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054503"
---
# Get-AzureSubscription

## STRESZCZENIe
Pobiera subskrypcje platformy Azure na koncie platformy Azure.

## POLECENIA

### ByName (domyślny)
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ById
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Domyślne
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Bieżącą
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureSubscription** pobiera abonamenty na koncie platformy Azure.
Za pomocą tego polecenia cmdlet możesz uzyskać informacje o subskrypcji i potoku abonamentu do innych poleceń cmdlet.

**Get-AzureSubscription** wymaga dostępu do kont platformy Azure.
Przed uruchomieniem polecenia **Get-AzureSubscription** należy uruchomić polecenie cmdlet **Add-AzureAccount** lub polecenia cmdlet, które pobierają i instalują plik ustawień publikowania ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.

W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

## Przykłady

### Przykład 1: Uzyskaj wszystkie subskrypcje
```
C:\PS>Get-AzureSubscription
```

To polecenie pobiera wszystkie subskrypcje na koncie.

### Przykład 2: Uzyskaj abonament według imienia i nazwiska
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

To polecenie pobiera tylko subskrypcję "MyProdSubsciption".

### Przykład 3: Uzyskaj abonament domyślny
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

To polecenie pobiera tylko nazwę subskrypcji domyślnej.
Polecenie najpierw pobiera subskrypcję, a następnie używa metody z kropką do uzyskania właściwości **abonamentname** subskrypcji.

### Przykład 4: uzyskiwanie wybranych właściwości subskrypcji
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

To polecenie zwraca listę z nazwą i certyfikatem bieżącej subskrypcji.
W celu uzyskania bieżącego abonamentu jest używane polecenie **Get-AzureSubscription** .
Następnie przekazuje abonament na polecenie **list format** , które wyświetla zaznaczone właściwości na liście.

### Przykład 5: używanie alternatywnego pliku danych subskrypcji
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

To polecenie pobiera abonamenty z pliku danych abonamentu C:\Temp\MySubscriptions.xml.
Użyj parametru **SubscriptionDataFile** , jeśli po uruchomieniu polecenia cmdlet **Add-AzureAccount** lub **Import-PublishSettingsFile** zostaną określone alternatywne pliki danych subskrypcji.

## PARAMETRÓW

### -Bieżące
Pobiera tylko bieżący abonament, czyli abonament oznaczony jako "bieżący". Domyślnie polecenie **Get-AzureSubscription** pobiera wszystkie subskrypcje na kontach platformy Azure.
Aby wyznaczyć abonament jako bieżący, użyj **bieżącego** parametru polecenia cmdlet **SELECT-AzureSubscription** .

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Wartość domyślna
Pobiera tylko domyślny abonament, czyli abonament oznaczony jako "domyślny". Domyślnie polecenie **Get-AzureSubscription** pobiera wszystkie subskrypcje na kontach platformy Azure.
Aby wyznaczyć abonament jako "domyślny", użyj **domyślnego** parametru polecenia cmdlet **SELECT-AzureSubscription** .

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtendedDetails
Zwraca informacje o przydziałach dla subskrypcji oprócz ustawień standardowych.

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

### -Subskrypcji
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subscriptionname
Pobiera tylko określoną subskrypcję.
Wprowadź nazwę subskrypcji.
W tej wartości uwzględniana jest wielkość liter.
Symbole wieloznaczne nie są obsługiwane.
Domyślnie polecenie **Get-AzureSubscription** pobiera wszystkie subskrypcje na kontach platformy Azure.

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
Możesz popotokować dane wejściowe dla właściwości **abonamentname** według nazwy, ale nie według wartości.

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Utilities. Common. WindowsAzureSubscription

## INFORMACYJN
* Get-AzureSubscription pobiera dane z pliku danych subskrypcji, które zostaną utworzone przez polecenia cmdlet **Add-AzureAccount** i **Import-PublishSettingsFile** .

## LINKI POKREWNE

[Dodaj-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[Import — AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureSubscription](./Remove-AzureSubscription.md)

[Set-AzureSubscription](./Set-AzureSubscription.md)


