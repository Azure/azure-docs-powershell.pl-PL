---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvhd
schema: 2.0.0
ms.openlocfilehash: 86a4cdb4fc0d6709d6cb9311d243f12dcb65e5de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899369"
---
# Save-AzureRmVhd

## STRESZCZENIe
Zapisuje pobrane obrazy VHD lokalnie.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ResourceGroupParameterSetName
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### StorageKeyParameterSetName
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Save-AzureRmVhd** zapisuje obrazy VHD z obiektu BLOB, w którym są one przechowywane do pliku.
Możesz określić liczbę wątków programu do pobierania plików, których używa proces, oraz czy zamienić plik, który już istnieje.

To polecenie cmdlet pobiera zawartość w taki sposób.
Nie dotyczy żadnych konwersji formatu wirtualnego dysku twardego (VHD).

## Przykłady

### Przykład 1: Pobieranie obrazu
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

To polecenie pobiera plik VHD i przechowuje go w ścieżce lokalnej C:\vhd\Win7Image.vhd.

### Przykład 2: Pobieranie obrazu i zastępowanie pliku lokalnego
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

To polecenie umożliwia pobranie pliku VHD i zapisanie go w ścieżce lokalnej.
Polecenie zawiera parametr *Zastąp* .
Dlatego jeśli C:\vhd\Win7Image.vhd już istnieje, to polecenie zastępuje je.

### Przykład 3: Pobieranie obrazu przy użyciu określonej liczby wątków
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

To polecenie umożliwia pobranie pliku VHD i zapisanie go w ścieżce lokalnej.
Polecenie określa wartość 32 dla parametru *NumberOfThreads* .
Polecenie cmdlet używa więc wątków 32 dla tej akcji.

### Przykład 4: Pobieranie obrazu i określanie klucza magazynu
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

To polecenie umożliwia pobranie pliku VHD i określenie klucza magazynu.

## PARAMETRÓW

### -AsJob
Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalFilePath
Określa ścieżkę lokalnego pliku zapisanego obrazu.

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NumberOfThreads
Określa liczbę wątków pobierania, które są używane podczas pobierania tego polecenia cmdlet.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverWrite
Wskazuje, że to polecenie cmdlet zastępuje plik określony przez plik *LocalFilePath* , jeśli istnieje.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów konta magazynu.

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceUri
Określa identyfikator URI (Uniform Resource Identifier) obiektu BLOB `Azure` .

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKey
Określa klucz magazynu konta magazynu obiektów BLOB.
Jeśli nie podano klucza, to polecenie cmdlet próbuje ustalić klucz magazynu konta w usłudze *SourceUri* na platformie Azure.

```yaml
Type: String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. models. VhdDownloadContext

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureRmVhd](./Add-AzureRMVhd.md)


