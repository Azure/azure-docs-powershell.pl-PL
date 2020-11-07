---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e816d29784ea8b2e69ba4b36162938f7a82007d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524001"
---
# <span data-ttu-id="9824b-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9824b-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="9824b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9824b-102">SYNOPSIS</span></span>
<span data-ttu-id="9824b-103">Pobiera listę udziałów plików.</span><span class="sxs-lookup"><span data-stu-id="9824b-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="9824b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9824b-104">SYNTAX</span></span>

### <span data-ttu-id="9824b-105">MatchingPrefix (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9824b-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9824b-106">Specjalnych</span><span class="sxs-lookup"><span data-stu-id="9824b-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="9824b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9824b-107">DESCRIPTION</span></span>
<span data-ttu-id="9824b-108">Polecenie cmdlet **Get-AzureStorageShare** pobiera listę udziałów plików dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="9824b-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="9824b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9824b-109">EXAMPLES</span></span>

### <span data-ttu-id="9824b-110">Przykład 1: uzyskiwanie udziału plików</span><span class="sxs-lookup"><span data-stu-id="9824b-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="9824b-111">To polecenie uzyskuje udział plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="9824b-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="9824b-112">Przykład 2: pobieranie wszystkich udziałów plików, które zaczynają się od ciągu</span><span class="sxs-lookup"><span data-stu-id="9824b-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="9824b-113">To polecenie pobiera wszystkie udziały plików, których nazwy zaczynają się od contoso.</span><span class="sxs-lookup"><span data-stu-id="9824b-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="9824b-114">Przykład 3: pobieranie wszystkich udziałów plików w określonym kontekście</span><span class="sxs-lookup"><span data-stu-id="9824b-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="9824b-115">W pierwszym poleceniu użyto polecenia cmdlet **New-AzureStorageContext** w celu utworzenia kontekstu przy użyciu parametru *Local* , a następnie zapisanie tego obiektu kontekstu w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="9824b-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>

<span data-ttu-id="9824b-116">Drugie polecenie pobiera udziały plików w obiekcie kontekstu przechowywanym w $Context.</span><span class="sxs-lookup"><span data-stu-id="9824b-116">The second command gets the file shares for the context object stored in $Context.</span></span>

## <span data-ttu-id="9824b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9824b-117">PARAMETERS</span></span>

### <span data-ttu-id="9824b-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9824b-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9824b-119">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="9824b-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9824b-120">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="9824b-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9824b-121">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="9824b-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9824b-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9824b-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9824b-123">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="9824b-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9824b-124">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="9824b-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9824b-125">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="9824b-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9824b-126">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="9824b-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9824b-127">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="9824b-127">The default value is 10.</span></span>

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

### <span data-ttu-id="9824b-128">-Context</span><span class="sxs-lookup"><span data-stu-id="9824b-128">-Context</span></span>
<span data-ttu-id="9824b-129">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9824b-129">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="9824b-130">Aby uzyskać kontekst, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="9824b-130">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="9824b-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9824b-131">-Name</span></span>
<span data-ttu-id="9824b-132">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="9824b-132">Specifies the name of the file share.</span></span>
<span data-ttu-id="9824b-133">To polecenie cmdlet umożliwia wyświetlenie udziału plików, który jest określany przez ten parametr, lub brak wartości w przypadku określenia nazwy udziału plików, który nie istnieje.</span><span class="sxs-lookup"><span data-stu-id="9824b-133">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

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

### <span data-ttu-id="9824b-134">-Prefix</span><span class="sxs-lookup"><span data-stu-id="9824b-134">-Prefix</span></span>
<span data-ttu-id="9824b-135">Określa prefiks dla udziałów plików.</span><span class="sxs-lookup"><span data-stu-id="9824b-135">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="9824b-136">To polecenie cmdlet umożliwia pobieranie udziałów plików, które pasują do prefiksu określanego przez ten parametr, lub nie ma udziałów plików, jeśli udziały plików nie pasują do określonego prefiksu.</span><span class="sxs-lookup"><span data-stu-id="9824b-136">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

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

### <span data-ttu-id="9824b-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9824b-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9824b-138">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="9824b-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9824b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9824b-139">CommonParameters</span></span>
<span data-ttu-id="9824b-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9824b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9824b-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9824b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9824b-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9824b-142">INPUTS</span></span>

## <span data-ttu-id="9824b-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9824b-143">OUTPUTS</span></span>

## <span data-ttu-id="9824b-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9824b-144">NOTES</span></span>

## <span data-ttu-id="9824b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9824b-145">RELATED LINKS</span></span>

[<span data-ttu-id="9824b-146">Nowe — AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9824b-146">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="9824b-147">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9824b-147">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)