---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareQuota.md
ms.openlocfilehash: 54636c226d3e8eb7ca9572a8f2e6c95e96981875
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719483"
---
# Set-AzureStorageShareQuota

## STRESZCZENIe
Umożliwia ustawienie pojemności magazynowania dla udziału.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Nazwaudziału
```
Set-AzureStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Udostępnij
```
Set-AzureStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureStorageShareQuota** określa pojemność magazynowania określonego udziału.

## Przykłady

### Przykład 1: Ustawianie pojemności miejsca do magazynowania dla udziału
```
PS C:\>Set-AzureStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

To polecenie ustawia pojemność magazynowania dla udziału o nazwie 1024 ContosoShare01 GB.

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
Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .

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

### -Przydział
Określa wartość przydziału w gigabajtach (GB).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
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

### -Share
Określa obiekt **CloudFileShare** reprezentujący udział, dla którego to polecenie cmdlet ustawia przydział.
Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.

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
Określa nazwę udziału pliku, dla którego ma zostać ustawiony przydział.

```yaml
Type: String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### IStorageContext

Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku

### CloudFileShare

Parametr "Udostępnij" akceptuje wartość typu "CloudFileShare" z procesu

### Ciąg

Parametr "nazwa_udziału" akceptuje wartość typu "String" z procesu

## WYSYŁA

### Microsoft. platformy windowsazure. Storage. File. FileShareProperties

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorageFileContent](./Get-AzureStorageFileContent.md)

[Get-AzureStorageShare](./Get-AzureStorageShare.md)

[Nowe — AzureStorageContext](./New-AzureStorageContext.md)
