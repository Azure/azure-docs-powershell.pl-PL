---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1bd97057cfafc48b3f1edd8539e7808056599117
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523678"
---
# <span data-ttu-id="b84ea-101">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="b84ea-101">New-AzureStorageDirectory</span></span>

## <span data-ttu-id="b84ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b84ea-102">SYNOPSIS</span></span>
<span data-ttu-id="b84ea-103">Tworzy katalog.</span><span class="sxs-lookup"><span data-stu-id="b84ea-103">Creates a directory.</span></span>

## <span data-ttu-id="b84ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b84ea-104">SYNTAX</span></span>

### <span data-ttu-id="b84ea-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b84ea-105">ShareName (Default)</span></span>
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="b84ea-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="b84ea-106">Share</span></span>
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b84ea-107">Directory</span><span class="sxs-lookup"><span data-stu-id="b84ea-107">Directory</span></span>
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b84ea-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b84ea-108">DESCRIPTION</span></span>
<span data-ttu-id="b84ea-109">Polecenie cmdlet **New-AzureStorageDirectory** tworzy katalog.</span><span class="sxs-lookup"><span data-stu-id="b84ea-109">The **New-AzureStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="b84ea-110">To polecenie cmdlet zwraca obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="b84ea-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="b84ea-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b84ea-111">EXAMPLES</span></span>

### <span data-ttu-id="b84ea-112">Przykład 1. Tworzenie folderu w udziale plików</span><span class="sxs-lookup"><span data-stu-id="b84ea-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="b84ea-113">To polecenie tworzy folder o nazwie ContosoWorkingFolder w udziale plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="b84ea-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="b84ea-114">Przykład 2: Tworzenie folderu w udziale plików określonym w obiekcie udostępniania plików</span><span class="sxs-lookup"><span data-stu-id="b84ea-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="b84ea-115">To polecenie używa polecenia cmdlet **Get-AzureStorageShare** w celu uzyskania udziału plików o nazwie ContosoShare06, a następnie przekazanie go do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="b84ea-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b84ea-116">Bieżące polecenie cmdlet tworzy folder o nazwie ContosoWorkingFolder w ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="b84ea-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="b84ea-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b84ea-117">PARAMETERS</span></span>

### <span data-ttu-id="b84ea-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b84ea-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b84ea-119">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="b84ea-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b84ea-120">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="b84ea-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b84ea-121">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="b84ea-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84ea-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b84ea-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b84ea-123">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b84ea-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b84ea-124">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b84ea-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b84ea-125">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="b84ea-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b84ea-126">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="b84ea-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b84ea-127">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="b84ea-127">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84ea-128">-Context</span><span class="sxs-lookup"><span data-stu-id="b84ea-128">-Context</span></span>
<span data-ttu-id="b84ea-129">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b84ea-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b84ea-130">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="b84ea-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b84ea-131">-Directory</span><span class="sxs-lookup"><span data-stu-id="b84ea-131">-Directory</span></span>
<span data-ttu-id="b84ea-132">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="b84ea-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="b84ea-133">To polecenie cmdlet tworzy folder w lokalizacji, w której określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b84ea-133">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="b84ea-134">Aby uzyskać katalog, użyj polecenia cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="b84ea-134">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="b84ea-135">Możesz również użyć polecenia cmdlet Get-AzureStorageFile, aby uzyskać katalog.</span><span class="sxs-lookup"><span data-stu-id="b84ea-135">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b84ea-136">-Path</span><span class="sxs-lookup"><span data-stu-id="b84ea-136">-Path</span></span>
<span data-ttu-id="b84ea-137">Określa ścieżkę do folderu.</span><span class="sxs-lookup"><span data-stu-id="b84ea-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="b84ea-138">To polecenie cmdlet tworzy folder dla ścieżki, którą to polecenie cmdlet określa.</span><span class="sxs-lookup"><span data-stu-id="b84ea-138">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b84ea-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b84ea-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b84ea-140">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="b84ea-140">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84ea-141">-Share</span><span class="sxs-lookup"><span data-stu-id="b84ea-141">-Share</span></span>
<span data-ttu-id="b84ea-142">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="b84ea-142">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="b84ea-143">To polecenie cmdlet tworzy folder w udziale plików, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b84ea-143">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="b84ea-144">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="b84ea-144">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="b84ea-145">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="b84ea-145">This object contains the storage context.</span></span>
<span data-ttu-id="b84ea-146">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="b84ea-146">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b84ea-147">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="b84ea-147">-ShareName</span></span>
<span data-ttu-id="b84ea-148">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="b84ea-148">Specifies the name of the file share.</span></span>
<span data-ttu-id="b84ea-149">To polecenie cmdlet tworzy folder w udziale plików, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b84ea-149">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84ea-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b84ea-150">CommonParameters</span></span>
<span data-ttu-id="b84ea-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b84ea-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b84ea-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b84ea-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b84ea-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b84ea-153">INPUTS</span></span>

## <span data-ttu-id="b84ea-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b84ea-154">OUTPUTS</span></span>

## <span data-ttu-id="b84ea-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b84ea-155">NOTES</span></span>

## <span data-ttu-id="b84ea-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b84ea-156">RELATED LINKS</span></span>

[<span data-ttu-id="b84ea-157">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="b84ea-157">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="b84ea-158">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="b84ea-158">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="b84ea-159">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b84ea-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b84ea-160">Nowe — AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="b84ea-160">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="b84ea-161">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="b84ea-161">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)
