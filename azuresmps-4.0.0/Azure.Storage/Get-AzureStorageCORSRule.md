---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c65daf144708340649b9f7b1566c5e5f2dd81e45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524042"
---
# Get-AzureStorageCORSRule

## STRESZCZENIe
Pobiera reguły specyfikacji CORS dla typu usługi magazynu.

## POLECENIA

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureStorageCORSRule** pobiera reguły specyfikacji CORS (Cross-Origin Resource Sharing) dla typu usługi Azure Storage.

## Przykłady

### Przykład 1: pobieranie reguł CORS usługi BLOB
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

To polecenie pobiera reguły CORS dla typu usługi BLOB.

## PARAMETRÓW

### -ClientTimeoutPerRequest
Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.
Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.
Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Określa maksymalną liczbę współbieżnych połączeń sieciowych.
Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.
Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.
Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.
Wartość domyślna to 10.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ServerTimeoutPerRequest
Określa długość limitu czasu dla części serwera żądania.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Określa typ usługi Azure Storage, dla którego to polecenie cmdlet pobiera reguły CORS.
Dopuszczalne wartości tego parametru to:

- Obiektów BLOB 
- Tworząc 
- Wykonany 
- Plik

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

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

###  
To polecenie cmdlet zwraca tablicę obiektów **PSCORSRule** , które reprezentują reguły specyfikacji CORS obecnie w usłudze.

## INFORMACYJN

## LINKI POKREWNE

[Remove-AzureStorageCORSRule](./Remove-AzureStorageCORSRule.md)

[Set-AzureStorageCORSRule](./Set-AzureStorageCORSRule.md)


