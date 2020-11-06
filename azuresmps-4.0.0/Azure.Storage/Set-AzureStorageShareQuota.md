---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 778c5020dc47bc8db7bda664b2e352045d851dfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524126"
---
# <span data-ttu-id="64719-101">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="64719-101">Set-AzureStorageShareQuota</span></span>

## <span data-ttu-id="64719-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64719-102">SYNOPSIS</span></span>
<span data-ttu-id="64719-103">Umożliwia ustawienie pojemności magazynowania dla udziału.</span><span class="sxs-lookup"><span data-stu-id="64719-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="64719-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64719-104">SYNTAX</span></span>

### <span data-ttu-id="64719-105">Nazwaudziału</span><span class="sxs-lookup"><span data-stu-id="64719-105">ShareName</span></span>
```
Set-AzureStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="64719-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="64719-106">Share</span></span>
```
Set-AzureStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="64719-107">Opis</span><span class="sxs-lookup"><span data-stu-id="64719-107">DESCRIPTION</span></span>
<span data-ttu-id="64719-108">Polecenie cmdlet **Set-AzureStorageShareQuota** określa pojemność magazynowania określonego udziału.</span><span class="sxs-lookup"><span data-stu-id="64719-108">The **Set-AzureStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="64719-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64719-109">EXAMPLES</span></span>

### <span data-ttu-id="64719-110">Przykład 1: Ustawianie pojemności miejsca do magazynowania dla udziału</span><span class="sxs-lookup"><span data-stu-id="64719-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzureStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="64719-111">To polecenie ustawia pojemność magazynowania dla udziału o nazwie 1024 ContosoShare01 GB.</span><span class="sxs-lookup"><span data-stu-id="64719-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="64719-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64719-112">PARAMETERS</span></span>

### <span data-ttu-id="64719-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="64719-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="64719-114">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="64719-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="64719-115">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="64719-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="64719-116">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="64719-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="64719-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="64719-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="64719-118">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="64719-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="64719-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="64719-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="64719-120">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="64719-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="64719-121">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="64719-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="64719-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="64719-122">The default value is 10.</span></span>

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

### <span data-ttu-id="64719-123">-Context</span><span class="sxs-lookup"><span data-stu-id="64719-123">-Context</span></span>
<span data-ttu-id="64719-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="64719-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="64719-125">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="64719-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="64719-126">-Przydział</span><span class="sxs-lookup"><span data-stu-id="64719-126">-Quota</span></span>
<span data-ttu-id="64719-127">Określa wartość przydziału w gigabajtach (GB).</span><span class="sxs-lookup"><span data-stu-id="64719-127">Specifies the quota value in gigabytes (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64719-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="64719-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="64719-129">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="64719-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="64719-130">-Share</span><span class="sxs-lookup"><span data-stu-id="64719-130">-Share</span></span>
<span data-ttu-id="64719-131">Określa obiekt **CloudFileShare** reprezentujący udział, dla którego to polecenie cmdlet ustawia przydział.</span><span class="sxs-lookup"><span data-stu-id="64719-131">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="64719-132">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="64719-132">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="64719-133">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="64719-133">-ShareName</span></span>
<span data-ttu-id="64719-134">Określa nazwę udziału pliku, dla którego ma zostać ustawiony przydział.</span><span class="sxs-lookup"><span data-stu-id="64719-134">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64719-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64719-135">CommonParameters</span></span>
<span data-ttu-id="64719-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64719-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64719-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64719-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64719-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64719-138">INPUTS</span></span>

## <span data-ttu-id="64719-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64719-139">OUTPUTS</span></span>

## <span data-ttu-id="64719-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64719-140">NOTES</span></span>

## <span data-ttu-id="64719-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64719-141">RELATED LINKS</span></span>

[<span data-ttu-id="64719-142">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="64719-142">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="64719-143">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="64719-143">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="64719-144">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="64719-144">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
