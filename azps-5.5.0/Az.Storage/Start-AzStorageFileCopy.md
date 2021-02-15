---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 578c32a27f53f586ec8a8013533e42928df48d30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183139"
---
# <span data-ttu-id="3a009-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3a009-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="3a009-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a009-102">SYNOPSIS</span></span>
<span data-ttu-id="3a009-103">Zaczyna kopiowanie pliku źródłowego.</span><span class="sxs-lookup"><span data-stu-id="3a009-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="3a009-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3a009-104">SYNTAX</span></span>

### <span data-ttu-id="3a009-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="3a009-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a009-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3a009-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a009-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="3a009-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a009-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="3a009-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a009-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="3a009-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a009-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="3a009-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a009-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="3a009-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a009-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="3a009-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a009-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="3a009-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a009-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="3a009-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a009-115">OPIS</span><span class="sxs-lookup"><span data-stu-id="3a009-115">DESCRIPTION</span></span>
<span data-ttu-id="3a009-116">Polecenie **cmdlet Start-AzStorageFileCopy** zaczyna kopiować plik źródłowy do pliku docelowego.</span><span class="sxs-lookup"><span data-stu-id="3a009-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="3a009-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3a009-117">EXAMPLES</span></span>

### <span data-ttu-id="3a009-118">Przykład 1. Rozpoczynanie operacji kopiowania z pliku do pliku przy użyciu nazwy udostępniania i nazwy pliku</span><span class="sxs-lookup"><span data-stu-id="3a009-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="3a009-119">To polecenie uruchamia operację kopiowania z pliku do pliku.</span><span class="sxs-lookup"><span data-stu-id="3a009-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="3a009-120">Polecenie określa nazwę udziału i nazwę pliku</span><span class="sxs-lookup"><span data-stu-id="3a009-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="3a009-121">Przykład 2. Rozpoczynanie operacji kopiowania z obiektu blob do pliku przy użyciu nazwy kontenera i nazwy obiektu blob</span><span class="sxs-lookup"><span data-stu-id="3a009-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="3a009-122">To polecenie uruchamia operację kopiowania z obiektu blob do pliku.</span><span class="sxs-lookup"><span data-stu-id="3a009-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="3a009-123">Polecenie określa nazwę kontenera i nazwę obiektu blob</span><span class="sxs-lookup"><span data-stu-id="3a009-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="3a009-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a009-124">PARAMETERS</span></span>

### <span data-ttu-id="3a009-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="3a009-125">-AbsoluteUri</span></span>
<span data-ttu-id="3a009-126">Określa URI pliku źródłowego.</span><span class="sxs-lookup"><span data-stu-id="3a009-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="3a009-127">Jeśli lokalizacja źródłowa wymaga podania poświadczeń, musisz je podać.</span><span class="sxs-lookup"><span data-stu-id="3a009-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="3a009-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3a009-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3a009-129">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="3a009-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3a009-130">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="3a009-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3a009-131">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="3a009-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3a009-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3a009-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3a009-133">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="3a009-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3a009-134">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="3a009-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3a009-135">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="3a009-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3a009-136">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="3a009-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3a009-137">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="3a009-137">The default value is 10.</span></span>

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

### <span data-ttu-id="3a009-138">— kontekst</span><span class="sxs-lookup"><span data-stu-id="3a009-138">-Context</span></span>
<span data-ttu-id="3a009-139">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3a009-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="3a009-140">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a009-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3a009-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a009-141">-DefaultProfile</span></span>
<span data-ttu-id="3a009-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a009-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a009-143">- DestContext</span><span class="sxs-lookup"><span data-stu-id="3a009-143">-DestContext</span></span>
<span data-ttu-id="3a009-144">Określa kontekst magazynu platformy Azure dla miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="3a009-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="3a009-145">Aby uzyskać kontekst, użyj **new-azstorageContext.**</span><span class="sxs-lookup"><span data-stu-id="3a009-145">To obtain a context, use **New-AzStorageContext**.</span></span>

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

### <span data-ttu-id="3a009-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="3a009-146">-DestFile</span></span>
<span data-ttu-id="3a009-147">Określa obiekt **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="3a009-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="3a009-148">Możesz utworzyć plik w chmurze lub uzyskać go za pomocą Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a009-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a009-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="3a009-149">-DestFilePath</span></span>
<span data-ttu-id="3a009-150">Określa ścieżkę pliku docelowego względem udziału docelowego.</span><span class="sxs-lookup"><span data-stu-id="3a009-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="3a009-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="3a009-151">-DestShareName</span></span>
<span data-ttu-id="3a009-152">Określa nazwę udziału docelowego.</span><span class="sxs-lookup"><span data-stu-id="3a009-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="3a009-153">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3a009-153">-Force</span></span>
<span data-ttu-id="3a009-154">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3a009-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a009-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3a009-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3a009-156">Określa długość okresu przeoencji dla części żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="3a009-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3a009-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="3a009-157">-SrcBlob</span></span>
<span data-ttu-id="3a009-158">Określa obiekt **CloudBlob.**</span><span class="sxs-lookup"><span data-stu-id="3a009-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="3a009-159">Obiekt blob w chmurze można utworzyć lub uzyskać za pomocą Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a009-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a009-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="3a009-160">-SrcBlobName</span></span>
<span data-ttu-id="3a009-161">Określa nazwę źródłowego obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="3a009-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="3a009-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="3a009-162">-SrcContainer</span></span>
<span data-ttu-id="3a009-163">Określa obiekt kontenera obiektów blob w chmurze.</span><span class="sxs-lookup"><span data-stu-id="3a009-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="3a009-164">Możesz utworzyć obiekt kontener obiektów blob w chmurze lub użyć Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a009-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a009-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="3a009-165">-SrcContainerName</span></span>
<span data-ttu-id="3a009-166">Określa nazwę kontenera źródłowego.</span><span class="sxs-lookup"><span data-stu-id="3a009-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="3a009-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="3a009-167">-SrcFile</span></span>
<span data-ttu-id="3a009-168">Określa obiekt **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="3a009-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="3a009-169">Możesz utworzyć plik w chmurze lub uzyskać go za pomocą pliku **Get-AzStorageFile.**</span><span class="sxs-lookup"><span data-stu-id="3a009-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases: CloudFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a009-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="3a009-170">-SrcFilePath</span></span>
<span data-ttu-id="3a009-171">Określa ścieżkę pliku źródłowego względem katalogu źródłowego lub udziału źródłowego.</span><span class="sxs-lookup"><span data-stu-id="3a009-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="3a009-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="3a009-172">-SrcShare</span></span>
<span data-ttu-id="3a009-173">Określa obiekt udziału plików w chmurze.</span><span class="sxs-lookup"><span data-stu-id="3a009-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="3a009-174">Możesz utworzyć udział plików w chmurze lub go uzyskać za pomocą Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a009-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: CloudFileShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a009-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="3a009-175">-SrcShareName</span></span>
<span data-ttu-id="3a009-176">Określa nazwę udziału źródłowego.</span><span class="sxs-lookup"><span data-stu-id="3a009-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="3a009-177">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a009-177">-Confirm</span></span>
<span data-ttu-id="3a009-178">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3a009-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a009-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a009-179">-WhatIf</span></span>
<span data-ttu-id="3a009-180">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a009-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a009-181">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3a009-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a009-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a009-182">CommonParameters</span></span>
<span data-ttu-id="3a009-183">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a009-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a009-184">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a009-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a009-185">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a009-185">INPUTS</span></span>

### <span data-ttu-id="3a009-186">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="3a009-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="3a009-187">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="3a009-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="3a009-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3a009-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3a009-189">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3a009-189">OUTPUTS</span></span>

### <span data-ttu-id="3a009-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="3a009-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="3a009-191">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3a009-191">NOTES</span></span>

## <span data-ttu-id="3a009-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a009-192">RELATED LINKS</span></span>

[<span data-ttu-id="3a009-193">Get-AzstorageBlob</span><span class="sxs-lookup"><span data-stu-id="3a009-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="3a009-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3a009-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="3a009-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="3a009-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="3a009-196">Get-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="3a009-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="3a009-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="3a009-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="3a009-198">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3a009-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
