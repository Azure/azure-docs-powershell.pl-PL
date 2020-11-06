---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
ms.openlocfilehash: c0c3aedf6c92df8b81beed92ef4ea779dd8ff131
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545904"
---
# <span data-ttu-id="9cc01-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9cc01-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="9cc01-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9cc01-102">SYNOPSIS</span></span>
<span data-ttu-id="9cc01-103">Pobiera listę udziałów plików.</span><span class="sxs-lookup"><span data-stu-id="9cc01-103">Gets a list of file shares.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cc01-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9cc01-104">SYNTAX</span></span>

### <span data-ttu-id="9cc01-105">MatchingPrefix (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9cc01-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9cc01-106">Specjalnych</span><span class="sxs-lookup"><span data-stu-id="9cc01-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [-SnapshotTime <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cc01-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9cc01-107">DESCRIPTION</span></span>
<span data-ttu-id="9cc01-108">Polecenie cmdlet **Get-AzureStorageShare** pobiera listę udziałów plików dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="9cc01-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="9cc01-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9cc01-109">EXAMPLES</span></span>

### <span data-ttu-id="9cc01-110">Przykład 1: uzyskiwanie udziału plików</span><span class="sxs-lookup"><span data-stu-id="9cc01-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="9cc01-111">To polecenie uzyskuje udział plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="9cc01-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="9cc01-112">Przykład 2: pobieranie wszystkich udziałów plików, które zaczynają się od ciągu</span><span class="sxs-lookup"><span data-stu-id="9cc01-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="9cc01-113">To polecenie pobiera wszystkie udziały plików, których nazwy zaczynają się od contoso.</span><span class="sxs-lookup"><span data-stu-id="9cc01-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="9cc01-114">Przykład 3: pobieranie wszystkich udziałów plików w określonym kontekście</span><span class="sxs-lookup"><span data-stu-id="9cc01-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="9cc01-115">W pierwszym poleceniu użyto polecenia cmdlet **New-AzureStorageContext** w celu utworzenia kontekstu przy użyciu parametru *Local* , a następnie zapisanie tego obiektu kontekstu w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="9cc01-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>

<span data-ttu-id="9cc01-116">Drugie polecenie pobiera udziały plików w obiekcie kontekstu przechowywanym w $Context.</span><span class="sxs-lookup"><span data-stu-id="9cc01-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="9cc01-117">Przykład 4: pobieranie migawki udziału plików o określonej nazwie udziału i SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="9cc01-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="9cc01-118">To polecenie uzyskuje migawkę udziału plików o określonej nazwie udziału i SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="9cc01-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="9cc01-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9cc01-119">PARAMETERS</span></span>

### <span data-ttu-id="9cc01-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9cc01-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9cc01-121">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="9cc01-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9cc01-122">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="9cc01-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9cc01-123">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="9cc01-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9cc01-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9cc01-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9cc01-125">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="9cc01-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9cc01-126">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="9cc01-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9cc01-127">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="9cc01-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9cc01-128">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="9cc01-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9cc01-129">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="9cc01-129">The default value is 10.</span></span>

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

### <span data-ttu-id="9cc01-130">-Context</span><span class="sxs-lookup"><span data-stu-id="9cc01-130">-Context</span></span>
<span data-ttu-id="9cc01-131">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9cc01-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="9cc01-132">Aby uzyskać kontekst, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="9cc01-132">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc01-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9cc01-133">-Name</span></span>
<span data-ttu-id="9cc01-134">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="9cc01-134">Specifies the name of the file share.</span></span>
<span data-ttu-id="9cc01-135">To polecenie cmdlet umożliwia wyświetlenie udziału plików, który jest określany przez ten parametr, lub brak wartości w przypadku określenia nazwy udziału plików, który nie istnieje.</span><span class="sxs-lookup"><span data-stu-id="9cc01-135">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: String
Parameter Sets: Specific
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc01-136">-Prefix</span><span class="sxs-lookup"><span data-stu-id="9cc01-136">-Prefix</span></span>
<span data-ttu-id="9cc01-137">Określa prefiks dla udziałów plików.</span><span class="sxs-lookup"><span data-stu-id="9cc01-137">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="9cc01-138">To polecenie cmdlet umożliwia pobieranie udziałów plików, które pasują do prefiksu określanego przez ten parametr, lub nie ma udziałów plików, jeśli udziały plików nie pasują do określonego prefiksu.</span><span class="sxs-lookup"><span data-stu-id="9cc01-138">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: String
Parameter Sets: MatchingPrefix
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc01-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9cc01-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9cc01-140">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="9cc01-140">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9cc01-141">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="9cc01-141">-SnapshotTime</span></span>
<span data-ttu-id="9cc01-142">SnapshotTime migawki udziału plików, który ma zostać odebrany.</span><span class="sxs-lookup"><span data-stu-id="9cc01-142">SnapshotTime of the file share snapshot to be received.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: Specific
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc01-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cc01-143">CommonParameters</span></span>
<span data-ttu-id="9cc01-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cc01-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cc01-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cc01-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cc01-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cc01-146">INPUTS</span></span>

### <span data-ttu-id="9cc01-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9cc01-147">IStorageContext</span></span>

<span data-ttu-id="9cc01-148">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="9cc01-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="9cc01-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9cc01-149">OUTPUTS</span></span>

## <span data-ttu-id="9cc01-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9cc01-150">NOTES</span></span>

## <span data-ttu-id="9cc01-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cc01-151">RELATED LINKS</span></span>

[<span data-ttu-id="9cc01-152">Nowe — AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9cc01-152">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="9cc01-153">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9cc01-153">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
