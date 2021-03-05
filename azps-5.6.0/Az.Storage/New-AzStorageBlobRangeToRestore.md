---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: 0f74ad9b146a0c5d2f2c65b7109fb57f56902834
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002593"
---
# New-AzStorageBlobRangeToRestore

## SYNOPSIS
Tworzy obiekt zakres obiektów blob w celu przywrócenia konta magazynu.

## SKŁADNIA

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzStorageBlobRangeToRestore** tworzy obiekt zakresu obiektów blob, który może być używany w przywróceniu azStorageBlobRange.

## PRZYKŁADY

### Przykład 1. Tworzy zakres obiektów blob do przywrócenia
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

To polecenie tworzy zakres obiektów blob do przywrócenia, który zaczyna się od container1/blob1 (include) i kończy się na kontenerze2/obiekcie blob2 (exclude).

### Przykład 2. Tworzy zakres obiektów blob, który przywróci pierwszy obiekt blob w kolejności alfabetycznej, do określonego obiektu blob (exclude)
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

To polecenie tworzy zakres obiektów blob, który przywraca z pierwszego obiektu blob w kolejności alfabetycznej do określonego kontenera obiektów blob2/blob2 (exclude)

### Przykład 3. Tworzy zakres obiektów blob, który przywróci określony obiekt blob (include) do ostatniego obiektu blob w kolejności alfabetycznej
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

To polecenie tworzy zakres obiektów blob, który zostanie przywrócony z określonego kontenera obiektów blob1/blob1 (include) do ostatniego obiektu blob w kolejności alfabetycznej.

### Przykład 4. Tworzy zakres obiektów blob, co spowoduje przywrócenie wszystkich obiektów blob
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

To polecenie tworzy zakres obiektów blob, co spowoduje przywrócenie wszystkich obiektów blob.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### -EndRange
Określ zakres końcowy przywracania obiektów blob.
Zakres końcowy zostanie wykluczony w przypadku obiektów blob przywracania.
Ustaw go jako pusty strng, aby przywrócić do końca.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRange
Określ zakres rozpoczęcia przywracania obiektów blob.
Zakres rozpoczęcia zostanie uwzględniony w obiektach blob przywracania.
Ustaw go jako pusty ciąg, który będzie przywracany od początku.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Brak

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange

## NOTATKI

## LINKI POKREWNE
