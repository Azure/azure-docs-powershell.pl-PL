---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
ms.openlocfilehash: 87e8792697093182d3ccd36d75ac072239f76e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977969"
---
# <span data-ttu-id="13b80-101">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="13b80-101">Remove-AzStorageDirectory</span></span>

## <span data-ttu-id="13b80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13b80-102">SYNOPSIS</span></span>
<span data-ttu-id="13b80-103">Usuwa katalog.</span><span class="sxs-lookup"><span data-stu-id="13b80-103">Deletes a directory.</span></span>

## <span data-ttu-id="13b80-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="13b80-104">SYNTAX</span></span>

### <span data-ttu-id="13b80-105">ShareName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="13b80-105">ShareName (Default)</span></span>
```
Remove-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13b80-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="13b80-106">Share</span></span>
```
Remove-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13b80-107">Katalog</span><span class="sxs-lookup"><span data-stu-id="13b80-107">Directory</span></span>
```
Remove-AzStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13b80-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="13b80-108">DESCRIPTION</span></span>
<span data-ttu-id="13b80-109">Polecenie **cmdlet Remove-AzStorageDirectory** usuwa katalog.</span><span class="sxs-lookup"><span data-stu-id="13b80-109">The **Remove-AzStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="13b80-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="13b80-110">EXAMPLES</span></span>

### <span data-ttu-id="13b80-111">Przykład 1. Usuwanie folderu</span><span class="sxs-lookup"><span data-stu-id="13b80-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="13b80-112">To polecenie usuwa folder o nazwie ContosoWorkingFolder z udziału plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="13b80-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="13b80-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13b80-113">PARAMETERS</span></span>

### <span data-ttu-id="13b80-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="13b80-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="13b80-115">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="13b80-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="13b80-116">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="13b80-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="13b80-117">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="13b80-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="13b80-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="13b80-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="13b80-119">Określa maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="13b80-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="13b80-120">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="13b80-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="13b80-121">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="13b80-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="13b80-122">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="13b80-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="13b80-123">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="13b80-123">The default value is 10.</span></span>

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

### <span data-ttu-id="13b80-124">— kontekst</span><span class="sxs-lookup"><span data-stu-id="13b80-124">-Context</span></span>
<span data-ttu-id="13b80-125">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="13b80-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="13b80-126">Aby uzyskać kontekst przechowywania, użyj polecenia cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="13b80-126">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="13b80-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13b80-127">-DefaultProfile</span></span>
<span data-ttu-id="13b80-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="13b80-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13b80-129">— Katalog</span><span class="sxs-lookup"><span data-stu-id="13b80-129">-Directory</span></span>
<span data-ttu-id="13b80-130">Określa folder jako obiekt **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="13b80-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="13b80-131">To polecenie cmdlet usuwa folder, który jest określany przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="13b80-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="13b80-132">Aby uzyskać katalog, użyj polecenia cmdlet New-AzStorageDirectory cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13b80-132">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="13b80-133">Aby uzyskać katalog, możesz również użyć polecenia cmdlet **Get-AzStorageFile.**</span><span class="sxs-lookup"><span data-stu-id="13b80-133">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="13b80-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13b80-134">-PassThru</span></span>
<span data-ttu-id="13b80-135">Wskazuje, że jeśli to polecenie cmdlet zakończy się powodzeniem, zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="13b80-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="13b80-136">Jeśli określisz ten parametr, a jeśli polecenie cmdlet nie powiedzie się z powodu nieodpowiedniej wartości parametru _Path,_ polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="13b80-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="13b80-137">Jeśli nie określisz tego parametru, to polecenie cmdlet nie zwróci wartości.</span><span class="sxs-lookup"><span data-stu-id="13b80-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="13b80-138">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="13b80-138">-Path</span></span>
<span data-ttu-id="13b80-139">Określa ścieżkę folderu.</span><span class="sxs-lookup"><span data-stu-id="13b80-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="13b80-140">Jeśli folder, który określa ten parametr, jest pusty, to polecenie cmdlet spowoduje usunięcie tego folderu.</span><span class="sxs-lookup"><span data-stu-id="13b80-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="13b80-141">Jeśli folder nie jest pusty, to polecenie cmdlet nie wprowadza żadnych zmian i zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="13b80-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="13b80-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="13b80-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="13b80-143">Określa długość okresu przeoencji dla części żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="13b80-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="13b80-144">— Udostępnij</span><span class="sxs-lookup"><span data-stu-id="13b80-144">-Share</span></span>
<span data-ttu-id="13b80-145">Określa obiekt **CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="13b80-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="13b80-146">To polecenie cmdlet usuwa folder w obszarze udziału plików, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="13b80-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="13b80-147">Aby uzyskać obiekt **CloudFileShare,** użyj Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13b80-147">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="13b80-148">Ten obiekt zawiera kontekst przechowywania.</span><span class="sxs-lookup"><span data-stu-id="13b80-148">This object contains the storage context.</span></span>
<span data-ttu-id="13b80-149">Jeśli określisz ten parametr, nie określaj *parametru kontekstowego.*</span><span class="sxs-lookup"><span data-stu-id="13b80-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="13b80-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="13b80-150">-ShareName</span></span>
<span data-ttu-id="13b80-151">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="13b80-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="13b80-152">To polecenie cmdlet usuwa folder w obszarze udziału plików, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="13b80-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="13b80-153">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13b80-153">-Confirm</span></span>
<span data-ttu-id="13b80-154">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="13b80-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13b80-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13b80-155">-WhatIf</span></span>
<span data-ttu-id="13b80-156">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13b80-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13b80-157">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="13b80-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13b80-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b80-158">CommonParameters</span></span>
<span data-ttu-id="13b80-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13b80-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b80-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13b80-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b80-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13b80-161">INPUTS</span></span>

### <span data-ttu-id="13b80-162">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="13b80-162">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="13b80-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="13b80-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="13b80-164">System.String</span><span class="sxs-lookup"><span data-stu-id="13b80-164">System.String</span></span>

### <span data-ttu-id="13b80-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="13b80-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="13b80-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13b80-166">OUTPUTS</span></span>

### <span data-ttu-id="13b80-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="13b80-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="13b80-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="13b80-168">NOTES</span></span>

## <span data-ttu-id="13b80-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13b80-169">RELATED LINKS</span></span>

[<span data-ttu-id="13b80-170">Get-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="13b80-170">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="13b80-171">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="13b80-171">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="13b80-172">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="13b80-172">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)
