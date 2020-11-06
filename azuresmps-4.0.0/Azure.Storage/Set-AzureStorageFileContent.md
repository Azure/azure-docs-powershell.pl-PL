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
# <span data-ttu-id="bc899-101">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bc899-101">Set-AzureStorageFileContent</span></span>

## <span data-ttu-id="bc899-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc899-102">SYNOPSIS</span></span>
<span data-ttu-id="bc899-103">Umożliwia przekazywanie zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="bc899-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="bc899-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc899-104">SYNTAX</span></span>

### <span data-ttu-id="bc899-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="bc899-105">ShareName (Default)</span></span>
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc899-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="bc899-106">Share</span></span>
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc899-107">Directory</span><span class="sxs-lookup"><span data-stu-id="bc899-107">Directory</span></span>
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc899-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bc899-108">DESCRIPTION</span></span>
<span data-ttu-id="bc899-109">Polecenie cmdlet **Set-AzureStorageFileContent** umożliwia przekazywanie zawartości pliku do pliku w określonym udziale.</span><span class="sxs-lookup"><span data-stu-id="bc899-109">The **Set-AzureStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="bc899-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc899-110">EXAMPLES</span></span>

### <span data-ttu-id="bc899-111">Przykład 1: przekazywanie pliku w bieżącym folderze</span><span class="sxs-lookup"><span data-stu-id="bc899-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="bc899-112">To polecenie wysyła plik o nazwie DataFile37 w bieżącym folderze jako plik o nazwie CurrentDataFile w folderze o nazwie ContosoWorkingFolder.</span><span class="sxs-lookup"><span data-stu-id="bc899-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="bc899-113">Przykład 2: przekazywanie wszystkich plików w bieżącym folderze</span><span class="sxs-lookup"><span data-stu-id="bc899-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="bc899-114">W tym przykładzie użyto kilku typowych poleceń cmdlet programu Windows PowerShell i bieżącego polecenia cmdlet, aby przekazać wszystkie pliki z bieżącego folderu do folderu głównego kontenera ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="bc899-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>

<span data-ttu-id="bc899-115">Pierwsze polecenie uzyskuje nazwę bieżącego folderu i zapisuje je w zmiennej $CurrentFolder.</span><span class="sxs-lookup"><span data-stu-id="bc899-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>

<span data-ttu-id="bc899-116">Drugie polecenie używa polecenia cmdlet **Get-AzureStorageShare** w celu uzyskania udziału plików o nazwie ContosoShare06, a następnie zapisanie go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="bc899-116">The second command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="bc899-117">Polecenie ostatnie pobiera zawartość bieżącego folderu i przekazuje każdemu z nich do polecenia cmdlet Where-Object przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="bc899-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bc899-118">Polecenie cmdlet umożliwia filtrowanie obiektów, które nie są plikami, a następnie przekazanie plików do polecenia cmdlet ForEach-Object.</span><span class="sxs-lookup"><span data-stu-id="bc899-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="bc899-119">Polecenie cmdlet uruchamia blok skryptu dla każdego pliku, który tworzy odpowiednią ścieżkę, a następnie używa bieżącego polecenia cmdlet do przekazania pliku.</span><span class="sxs-lookup"><span data-stu-id="bc899-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="bc899-120">Wynik ma taką samą nazwę i taką samą położenie względne, co pozostałe pliki, które przykłada są ładowane.</span><span class="sxs-lookup"><span data-stu-id="bc899-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="bc899-121">Aby uzyskać więcej informacji na temat bloków skryptów, wpisz ciąg `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="bc899-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

## <span data-ttu-id="bc899-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc899-122">PARAMETERS</span></span>

### <span data-ttu-id="bc899-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bc899-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bc899-124">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="bc899-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bc899-125">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="bc899-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bc899-126">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="bc899-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bc899-127">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bc899-127">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bc899-128">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="bc899-128">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bc899-129">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="bc899-129">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bc899-130">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="bc899-130">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bc899-131">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="bc899-131">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bc899-132">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="bc899-132">The default value is 10.</span></span>

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

### <span data-ttu-id="bc899-133">-Context</span><span class="sxs-lookup"><span data-stu-id="bc899-133">-Context</span></span>
<span data-ttu-id="bc899-134">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="bc899-134">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bc899-135">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="bc899-135">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="bc899-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="bc899-136">-Directory</span></span>
<span data-ttu-id="bc899-137">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="bc899-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="bc899-138">To polecenie cmdlet umożliwia przekazanie pliku do folderu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="bc899-138">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="bc899-139">Aby uzyskać katalog, użyj polecenia cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="bc899-139">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="bc899-140">Możesz również użyć polecenia cmdlet Get-AzureStorageFile, aby uzyskać katalog.</span><span class="sxs-lookup"><span data-stu-id="bc899-140">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="bc899-141">-Force</span><span class="sxs-lookup"><span data-stu-id="bc899-141">-Force</span></span>
<span data-ttu-id="bc899-142">Wskazuje, że to polecenie cmdlet zastępuje istniejący plik magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bc899-142">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="bc899-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc899-143">-PassThru</span></span>
<span data-ttu-id="bc899-144">Wskazuje, że to polecenie cmdlet zwraca obiekt **AzureStorageFile** , który tworzy lub przekazuje.</span><span class="sxs-lookup"><span data-stu-id="bc899-144">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="bc899-145">-Path</span><span class="sxs-lookup"><span data-stu-id="bc899-145">-Path</span></span>
<span data-ttu-id="bc899-146">Określa ścieżkę do pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="bc899-146">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="bc899-147">To polecenie cmdlet umożliwia przekazywanie zawartości do pliku, który jest określany przez ten parametr, lub do pliku w folderze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="bc899-147">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="bc899-148">Jeśli określisz folder, to polecenie cmdlet utworzy plik mający taką samą nazwę jak plik źródłowy.</span><span class="sxs-lookup"><span data-stu-id="bc899-148">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>

<span data-ttu-id="bc899-149">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie jego zawartości w tym pliku.</span><span class="sxs-lookup"><span data-stu-id="bc899-149">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="bc899-150">Jeśli określisz plik, który już istnieje, i określisz parametr _Force_ , to polecenie cmdlet zastąpi zawartość pliku.</span><span class="sxs-lookup"><span data-stu-id="bc899-150">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="bc899-151">Jeśli określisz plik, który już istnieje, i nie określisz _siły_ , to polecenie cmdlet nie zmieni się i zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="bc899-151">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>

<span data-ttu-id="bc899-152">Jeśli określisz ścieżkę do folderu, który nie istnieje, to polecenie cmdlet nie zmieni się i zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="bc899-152">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>


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

### <span data-ttu-id="bc899-153">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bc899-153">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bc899-154">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="bc899-154">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="bc899-155">-Share</span><span class="sxs-lookup"><span data-stu-id="bc899-155">-Share</span></span>
<span data-ttu-id="bc899-156">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="bc899-156">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="bc899-157">To polecenie cmdlet przekazuje do pliku w udziale pliku ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="bc899-157">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="bc899-158">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="bc899-158">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="bc899-159">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="bc899-159">This object contains the storage context.</span></span>
<span data-ttu-id="bc899-160">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="bc899-160">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="bc899-161">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="bc899-161">-ShareName</span></span>
<span data-ttu-id="bc899-162">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="bc899-162">Specifies the name of the file share.</span></span>
<span data-ttu-id="bc899-163">To polecenie cmdlet przekazuje do pliku w udziale pliku ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="bc899-163">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="bc899-164">-Source</span><span class="sxs-lookup"><span data-stu-id="bc899-164">-Source</span></span>
<span data-ttu-id="bc899-165">Określa plik źródłowy, który jest wysyłany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc899-165">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="bc899-166">Jeśli określisz plik, który nie istnieje, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="bc899-166">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bc899-167">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bc899-167">-Confirm</span></span>
<span data-ttu-id="bc899-168">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc899-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc899-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc899-169">-WhatIf</span></span>
<span data-ttu-id="bc899-170">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc899-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc899-171">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bc899-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc899-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc899-172">CommonParameters</span></span>
<span data-ttu-id="bc899-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc899-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc899-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc899-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc899-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc899-175">INPUTS</span></span>

## <span data-ttu-id="bc899-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc899-176">OUTPUTS</span></span>

## <span data-ttu-id="bc899-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc899-177">NOTES</span></span>

## <span data-ttu-id="bc899-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc899-178">RELATED LINKS</span></span>

[<span data-ttu-id="bc899-179">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="bc899-179">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="bc899-180">Nowe — AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="bc899-180">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="bc899-181">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bc899-181">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)
