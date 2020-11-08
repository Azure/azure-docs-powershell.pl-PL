---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 99DC239C-EA68-4830-9345-762CD6A3F68C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 320b95add2806f48121151a71bdf36a572fa05a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054684"
---
# Add-AzureVhd

## STRESZCZENIe
Umożliwia przekazywanie pliku VHD z komputera lokalnego do obiektu BLOB na koncie magazynu w chmurze na platformie Azure.

## POLECENIA

```
Add-AzureVhd [-Destination] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfUploaderThreads] <Int32>]
 [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzureVhd** umożliwia przekazywanie danych z lokalnego obrazu wirtualnego dysku twardego (VHD) na konto magazynu obiektów BLOB jako naprawione obrazy VHD.
Zawiera parametry umożliwiające skonfigurowanie procesu przekazywania, takie jak określenie liczby wątków przekazujący, które będą używane lub zastępowaniem obiektu BLOB, który już istnieje w określonym docelowym identyfikatorze URI.
W przypadku obrazów lokalnego dysku VHD scenariusz poprawiania jest również obsługiwany, aby można było przekazać różnicowe obrazy dysków bez konieczności przekazywania już przekazanych obrazów podstawowych. Jest też obsługiwany identyfikator URI (Shared Access Signature, SAS).

## Przykłady

### Przykład 1: Dodawanie pliku VHD
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

To polecenie powoduje dodanie pliku VHD do konta magazynu.

### Przykład 2: Dodawanie pliku VHD i zastępowanie miejsca docelowego
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

To polecenie powoduje dodanie pliku VHD do konta magazynu.

### Przykład 3: Dodawanie pliku VHD i Określanie liczby wątków
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

To polecenie umożliwia dodanie pliku VHD do konta magazynu i określenie liczby wątków, które mają zostać użyte do przekazania pliku.

### Przykład 4: Dodawanie pliku VHD i Określanie identyfikatora URI SAS
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01-09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveOSIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

To polecenie umożliwia dodanie pliku VHD do konta magazynu i określenie identyfikatora URI SAS.

## PARAMETRÓW

### -BaseImageUriToPatch
Określa identyfikator URI podstawowego obiektu BLOB obrazu w usłudze Azure Blob Storage.
Obsługiwane są również skojarzenia zabezpieczeń w danych wejściowych URI.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Miejsce docelowe
Określa identyfikator URI do obiektu BLOB w magazynie obiektów blob platformy Microsoft Azure.
Obsługiwane są skojarzenia zabezpieczeń w wejściowych identyfikatorze URI.
Jednak w scenariuszach poprawiania lokalizacja docelowa nie może być identyfikatorem URI SAS.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.

Dopuszczalne wartości tego parametru to:

- Kontynuacj
- Ignorować
- Inquire
- SilentlyContinue
- Przestaw
- Wykonywanie

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Określa zmienną informacyjną.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalFilePath
Gatunek ścieżka pliku lokalnego pliku VHD.

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberOfUploaderThreads
Określa liczbę wątków, które mają być używane do przekazywania.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OverWrite
Określa, że to polecenie cmdlet usuwa istniejący obiekt BLOB w określonym docelowym identyfikatorze URI, jeśli istnieje.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

[Zapisz — AzureVhd](./Save-AzureVhd.md)


