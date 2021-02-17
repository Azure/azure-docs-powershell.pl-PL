---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239250"
---
# New-AzBatchResourceFile

## SYNOPSIS
Tworzy plik zasobu do użycia `New-AzBatchTask` według.

## SKŁADNIA

### HttpUrl (domyślne)
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

## OPIS
Tworzy plik zasobu do użycia `New-AzBatchTask` według.

## PRZYKŁADY

### Przykład 1. Tworzenie pliku zasobu za pomocą adresu URL HTTP, który wskaże pojedynczy plik
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Tworzy odwołanie `PSResourceFile` do adresu URL HTTP.

### Przykład 2. Tworzenie pliku zasobu z adresu URL kontenera magazynu platformy Azure
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Tworzy odwołanie `PSResourceFile` do adresu URL kontenera magazynu platformy Azure. Wszystkie pliki w kontenerze zostaną pobrane do określonego folderu.

### Przykład 3. Tworzenie pliku zasobu z nazwy kontenera autowy magazynowania
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Tworzy odwołanie `PSResourceFile` do nazwy kontenera autowy magazynowania. Wszystkie pliki w kontenerze zostaną pobrane do określonego folderu.

## PARAMETERS

### -AutoStorageContainerName
Nazwa kontenera magazynu na koncie automatycznego magazynu.

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
Pobiera prefiks obiektu blob do użycia podczas pobierania obiektów blob z kontenera magazynu platformy Azure.
Zostaną pobrane tylko obiekty blob, których nazwy zaczynają się od określonego prefiksu.
Ten prefiks może być częściową nazwą pliku lub podkategoriam.
Jeśli nie określono prefiksu, zostaną pobrane wszystkie pliki w kontenerze.

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

### -FileMode
Pobiera atrybut trybu uprawnień pliku w formacie ósemkowym.
Ta właściwość ma zastosowanie tylko wtedy, gdy plik zasobu zostanie pobrany do węzła systemu Linux.
Jeśli ta właściwość nie jest określona dla węzła systemu Linux, wartość domyślna to 0770.

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

### - FilePath
Lokalizacja w węźle obliczeniowym, do której należy pobrać pliki, względem katalogu roboczego zadania. Jeśli parametr HttpUrl jest określony, wymagany jest program FilePath i opisuje ścieżkę, do której zostanie pobrany plik, wraz z nazwą pliku. W przeciwnym razie, jeśli określono parametry AutoStorageContainerName lub StorageContainerUrl, program FilePath jest opcjonalny i jest katalogiem do pobierania plików. W przypadku użycia programu FilePath jako katalogu każda struktura katalogu już skojarzona z danymi wejściowymi zostanie zachowana w pełni i dołączona do określonego katalogu FilePath. Określona ścieżka względna nie może wychodzić z katalogu roboczego zadania (na przykład za pomocą ".").

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

### - HttpUrl
Adres URL pliku do pobrania.
Jeśli adres URL to magazyn obiektów blob platformy Azure, musi być czytelny przy użyciu dostępu anonimowego; oznacza to, że usługa wsadowa nie prezentuje żadnych poświadczeń podczas pobierania obiektu blob.
Istnieją dwa sposoby uzyskiwania takiego adresu URL dla obiektu blob w magazynie platformy Azure: obejmują podpis dostępu udostępnionego (SAS, Shared Access Signature), który udziela uprawnień do odczytu obiektu blob, lub ustaw wartość ACL dla obiektu blob lub jego kontenera, aby zezwolić na dostęp publiczny.

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

### - StorageContainerUrl
Adres URL kontenera obiektów blob w magazynie obiektów blob platformy Azure.
Ten adres URL musi być czytelny i dostępny do listy przy użyciu dostępu anonimowego; oznacza to, że usługa wsadowa nie prezentuje żadnych poświadczeń podczas pobierania obiektów blob z kontenera.
Istnieją dwa sposoby uzyskiwania takiego adresu URL dla kontenera w magazynie platformy Azure: obejmują podpis dostępu udostępnionego (SAS, Shared Access Signature) udzielanie uprawnień do odczytu kontenera lub ustawienie listy ACL dla kontenera, aby zezwolić na dostęp publiczny.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Brak

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Batch. Models.PSResourceFile

## NOTATKI

## LINKI POKREWNE

[New-AzBatchTask](./New-AzBatchTask.md)