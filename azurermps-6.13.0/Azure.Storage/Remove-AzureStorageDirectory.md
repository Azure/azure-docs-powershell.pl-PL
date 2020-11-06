---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
ms.openlocfilehash: 6df60027ff2c25a8f2c1c948d04213cfc6d6158e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526434"
---
# <span data-ttu-id="10054-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="10054-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="10054-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10054-102">SYNOPSIS</span></span>
<span data-ttu-id="10054-103">Usuwa katalog.</span><span class="sxs-lookup"><span data-stu-id="10054-103">Deletes a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10054-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10054-104">SYNTAX</span></span>

### <span data-ttu-id="10054-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="10054-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10054-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="10054-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10054-107">Directory</span><span class="sxs-lookup"><span data-stu-id="10054-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10054-108">Opis</span><span class="sxs-lookup"><span data-stu-id="10054-108">DESCRIPTION</span></span>
<span data-ttu-id="10054-109">Polecenie cmdlet **Remove-AzureStorageDirectory** Usuwa katalog.</span><span class="sxs-lookup"><span data-stu-id="10054-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="10054-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10054-110">EXAMPLES</span></span>

### <span data-ttu-id="10054-111">Przykład 1. Usuń folder</span><span class="sxs-lookup"><span data-stu-id="10054-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="10054-112">To polecenie usuwa folder o nazwie ContosoWorkingFolder z udziału plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="10054-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="10054-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10054-113">PARAMETERS</span></span>

### <span data-ttu-id="10054-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="10054-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="10054-115">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="10054-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="10054-116">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="10054-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="10054-117">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="10054-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="10054-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="10054-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="10054-119">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="10054-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="10054-120">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="10054-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="10054-121">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="10054-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="10054-122">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="10054-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="10054-123">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="10054-123">The default value is 10.</span></span>

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

### <span data-ttu-id="10054-124">-Context</span><span class="sxs-lookup"><span data-stu-id="10054-124">-Context</span></span>
<span data-ttu-id="10054-125">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="10054-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="10054-126">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="10054-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="10054-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10054-127">-DefaultProfile</span></span>
<span data-ttu-id="10054-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="10054-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10054-129">-Directory</span><span class="sxs-lookup"><span data-stu-id="10054-129">-Directory</span></span>
<span data-ttu-id="10054-130">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="10054-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="10054-131">To polecenie cmdlet umożliwia usunięcie folderu, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="10054-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="10054-132">Aby uzyskać katalog, użyj polecenia cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="10054-132">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="10054-133">Aby uzyskać katalog, możesz również użyć polecenia cmdlet **Get-AzureStorageFile** .</span><span class="sxs-lookup"><span data-stu-id="10054-133">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="10054-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10054-134">-PassThru</span></span>
<span data-ttu-id="10054-135">Wskazuje, że jeśli to polecenie cmdlet powiedzie się, zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="10054-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="10054-136">Jeśli określisz ten parametr, a jeśli polecenie cmdlet nie powiodło się z powodu nieodpowiedniej wartości parametru _Path_ , polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="10054-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="10054-137">Jeśli nie podano tego parametru, to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="10054-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="10054-138">-Path</span><span class="sxs-lookup"><span data-stu-id="10054-138">-Path</span></span>
<span data-ttu-id="10054-139">Określa ścieżkę do folderu.</span><span class="sxs-lookup"><span data-stu-id="10054-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="10054-140">Jeśli folder, który określi ten parametr, jest pusty, to polecenie cmdlet usuwa ten folder.</span><span class="sxs-lookup"><span data-stu-id="10054-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="10054-141">Jeśli folder nie jest pusty, to polecenie cmdlet nie zmienia się i zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="10054-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10054-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="10054-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="10054-143">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="10054-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="10054-144">-Share</span><span class="sxs-lookup"><span data-stu-id="10054-144">-Share</span></span>
<span data-ttu-id="10054-145">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="10054-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="10054-146">To polecenie cmdlet usuwa folder w obszarze udział pliku, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="10054-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="10054-147">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="10054-147">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="10054-148">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="10054-148">This object contains the storage context.</span></span>
<span data-ttu-id="10054-149">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="10054-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="10054-150">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="10054-150">-ShareName</span></span>
<span data-ttu-id="10054-151">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="10054-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="10054-152">To polecenie cmdlet usuwa folder w obszarze udział pliku, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="10054-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="10054-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10054-153">-Confirm</span></span>
<span data-ttu-id="10054-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10054-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10054-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10054-155">-WhatIf</span></span>
<span data-ttu-id="10054-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10054-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10054-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="10054-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10054-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10054-158">CommonParameters</span></span>
<span data-ttu-id="10054-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10054-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10054-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10054-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10054-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10054-161">INPUTS</span></span>

### <span data-ttu-id="10054-162">Microsoft. platformy windowsazure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="10054-162">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="10054-163">Parametry: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="10054-163">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="10054-164">Microsoft. platformy windowsazure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="10054-164">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="10054-165">Parametry: katalog (ByValue)</span><span class="sxs-lookup"><span data-stu-id="10054-165">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="10054-166">System. String</span><span class="sxs-lookup"><span data-stu-id="10054-166">System.String</span></span>

### <span data-ttu-id="10054-167">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="10054-167">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="10054-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10054-168">OUTPUTS</span></span>

### <span data-ttu-id="10054-169">Microsoft. platformy windowsazure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="10054-169">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="10054-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10054-170">NOTES</span></span>

## <span data-ttu-id="10054-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10054-171">RELATED LINKS</span></span>

[<span data-ttu-id="10054-172">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="10054-172">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="10054-173">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="10054-173">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="10054-174">Nowe — AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="10054-174">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)
