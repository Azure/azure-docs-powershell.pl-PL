---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: 76d66d31856b2889484f1d786ef81295e8f27bc1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707578"
---
# <span data-ttu-id="5939c-101">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="5939c-101">New-AzStorageDirectory</span></span>

## <span data-ttu-id="5939c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5939c-102">SYNOPSIS</span></span>
<span data-ttu-id="5939c-103">Tworzy katalog.</span><span class="sxs-lookup"><span data-stu-id="5939c-103">Creates a directory.</span></span>

## <span data-ttu-id="5939c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5939c-104">SYNTAX</span></span>

### <span data-ttu-id="5939c-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="5939c-105">ShareName (Default)</span></span>
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5939c-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="5939c-106">Share</span></span>
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="5939c-107">Directory</span><span class="sxs-lookup"><span data-stu-id="5939c-107">Directory</span></span>
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="5939c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5939c-108">DESCRIPTION</span></span>
<span data-ttu-id="5939c-109">Polecenie cmdlet **New-AzStorageDirectory** tworzy katalog.</span><span class="sxs-lookup"><span data-stu-id="5939c-109">The **New-AzStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="5939c-110">To polecenie cmdlet zwraca obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="5939c-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="5939c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5939c-111">EXAMPLES</span></span>

### <span data-ttu-id="5939c-112">Przykład 1. Tworzenie folderu w udziale plików</span><span class="sxs-lookup"><span data-stu-id="5939c-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="5939c-113">To polecenie tworzy folder o nazwie ContosoWorkingFolder w udziale plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="5939c-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="5939c-114">Przykład 2: Tworzenie folderu w udziale plików określonym w obiekcie udostępniania plików</span><span class="sxs-lookup"><span data-stu-id="5939c-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="5939c-115">To polecenie używa polecenia cmdlet **Get-AzStorageShare** w celu uzyskania udziału plików o nazwie ContosoShare06, a następnie przekazanie go do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="5939c-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5939c-116">Bieżące polecenie cmdlet tworzy folder o nazwie ContosoWorkingFolder w ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="5939c-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="5939c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5939c-117">PARAMETERS</span></span>

### <span data-ttu-id="5939c-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5939c-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5939c-119">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="5939c-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5939c-120">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="5939c-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5939c-121">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="5939c-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5939c-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5939c-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5939c-123">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="5939c-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5939c-124">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="5939c-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5939c-125">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="5939c-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5939c-126">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="5939c-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5939c-127">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="5939c-127">The default value is 10.</span></span>

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

### <span data-ttu-id="5939c-128">-Context</span><span class="sxs-lookup"><span data-stu-id="5939c-128">-Context</span></span>
<span data-ttu-id="5939c-129">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5939c-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5939c-130">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="5939c-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="5939c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5939c-131">-DefaultProfile</span></span>
<span data-ttu-id="5939c-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5939c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5939c-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="5939c-133">-Directory</span></span>
<span data-ttu-id="5939c-134">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="5939c-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="5939c-135">To polecenie cmdlet tworzy folder w lokalizacji, w której określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5939c-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="5939c-136">Aby uzyskać katalog, użyj polecenia cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="5939c-136">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="5939c-137">Możesz również użyć polecenia cmdlet Get-AzStorageFile, aby uzyskać katalog.</span><span class="sxs-lookup"><span data-stu-id="5939c-137">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="5939c-138">-Path</span><span class="sxs-lookup"><span data-stu-id="5939c-138">-Path</span></span>
<span data-ttu-id="5939c-139">Określa ścieżkę do folderu.</span><span class="sxs-lookup"><span data-stu-id="5939c-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="5939c-140">To polecenie cmdlet tworzy folder dla ścieżki, którą to polecenie cmdlet określa.</span><span class="sxs-lookup"><span data-stu-id="5939c-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="5939c-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5939c-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5939c-142">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="5939c-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="5939c-143">-Share</span><span class="sxs-lookup"><span data-stu-id="5939c-143">-Share</span></span>
<span data-ttu-id="5939c-144">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="5939c-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="5939c-145">To polecenie cmdlet tworzy folder w udziale plików, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5939c-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="5939c-146">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="5939c-146">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="5939c-147">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="5939c-147">This object contains the storage context.</span></span>
<span data-ttu-id="5939c-148">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="5939c-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="5939c-149">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="5939c-149">-ShareName</span></span>
<span data-ttu-id="5939c-150">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="5939c-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="5939c-151">To polecenie cmdlet tworzy folder w udziale plików, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5939c-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="5939c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5939c-152">CommonParameters</span></span>
<span data-ttu-id="5939c-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5939c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5939c-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5939c-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5939c-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5939c-155">INPUTS</span></span>

### <span data-ttu-id="5939c-156">Microsoft. platformy windowsazure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="5939c-156">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="5939c-157">Microsoft. platformy windowsazure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="5939c-157">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="5939c-158">System. String</span><span class="sxs-lookup"><span data-stu-id="5939c-158">System.String</span></span>

### <span data-ttu-id="5939c-159">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5939c-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5939c-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5939c-160">OUTPUTS</span></span>

### <span data-ttu-id="5939c-161">Microsoft. platformy windowsazure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="5939c-161">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="5939c-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5939c-162">NOTES</span></span>

## <span data-ttu-id="5939c-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5939c-163">RELATED LINKS</span></span>

[<span data-ttu-id="5939c-164">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="5939c-164">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="5939c-165">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="5939c-165">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="5939c-166">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5939c-166">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="5939c-167">Nowe — AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="5939c-167">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="5939c-168">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="5939c-168">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)