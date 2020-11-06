---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRMVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRMVhd.md
ms.openlocfilehash: aee844d36fb2083e56415b34032cf928cb01d99e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550324"
---
# Add-AzureRmVhd

## STRESZCZENIe
Umożliwia przekazywanie wirtualnego dysku twardego z lokalnej maszyny wirtualnej do obiektu BLOB na koncie magazynu w chmurze na platformie Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Add-AzureRmVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzureRmVhd** umożliwia przekazywanie lokalnych wirtualnych dysków twardych w formacie pliku VHD do konta magazynu obiektów BLOB jako wirtualnych dysków twardych.
Możesz skonfigurować liczbę wątków przekazujący, które będą używane lub zastępować istniejący obiekt BLOB w określonym docelowym identyfikatorze URI.
Obsługiwane są również możliwości przekazywania wersji z poprawki do pliku VHD lokalnego.
Po przekazaniu podstawowego wirtualnego dysku twardego już można przekazać dyski różnicowe, które używają podstawowego obrazu jako elementu nadrzędnego.
Jest obsługiwany także identyfikator URI (Shared Access Signature).

## Przykłady

### Przykład 1: Dodawanie pliku VHD
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

To polecenie powoduje dodanie pliku VHD do konta magazynu.

### Przykład 2: Dodawanie pliku VHD i zastępowanie miejsca docelowego
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

To polecenie powoduje dodanie pliku VHD do konta magazynu.
Polecenie zastępuje istniejący plik.

### Przykład 3: Dodawanie pliku VHD i Określanie liczby wątków
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

To polecenie powoduje dodanie pliku VHD do konta magazynu.
Polecenie określa liczbę wątków, które mają być używane do przekazania pliku.

### Przykład 4: Dodawanie pliku VHD i Określanie identyfikatora URI SAS
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

To polecenie umożliwia dodanie pliku VHD do konta magazynu i określenie identyfikatora URI SAS.

## PARAMETRÓW

### -AsJob
Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.

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
Określa identyfikator URI podstawowego obiektu BLOB obrazu w usłudze Azure Blob Storage.
Jako wartość tego parametru można określić skojarzenia zabezpieczeń.

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Miejsce docelowe
Określa identyfikator URI obiektu BLOB w magazynie obiektów BLOB.
Parametr obsługuje identyfikator URI SAS, chociaż miejsce docelowe scenariuszy poprawek nie może być identyfikatorem URI SAS.

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

### -LocalFilePath
Określa ścieżkę lokalnego pliku VHD.

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
Określa liczbę wątków przekazujący, które mają być używane podczas przekazywania pliku VHD.

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
Wskazuje, że to polecenie cmdlet zastąpi istniejący obiekt BLOB w określonym docelowym identyfikatorze URI, jeśli taki istnieje.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### System. URI

### System. IO. FileInfo

### System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

### System. Management. Automation. SwitchParameter

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. models. VhdUploadContext

## INFORMACYJN

## LINKI POKREWNE

[Zapisz — AzureRmVhd](./Save-AzureRmVhd.md)


