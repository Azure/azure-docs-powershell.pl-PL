---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055295"
---
# Get-AzureRemoteAppCollection

## STRESZCZENIe
Pobiera informacje o kolekcji funkcji Azure RemoteApp.

## POLECENIA

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRemoteAppCollection** pobiera informacje o kolekcjach funkcji Azure RemoteApp na platformie Microsoft Azure.
Zwraca obiekt z informacją dotyczącą określonej kolekcji lub, jeśli kolekcja nie jest określona, dla wszystkich kolekcji w bieżącej subskrypcji.

## Przykłady

### Przykład 1: Pobieranie listy wszystkich kolekcji
```
PS C:\> Get-AzureRemoteAppCollection
```

To polecenie zwraca listę wszystkich kolekcji funkcji RemoteApp w usłudze Azure w ramach subskrypcji.

### Przykład 2: uzyskiwanie informacji o określonej kolekcji
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

To polecenie zwraca informacje o kolekcji funkcji Azure RemoteApp o nazwie ContosoApps.

### Przykład 3: Pobieranie listy kolekcji przy użyciu symboli wieloznacznych
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

To polecenie zwraca listę wszystkich funkcji finansowych dopasowania kolekcji usługi Azure RemoteApp *.

## PARAMETRÓW

### -CollectionName
Określa nazwę kolekcji funkcji Azure RemoteApp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

[Nowe — AzureRemoteAppCollection](./New-AzureRemoteAppCollection.md)

[Remove-AzureRemoteAppCollection](./Remove-AzureRemoteAppCollection.md)

[Set-AzureRemoteAppCollection](./Set-AzureRemoteAppCollection.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


