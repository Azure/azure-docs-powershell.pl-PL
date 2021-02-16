---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 3c90e02194fa761bbb0fc00e11ea09d03ca00c1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176658"
---
# Get-AzStorageFileContent

## SYNOPSIS
Pobiera zawartość pliku.

## SKŁADNIA

### ShareName (Domyślna)
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### Udostępnij
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### Katalog
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### Plik
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzStorageFileContent** pobiera zawartość pliku, a następnie zapisuje go w określone przez Ciebie lokalizacji docelowej.
To polecenie cmdlet nie zwraca zawartości pliku.

## PRZYKŁADY

### Przykład 1. Pobieranie pliku z folderu
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

To polecenie pobiera plik o nazwie CurrentDataFile w folderze ContosoWorkingFolder z udziału plików ContosoShare06 do bieżącego folderu.

### Przykład 2. Pobieranie plików z przykładowego udziału plików
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

W tym przykładzie są pobierane pliki z przykładowego udziału plików

### Przykład 3. Pobieranie pliku platformy Azure do pliku lokalnego i korzystanie z właściwości SMB pliku platformy Azure (Attributtes file Attributtes, File Creation Time, File Last Write Time) w pliku lokalnym.
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

W tym przykładzie plik platformy Azure jest pobierany do pliku lokalnego i ma właściwości SMB pliku platformy Azure (Attributtes, File Creation Time, File Last Write Time) w pliku lokalnym.

## PARAMETERS

### — AsJob
Uruchom polecenie cmdlet w tle.

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

### — CheckMd5
Określa, czy należy sprawdzić sumę Md5 dla pobranego pliku.

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

### -ClientTimeoutPerRequest
Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi. Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania. Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.

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
Określa maksymalną jednoczesną liczbę połączeń sieciowych. Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych. Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową. Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę. Wartość domyślna to 10.

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
Określa kontekst magazynu platformy Azure. Aby uzyskać kontekst, użyj polecenia cmdlet New-AzStorageContext cmdlet.

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

### — miejsce docelowe
Określa ścieżkę docelową.
To polecenie cmdlet pobiera zawartość pliku do lokalizacji, która jest określana przez ten parametr.
Jeśli określisz ścieżkę nieistniecego pliku, to polecenie cmdlet utworzy ten plik i zapisze zawartość nowego pliku.
Jeśli określisz ścieżkę pliku, który już istnieje, i określisz parametr *Force,* polecenie cmdlet zastąpi plik.
Jeśli określisz ścieżkę istniejącego pliku i nie określisz wymuś, polecenie cmdlet wyświetli monit przed kontynuowaniem.
Jeśli określisz ścieżkę folderu, to polecenie cmdlet spróbuje utworzyć plik, który ma nazwę pliku magazynu platformy Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Katalog
Określa folder jako obiekt **CloudFileDirectory.**
To polecenie cmdlet pobiera zawartość pliku w folderze, który określa ten parametr.
Aby uzyskać katalog, użyj polecenia cmdlet New-AzStorageDirectory cmdlet.
Możesz również użyć polecenia cmdlet Get-AzStorageFile, aby uzyskać katalog.

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

### — Plik
Określa plik jako obiekt **CloudFile.**
To polecenie cmdlet pobiera plik, który jest określany przez ten parametr.
Aby uzyskać obiekt **CloudFile,** użyj Get-AzStorageFile cmdlet.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### — Wymuszanie
Jeśli określisz ścieżkę nieistniecego pliku, to polecenie cmdlet utworzy ten plik i zapisze zawartość nowego pliku.
Jeśli określisz ścieżkę pliku, który już istnieje, i określisz parametr *Force,* polecenie cmdlet zastąpi plik.
Jeśli określisz ścieżkę istniejącego pliku i nie określisz wymuś, polecenie cmdlet wyświetli monit przed kontynuowaniem.
Jeśli określisz ścieżkę folderu, to polecenie cmdlet spróbuje utworzyć plik, który ma nazwę pliku magazynu platformy Azure.

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

### -PassThru
Wskazuje, że to polecenie cmdlet zwraca pobrany obiekt **AzureStorageFile.**

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

### — Ścieżka
Określa ścieżkę pliku.
To polecenie cmdlet pobiera zawartość pliku określaną przez ten parametr.
Jeśli plik nie istnieje, to polecenie cmdlet zwraca błąd.

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreserveSMBAttribute
Zachowaj właściwości źródłowego pliku SMB (Attributtes file, File Creation Time, File Last Write Time) w pliku docelowym. Ten parametr jest dostępny tylko w systemie Windows.

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

### -ServerTimeoutPerRequest
Określa interwał po stronie usługi (w sekundach) dla żądania. Jeśli po upływie określonego interwału usługa przetwarza żądanie, usługa magazynu zwraca błąd.

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
To polecenie cmdlet pobiera zawartość pliku z udziału, który określa ten parametr.
Aby uzyskać obiekt **CloudFileShare,** użyj Get-AzStorageShare cmdlet.
Ten obiekt zawiera kontekst przechowywania.
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
To polecenie cmdlet pobiera zawartość pliku z udziału, który określa ten parametr.

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

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Storage.File.CloudFileShare

### Microsoft.Azure.Storage.File.CloudFileDirectory

### Microsoft.Azure.Storage.File.CloudFile

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## OUTPUTS

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile

## NOTATKI

## LINKI POKREWNE

[Get-AzStorageFile](./Get-AzStorageFile.md)

[Set-azstorageFileContent](./Set-AzStorageFileContent.md)


