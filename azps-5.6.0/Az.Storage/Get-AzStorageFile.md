---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: e61171faba3661ad1d518641655ad87f06771ae6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997095"
---
# Get-AzStorageFile

## SYNOPSIS
Lista katalogów i plików dla ścieżki.

## SKŁADNIA

### ShareName (domyślna)
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Udostępnij
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Katalog
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzStorageFile** zawiera listę katalogów i plików dla owego udziału lub katalogu.
Określ parametr *Ścieżka,* aby uzyskać wystąpienie katalogu lub pliku w określonej ścieżce.
To polecenie cmdlet zwraca **obiekty AzureStorageFile** i **AzureStorageDirectory.**
Właściwość **IsDirectory** umożliwia rozróżnienie folderów i plików.

## PRZYKŁADY

### Przykład 1. Lista katalogów w udostępniniu
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

To polecenie wyświetla listę tylko katalogów w użytce ContosoShare06.
Najpierw pobiera zarówno pliki, jak i katalogi, przekazuje je do operatora **where** przy użyciu operatora potoku, a następnie odrzuca wszystkie obiekty o typie innym niż "AzureStorageFileDirectory".

### Przykład 2. Lista katalogu plików
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

To polecenie zawiera listę plików i folderów w katalogu ContosoWorkingFolder w ramach udziału ContosoShare06.
Najpierw pobiera wystąpienie katalogu, a następnie potokuje je do polecenia cmdlet **Get-AzStorageFile,** aby wyświetlić katalog.

## PARAMETERS

### -ClientTimeoutPerRequest
Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.
Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.
Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Określa maksymalną liczbę jednoczesnych połączeń sieciowych.
Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.
Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.
Ten parametr może pomóc zminimalizować problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.
Wartość domyślna to 10.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — kontekst
Określa kontekst magazynu platformy Azure.
Aby uzyskać kontekst magazynu, użyj New-AzStorageContext cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Katalog
Określa folder jako obiekt **CloudFileDirectory.**
To polecenie cmdlet pobiera folder, który określa ten parametr.
Aby uzyskać katalog, użyj polecenia cmdlet New-AzStorageDirectory cmdlet.
Aby uzyskać katalog, możesz również użyć polecenia cmdlet **Get-AzStorageFile.**

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### — Ścieżka
Określa ścieżkę folderu.
Jeśli parametr Path zostanie *pominięty,* plik **Get-AzStorageFile** będzie zawierał listę katalogów i plików w określonym udziału plików lub katalogu.
Jeśli parametr Path *zostanie* podany, funkcja **Get-AzStorageFile** zwróci wystąpienie katalogu lub pliku w określonej ścieżce.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.
Jeśli po upływie określonego interwału usługa przetwarza żądanie, usługa magazynu zwraca błąd.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Udostępnij
Określa obiekt **CloudFileShare.**
To polecenie cmdlet pobiera plik lub katalog z udziału plików, który określa ten parametr.
Aby uzyskać obiekt **CloudFileShare,** użyj Get-AzStorageShare cmdlet.
Ten obiekt zawiera kontekst magazynu.
Jeśli określisz ten parametr, nie określaj *parametru kontekstowego.*

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ShareName
Określa nazwę udziału plików.
To polecenie cmdlet pobiera plik lub katalog z udziału plików, który określa ten parametr.

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Storage.File.CloudFileShare

### Microsoft.Azure.Storage.File.CloudFileDirectory

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## DANE WYJŚCIOWE

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile

## NOTATKI

## LINKI POKREWNE

[Get-AzstorageFileContent](./Get-AzStorageFileContent.md)

[New-AzStorageDirectory](./New-AzStorageDirectory.md)

[Remove-AzStorageDirectory](./Remove-AzStorageDirectory.md)

[Remove-azstorageFile](./Remove-AzStorageFile.md)

[Set-azstorageFileContent](./Set-AzStorageFileContent.md)


