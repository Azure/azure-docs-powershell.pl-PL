---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: 99809e5115cb256b8e546334efce0e6e399be04f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195699"
---
# <span data-ttu-id="836e4-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="836e4-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="836e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="836e4-102">SYNOPSIS</span></span>
<span data-ttu-id="836e4-103">Usuwa plik.</span><span class="sxs-lookup"><span data-stu-id="836e4-103">Deletes a file.</span></span>

## <span data-ttu-id="836e4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="836e4-104">SYNTAX</span></span>

### <span data-ttu-id="836e4-105">ShareName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="836e4-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="836e4-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="836e4-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="836e4-107">Katalog</span><span class="sxs-lookup"><span data-stu-id="836e4-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="836e4-108">Plik</span><span class="sxs-lookup"><span data-stu-id="836e4-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="836e4-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="836e4-109">DESCRIPTION</span></span>
<span data-ttu-id="836e4-110">Polecenie cmdlet **Remove-AzStorageFile** usuwa plik.</span><span class="sxs-lookup"><span data-stu-id="836e4-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="836e4-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="836e4-111">EXAMPLES</span></span>

### <span data-ttu-id="836e4-112">Przykład 1. Usuwanie pliku z udziału plików</span><span class="sxs-lookup"><span data-stu-id="836e4-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="836e4-113">To polecenie usuwa plik o nazwie ContosoFile22 z udziału plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="836e4-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="836e4-114">Przykład 2. Uzyskiwanie pliku z udziału plików przy użyciu obiektu udziału plików</span><span class="sxs-lookup"><span data-stu-id="836e4-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="836e4-115">To polecenie używa polecenia cmdlet **Get-AzStorageShare** w celu uzyskania udziału plików o nazwie ContosoShare06, a następnie przekazuje ten obiekt do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="836e4-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="836e4-116">Bieżące polecenie usuwa plik o nazwie ContosoFile22 z pliku ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="836e4-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="836e4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="836e4-117">PARAMETERS</span></span>

### <span data-ttu-id="836e4-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="836e4-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="836e4-119">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="836e4-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="836e4-120">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="836e4-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="836e4-121">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="836e4-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="836e4-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="836e4-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="836e4-123">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="836e4-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="836e4-124">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="836e4-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="836e4-125">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="836e4-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="836e4-126">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="836e4-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="836e4-127">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="836e4-127">The default value is 10.</span></span>

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

### <span data-ttu-id="836e4-128">— kontekst</span><span class="sxs-lookup"><span data-stu-id="836e4-128">-Context</span></span>
<span data-ttu-id="836e4-129">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="836e4-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="836e4-130">Aby uzyskać kontekst magazynowania, użyj polecenia cmdlet [New-azStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="836e4-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="836e4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="836e4-131">-DefaultProfile</span></span>
<span data-ttu-id="836e4-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="836e4-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="836e4-133">— Katalog</span><span class="sxs-lookup"><span data-stu-id="836e4-133">-Directory</span></span>
<span data-ttu-id="836e4-134">Określa folder jako obiekt **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="836e4-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="836e4-135">To polecenie cmdlet usuwa plik z folderu, który jest określany przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="836e4-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="836e4-136">— Plik</span><span class="sxs-lookup"><span data-stu-id="836e4-136">-File</span></span>
<span data-ttu-id="836e4-137">Określa plik jako obiekt **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="836e4-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="836e4-138">To polecenie cmdlet usuwa plik, który jest określany przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="836e4-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="836e4-139">Aby uzyskać obiekt **CloudFile,** użyj Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="836e4-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="836e4-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="836e4-140">-PassThru</span></span>
<span data-ttu-id="836e4-141">Wskazuje, że to polecenie cmdlet zwraca **wartość** logiczną, która odzwierciedla sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="836e4-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="836e4-142">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="836e4-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="836e4-143">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="836e4-143">-Path</span></span>
<span data-ttu-id="836e4-144">Określa ścieżkę pliku.</span><span class="sxs-lookup"><span data-stu-id="836e4-144">Specifies the path of a file.</span></span>
<span data-ttu-id="836e4-145">To polecenie cmdlet usuwa plik, który jest określany przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="836e4-145">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="836e4-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="836e4-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="836e4-147">Określa długość okresu, przez który uchybnia część żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="836e4-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="836e4-148">— Udostępnij</span><span class="sxs-lookup"><span data-stu-id="836e4-148">-Share</span></span>
<span data-ttu-id="836e4-149">Określa obiekt **CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="836e4-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="836e4-150">To polecenie cmdlet usuwa plik z udziału, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="836e4-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="836e4-151">Aby uzyskać obiekt **CloudFileShare,** użyj Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="836e4-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="836e4-152">Ten obiekt zawiera kontekst przechowywania.</span><span class="sxs-lookup"><span data-stu-id="836e4-152">This object contains the storage context.</span></span>
<span data-ttu-id="836e4-153">Jeśli określisz ten parametr, nie określaj *parametru kontekstowego.*</span><span class="sxs-lookup"><span data-stu-id="836e4-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="836e4-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="836e4-154">-ShareName</span></span>
<span data-ttu-id="836e4-155">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="836e4-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="836e4-156">To polecenie cmdlet usuwa plik z udziału, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="836e4-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="836e4-157">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="836e4-157">-Confirm</span></span>
<span data-ttu-id="836e4-158">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="836e4-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="836e4-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="836e4-159">-WhatIf</span></span>
<span data-ttu-id="836e4-160">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="836e4-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="836e4-161">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="836e4-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="836e4-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="836e4-162">CommonParameters</span></span>
<span data-ttu-id="836e4-163">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="836e4-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="836e4-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="836e4-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="836e4-165">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="836e4-165">INPUTS</span></span>

### <span data-ttu-id="836e4-166">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="836e4-166">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="836e4-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="836e4-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="836e4-168">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="836e4-168">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="836e4-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="836e4-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="836e4-170">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="836e4-170">OUTPUTS</span></span>

### <span data-ttu-id="836e4-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="836e4-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="836e4-172">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="836e4-172">NOTES</span></span>

## <span data-ttu-id="836e4-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="836e4-173">RELATED LINKS</span></span>

[<span data-ttu-id="836e4-174">Get-AzstorageFile</span><span class="sxs-lookup"><span data-stu-id="836e4-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="836e4-175">Get-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="836e4-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="836e4-176">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="836e4-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
