---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
ms.openlocfilehash: 7d015a9f3255672e0de0c85a5ff8390bc3cde68e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050466"
---
# <span data-ttu-id="c948e-101">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c948e-101">Stop-AzStorageFileCopy</span></span>

## <span data-ttu-id="c948e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c948e-102">SYNOPSIS</span></span>
<span data-ttu-id="c948e-103">Zatrzymuje operację kopiowania w określonym pliku docelowym.</span><span class="sxs-lookup"><span data-stu-id="c948e-103">Stops a copy operation to the specified destination file.</span></span>

## <span data-ttu-id="c948e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c948e-104">SYNTAX</span></span>

### <span data-ttu-id="c948e-105">Nazwaudziału</span><span class="sxs-lookup"><span data-stu-id="c948e-105">ShareName</span></span>
```
Stop-AzStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c948e-106">Plik</span><span class="sxs-lookup"><span data-stu-id="c948e-106">File</span></span>
```
Stop-AzStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c948e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c948e-107">DESCRIPTION</span></span>
<span data-ttu-id="c948e-108">Polecenie cmdlet **stop-AzStorageFileCopy** zatrzymuje kopiowanie pliku do pliku docelowego.</span><span class="sxs-lookup"><span data-stu-id="c948e-108">The **Stop-AzStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="c948e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c948e-109">EXAMPLES</span></span>

### <span data-ttu-id="c948e-110">Przykład 1: zatrzymanie operacji kopiowania</span><span class="sxs-lookup"><span data-stu-id="c948e-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="c948e-111">To polecenie zatrzymuje kopiowanie pliku o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="c948e-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="c948e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c948e-112">PARAMETERS</span></span>

### <span data-ttu-id="c948e-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c948e-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c948e-114">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="c948e-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c948e-115">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="c948e-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c948e-116">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="c948e-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c948e-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c948e-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c948e-118">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c948e-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c948e-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c948e-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c948e-120">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="c948e-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c948e-121">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="c948e-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c948e-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="c948e-122">The default value is 10.</span></span>

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

### <span data-ttu-id="c948e-123">-Context</span><span class="sxs-lookup"><span data-stu-id="c948e-123">-Context</span></span>
<span data-ttu-id="c948e-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c948e-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c948e-125">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="c948e-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c948e-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="c948e-126">-CopyId</span></span>
<span data-ttu-id="c948e-127">Określa identyfikator operacji kopiowania.</span><span class="sxs-lookup"><span data-stu-id="c948e-127">Specifies the ID of the copy operation.</span></span>

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

### <span data-ttu-id="c948e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c948e-128">-DefaultProfile</span></span>
<span data-ttu-id="c948e-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c948e-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c948e-130">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="c948e-130">-File</span></span>
<span data-ttu-id="c948e-131">Określa obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="c948e-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="c948e-132">Możesz utworzyć plik w chmurze lub uzyskać go za pomocą polecenia cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="c948e-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c948e-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="c948e-133">-FilePath</span></span>
<span data-ttu-id="c948e-134">Określa ścieżkę pliku.</span><span class="sxs-lookup"><span data-stu-id="c948e-134">Specifies the path of a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c948e-135">-Force</span><span class="sxs-lookup"><span data-stu-id="c948e-135">-Force</span></span>
<span data-ttu-id="c948e-136">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c948e-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c948e-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c948e-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c948e-138">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="c948e-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c948e-139">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="c948e-139">-ShareName</span></span>
<span data-ttu-id="c948e-140">Określa nazwę udziału.</span><span class="sxs-lookup"><span data-stu-id="c948e-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="c948e-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c948e-141">-Confirm</span></span>
<span data-ttu-id="c948e-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c948e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c948e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c948e-143">-WhatIf</span></span>
<span data-ttu-id="c948e-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c948e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c948e-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c948e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c948e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c948e-146">CommonParameters</span></span>
<span data-ttu-id="c948e-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c948e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c948e-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c948e-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c948e-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c948e-149">INPUTS</span></span>

### <span data-ttu-id="c948e-150">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="c948e-150">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="c948e-151">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c948e-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c948e-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c948e-152">OUTPUTS</span></span>

### <span data-ttu-id="c948e-153">System. void</span><span class="sxs-lookup"><span data-stu-id="c948e-153">System.Void</span></span>

## <span data-ttu-id="c948e-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c948e-154">NOTES</span></span>

## <span data-ttu-id="c948e-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c948e-155">RELATED LINKS</span></span>

[<span data-ttu-id="c948e-156">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="c948e-156">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="c948e-157">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="c948e-157">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="c948e-158">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c948e-158">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="c948e-159">Start — AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c948e-159">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)
