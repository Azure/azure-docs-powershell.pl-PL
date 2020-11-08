---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
ms.openlocfilehash: d25ebb69521ea1e16dc5ff5103ea64819202e2d1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051245"
---
# <span data-ttu-id="3a2fb-101">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="3a2fb-101">Get-AzStorageShare</span></span>

## <span data-ttu-id="3a2fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a2fb-102">SYNOPSIS</span></span>
<span data-ttu-id="3a2fb-103">Pobiera listę udziałów plików.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="3a2fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a2fb-104">SYNTAX</span></span>

### <span data-ttu-id="3a2fb-105">MatchingPrefix (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3a2fb-105">MatchingPrefix (Default)</span></span>
```
Get-AzStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a2fb-106">Specjalnych</span><span class="sxs-lookup"><span data-stu-id="3a2fb-106">Specific</span></span>
```
Get-AzStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3a2fb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3a2fb-107">DESCRIPTION</span></span>
<span data-ttu-id="3a2fb-108">Polecenie cmdlet **Get-AzStorageShare** pobiera listę udziałów plików dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-108">The **Get-AzStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="3a2fb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a2fb-109">EXAMPLES</span></span>

### <span data-ttu-id="3a2fb-110">Przykład 1: uzyskiwanie udziału plików</span><span class="sxs-lookup"><span data-stu-id="3a2fb-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="3a2fb-111">To polecenie uzyskuje udział plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="3a2fb-112">Przykład 2: pobieranie wszystkich udziałów plików, które zaczynają się od ciągu</span><span class="sxs-lookup"><span data-stu-id="3a2fb-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "Contoso"
```

<span data-ttu-id="3a2fb-113">To polecenie pobiera wszystkie udziały plików, których nazwy zaczynają się od contoso.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="3a2fb-114">Przykład 3: pobieranie wszystkich udziałów plików w określonym kontekście</span><span class="sxs-lookup"><span data-stu-id="3a2fb-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzStorageContext -Local
PS C:\> Get-AzStorageShare -Context $Context
```

<span data-ttu-id="3a2fb-115">W pierwszym poleceniu użyto polecenia cmdlet **New-AzStorageContext** w celu utworzenia kontekstu przy użyciu parametru *Local* , a następnie zapisanie tego obiektu kontekstu w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-115">The first command uses the **New-AzStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="3a2fb-116">Drugie polecenie pobiera udziały plików w obiekcie kontekstu przechowywanym w $Context.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="3a2fb-117">Przykład 4: pobieranie migawki udziału plików o określonej nazwie udziału i SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="3a2fb-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="3a2fb-118">To polecenie uzyskuje migawkę udziału plików o określonej nazwie udziału i SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="3a2fb-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a2fb-119">PARAMETERS</span></span>

### <span data-ttu-id="3a2fb-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3a2fb-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3a2fb-121">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3a2fb-122">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3a2fb-123">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3a2fb-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3a2fb-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3a2fb-125">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3a2fb-126">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3a2fb-127">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3a2fb-128">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3a2fb-129">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-129">The default value is 10.</span></span>

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

### <span data-ttu-id="3a2fb-130">-Context</span><span class="sxs-lookup"><span data-stu-id="3a2fb-130">-Context</span></span>
<span data-ttu-id="3a2fb-131">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="3a2fb-132">Aby uzyskać kontekst, użyj polecenia cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="3a2fb-132">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a2fb-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a2fb-133">-DefaultProfile</span></span>
<span data-ttu-id="3a2fb-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a2fb-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a2fb-135">-Name</span></span>
<span data-ttu-id="3a2fb-136">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="3a2fb-137">To polecenie cmdlet umożliwia wyświetlenie udziału plików, który jest określany przez ten parametr, lub brak wartości w przypadku określenia nazwy udziału plików, który nie istnieje.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a2fb-138">-Prefix</span><span class="sxs-lookup"><span data-stu-id="3a2fb-138">-Prefix</span></span>
<span data-ttu-id="3a2fb-139">Określa prefiks dla udziałów plików.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="3a2fb-140">To polecenie cmdlet umożliwia pobieranie udziałów plików, które pasują do prefiksu określanego przez ten parametr, lub nie ma udziałów plików, jeśli udziały plików nie pasują do określonego prefiksu.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a2fb-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3a2fb-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3a2fb-142">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3a2fb-143">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="3a2fb-143">-SnapshotTime</span></span>
<span data-ttu-id="3a2fb-144">SnapshotTime migawki udziału plików, który ma zostać odebrany.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-144">SnapshotTime of the file share snapshot to be received.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a2fb-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a2fb-145">CommonParameters</span></span>
<span data-ttu-id="3a2fb-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a2fb-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a2fb-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a2fb-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a2fb-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a2fb-148">INPUTS</span></span>

### <span data-ttu-id="3a2fb-149">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3a2fb-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3a2fb-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a2fb-150">OUTPUTS</span></span>

### <span data-ttu-id="3a2fb-151">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="3a2fb-151">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="3a2fb-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a2fb-152">NOTES</span></span>

## <span data-ttu-id="3a2fb-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a2fb-153">RELATED LINKS</span></span>

[<span data-ttu-id="3a2fb-154">Nowe — AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="3a2fb-154">New-AzStorageShare</span></span>](./New-AzStorageShare.md)

[<span data-ttu-id="3a2fb-155">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="3a2fb-155">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
