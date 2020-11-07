---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragefile
schema: 2.0.0
ms.openlocfilehash: cfb5a3255a91c7a7206ba0729c20e4d0c68c3ea2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899165"
---
# <span data-ttu-id="9a3b5-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="9a3b5-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="9a3b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a3b5-102">SYNOPSIS</span></span>
<span data-ttu-id="9a3b5-103">Usuwa plik.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-103">Deletes a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a3b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a3b5-104">SYNTAX</span></span>

### <span data-ttu-id="9a3b5-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9a3b5-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a3b5-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="9a3b5-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a3b5-107">Directory</span><span class="sxs-lookup"><span data-stu-id="9a3b5-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a3b5-108">Plik</span><span class="sxs-lookup"><span data-stu-id="9a3b5-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a3b5-109">Opis</span><span class="sxs-lookup"><span data-stu-id="9a3b5-109">DESCRIPTION</span></span>
<span data-ttu-id="9a3b5-110">Polecenie cmdlet **Remove-AzureStorageFile** usuwa plik.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="9a3b5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a3b5-111">EXAMPLES</span></span>

### <span data-ttu-id="9a3b5-112">Przykład 1: usuwanie pliku z udziału plików</span><span class="sxs-lookup"><span data-stu-id="9a3b5-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="9a3b5-113">To polecenie usuwa plik o nazwie ContosoFile22 z udziału plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="9a3b5-114">Przykład 2: uzyskiwanie pliku z udziału plików za pomocą obiektu udostępniania plików</span><span class="sxs-lookup"><span data-stu-id="9a3b5-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="9a3b5-115">To polecenie korzysta z polecenia cmdlet **Get-AzureStorageShare** w celu uzyskania udziału plików o nazwie ContosoShare06, a następnie przekazanie tego obiektu do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9a3b5-116">Bieżące polecenie usuwa plik o nazwie ContosoFile22 z ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="9a3b5-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a3b5-117">PARAMETERS</span></span>

### <span data-ttu-id="9a3b5-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9a3b5-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9a3b5-119">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9a3b5-120">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9a3b5-121">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9a3b5-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9a3b5-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9a3b5-123">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9a3b5-124">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9a3b5-125">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9a3b5-126">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9a3b5-127">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-127">The default value is 10.</span></span>

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

### <span data-ttu-id="9a3b5-128">-Context</span><span class="sxs-lookup"><span data-stu-id="9a3b5-128">-Context</span></span>
<span data-ttu-id="9a3b5-129">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9a3b5-130">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="9a3b5-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="9a3b5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a3b5-131">-DefaultProfile</span></span>
<span data-ttu-id="9a3b5-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a3b5-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="9a3b5-133">-Directory</span></span>
<span data-ttu-id="9a3b5-134">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="9a3b5-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="9a3b5-135">To polecenie cmdlet usuwa plik znajdujący się w folderze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="9a3b5-136">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="9a3b5-136">-File</span></span>
<span data-ttu-id="9a3b5-137">Określa plik jako obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="9a3b5-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="9a3b5-138">To polecenie cmdlet umożliwia usunięcie pliku, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="9a3b5-139">Aby uzyskać obiekt **CloudFile** , użyj polecenia cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-139">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="9a3b5-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a3b5-140">-PassThru</span></span>
<span data-ttu-id="9a3b5-141">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="9a3b5-142">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="9a3b5-143">-Path</span><span class="sxs-lookup"><span data-stu-id="9a3b5-143">-Path</span></span>
<span data-ttu-id="9a3b5-144">Określa ścieżkę pliku.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-144">Specifies the path of a file.</span></span>
<span data-ttu-id="9a3b5-145">To polecenie cmdlet usuwa plik, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-145">This cmdlet deletes the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="9a3b5-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9a3b5-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9a3b5-147">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9a3b5-148">-Share</span><span class="sxs-lookup"><span data-stu-id="9a3b5-148">-Share</span></span>
<span data-ttu-id="9a3b5-149">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="9a3b5-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="9a3b5-150">To polecenie cmdlet usuwa plik w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="9a3b5-151">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-151">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="9a3b5-152">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-152">This object contains the storage context.</span></span>
<span data-ttu-id="9a3b5-153">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="9a3b5-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="9a3b5-154">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="9a3b5-154">-ShareName</span></span>
<span data-ttu-id="9a3b5-155">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="9a3b5-156">To polecenie cmdlet usuwa plik w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="9a3b5-157">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a3b5-157">-Confirm</span></span>
<span data-ttu-id="9a3b5-158">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a3b5-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a3b5-159">-WhatIf</span></span>
<span data-ttu-id="9a3b5-160">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a3b5-161">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a3b5-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a3b5-162">CommonParameters</span></span>
<span data-ttu-id="9a3b5-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a3b5-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a3b5-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a3b5-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a3b5-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a3b5-165">INPUTS</span></span>

### <span data-ttu-id="9a3b5-166">Microsoft. platformy windowsazure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="9a3b5-166">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="9a3b5-167">Parametry: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9a3b5-167">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="9a3b5-168">Microsoft. platformy windowsazure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="9a3b5-168">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="9a3b5-169">Parametry: katalog (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9a3b5-169">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="9a3b5-170">Microsoft. platformy windowsazure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="9a3b5-170">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="9a3b5-171">Parametry: plik (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9a3b5-171">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="9a3b5-172">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9a3b5-172">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9a3b5-173">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a3b5-173">OUTPUTS</span></span>

### <span data-ttu-id="9a3b5-174">Microsoft. platformy windowsazure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="9a3b5-174">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="9a3b5-175">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a3b5-175">NOTES</span></span>

## <span data-ttu-id="9a3b5-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a3b5-176">RELATED LINKS</span></span>

[<span data-ttu-id="9a3b5-177">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="9a3b5-177">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="9a3b5-178">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9a3b5-178">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="9a3b5-179">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9a3b5-179">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
