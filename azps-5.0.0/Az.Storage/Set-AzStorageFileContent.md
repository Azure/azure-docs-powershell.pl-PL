---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 3fed30a260532378274e2df815d6e4b252c018f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224731"
---
# Set-AzStorageFileContent

## STRESZCZENIe
Umożliwia przekazywanie zawartości pliku.

## POLECENIA

### Nazwa_udziału (domyślnie)
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### Udostępnij
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### Directory
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzStorageFileContent** umożliwia przekazywanie zawartości pliku do pliku w określonym udziale.

## Przykłady

### Przykład 1: przekazywanie pliku w bieżącym folderze
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

To polecenie wysyła plik o nazwie DataFile37 w bieżącym folderze jako plik o nazwie CurrentDataFile w folderze o nazwie ContosoWorkingFolder.

### Przykład 2: przekazywanie wszystkich plików w bieżącym folderze
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

W tym przykładzie użyto kilku typowych poleceń cmdlet programu Windows PowerShell i bieżącego polecenia cmdlet, aby przekazać wszystkie pliki z bieżącego folderu do folderu głównego kontenera ContosoShare06.
Pierwsze polecenie uzyskuje nazwę bieżącego folderu i zapisuje je w zmiennej $CurrentFolder.
Drugie polecenie używa polecenia cmdlet **Get-AzStorageShare** w celu uzyskania udziału plików o nazwie ContosoShare06, a następnie zapisanie go w zmiennej $Container.
Polecenie ostatnie pobiera zawartość bieżącego folderu i przekazuje każdemu z nich do polecenia cmdlet Where-Object przy użyciu operatora potoku.
Polecenie cmdlet umożliwia filtrowanie obiektów, które nie są plikami, a następnie przekazanie plików do polecenia cmdlet ForEach-Object.
Polecenie cmdlet uruchamia blok skryptu dla każdego pliku, który tworzy odpowiednią ścieżkę, a następnie używa bieżącego polecenia cmdlet do przekazania pliku.
Wynik ma taką samą nazwę i taką samą położenie względne, co pozostałe pliki, które przykłada są ładowane.
Aby uzyskać więcej informacji na temat bloków skryptów, wpisz ciąg `Get-Help about_Script_Blocks` .

### Przykład 3: przekazywanie pliku lokalnego do pliku platformy Azure i perserve właściwości lokalnego pliku SMB (plik attributtes, czas tworzenia pliku, czas ostatniego zapisu pliku) w pliku platformy Azure.
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

W tym przykładzie jest wysyłany plik lokalny do pliku systemu Azure, a perserves właściwości lokalnego pliku SMB (plik attributtes, czas tworzenia pliku, czas ostatniego zapisu pliku) w pliku platformy Azure.

## PARAMETRÓW

### -AsJob
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

### -ClientTimeoutPerRequest
Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.
Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.
Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.

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
Określa maksymalną liczbę współbieżnych połączeń sieciowych.
Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.
Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.
Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.
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

### -Context
Określa kontekst usługi Azure Storage.
Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Directory
Określa folder jako obiekt **CloudFileDirectory** .
To polecenie cmdlet umożliwia przekazanie pliku do folderu, który określa ten parametr.
Aby uzyskać katalog, użyj polecenia cmdlet New-AzStorageDirectory.
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

### -Force
Wskazuje, że to polecenie cmdlet zastępuje istniejący plik magazynu platformy Azure.

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
Wskazuje, że to polecenie cmdlet zwraca obiekt **AzureStorageFile** , który tworzy lub przekazuje.

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

### -Path
Określa ścieżkę do pliku lub folderu.
To polecenie cmdlet umożliwia przekazywanie zawartości do pliku, który jest określany przez ten parametr, lub do pliku w folderze, który określa ten parametr.
Jeśli określisz folder, to polecenie cmdlet utworzy plik mający taką samą nazwę jak plik źródłowy.
Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie jego zawartości w tym pliku.
Jeśli określisz plik, który już istnieje, i określisz parametr _Force_ , to polecenie cmdlet zastąpi zawartość pliku.
Jeśli określisz plik, który już istnieje, i nie określisz _siły_ , to polecenie cmdlet nie zmieni się i zwróci błąd.
Jeśli określisz ścieżkę do folderu, który nie istnieje, to polecenie cmdlet nie zmieni się i zwróci błąd.

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

### -PreserveSMBAttribute
Zachowanie właściwości pliku źródłowego SMB (plik attributtes, czas tworzenia pliku, czas ostatniego zapisu pliku) w pliku docelowym. Ten parametr jest dostępny tylko w systemie Windows.

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
Określa długość limitu czasu dla części serwera żądania.

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

### -Share
Określa obiekt **CloudFileShare** .
To polecenie cmdlet przekazuje do pliku w udziale pliku ten parametr określa.
Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzStorageShare.
Ten obiekt zawiera kontekst miejsca do magazynowania.
W przypadku określenia tego parametru nie określaj parametru *kontekstu* .

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

### -Nazwa_udziału
Określa nazwę udziału plików.
To polecenie cmdlet przekazuje do pliku w udziale pliku ten parametr określa.

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

### -Source
Określa plik źródłowy, który jest wysyłany przez to polecenie cmdlet.
Jeśli określisz plik, który nie istnieje, to polecenie cmdlet zwróci błąd.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Storage. File. CloudFileShare

### Microsoft. Azure. Storage. File. CloudFileDirectory

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageFile

## INFORMACYJN

## LINKI POKREWNE

[Remove-AzStorageDirectory](./Remove-AzStorageDirectory.md)

[Nowe — AzStorageDirectory](./New-AzStorageDirectory.md)

[Get-AzStorageFileContent](./Get-AzStorageFileContent.md)
