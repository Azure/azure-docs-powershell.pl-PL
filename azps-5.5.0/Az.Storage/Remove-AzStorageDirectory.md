---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
ms.openlocfilehash: 3ac8cb302c65fd42fdd699588b71bc1b081cc9d2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195714"
---
# <span data-ttu-id="4ce86-101">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="4ce86-101">Remove-AzStorageDirectory</span></span>

## <span data-ttu-id="4ce86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ce86-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce86-103">Usuwa katalog.</span><span class="sxs-lookup"><span data-stu-id="4ce86-103">Deletes a directory.</span></span>

## <span data-ttu-id="4ce86-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4ce86-104">SYNTAX</span></span>

### <span data-ttu-id="4ce86-105">ShareName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="4ce86-105">ShareName (Default)</span></span>
```
Remove-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ce86-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="4ce86-106">Share</span></span>
```
Remove-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ce86-107">Katalog</span><span class="sxs-lookup"><span data-stu-id="4ce86-107">Directory</span></span>
```
Remove-AzStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ce86-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4ce86-108">DESCRIPTION</span></span>
<span data-ttu-id="4ce86-109">Polecenie **cmdlet Remove-AzStorageDirectory** usuwa katalog.</span><span class="sxs-lookup"><span data-stu-id="4ce86-109">The **Remove-AzStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="4ce86-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4ce86-110">EXAMPLES</span></span>

### <span data-ttu-id="4ce86-111">Przykład 1. Usuwanie folderu</span><span class="sxs-lookup"><span data-stu-id="4ce86-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="4ce86-112">To polecenie usuwa folder o nazwie ContosoWorkingFolder z udziału plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="4ce86-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="4ce86-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ce86-113">PARAMETERS</span></span>

### <span data-ttu-id="4ce86-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4ce86-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4ce86-115">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="4ce86-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4ce86-116">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="4ce86-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4ce86-117">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="4ce86-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4ce86-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4ce86-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4ce86-119">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="4ce86-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4ce86-120">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="4ce86-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4ce86-121">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="4ce86-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4ce86-122">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="4ce86-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4ce86-123">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="4ce86-123">The default value is 10.</span></span>

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

### <span data-ttu-id="4ce86-124">— kontekst</span><span class="sxs-lookup"><span data-stu-id="4ce86-124">-Context</span></span>
<span data-ttu-id="4ce86-125">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4ce86-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4ce86-126">Aby uzyskać kontekst magazynowania, użyj polecenia cmdlet [New-azStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="4ce86-126">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4ce86-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce86-127">-DefaultProfile</span></span>
<span data-ttu-id="4ce86-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ce86-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ce86-129">— Katalog</span><span class="sxs-lookup"><span data-stu-id="4ce86-129">-Directory</span></span>
<span data-ttu-id="4ce86-130">Określa folder jako obiekt **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="4ce86-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="4ce86-131">To polecenie cmdlet usuwa folder, który jest określany przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="4ce86-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="4ce86-132">Aby uzyskać katalog, użyj polecenia cmdlet New-AzStorageDirectory cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ce86-132">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="4ce86-133">Aby uzyskać katalog, możesz również użyć polecenia cmdlet **Get-AzStorageFile.**</span><span class="sxs-lookup"><span data-stu-id="4ce86-133">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="4ce86-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ce86-134">-PassThru</span></span>
<span data-ttu-id="4ce86-135">Wskazuje, że jeśli to polecenie cmdlet zakończy się powodzeniem, zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="4ce86-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="4ce86-136">Jeśli określisz ten parametr, a jeśli polecenie cmdlet nie powiedzie się z powodu nieodpowiedniej wartości parametru _Path,_ polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="4ce86-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="4ce86-137">Jeśli nie określisz tego parametru, to polecenie cmdlet nie zwróci wartości.</span><span class="sxs-lookup"><span data-stu-id="4ce86-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4ce86-138">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="4ce86-138">-Path</span></span>
<span data-ttu-id="4ce86-139">Określa ścieżkę folderu.</span><span class="sxs-lookup"><span data-stu-id="4ce86-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="4ce86-140">Jeśli folder, który określa ten parametr, jest pusty, to polecenie cmdlet spowoduje usunięcie tego folderu.</span><span class="sxs-lookup"><span data-stu-id="4ce86-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="4ce86-141">Jeśli folder nie jest pusty, to polecenie cmdlet nie wprowadza żadnych zmian i zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="4ce86-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="4ce86-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4ce86-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4ce86-143">Określa długość okresu przeoencji dla części żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="4ce86-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4ce86-144">— Udostępnianie</span><span class="sxs-lookup"><span data-stu-id="4ce86-144">-Share</span></span>
<span data-ttu-id="4ce86-145">Określa obiekt **CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="4ce86-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="4ce86-146">To polecenie cmdlet usuwa folder w obszarze udziału plików, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="4ce86-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="4ce86-147">Aby uzyskać obiekt **CloudFileShare,** użyj Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ce86-147">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="4ce86-148">Ten obiekt zawiera kontekst przechowywania.</span><span class="sxs-lookup"><span data-stu-id="4ce86-148">This object contains the storage context.</span></span>
<span data-ttu-id="4ce86-149">Jeśli określisz ten parametr, nie określaj *parametru kontekstowego.*</span><span class="sxs-lookup"><span data-stu-id="4ce86-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="4ce86-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4ce86-150">-ShareName</span></span>
<span data-ttu-id="4ce86-151">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="4ce86-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="4ce86-152">To polecenie cmdlet usuwa folder w obszarze udziału plików, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="4ce86-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="4ce86-153">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ce86-153">-Confirm</span></span>
<span data-ttu-id="4ce86-154">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4ce86-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ce86-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ce86-155">-WhatIf</span></span>
<span data-ttu-id="4ce86-156">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ce86-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ce86-157">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4ce86-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ce86-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce86-158">CommonParameters</span></span>
<span data-ttu-id="4ce86-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ce86-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce86-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ce86-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce86-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ce86-161">INPUTS</span></span>

### <span data-ttu-id="4ce86-162">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="4ce86-162">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="4ce86-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="4ce86-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="4ce86-164">System.String</span><span class="sxs-lookup"><span data-stu-id="4ce86-164">System.String</span></span>

### <span data-ttu-id="4ce86-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4ce86-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4ce86-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ce86-166">OUTPUTS</span></span>

### <span data-ttu-id="4ce86-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="4ce86-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="4ce86-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4ce86-168">NOTES</span></span>

## <span data-ttu-id="4ce86-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ce86-169">RELATED LINKS</span></span>

[<span data-ttu-id="4ce86-170">Get-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="4ce86-170">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="4ce86-171">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4ce86-171">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="4ce86-172">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="4ce86-172">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)
