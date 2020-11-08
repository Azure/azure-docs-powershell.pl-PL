---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: 99809e5115cb256b8e546334efce0e6e399be04f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224772"
---
# <span data-ttu-id="3967b-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="3967b-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="3967b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3967b-102">SYNOPSIS</span></span>
<span data-ttu-id="3967b-103">Usuwa plik.</span><span class="sxs-lookup"><span data-stu-id="3967b-103">Deletes a file.</span></span>

## <span data-ttu-id="3967b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3967b-104">SYNTAX</span></span>

### <span data-ttu-id="3967b-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3967b-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3967b-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="3967b-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3967b-107">Directory</span><span class="sxs-lookup"><span data-stu-id="3967b-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3967b-108">Plik</span><span class="sxs-lookup"><span data-stu-id="3967b-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3967b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3967b-109">DESCRIPTION</span></span>
<span data-ttu-id="3967b-110">Polecenie cmdlet **Remove-AzStorageFile** usuwa plik.</span><span class="sxs-lookup"><span data-stu-id="3967b-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="3967b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3967b-111">EXAMPLES</span></span>

### <span data-ttu-id="3967b-112">Przykład 1: usuwanie pliku z udziału plików</span><span class="sxs-lookup"><span data-stu-id="3967b-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="3967b-113">To polecenie usuwa plik o nazwie ContosoFile22 z udziału plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="3967b-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="3967b-114">Przykład 2: uzyskiwanie pliku z udziału plików za pomocą obiektu udostępniania plików</span><span class="sxs-lookup"><span data-stu-id="3967b-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="3967b-115">To polecenie korzysta z polecenia cmdlet **Get-AzStorageShare** w celu uzyskania udziału plików o nazwie ContosoShare06, a następnie przekazanie tego obiektu do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="3967b-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3967b-116">Bieżące polecenie usuwa plik o nazwie ContosoFile22 z ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="3967b-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="3967b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3967b-117">PARAMETERS</span></span>

### <span data-ttu-id="3967b-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3967b-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3967b-119">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="3967b-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3967b-120">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="3967b-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3967b-121">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="3967b-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3967b-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3967b-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3967b-123">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="3967b-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3967b-124">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="3967b-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3967b-125">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="3967b-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3967b-126">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="3967b-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3967b-127">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="3967b-127">The default value is 10.</span></span>

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

### <span data-ttu-id="3967b-128">-Context</span><span class="sxs-lookup"><span data-stu-id="3967b-128">-Context</span></span>
<span data-ttu-id="3967b-129">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="3967b-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3967b-130">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="3967b-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="3967b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3967b-131">-DefaultProfile</span></span>
<span data-ttu-id="3967b-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3967b-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3967b-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="3967b-133">-Directory</span></span>
<span data-ttu-id="3967b-134">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="3967b-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="3967b-135">To polecenie cmdlet usuwa plik znajdujący się w folderze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="3967b-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="3967b-136">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="3967b-136">-File</span></span>
<span data-ttu-id="3967b-137">Określa plik jako obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="3967b-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="3967b-138">To polecenie cmdlet umożliwia usunięcie pliku, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="3967b-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="3967b-139">Aby uzyskać obiekt **CloudFile** , użyj polecenia cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="3967b-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="3967b-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3967b-140">-PassThru</span></span>
<span data-ttu-id="3967b-141">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="3967b-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="3967b-142">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="3967b-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="3967b-143">-Path</span><span class="sxs-lookup"><span data-stu-id="3967b-143">-Path</span></span>
<span data-ttu-id="3967b-144">Określa ścieżkę pliku.</span><span class="sxs-lookup"><span data-stu-id="3967b-144">Specifies the path of a file.</span></span>
<span data-ttu-id="3967b-145">To polecenie cmdlet usuwa plik, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="3967b-145">This cmdlet deletes the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="3967b-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3967b-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3967b-147">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="3967b-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3967b-148">-Share</span><span class="sxs-lookup"><span data-stu-id="3967b-148">-Share</span></span>
<span data-ttu-id="3967b-149">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="3967b-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="3967b-150">To polecenie cmdlet usuwa plik w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="3967b-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="3967b-151">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="3967b-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="3967b-152">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="3967b-152">This object contains the storage context.</span></span>
<span data-ttu-id="3967b-153">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="3967b-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="3967b-154">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="3967b-154">-ShareName</span></span>
<span data-ttu-id="3967b-155">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="3967b-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="3967b-156">To polecenie cmdlet usuwa plik w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="3967b-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="3967b-157">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3967b-157">-Confirm</span></span>
<span data-ttu-id="3967b-158">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3967b-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3967b-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3967b-159">-WhatIf</span></span>
<span data-ttu-id="3967b-160">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3967b-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3967b-161">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3967b-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3967b-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3967b-162">CommonParameters</span></span>
<span data-ttu-id="3967b-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3967b-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3967b-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3967b-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3967b-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3967b-165">INPUTS</span></span>

### <span data-ttu-id="3967b-166">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="3967b-166">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="3967b-167">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="3967b-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="3967b-168">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="3967b-168">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="3967b-169">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3967b-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3967b-170">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3967b-170">OUTPUTS</span></span>

### <span data-ttu-id="3967b-171">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="3967b-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="3967b-172">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3967b-172">NOTES</span></span>

## <span data-ttu-id="3967b-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3967b-173">RELATED LINKS</span></span>

[<span data-ttu-id="3967b-174">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="3967b-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="3967b-175">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="3967b-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="3967b-176">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3967b-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
