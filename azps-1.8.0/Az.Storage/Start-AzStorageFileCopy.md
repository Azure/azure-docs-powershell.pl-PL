---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: fb9574f90041961f47ef3a430f9512917a4c6dac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707489"
---
# <span data-ttu-id="2a8ef-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2a8ef-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="2a8ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a8ef-102">SYNOPSIS</span></span>
<span data-ttu-id="2a8ef-103">Rozpoczyna kopiowanie pliku źródłowego.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="2a8ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a8ef-104">SYNTAX</span></span>

### <span data-ttu-id="2a8ef-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="2a8ef-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a8ef-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2a8ef-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a8ef-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="2a8ef-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a8ef-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="2a8ef-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a8ef-109">Nazwaudziału</span><span class="sxs-lookup"><span data-stu-id="2a8ef-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a8ef-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="2a8ef-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a8ef-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="2a8ef-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a8ef-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="2a8ef-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a8ef-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="2a8ef-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a8ef-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="2a8ef-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a8ef-115">Opis</span><span class="sxs-lookup"><span data-stu-id="2a8ef-115">DESCRIPTION</span></span>
<span data-ttu-id="2a8ef-116">Polecenie cmdlet **Start-AzStorageFileCopy** rozpoczyna kopiowanie pliku źródłowego do pliku docelowego.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="2a8ef-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a8ef-117">EXAMPLES</span></span>

### <span data-ttu-id="2a8ef-118">Przykład 1: Rozpoczynanie operacji kopiowania z pliku do pliku przy użyciu nazwy udziału i nazwy pliku</span><span class="sxs-lookup"><span data-stu-id="2a8ef-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="2a8ef-119">To polecenie rozpoczyna operację kopiowania z pliku do pliku.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="2a8ef-120">Polecenie określa nazwę udziału i nazwę pliku</span><span class="sxs-lookup"><span data-stu-id="2a8ef-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="2a8ef-121">Przykład 2: Rozpoczynanie operacji kopiowania z obiektu BLOB do pliku przy użyciu nazwy kontenera i nazwy obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="2a8ef-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="2a8ef-122">To polecenie rozpoczyna operację kopiowania z obiektu BLOB do pliku.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="2a8ef-123">Polecenie określa nazwę kontenera i nazwę obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="2a8ef-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="2a8ef-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a8ef-124">PARAMETERS</span></span>

### <span data-ttu-id="2a8ef-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="2a8ef-125">-AbsoluteUri</span></span>
<span data-ttu-id="2a8ef-126">Określa identyfikator URI pliku źródłowego.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="2a8ef-127">Jeśli lokalizacja źródłowa wymaga poświadczenia, należy ją podać.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-127">If the source location requires a credential, you must provide one.</span></span>

```yaml
Type: System.String
Parameter Sets: UriToFilePath, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ef-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2a8ef-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2a8ef-129">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2a8ef-130">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2a8ef-131">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2a8ef-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2a8ef-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2a8ef-133">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2a8ef-134">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2a8ef-135">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2a8ef-136">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2a8ef-137">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-137">The default value is 10.</span></span>

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

### <span data-ttu-id="2a8ef-138">-Context</span><span class="sxs-lookup"><span data-stu-id="2a8ef-138">-Context</span></span>
<span data-ttu-id="2a8ef-139">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="2a8ef-140">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ShareName
Aliases: SrcContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ef-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a8ef-141">-DefaultProfile</span></span>
<span data-ttu-id="2a8ef-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a8ef-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="2a8ef-143">-DestContext</span></span>
<span data-ttu-id="2a8ef-144">Określa kontekst miejsca docelowego w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="2a8ef-145">Aby uzyskać kontekst, użyj funkcji **New-AzStorageContext**.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-145">To obtain a context, use **New-AzStorageContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ef-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="2a8ef-146">-DestFile</span></span>
<span data-ttu-id="2a8ef-147">Określa obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="2a8ef-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="2a8ef-148">Możesz utworzyć plik w chmurze lub uzyskać go za pomocą polecenia cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ef-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="2a8ef-149">-DestFilePath</span></span>
<span data-ttu-id="2a8ef-150">Określa ścieżkę pliku docelowego względem udziału docelowego.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-150">Specifies the path of the destination file relative to the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ef-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="2a8ef-151">-DestShareName</span></span>
<span data-ttu-id="2a8ef-152">Określa nazwę udziału docelowego.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-152">Specifies the name of the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ef-153">-Force</span><span class="sxs-lookup"><span data-stu-id="2a8ef-153">-Force</span></span>
<span data-ttu-id="2a8ef-154">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2a8ef-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2a8ef-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2a8ef-156">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="2a8ef-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="2a8ef-157">-SrcBlob</span></span>
<span data-ttu-id="2a8ef-158">Określa obiekt **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="2a8ef-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="2a8ef-159">Możesz utworzyć obiekt BLOB chmury lub uzyskać go za pomocą polecenia cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ef-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="2a8ef-160">-SrcBlobName</span></span>
<span data-ttu-id="2a8ef-161">Określa nazwę źródłowego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-161">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ef-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="2a8ef-162">-SrcContainer</span></span>
<span data-ttu-id="2a8ef-163">Określa obiekt kontenera obiektu BLOB chmury.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="2a8ef-164">Możesz utworzyć obiekt kontenera obiektu BLOB chmury lub użyć polecenia cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ef-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="2a8ef-165">-SrcContainerName</span></span>
<span data-ttu-id="2a8ef-166">Określa nazwę kontenera źródłowego.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-166">Specifies the name of the source container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ef-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="2a8ef-167">-SrcFile</span></span>
<span data-ttu-id="2a8ef-168">Określa obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="2a8ef-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="2a8ef-169">Możesz utworzyć plik w chmurze lub uzyskać go za pomocą polecenia **Get-AzStorageFile**.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ef-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="2a8ef-170">-SrcFilePath</span></span>
<span data-ttu-id="2a8ef-171">Określa ścieżkę pliku źródłowego względem katalogu źródłowego lub udziału źródłowego.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ef-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="2a8ef-172">-SrcShare</span></span>
<span data-ttu-id="2a8ef-173">Określa obiekt udostępniania plików w chmurze.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="2a8ef-174">Możesz utworzyć udział plików w chmurze lub uzyskać go za pomocą polecenia cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ef-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="2a8ef-175">-SrcShareName</span></span>
<span data-ttu-id="2a8ef-176">Określa nazwę udziału źródłowego.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-176">Specifies the name of the source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ef-177">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a8ef-177">-Confirm</span></span>
<span data-ttu-id="2a8ef-178">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a8ef-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a8ef-179">-WhatIf</span></span>
<span data-ttu-id="2a8ef-180">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a8ef-181">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a8ef-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a8ef-182">CommonParameters</span></span>
<span data-ttu-id="2a8ef-183">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a8ef-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a8ef-184">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a8ef-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a8ef-185">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a8ef-185">INPUTS</span></span>

### <span data-ttu-id="2a8ef-186">Microsoft. platformy windowsazure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2a8ef-186">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="2a8ef-187">Microsoft. platformy windowsazure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="2a8ef-187">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="2a8ef-188">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2a8ef-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2a8ef-189">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a8ef-189">OUTPUTS</span></span>

### <span data-ttu-id="2a8ef-190">System. void</span><span class="sxs-lookup"><span data-stu-id="2a8ef-190">System.Void</span></span>

## <span data-ttu-id="2a8ef-191">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a8ef-191">NOTES</span></span>

## <span data-ttu-id="2a8ef-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a8ef-192">RELATED LINKS</span></span>

[<span data-ttu-id="2a8ef-193">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2a8ef-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="2a8ef-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2a8ef-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="2a8ef-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="2a8ef-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="2a8ef-196">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="2a8ef-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="2a8ef-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="2a8ef-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="2a8ef-198">Zatrzymaj — AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2a8ef-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)