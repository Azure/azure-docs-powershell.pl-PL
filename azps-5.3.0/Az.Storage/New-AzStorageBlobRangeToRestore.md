---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501178"
---
# New-AzStorageBlobRangeToRestore

## STRESZCZENIe
Tworzy obiekt zakresu BLOB w celu przywrócenia konta magazynu.

## POLECENIA

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzStorageBlobRangeToRestore** tworzy obiekt Range obiektu BLOB, którego można użyć w funkcji Restore-AzStorageBlobRange.

## Przykłady

### Przykład 1: Tworzenie zakresu obiektu BLOB do przywrócenia
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

To polecenie tworzy zakres obiektu BLOB do przywrócenia, który rozpoczyna się od container1/blob1 (dołączanie) i kończy się na container2/blob2 (Exclude).

### Przykład 2: tworzy zakres obiektu BLOB, który zostanie przywrócony z pierwszego obiektu BLOB w kolejności alfabetycznej, do określonego obiektu BLOB (Wyklucz)
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

To polecenie tworzy zakres obiektu BLOB, który zostanie przywrócony z pierwszego obiektu BLOB kolejności alfabetycznej do określonego obiektu BLOB container2/blob2 (Wyklucz).

### Przykład 3: tworzy zakres obiektu BLOB, który zostanie przywrócony z określonego obiektu BLOB (include), do ostatniego obiektu BLOB w kolejności alfabetycznej.
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

To polecenie tworzy zakres obiektu BLOB, który zostanie przywrócony z określonego obiektu BLOB container1/blob1 (include), do ostatniego obiektu BLOB w kolejności alfabetycznej.

### Przykład 4: tworzy zakres BLOB, który przywraca wszystkie obiekty blob
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

To polecenie tworzy zakres obiektu BLOB, w którym zostaną przywrócone wszystkie obiekty blob.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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
Określ zakres końcowy przywracania obiektu BLOB.
Zakres końcowy zostanie wykluczony w obszarze Przywróć obiekty blob.
Ustaw ją jako pustą strng, aby przywrócić jej koniec.

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
Określ zakres początkowy przywracania obiektu BLOB.
Zakres początkowy zostanie dołączony do funkcji Przywróć obiekty blob.
Ustaw ją jako ciąg pusty, aby przywrócić z początku.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. Management. Storage. models. PSBlobRestoreRange

## INFORMACYJN

## LINKI POKREWNE
