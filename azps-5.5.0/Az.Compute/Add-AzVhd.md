---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: d0031ad2a6b4c38937e7faaf0743d6181608ff15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199347"
---
# Add-AzVhd

## SYNOPSIS
Przekazanie wirtualnego dysku twardego z lokalnej maszyny wirtualnej do obiektu blob w koncie magazynu w chmurze na platformie Azure.

## SKŁADNIA

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Add-AzVhd** jest przekazywania lokalnych wirtualnych dysków twardych w formacie vhd do konta magazynu obiektów blob w przypadku naprawień wirtualnych dysków twardych.
Możesz skonfigurować liczbę wątków przekazywania, które będą używane, lub zastąpić istniejący obiekt blob w określonym docelowym URI.
Obsługiwana jest również możliwość przekazywania poprawionej wersji lokalnego pliku vhd.
Gdy podstawowy wirtualny dysk twardy został już przekazany, możesz przekazać inne dyski, które używają obrazu podstawowego jako elementu nadrzędnego.
Obsługiwany jest również interfejs URI podpisu dostępu udostępnionego (SAS).

## PRZYKŁADY

### Przykład 1. Dodawanie pliku VHD
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

To polecenie powoduje dodanie pliku vhd do konta magazynu.

### Przykład 2. Dodawanie pliku VHD i zastępowanie miejsca docelowego
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

To polecenie powoduje dodanie pliku vhd do konta magazynu.
Polecenie zastąpi istniejący plik.

### Przykład 3. Dodawanie pliku VHD i określanie liczby wątków
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

To polecenie powoduje dodanie pliku vhd do konta magazynu.
To polecenie określa liczbę wątków, które mają być służące do przekazywania pliku.

### Przykład 4. Dodawanie pliku VHD i określanie URI SAS
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

To polecenie powoduje dodanie pliku vhd do konta magazynu i określenie URI SAS.

## PARAMETERS

### — AsJob
Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BaseImageUriToPatch
Określa wartość URI dla obiektu blob obrazu podstawowego w magazynie obiektów blob platformy Azure.
Sygnaturę SAS można określić jako wartość dla tego parametru.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### — miejsce docelowe
Określa URI obiektu blob w magazynie obiektów blob.
Parametr obsługuje URI SAS, chociaż miejsce docelowe scenariuszy poprawiania nie może być URI SAS.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - LocalFilePath
Określa ścieżkę lokalnego pliku vhd.

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberOfUploaderThreads
Określa liczbę wątków przekazywania, które mają być używane podczas przekazywania pliku vhd.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OverWrite
Wskazuje, że to polecenie cmdlet zastępuje istniejący obiekt blob w określonym docelowym URI, jeśli istnieje.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### System.Uri

### System.IO.FileInfo

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Management.Automation.SwitchParameters

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Models.VhdUploadContext

## NOTATKI

## LINKI POKREWNE

[Save-Azvhd](./Save-AzVhd.md)


