---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragedirectory
schema: 2.0.0
ms.openlocfilehash: 0a474171b7659346a1d921f98920a9befc85eea8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898828"
---
# <span data-ttu-id="19898-101">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="19898-101">New-AzureStorageDirectory</span></span>

## <span data-ttu-id="19898-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19898-102">SYNOPSIS</span></span>
<span data-ttu-id="19898-103">Tworzy katalog.</span><span class="sxs-lookup"><span data-stu-id="19898-103">Creates a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19898-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19898-104">SYNTAX</span></span>

### <span data-ttu-id="19898-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="19898-105">ShareName (Default)</span></span>
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="19898-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="19898-106">Share</span></span>
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="19898-107">Directory</span><span class="sxs-lookup"><span data-stu-id="19898-107">Directory</span></span>
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="19898-108">Opis</span><span class="sxs-lookup"><span data-stu-id="19898-108">DESCRIPTION</span></span>
<span data-ttu-id="19898-109">Polecenie cmdlet **New-AzureStorageDirectory** tworzy katalog.</span><span class="sxs-lookup"><span data-stu-id="19898-109">The **New-AzureStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="19898-110">To polecenie cmdlet zwraca obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="19898-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="19898-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19898-111">EXAMPLES</span></span>

### <span data-ttu-id="19898-112">Przykład 1. Tworzenie folderu w udziale plików</span><span class="sxs-lookup"><span data-stu-id="19898-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="19898-113">To polecenie tworzy folder o nazwie ContosoWorkingFolder w udziale plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="19898-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="19898-114">Przykład 2: Tworzenie folderu w udziale plików określonym w obiekcie udostępniania plików</span><span class="sxs-lookup"><span data-stu-id="19898-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="19898-115">To polecenie używa polecenia cmdlet **Get-AzureStorageShare** w celu uzyskania udziału plików o nazwie ContosoShare06, a następnie przekazanie go do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="19898-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="19898-116">Bieżące polecenie cmdlet tworzy folder o nazwie ContosoWorkingFolder w ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="19898-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="19898-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19898-117">PARAMETERS</span></span>

### <span data-ttu-id="19898-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="19898-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="19898-119">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="19898-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="19898-120">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="19898-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="19898-121">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="19898-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="19898-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="19898-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="19898-123">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="19898-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="19898-124">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="19898-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="19898-125">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="19898-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="19898-126">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="19898-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="19898-127">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="19898-127">The default value is 10.</span></span>

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

### <span data-ttu-id="19898-128">-Context</span><span class="sxs-lookup"><span data-stu-id="19898-128">-Context</span></span>
<span data-ttu-id="19898-129">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="19898-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="19898-130">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="19898-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="19898-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19898-131">-DefaultProfile</span></span>
<span data-ttu-id="19898-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19898-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19898-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="19898-133">-Directory</span></span>
<span data-ttu-id="19898-134">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="19898-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="19898-135">To polecenie cmdlet tworzy folder w lokalizacji, w której określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="19898-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="19898-136">Aby uzyskać katalog, użyj polecenia cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="19898-136">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="19898-137">Możesz również użyć polecenia cmdlet Get-AzureStorageFile, aby uzyskać katalog.</span><span class="sxs-lookup"><span data-stu-id="19898-137">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="19898-138">-Path</span><span class="sxs-lookup"><span data-stu-id="19898-138">-Path</span></span>
<span data-ttu-id="19898-139">Określa ścieżkę do folderu.</span><span class="sxs-lookup"><span data-stu-id="19898-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="19898-140">To polecenie cmdlet tworzy folder dla ścieżki, którą to polecenie cmdlet określa.</span><span class="sxs-lookup"><span data-stu-id="19898-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="19898-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="19898-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="19898-142">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="19898-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="19898-143">-Share</span><span class="sxs-lookup"><span data-stu-id="19898-143">-Share</span></span>
<span data-ttu-id="19898-144">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="19898-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="19898-145">To polecenie cmdlet tworzy folder w udziale plików, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="19898-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="19898-146">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="19898-146">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="19898-147">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="19898-147">This object contains the storage context.</span></span>
<span data-ttu-id="19898-148">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="19898-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="19898-149">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="19898-149">-ShareName</span></span>
<span data-ttu-id="19898-150">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="19898-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="19898-151">To polecenie cmdlet tworzy folder w udziale plików, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="19898-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="19898-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19898-152">CommonParameters</span></span>
<span data-ttu-id="19898-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19898-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19898-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19898-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19898-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19898-155">INPUTS</span></span>

### <span data-ttu-id="19898-156">Microsoft. platformy windowsazure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="19898-156">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="19898-157">Parametry: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="19898-157">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="19898-158">Microsoft. platformy windowsazure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="19898-158">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="19898-159">Parametry: katalog (ByValue)</span><span class="sxs-lookup"><span data-stu-id="19898-159">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="19898-160">System. String</span><span class="sxs-lookup"><span data-stu-id="19898-160">System.String</span></span>

### <span data-ttu-id="19898-161">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="19898-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="19898-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19898-162">OUTPUTS</span></span>

### <span data-ttu-id="19898-163">Microsoft. platformy windowsazure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="19898-163">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="19898-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19898-164">NOTES</span></span>

## <span data-ttu-id="19898-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19898-165">RELATED LINKS</span></span>

[<span data-ttu-id="19898-166">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="19898-166">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="19898-167">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="19898-167">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="19898-168">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="19898-168">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="19898-169">Nowe — AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="19898-169">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="19898-170">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="19898-170">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)
