---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
ms.openlocfilehash: 84192a4715087d5ae896067e02ab07ef27574410
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524765"
---
# <span data-ttu-id="7e3ec-101">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7e3ec-101">Set-AzureStorageFileContent</span></span>

## <span data-ttu-id="7e3ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e3ec-102">SYNOPSIS</span></span>
<span data-ttu-id="7e3ec-103">Umożliwia przekazywanie zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-103">Uploads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e3ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e3ec-104">SYNTAX</span></span>

### <span data-ttu-id="7e3ec-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7e3ec-105">ShareName (Default)</span></span>
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e3ec-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="7e3ec-106">Share</span></span>
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e3ec-107">Directory</span><span class="sxs-lookup"><span data-stu-id="7e3ec-107">Directory</span></span>
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e3ec-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7e3ec-108">DESCRIPTION</span></span>
<span data-ttu-id="7e3ec-109">Polecenie cmdlet **Set-AzureStorageFileContent** umożliwia przekazywanie zawartości pliku do pliku w określonym udziale.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-109">The **Set-AzureStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="7e3ec-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e3ec-110">EXAMPLES</span></span>

### <span data-ttu-id="7e3ec-111">Przykład 1: przekazywanie pliku w bieżącym folderze</span><span class="sxs-lookup"><span data-stu-id="7e3ec-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="7e3ec-112">To polecenie wysyła plik o nazwie DataFile37 w bieżącym folderze jako plik o nazwie CurrentDataFile w folderze o nazwie ContosoWorkingFolder.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="7e3ec-113">Przykład 2: przekazywanie wszystkich plików w bieżącym folderze</span><span class="sxs-lookup"><span data-stu-id="7e3ec-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="7e3ec-114">W tym przykładzie użyto kilku typowych poleceń cmdlet programu Windows PowerShell i bieżącego polecenia cmdlet, aby przekazać wszystkie pliki z bieżącego folderu do folderu głównego kontenera ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="7e3ec-115">Pierwsze polecenie uzyskuje nazwę bieżącego folderu i zapisuje je w zmiennej $CurrentFolder.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="7e3ec-116">Drugie polecenie używa polecenia cmdlet **Get-AzureStorageShare** w celu uzyskania udziału plików o nazwie ContosoShare06, a następnie zapisanie go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-116">The second command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="7e3ec-117">Polecenie ostatnie pobiera zawartość bieżącego folderu i przekazuje każdemu z nich do polecenia cmdlet Where-Object przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7e3ec-118">Polecenie cmdlet umożliwia filtrowanie obiektów, które nie są plikami, a następnie przekazanie plików do polecenia cmdlet ForEach-Object.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="7e3ec-119">Polecenie cmdlet uruchamia blok skryptu dla każdego pliku, który tworzy odpowiednią ścieżkę, a następnie używa bieżącego polecenia cmdlet do przekazania pliku.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="7e3ec-120">Wynik ma taką samą nazwę i taką samą położenie względne, co pozostałe pliki, które przykłada są ładowane.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="7e3ec-121">Aby uzyskać więcej informacji na temat bloków skryptów, wpisz ciąg `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="7e3ec-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

## <span data-ttu-id="7e3ec-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e3ec-122">PARAMETERS</span></span>

### <span data-ttu-id="7e3ec-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7e3ec-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7e3ec-124">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7e3ec-125">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7e3ec-126">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7e3ec-127">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7e3ec-127">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7e3ec-128">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-128">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7e3ec-129">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-129">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7e3ec-130">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-130">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7e3ec-131">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-131">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7e3ec-132">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-132">The default value is 10.</span></span>

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

### <span data-ttu-id="7e3ec-133">-Context</span><span class="sxs-lookup"><span data-stu-id="7e3ec-133">-Context</span></span>
<span data-ttu-id="7e3ec-134">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-134">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7e3ec-135">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="7e3ec-135">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="7e3ec-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e3ec-136">-DefaultProfile</span></span>
<span data-ttu-id="7e3ec-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e3ec-138">-Directory</span><span class="sxs-lookup"><span data-stu-id="7e3ec-138">-Directory</span></span>
<span data-ttu-id="7e3ec-139">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="7e3ec-139">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="7e3ec-140">To polecenie cmdlet umożliwia przekazanie pliku do folderu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-140">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="7e3ec-141">Aby uzyskać katalog, użyj polecenia cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-141">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="7e3ec-142">Możesz również użyć polecenia cmdlet Get-AzureStorageFile, aby uzyskać katalog.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-142">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e3ec-143">-Force</span><span class="sxs-lookup"><span data-stu-id="7e3ec-143">-Force</span></span>
<span data-ttu-id="7e3ec-144">Wskazuje, że to polecenie cmdlet zastępuje istniejący plik magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-144">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="7e3ec-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e3ec-145">-PassThru</span></span>
<span data-ttu-id="7e3ec-146">Wskazuje, że to polecenie cmdlet zwraca obiekt **AzureStorageFile** , który tworzy lub przekazuje.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-146">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="7e3ec-147">-Path</span><span class="sxs-lookup"><span data-stu-id="7e3ec-147">-Path</span></span>
<span data-ttu-id="7e3ec-148">Określa ścieżkę do pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-148">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="7e3ec-149">To polecenie cmdlet umożliwia przekazywanie zawartości do pliku, który jest określany przez ten parametr, lub do pliku w folderze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-149">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="7e3ec-150">Jeśli określisz folder, to polecenie cmdlet utworzy plik mający taką samą nazwę jak plik źródłowy.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-150">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="7e3ec-151">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie jego zawartości w tym pliku.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-151">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="7e3ec-152">Jeśli określisz plik, który już istnieje, i określisz parametr _Force_ , to polecenie cmdlet zastąpi zawartość pliku.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-152">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="7e3ec-153">Jeśli określisz plik, który już istnieje, i nie określisz _siły_ , to polecenie cmdlet nie zmieni się i zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-153">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="7e3ec-154">Jeśli określisz ścieżkę do folderu, który nie istnieje, to polecenie cmdlet nie zmieni się i zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-154">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="7e3ec-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7e3ec-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7e3ec-156">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7e3ec-157">-Share</span><span class="sxs-lookup"><span data-stu-id="7e3ec-157">-Share</span></span>
<span data-ttu-id="7e3ec-158">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="7e3ec-158">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="7e3ec-159">To polecenie cmdlet przekazuje do pliku w udziale pliku ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-159">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="7e3ec-160">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-160">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="7e3ec-161">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-161">This object contains the storage context.</span></span>
<span data-ttu-id="7e3ec-162">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="7e3ec-162">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e3ec-163">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="7e3ec-163">-ShareName</span></span>
<span data-ttu-id="7e3ec-164">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-164">Specifies the name of the file share.</span></span>
<span data-ttu-id="7e3ec-165">To polecenie cmdlet przekazuje do pliku w udziale pliku ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-165">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="7e3ec-166">-Source</span><span class="sxs-lookup"><span data-stu-id="7e3ec-166">-Source</span></span>
<span data-ttu-id="7e3ec-167">Określa plik źródłowy, który jest wysyłany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-167">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="7e3ec-168">Jeśli określisz plik, który nie istnieje, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-168">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7e3ec-169">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e3ec-169">-Confirm</span></span>
<span data-ttu-id="7e3ec-170">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e3ec-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e3ec-171">-WhatIf</span></span>
<span data-ttu-id="7e3ec-172">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e3ec-173">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e3ec-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e3ec-174">CommonParameters</span></span>
<span data-ttu-id="7e3ec-175">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e3ec-176">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e3ec-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e3ec-177">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e3ec-177">INPUTS</span></span>

### <span data-ttu-id="7e3ec-178">Microsoft. platformy windowsazure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="7e3ec-178">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="7e3ec-179">Parametry: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7e3ec-179">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="7e3ec-180">Microsoft. platformy windowsazure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="7e3ec-180">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="7e3ec-181">Parametry: katalog (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7e3ec-181">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="7e3ec-182">System. String</span><span class="sxs-lookup"><span data-stu-id="7e3ec-182">System.String</span></span>

### <span data-ttu-id="7e3ec-183">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7e3ec-183">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7e3ec-184">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e3ec-184">OUTPUTS</span></span>

### <span data-ttu-id="7e3ec-185">Microsoft. platformy windowsazure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="7e3ec-185">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="7e3ec-186">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e3ec-186">NOTES</span></span>

## <span data-ttu-id="7e3ec-187">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e3ec-187">RELATED LINKS</span></span>

[<span data-ttu-id="7e3ec-188">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="7e3ec-188">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="7e3ec-189">Nowe — AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="7e3ec-189">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="7e3ec-190">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7e3ec-190">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)