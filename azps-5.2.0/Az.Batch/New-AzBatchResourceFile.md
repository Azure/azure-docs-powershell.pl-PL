---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361328"
---
# New-AzBatchResourceFile

## STRESZCZENIe
Tworzy plik zasobów do użycia przez `New-AzBatchTask` .

## POLECENIA

### HttpUrl (domyślny)
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageContainerUrl
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AutoStorageContainerName
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Tworzy plik zasobów do użycia przez `New-AzBatchTask` .

## Przykłady

### Przykład 1. Tworzenie pliku zasobów na podstawie adresu URL HTTP wskazującego jeden plik
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Tworzy `PSResourceFile` odwołanie do adresu URL http.

### Przykład 2: Tworzenie pliku zasobów na podstawie adresu URL kontenera magazynu platformy Azure
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Tworzy `PSResourceFile` odwołanie do adresu URL kontenera usługi Azure Storage. Wszystkie pliki w kontenerze zostaną pobrane do określonego folderu.

### Przykład 3: Tworzenie pliku zasobów na podstawie nazwy kontenera automatycznego przechowywania
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Tworzy `PSResourceFile` odwołanie do nazwy kontenera automatycznego przechowywania. Wszystkie pliki w kontenerze zostaną pobrane do określonego folderu.

## PARAMETRÓW

### -AutoStorageContainerName
Nazwa kontenera magazynu na koncie Auto-pamięci.

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobPrefix
Pobiera prefiks obiektu BLOB, który ma być używany podczas pobierania plików BLOB z kontenera magazynu platformy Azure.
Zostaną pobrane tylko te obiekty blob, których nazwy zaczynają się od określonego prefiksu.
Ten prefiks może być częściową nazwą pliku lub podkatalogiem.
Jeśli nie podano prefiksu, wszystkie pliki w kontenerze zostaną pobrane.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileMode
Pobiera atrybut tryb uprawnień do pliku w formacie ósemkowym.
Ta właściwość jest dostępna tylko w przypadku pobrania pliku zasobu do węzła Linux.
Jeśli ta właściwość nie jest określona dla węzła Linux, wartość domyślna to 0770.

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

### -FilePath
Lokalizacja w węźle obliczeniowym, do której mają zostać pobrane pliki, względem katalogu roboczego zadania. Jeśli parametr HttpUrl jest określony, ścieżka FilePath jest wymagana i zawiera opis ścieżki, do której plik będzie pobierany, łącznie z nazwą pliku. W przeciwnym razie, jeśli określono parametry AutoStorageContainerName lub StorageContainerUrl, ścieżka FilePath jest opcjonalna i katalog, do którego mają zostać pobrane pliki. W przypadku, gdy ścieżka FilePath jest używana jako katalog, każda struktura katalogów już skojarzona z danymi wejściowymi zostanie zachowana w całości i dołączona do określonego katalogu FilePath. Określona ścieżka względna nie może być rozdzielona w katalogu roboczym zadania (na przykład przy użyciu '.. ').

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpUrl
Adres URL pliku, który ma zostać pobrany.
Jeśli adres URL to usługa Azure Blob Storage, należy ją odczytać za pomocą anonimowego dostępu; oznacza to, że podczas pobierania obiektu BLOB usługa przetwarzania wsadowego nie przedstawia żadnych poświadczeń.
Istnieją dwa sposoby uzyskiwania takiego adresu URL dla obiektu BLOB w usłudze Azure Storage: dołączanie do obiektu BLOB uprawnień do odczytu (udostępnionego podpisu dostępu) lub ustawianie listy ACL dla obiektu BLOB lub jego kontenera w celu umożliwienia dostępu publicznego.

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerUrl
Adres URL kontenera obiektu BLOB w magazynie obiektów blob platformy Azure.
Ten adres URL musi być możliwy do odczytania i może być listowy za pomocą anonimowego dostępu; oznacza to, że usługa przetwarzania wsadowego nie przedstawia żadnych poświadczeń podczas pobierania plików BLOB z kontenera.
Istnieją dwa sposoby uzyskiwania takiego adresu URL kontenera w usłudze Azure Storage: dołączanie do tego kontenera uprawnień dostępu współużytkowanego (SAS) lub ustawianie listy ACL kontenera, aby umożliwić dostęp publiczny.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft.Azure.Commands.Batch. Modele. PSResourceFile

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzBatchTask](./New-AzBatchTask.md)