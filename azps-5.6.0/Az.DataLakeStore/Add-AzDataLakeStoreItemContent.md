---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: aa2fe76f221ce412c0e47f7a43b1dba551131f45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994393"
---
# Add-AzDataLakeStoreItemContent

## SYNOPSIS
Dodaje zawartość do elementu w sklepie Data Lake Store.

## SKŁADNIA

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Add-AzDataLakeStoreItemContent** dodaje zawartość do elementu w sklepie Azure Data Lake Store.

## PRZYKŁADY

### Przykład 1. Dodawanie zawartości do pliku
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

To polecenie dodaje zawartość do pliku myFile.txt.

## PARAMETERS

### — Konto
Określa nazwę konta sklepu Data Lake Store.

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### — Kodowanie
Określa kodowanie elementu do utworzenia.
Dopuszczalne wartości dla tego parametru to:
- Nieznany
- Ciąg
- Unicode
- Bajt
- BigEndianUnicode
- UTF8
- UTF7
- Ascii
- Domyślne
- Oem
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

### — Ścieżka
Określa ścieżkę elementu do zmodyfikowania w sklepie Data Lake Store, zaczynając od katalogu głównego (/).

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

### — Wartość
Określa zawartość do dodania do elementu.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance

### System.Object

### System.Text.Encoding

## DANE WYJŚCIOWE

### System.Boolean

## NOTATKI

## LINKI POKREWNE

[Get-AzDataLakeStoreItemContent](./Get-AzDataLakeStoreItemContent.md)


