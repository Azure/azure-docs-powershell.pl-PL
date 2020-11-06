---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd066a57ac63b0126120652750c669e6afde36bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523322"
---
# Set-AzureStorageFileContent

## STRESZCZENIe
Umożliwia przekazywanie zawartości pliku.

## POLECENIA

### Nazwa_udziału (domyślnie)
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Udostępnij
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Directory
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureStorageFileContent** umożliwia przekazywanie zawartości pliku do pliku w określonym udziale.

## Przykłady

### Przykład 1: przekazywanie pliku w bieżącym folderze
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

To polecenie wysyła plik o nazwie DataFile37 w bieżącym folderze jako plik o nazwie CurrentDataFile w folderze o nazwie ContosoWorkingFolder.

### Przykład 2: przekazywanie wszystkich plików w bieżącym folderze
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

W tym przykładzie użyto kilku typowych poleceń cmdlet programu Windows PowerShell i bieżącego polecenia cmdlet, aby przekazać wszystkie pliki z bieżącego folderu do folderu głównego kontenera ContosoShare06.

Pierwsze polecenie uzyskuje nazwę bieżącego folderu i zapisuje je w zmiennej $CurrentFolder.

Drugie polecenie używa polecenia cmdlet **Get-AzureStorageShare** w celu uzyskania udziału plików o nazwie ContosoShare06, a następnie zapisanie go w zmiennej $Container.

Polecenie ostatnie pobiera zawartość bieżącego folderu i przekazuje każdemu z nich do polecenia cmdlet Where-Object przy użyciu operatora potoku.
Polecenie cmdlet umożliwia filtrowanie obiektów, które nie są plikami, a następnie przekazanie plików do polecenia cmdlet ForEach-Object.
Polecenie cmdlet uruchamia blok skryptu dla każdego pliku, który tworzy odpowiednią ścieżkę, a następnie używa bieżącego polecenia cmdlet do przekazania pliku.
Wynik ma taką samą nazwę i taką samą położenie względne, co pozostałe pliki, które przykłada są ładowane.
Aby uzyskać więcej informacji na temat bloków skryptów, wpisz ciąg `Get-Help about_Script_Blocks` .

## PARAMETRÓW

### -ClientTimeoutPerRequest
Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.
Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.
Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

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
Type: Int32
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
Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Directory
Określa folder jako obiekt **CloudFileDirectory** .
To polecenie cmdlet umożliwia przekazanie pliku do folderu, który określa ten parametr.
Aby uzyskać katalog, użyj polecenia cmdlet New-AzureStorageDirectory.
Możesz również użyć polecenia cmdlet Get-AzureStorageFile, aby uzyskać katalog.

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Wskazuje, że to polecenie cmdlet zastępuje istniejący plik magazynu platformy Azure.

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

### -PassThru
Wskazuje, że to polecenie cmdlet zwraca obiekt **AzureStorageFile** , który tworzy lub przekazuje.

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

### -Path
Określa ścieżkę do pliku lub folderu.
To polecenie cmdlet umożliwia przekazywanie zawartości do pliku, który jest określany przez ten parametr, lub do pliku w folderze, który określa ten parametr.
Jeśli określisz folder, to polecenie cmdlet utworzy plik mający taką samą nazwę jak plik źródłowy.

Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie jego zawartości w tym pliku.
Jeśli określisz plik, który już istnieje, i określisz parametr _Force_ , to polecenie cmdlet zastąpi zawartość pliku.
Jeśli określisz plik, który już istnieje, i nie określisz _siły_ , to polecenie cmdlet nie zmieni się i zwróci błąd.

Jeśli określisz ścieżkę do folderu, który nie istnieje, to polecenie cmdlet nie zmieni się i zwróci błąd.


```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Określa długość limitu czasu dla części serwera żądania.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Share
Określa obiekt **CloudFileShare** .
To polecenie cmdlet przekazuje do pliku w udziale pliku ten parametr określa.
Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.
Ten obiekt zawiera kontekst miejsca do magazynowania.
W przypadku określenia tego parametru nie określaj parametru *kontekstu* .

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nazwa_udziału
Określa nazwę udziału plików.
To polecenie cmdlet przekazuje do pliku w udziale pliku ten parametr określa.

```yaml
Type: String
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
Type: String
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
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Remove-AzureStorageDirectory](./Remove-AzureStorageDirectory.md)

[Nowe — AzureStorageDirectory](./New-AzureStorageDirectory.md)

[Get-AzureStorageFileContent](./Get-AzureStorageFileContent.md)
