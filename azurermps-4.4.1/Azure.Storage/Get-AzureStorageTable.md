---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3ba13fb1ee18f5dcc35b81ff70ebd7c5a61d1e4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525854"
---
# Get-AzureStorageTable

## STRESZCZENIe
Wyświetla listę tabel magazynu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Tabelaname (domyślna)
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### TablePrefix
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureStorageTable** zawiera listę tabel magazynu skojarzonych z kontem magazynu na platformie Azure.

## Przykłady

### Przykład 1. Lista wszystkich tabel magazynu platformy Azure
```
PS C:\>Get-AzureStorageTable
```

To polecenie pobiera wszystkie tabele magazynowania dla konta magazynu.

### Przykład 2: wyświetlanie tabeli magazynu platformy Azure przy użyciu znaku wieloznacznego
```
PS C:\>Get-AzureStorageTable -Name table*
```

To polecenie używa symboli wieloznacznych w celu uzyskania tabel przechowywania, których nazwa zaczyna się od tabeli.

### Przykład 3: Tworzenie listy tabel magazynu platformy Azure przy użyciu prefiksu nazwy tabeli
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

W tym poleceniu jest używany parametr *prefix* umożliwiający pobranie tabel magazynu, których nazwa zaczyna się od tabeli.

## PARAMETRÓW

### -Context
Określa kontekst miejsca do magazynowania.
Aby ją utworzyć, możesz użyć New-AzureStorageContext polecenia cmdlet.

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

### -Name (nazwa)
Określa nazwę tabeli.
Jeśli nazwa tabeli jest pusta, polecenie cmdlet wyświetla wszystkie tabele.
W przeciwnym razie wyświetla wszystkie tabele zgodne z określoną nazwą lub wzorcem zwykłej nazwy.

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### -Prefix
Określa prefiks stosowany w nazwie tabeli lub tabel, które chcesz pobrać.
Za pomocą tej pozycji można znaleźć wszystkie tabele, które zaczynają się od tego samego ciągu, na przykład tabelę.

```yaml
Type: String
Parameter Sets: TablePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### IStorageContext

Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku

### Ciąg

Parametr "nazwa" akceptuje wartość typu "String" z procesu

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageTable

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureStorageTable](./New-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


