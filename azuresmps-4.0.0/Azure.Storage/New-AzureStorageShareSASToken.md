---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: ''
schema: 2.0.0
ms.openlocfilehash: 427276a496108a48b69fd81cb5835d74859c25b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523565"
---
# New-AzureStorageShareSASToken

## STRESZCZENIe
Wygeneruj token podpisu dostępu współdzielonego dla udziału magazynu platformy Azure.

## POLECENIA

### SasPolicy
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### SasPermission
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureStorageShareSASToken** generuje token podpisu dostępu współdzielonego dla udziału w usłudze Azure Storage.

## Przykłady

### Przykład 1. Wygeneruj token podpisu dostępu współdzielonego dla udziału
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

To polecenie tworzy token podpisu dostępu współdzielonego dla udziału o nazwie ContosoShare.

### Przykład 2: generowanie wielu tokenów podpisu dostępu współdzielonego za pomocą potoku
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

To polecenie pobiera wszystkie udziały w magazynie, które pasują do testu prefiksu.
Polecenie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.
Bieżące polecenie cmdlet tworzy token dostępu współdzielonego dla każdego udziału miejsca do magazynowania, który ma określone uprawnienia.

### Przykład 3: generowanie tokenu podpisu z dostępem udostępnionym korzystającym z zasad dostępu współużytkowanego
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

To polecenie tworzy token podpisu dostępu współdzielonego dla udziału magazynu o nazwie ContosoShare, który zawiera zasady o nazwie ContosoPolicy03.

## PARAMETRÓW

### -Context
Określa kontekst usługi Azure Storage.
Aby uzyskać kontekst, użyj polecenia cmdlet New-AzureStorageContext.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ExpiryTime
Określa czas, po upływie którego podpis udostępniony jest nieprawidłowy.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullUri
Wskazuje, że to polecenie cmdlet zwróci pełny identyfikator URI obiektu BLOB i token podpisu dostępu współdzielonego.

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

### -IPAddressOrRange
Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.
Zakresem jest włącznie.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Uprawnienie
Określa uprawnienia w tokenie umożliwiające uzyskanie dostępu do udziału i plików w udziale.

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Policy
Określa zapisane zasady dostępu dla udziału.

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol (protokół)
Określa protokół dozwolony dla żądania.
Dopuszczalne wartości tego parametru to:
* HttpsOnly
* HttpsOrHttp

Wartość domyślna to HttpsOrHttp.

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nazwa_udziału
Określa nazwę udziału magazynu.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -StartTime
Określa czas, po upływie którego podpis udostępniony będzie ważny.

```yaml
Type: DateTime
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
* Słowa kluczowe: typowe, Azure, usługi, dane, przechowywanie, obiekt BLOB, kolejka, tabela

## LINKI POKREWNE

[Get-AzureStorageShare](./Get-AzureStorageShare.md)

[Nowe — AzureStorageFileSASToken](./New-AzureStorageFileSASToken.md)
