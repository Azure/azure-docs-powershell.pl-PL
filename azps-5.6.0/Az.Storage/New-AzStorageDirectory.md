---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: 6f44f1545eea4e515064873cdc77f8b34819fabc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002474"
---
# <span data-ttu-id="2561e-101">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="2561e-101">New-AzStorageDirectory</span></span>

## <span data-ttu-id="2561e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2561e-102">SYNOPSIS</span></span>
<span data-ttu-id="2561e-103">Tworzy katalog.</span><span class="sxs-lookup"><span data-stu-id="2561e-103">Creates a directory.</span></span>

## <span data-ttu-id="2561e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2561e-104">SYNTAX</span></span>

### <span data-ttu-id="2561e-105">ShareName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="2561e-105">ShareName (Default)</span></span>
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2561e-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="2561e-106">Share</span></span>
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="2561e-107">Katalog</span><span class="sxs-lookup"><span data-stu-id="2561e-107">Directory</span></span>
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="2561e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="2561e-108">DESCRIPTION</span></span>
<span data-ttu-id="2561e-109">Polecenie cmdlet **New-AzStorageDirectory** tworzy katalog.</span><span class="sxs-lookup"><span data-stu-id="2561e-109">The **New-AzStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="2561e-110">To polecenie cmdlet zwraca obiekt **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="2561e-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="2561e-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2561e-111">EXAMPLES</span></span>

### <span data-ttu-id="2561e-112">Przykład 1. Tworzenie folderu w udziału plików</span><span class="sxs-lookup"><span data-stu-id="2561e-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="2561e-113">To polecenie tworzy folder o nazwie ContosoWorkingFolder w udostępnionym pliku o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="2561e-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="2561e-114">Przykład 2. Tworzenie folderu w udziału plików określonym w obiekcie udziału plików</span><span class="sxs-lookup"><span data-stu-id="2561e-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="2561e-115">To polecenie używa polecenia cmdlet **Get-AzStorageShare** w celu uzyskania udziału plików o nazwie ContosoShare06, a następnie przekazuje go do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="2561e-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2561e-116">Bieżące polecenie cmdlet tworzy folder o nazwie ContosoWorkingFolder w programie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="2561e-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="2561e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2561e-117">PARAMETERS</span></span>

### <span data-ttu-id="2561e-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2561e-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2561e-119">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="2561e-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2561e-120">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="2561e-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2561e-121">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="2561e-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2561e-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2561e-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2561e-123">Określa maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="2561e-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2561e-124">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="2561e-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2561e-125">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="2561e-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2561e-126">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="2561e-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2561e-127">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="2561e-127">The default value is 10.</span></span>

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

### <span data-ttu-id="2561e-128">— kontekst</span><span class="sxs-lookup"><span data-stu-id="2561e-128">-Context</span></span>
<span data-ttu-id="2561e-129">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2561e-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2561e-130">Aby uzyskać kontekst przechowywania, użyj polecenia cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="2561e-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="2561e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2561e-131">-DefaultProfile</span></span>
<span data-ttu-id="2561e-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2561e-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2561e-133">— Katalog</span><span class="sxs-lookup"><span data-stu-id="2561e-133">-Directory</span></span>
<span data-ttu-id="2561e-134">Określa folder jako obiekt **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="2561e-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="2561e-135">To polecenie cmdlet tworzy folder w lokalizacji, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="2561e-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="2561e-136">Aby uzyskać katalog, użyj polecenia cmdlet New-AzStorageDirectory cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2561e-136">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="2561e-137">Możesz również użyć polecenia cmdlet Get-AzStorageFile, aby uzyskać katalog.</span><span class="sxs-lookup"><span data-stu-id="2561e-137">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="2561e-138">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="2561e-138">-Path</span></span>
<span data-ttu-id="2561e-139">Określa ścieżkę folderu.</span><span class="sxs-lookup"><span data-stu-id="2561e-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="2561e-140">To polecenie cmdlet tworzy folder dla ścieżki, którą określa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2561e-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2561e-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2561e-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2561e-142">Określa długość okresu przeoencji dla części żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="2561e-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="2561e-143">— Udostępnij</span><span class="sxs-lookup"><span data-stu-id="2561e-143">-Share</span></span>
<span data-ttu-id="2561e-144">Określa obiekt **CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="2561e-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="2561e-145">To polecenie cmdlet tworzy w udziału plików folder, który jest określany przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="2561e-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="2561e-146">Aby uzyskać obiekt **CloudFileShare,** użyj Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2561e-146">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="2561e-147">Ten obiekt zawiera kontekst przechowywania.</span><span class="sxs-lookup"><span data-stu-id="2561e-147">This object contains the storage context.</span></span>
<span data-ttu-id="2561e-148">Jeśli określisz ten parametr, nie określaj *parametru kontekstowego.*</span><span class="sxs-lookup"><span data-stu-id="2561e-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="2561e-149">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2561e-149">-ShareName</span></span>
<span data-ttu-id="2561e-150">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="2561e-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="2561e-151">To polecenie cmdlet tworzy w udziału plików folder, który jest określany przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="2561e-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="2561e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2561e-152">CommonParameters</span></span>
<span data-ttu-id="2561e-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2561e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2561e-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2561e-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2561e-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2561e-155">INPUTS</span></span>

### <span data-ttu-id="2561e-156">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="2561e-156">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="2561e-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="2561e-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="2561e-158">System.String</span><span class="sxs-lookup"><span data-stu-id="2561e-158">System.String</span></span>

### <span data-ttu-id="2561e-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2561e-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2561e-160">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2561e-160">OUTPUTS</span></span>

### <span data-ttu-id="2561e-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="2561e-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="2561e-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2561e-162">NOTES</span></span>

## <span data-ttu-id="2561e-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2561e-163">RELATED LINKS</span></span>

[<span data-ttu-id="2561e-164">Get-AzstorageFile</span><span class="sxs-lookup"><span data-stu-id="2561e-164">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="2561e-165">Get-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="2561e-165">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="2561e-166">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2561e-166">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="2561e-167">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="2561e-167">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="2561e-168">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="2561e-168">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)
