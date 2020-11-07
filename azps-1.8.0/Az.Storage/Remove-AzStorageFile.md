---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: cfe3a924f9ce1d911c4e6e01fc7b35adc54537a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707532"
---
# <span data-ttu-id="79bfa-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="79bfa-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="79bfa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="79bfa-103">Usuwa plik.</span><span class="sxs-lookup"><span data-stu-id="79bfa-103">Deletes a file.</span></span>

## <span data-ttu-id="79bfa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79bfa-104">SYNTAX</span></span>

### <span data-ttu-id="79bfa-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="79bfa-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79bfa-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="79bfa-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79bfa-107">Directory</span><span class="sxs-lookup"><span data-stu-id="79bfa-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79bfa-108">Plik</span><span class="sxs-lookup"><span data-stu-id="79bfa-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79bfa-109">Opis</span><span class="sxs-lookup"><span data-stu-id="79bfa-109">DESCRIPTION</span></span>
<span data-ttu-id="79bfa-110">Polecenie cmdlet **Remove-AzStorageFile** usuwa plik.</span><span class="sxs-lookup"><span data-stu-id="79bfa-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="79bfa-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79bfa-111">EXAMPLES</span></span>

### <span data-ttu-id="79bfa-112">Przykład 1: usuwanie pliku z udziału plików</span><span class="sxs-lookup"><span data-stu-id="79bfa-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="79bfa-113">To polecenie usuwa plik o nazwie ContosoFile22 z udziału plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="79bfa-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="79bfa-114">Przykład 2: uzyskiwanie pliku z udziału plików za pomocą obiektu udostępniania plików</span><span class="sxs-lookup"><span data-stu-id="79bfa-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="79bfa-115">To polecenie korzysta z polecenia cmdlet **Get-AzStorageShare** w celu uzyskania udziału plików o nazwie ContosoShare06, a następnie przekazanie tego obiektu do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="79bfa-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="79bfa-116">Bieżące polecenie usuwa plik o nazwie ContosoFile22 z ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="79bfa-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="79bfa-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79bfa-117">PARAMETERS</span></span>

### <span data-ttu-id="79bfa-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="79bfa-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="79bfa-119">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="79bfa-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="79bfa-120">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="79bfa-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="79bfa-121">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="79bfa-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="79bfa-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="79bfa-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="79bfa-123">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="79bfa-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="79bfa-124">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="79bfa-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="79bfa-125">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="79bfa-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="79bfa-126">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="79bfa-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="79bfa-127">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="79bfa-127">The default value is 10.</span></span>

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

### <span data-ttu-id="79bfa-128">-Context</span><span class="sxs-lookup"><span data-stu-id="79bfa-128">-Context</span></span>
<span data-ttu-id="79bfa-129">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="79bfa-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="79bfa-130">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="79bfa-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="79bfa-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79bfa-131">-DefaultProfile</span></span>
<span data-ttu-id="79bfa-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79bfa-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79bfa-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="79bfa-133">-Directory</span></span>
<span data-ttu-id="79bfa-134">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="79bfa-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="79bfa-135">To polecenie cmdlet usuwa plik znajdujący się w folderze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="79bfa-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="79bfa-136">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="79bfa-136">-File</span></span>
<span data-ttu-id="79bfa-137">Określa plik jako obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="79bfa-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="79bfa-138">To polecenie cmdlet umożliwia usunięcie pliku, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="79bfa-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="79bfa-139">Aby uzyskać obiekt **CloudFile** , użyj polecenia cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="79bfa-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79bfa-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79bfa-140">-PassThru</span></span>
<span data-ttu-id="79bfa-141">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="79bfa-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="79bfa-142">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="79bfa-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="79bfa-143">-Path</span><span class="sxs-lookup"><span data-stu-id="79bfa-143">-Path</span></span>
<span data-ttu-id="79bfa-144">Określa ścieżkę pliku.</span><span class="sxs-lookup"><span data-stu-id="79bfa-144">Specifies the path of a file.</span></span>
<span data-ttu-id="79bfa-145">To polecenie cmdlet usuwa plik, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="79bfa-145">This cmdlet deletes the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="79bfa-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="79bfa-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="79bfa-147">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="79bfa-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="79bfa-148">-Share</span><span class="sxs-lookup"><span data-stu-id="79bfa-148">-Share</span></span>
<span data-ttu-id="79bfa-149">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="79bfa-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="79bfa-150">To polecenie cmdlet usuwa plik w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="79bfa-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="79bfa-151">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="79bfa-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="79bfa-152">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="79bfa-152">This object contains the storage context.</span></span>
<span data-ttu-id="79bfa-153">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="79bfa-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="79bfa-154">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="79bfa-154">-ShareName</span></span>
<span data-ttu-id="79bfa-155">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="79bfa-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="79bfa-156">To polecenie cmdlet usuwa plik w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="79bfa-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="79bfa-157">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79bfa-157">-Confirm</span></span>
<span data-ttu-id="79bfa-158">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79bfa-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79bfa-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79bfa-159">-WhatIf</span></span>
<span data-ttu-id="79bfa-160">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79bfa-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79bfa-161">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79bfa-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79bfa-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79bfa-162">CommonParameters</span></span>
<span data-ttu-id="79bfa-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79bfa-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79bfa-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79bfa-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79bfa-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79bfa-165">INPUTS</span></span>

### <span data-ttu-id="79bfa-166">Microsoft. platformy windowsazure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="79bfa-166">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="79bfa-167">Microsoft. platformy windowsazure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="79bfa-167">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="79bfa-168">Microsoft. platformy windowsazure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="79bfa-168">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="79bfa-169">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="79bfa-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="79bfa-170">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79bfa-170">OUTPUTS</span></span>

### <span data-ttu-id="79bfa-171">Microsoft. platformy windowsazure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="79bfa-171">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="79bfa-172">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79bfa-172">NOTES</span></span>

## <span data-ttu-id="79bfa-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79bfa-173">RELATED LINKS</span></span>

[<span data-ttu-id="79bfa-174">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="79bfa-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="79bfa-175">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="79bfa-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="79bfa-176">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="79bfa-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)