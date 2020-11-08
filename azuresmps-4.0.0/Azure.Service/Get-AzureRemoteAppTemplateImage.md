---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055545"
---
# Get-AzureRemoteAppTemplateImage

## STRESZCZENIe
Pobiera informacje o obrazach szablonów usługi Azure RemoteApp.

## POLECENIA

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRemoteAppTemplateImage** pobiera informacje o obrazach szablonów usługi Azure RemoteApp na platformie Microsoft Azure.
To polecenie cmdlet zwraca obiekt zawierający informacje o określonym obrazie szablonu.
Jeśli nie określono żadnego obrazu szablonu, pobiera on informacje o wszystkich obrazach szablonów w bieżącej subskrypcji.

## Przykłady

### Przykład 1. Pobieranie listy wszystkich obrazów szablonów
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

To polecenie zwraca listę wszystkich obrazów szablonów.

### Przykład 2: uzyskiwanie informacji o określonym obrazie szablonu
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

To polecenie pobiera informacje o obrazie szablonu o nazwie ContosoApps.

## PARAMETRÓW

### -ImageName
Określa nazwę obrazu szablonu usługi Azure RemoteApp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
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

[Get-AzureRemoteAppCollection](./Get-AzureRemoteAppCollection.md)

[Get-AzureRemoteAppStartMenuProgram](./Get-AzureRemoteAppStartMenuProgram.md)


