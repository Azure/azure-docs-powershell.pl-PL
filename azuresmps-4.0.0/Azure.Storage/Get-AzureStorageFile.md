---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3b84deae0307114efa274cdfa6fc708d1b268ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524033"
---
# Get-AzureStorageFile

## STRESZCZENIe
Wyświetla listę katalogów i plików ścieżki.

## POLECENIA

### Nazwa_udziału (domyślnie)
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Udostępnij
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Directory
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureStorageFile** zawiera listę katalogów i plików dla określonego udziału lub katalogu.
Określ parametr *Path* , aby uzyskać wystąpienie katalogu lub pliku w określonej ścieżce.

To polecenie cmdlet zwraca obiekty **AzureStorageFile** i **AzureStorageDirectory** .
Właściwości **IsDirectory** można użyć w celu rozróżnienia folderów i plików.

## Przykłady

### Przykład 1: Wyświetlanie listy katalogów w udziale
```
PS C:\>Get-AzureStorageFile -ShareName "share1" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

To polecenie wyświetla listę tylko katalogów w ContosoShare06 udostępniania.
Po pierwsze pobiera zarówno pliki, jak i katalogi, przekazuje je operatorowi **WHERE** za pomocą operatora potoku, a następnie odrzuca wszystkie obiekty, których typ nie jest "CloudFileDirectory".

### Przykład 2: wyświetlanie katalogu plików
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

To polecenie wyświetla listę plików i folderów w katalogu ContosoWorkingFolder w obszarze Udostępnij ContosoShare06.
Najpierw otrzymuje ono wystąpienie katalogu, a następnie przejdzie do polecenia cmdlet **Get-AzureStorageFile** w celu utworzenia listy katalogów.

## PARAMETRÓW

### -ClientTimeoutPerRequest
Określa interwał limitu czasu po stronie klienta (w sekundach) dla jednego żądania usługi.
Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wysłania żądania.
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
Ten parametr może pomóc w ograniczeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.
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
Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Directory
Określa folder jako obiekt **CloudFileDirectory** .
To polecenie cmdlet spowoduje wyświetlenie folderu, który określi ten parametr.
Aby uzyskać katalog, użyj polecenia cmdlet New-AzureStorageDirectory.
Aby uzyskać katalog, możesz również użyć polecenia cmdlet **Get-AzureStorageFile** .

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Path
Określa ścieżkę do folderu.

W przypadku pominięcia parametru *Path* polecenie **Get-AzureStorageFile** wyświetla listę katalogów i plików w określonym udziale plików lub katalogu.
Jeśli dołączasz parametr *Path* , funkcja **Get-AzureStorageFile** zwraca wystąpienie katalogu lub pliku w określonej ścieżce.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.
Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.

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

### -Share
Określa obiekt **CloudFileShare** .
To polecenie cmdlet pobiera plik lub katalog z udziału plików, który ten parametr określa.
Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.
Ten obiekt zawiera kontekst miejsca do magazynowania.
W przypadku określenia tego parametru nie określaj parametru *kontekstu* .

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nazwa_udziału
Określa nazwę udziału plików.
To polecenie cmdlet pobiera plik lub katalog z udziału plików, który ten parametr określa.

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

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

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorageFileContent](./Get-AzureStorageFileContent.md)

[Nowe — AzureStorageDirectory](./New-AzureStorageDirectory.md)

[Remove-AzureStorageDirectory](./Remove-AzureStorageDirectory.md)

[Remove-AzureStorageFile](./Remove-AzureStorageFile.md)

[Set-AzureStorageFileContent](./Set-AzureStorageFileContent.md)


