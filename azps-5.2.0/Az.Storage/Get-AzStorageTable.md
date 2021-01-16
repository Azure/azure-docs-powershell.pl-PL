---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349561"
---
# Get-AzStorageTable

## STRESZCZENIe
Wyświetla listę tabel magazynu.

## POLECENIA

### Tabelaname (domyślna)
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TablePrefix
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzStorageTable** zawiera listę tabel magazynu skojarzonych z kontem magazynu na platformie Azure.

## Przykłady

### Przykład 1. Lista wszystkich tabel magazynu platformy Azure
```
PS C:\>Get-AzStorageTable
```

To polecenie pobiera wszystkie tabele magazynowania dla konta magazynu.

### Przykład 2: wyświetlanie tabeli magazynu platformy Azure przy użyciu znaku wieloznacznego
```
PS C:\>Get-AzStorageTable -Name table*
```

To polecenie używa symboli wieloznacznych w celu uzyskania tabel przechowywania, których nazwa zaczyna się od tabeli.

### Przykład 3: Tworzenie listy tabel magazynu platformy Azure przy użyciu prefiksu nazwy tabeli
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

W tym poleceniu jest używany parametr *prefix* umożliwiający pobranie tabel magazynu, których nazwa zaczyna się od tabeli.

## PARAMETRÓW

### -Context
Określa kontekst miejsca do magazynowania.
Aby ją utworzyć, możesz użyć New-AzStorageContext polecenia cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę tabeli.
Jeśli nazwa tabeli jest pusta, polecenie cmdlet wyświetla wszystkie tabele.
W przeciwnym razie wyświetla wszystkie tabele zgodne z określoną nazwą lub wzorcem zwykłej nazwy.

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
Określa prefiks stosowany w nazwie tabeli lub tabel, które chcesz pobrać.
Za pomocą tej pozycji można znaleźć wszystkie tabele, które zaczynają się od tego samego ciągu, na przykład tabelę.

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageTable

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzStorageTable](./New-AzStorageTable.md)

[Remove-AzStorageTable](./Remove-AzStorageTable.md)


