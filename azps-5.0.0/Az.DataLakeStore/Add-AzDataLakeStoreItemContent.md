---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 3cf411e75e2a3ec430f13354015d5b6e271c840c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305694"
---
# Add-AzDataLakeStoreItemContent

## STRESZCZENIe
Dodawanie zawartości do elementu w sklepie Data Lake Store.

## POLECENIA

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzDataLakeStoreItemContent** umożliwia dodanie zawartości do elementu w usłudze Azure Data Lake Store.

## Przykłady

### Przykład 1. Dodawanie zawartości do pliku
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

To polecenie umożliwia dodanie zawartości do pliku myFile.txt.

## PARAMETRÓW

### — Konto
Określa nazwę konta usługi Data Lake Store.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Encoding
Określa kodowanie elementu, który ma zostać utworzony.
Dopuszczalne wartości tego parametru to:
- Wiadom
- Ciąg
- Ze
- Jednobajtowe
- BigEndianUnicode
- UTF8
- UTF7
- Znaki
- Domyślne
- Equipment
- BigEndianUTF32

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Określa ścieżkę elementu, który należy zmodyfikować, rozpoczynając od katalogu głównego (/).

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value
Określa zawartość, którą należy dodać do elementu.

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance

### System. Object

### System. Text. Encoding

## WYSYŁA

### System. Boolean

## INFORMACYJN

## LINKI POKREWNE

[Get-AzDataLakeStoreItemContent](./Get-AzDataLakeStoreItemContent.md)


