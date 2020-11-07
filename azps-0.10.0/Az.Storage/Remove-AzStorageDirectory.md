---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
ms.openlocfilehash: 0668f82d8bc121d3a38f9cacc236b04d3995df0f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892085"
---
# <span data-ttu-id="2844e-101">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="2844e-101">Remove-AzStorageDirectory</span></span>

## <span data-ttu-id="2844e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2844e-102">SYNOPSIS</span></span>
<span data-ttu-id="2844e-103">Usuwa katalog.</span><span class="sxs-lookup"><span data-stu-id="2844e-103">Deletes a directory.</span></span>

## <span data-ttu-id="2844e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2844e-104">SYNTAX</span></span>

### <span data-ttu-id="2844e-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2844e-105">ShareName (Default)</span></span>
```
Remove-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2844e-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="2844e-106">Share</span></span>
```
Remove-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2844e-107">Directory</span><span class="sxs-lookup"><span data-stu-id="2844e-107">Directory</span></span>
```
Remove-AzStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2844e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2844e-108">DESCRIPTION</span></span>
<span data-ttu-id="2844e-109">Polecenie cmdlet **Remove-AzStorageDirectory** Usuwa katalog.</span><span class="sxs-lookup"><span data-stu-id="2844e-109">The **Remove-AzStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="2844e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2844e-110">EXAMPLES</span></span>

### <span data-ttu-id="2844e-111">Przykład 1. Usuń folder</span><span class="sxs-lookup"><span data-stu-id="2844e-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="2844e-112">To polecenie usuwa folder o nazwie ContosoWorkingFolder z udziału plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="2844e-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="2844e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2844e-113">PARAMETERS</span></span>

### <span data-ttu-id="2844e-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2844e-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2844e-115">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="2844e-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2844e-116">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="2844e-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2844e-117">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="2844e-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2844e-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2844e-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2844e-119">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="2844e-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2844e-120">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="2844e-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2844e-121">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="2844e-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2844e-122">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="2844e-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2844e-123">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="2844e-123">The default value is 10.</span></span>

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

### <span data-ttu-id="2844e-124">-Context</span><span class="sxs-lookup"><span data-stu-id="2844e-124">-Context</span></span>
<span data-ttu-id="2844e-125">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2844e-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2844e-126">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="2844e-126">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="2844e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2844e-127">-DefaultProfile</span></span>
<span data-ttu-id="2844e-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2844e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2844e-129">-Directory</span><span class="sxs-lookup"><span data-stu-id="2844e-129">-Directory</span></span>
<span data-ttu-id="2844e-130">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="2844e-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="2844e-131">To polecenie cmdlet umożliwia usunięcie folderu, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="2844e-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="2844e-132">Aby uzyskać katalog, użyj polecenia cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="2844e-132">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="2844e-133">Aby uzyskać katalog, możesz również użyć polecenia cmdlet **Get-AzStorageFile** .</span><span class="sxs-lookup"><span data-stu-id="2844e-133">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="2844e-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2844e-134">-PassThru</span></span>
<span data-ttu-id="2844e-135">Wskazuje, że jeśli to polecenie cmdlet powiedzie się, zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="2844e-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="2844e-136">Jeśli określisz ten parametr, a jeśli polecenie cmdlet nie powiodło się z powodu nieodpowiedniej wartości parametru _Path_ , polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="2844e-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="2844e-137">Jeśli nie podano tego parametru, to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="2844e-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="2844e-138">-Path</span><span class="sxs-lookup"><span data-stu-id="2844e-138">-Path</span></span>
<span data-ttu-id="2844e-139">Określa ścieżkę do folderu.</span><span class="sxs-lookup"><span data-stu-id="2844e-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="2844e-140">Jeśli folder, który określi ten parametr, jest pusty, to polecenie cmdlet usuwa ten folder.</span><span class="sxs-lookup"><span data-stu-id="2844e-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="2844e-141">Jeśli folder nie jest pusty, to polecenie cmdlet nie zmienia się i zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="2844e-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="2844e-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2844e-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2844e-143">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="2844e-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="2844e-144">-Share</span><span class="sxs-lookup"><span data-stu-id="2844e-144">-Share</span></span>
<span data-ttu-id="2844e-145">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="2844e-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="2844e-146">To polecenie cmdlet usuwa folder w obszarze udział pliku, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="2844e-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="2844e-147">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="2844e-147">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="2844e-148">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="2844e-148">This object contains the storage context.</span></span>
<span data-ttu-id="2844e-149">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="2844e-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="2844e-150">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="2844e-150">-ShareName</span></span>
<span data-ttu-id="2844e-151">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="2844e-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="2844e-152">To polecenie cmdlet usuwa folder w obszarze udział pliku, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="2844e-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="2844e-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2844e-153">-Confirm</span></span>
<span data-ttu-id="2844e-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2844e-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2844e-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2844e-155">-WhatIf</span></span>
<span data-ttu-id="2844e-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2844e-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2844e-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2844e-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2844e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2844e-158">CommonParameters</span></span>
<span data-ttu-id="2844e-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2844e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2844e-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2844e-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2844e-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2844e-161">INPUTS</span></span>

### <span data-ttu-id="2844e-162">Microsoft. WindowsAz. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="2844e-162">Microsoft.WindowsAz.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="2844e-163">Parametry: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2844e-163">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="2844e-164">Microsoft. WindowsAz. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="2844e-164">Microsoft.WindowsAz.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="2844e-165">Parametry: katalog (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2844e-165">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="2844e-166">System. String</span><span class="sxs-lookup"><span data-stu-id="2844e-166">System.String</span></span>

### <span data-ttu-id="2844e-167">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2844e-167">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2844e-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2844e-168">OUTPUTS</span></span>

### <span data-ttu-id="2844e-169">Microsoft. WindowsAz. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="2844e-169">Microsoft.WindowsAz.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="2844e-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2844e-170">NOTES</span></span>

## <span data-ttu-id="2844e-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2844e-171">RELATED LINKS</span></span>

[<span data-ttu-id="2844e-172">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="2844e-172">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="2844e-173">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2844e-173">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="2844e-174">Nowe — AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="2844e-174">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)
