---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 35588231-CBAC-4411-9531-9A06BD298ACA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7fdcad4b3a0f41f0589e49d4b33a767b93267855
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054514"
---
# Get-AzureStorageKey

## STRESZCZENIe
Zwraca klucze konta podstawowego i pomocniczego magazynu dla konta usługi Azure Storage.

## POLECENIA

```
Get-AzureStorageKey [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureStorageKey** zwraca obiekt o nazwie konta usługi Azure Storage, podstawowym kluczu konta oraz kluczu konta pomocniczego określonego konta usługi Azure Storage jako właściwości.

## Przykłady

### Przykład 1: uzyskiwanie obiektu zawierającego klucze magazynu podstawowego i pomocniczego
```
PS C:\> Get-AzureStorageKey -StorageAccountName "ContosoStore01"
```

To polecenie pobiera obiekt z podstawowym i pomocniczym kluczem magazynu dla konta magazynu usługi ContosoStore01.

### Przykład 2: Uzyskiwanie klucza podstawowego konta magazynu i przechowywanie go w zmiennej
```
PS C:\> $ContosoStoreKey = (Get-AzureStorageKey -StorageAccountName "ContosoStore01").Primary
```

To polecenie powoduje umieszczenie klucza podstawowego konta magazynu dla konta magazynu ContosoStore01 w zmiennej $ContosoStoreKey.

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

### -StorageAccountName
Określa nazwę konta magazynu.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN
* Aby uzyskać pomoc dotyczącą Node.js, użyj `help node-dev` polecenia. Aby uzyskać pomoc dotyczącą rozszerzeń PHP, użyj `help php-dev` polecenia.

## LINKI POKREWNE

[Get-AzureStorageAccount](./Get-AzureStorageAccount.md)

[Nowe — AzureStorageAccount](./New-AzureStorageAccount.md)

[Nowe — AzureStorageKey](./New-AzureStorageKey.md)

[Remove-AzureStorageAccount](./Remove-AzureStorageAccount.md)

[Set-AzureStorageAccount](./Set-AzureStorageAccount.md)


