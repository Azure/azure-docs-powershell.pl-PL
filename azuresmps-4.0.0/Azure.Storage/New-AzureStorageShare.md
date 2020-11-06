---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: ''
schema: 2.0.0
ms.openlocfilehash: 381bfc62ed3a80b650b61b11790a87658a75ee9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523566"
---
# <span data-ttu-id="2a5e7-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="2a5e7-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="2a5e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="2a5e7-103">Umożliwia utworzenie udziału plików.</span><span class="sxs-lookup"><span data-stu-id="2a5e7-103">Creates a file share.</span></span>

## <span data-ttu-id="2a5e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a5e7-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2a5e7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2a5e7-105">DESCRIPTION</span></span>
<span data-ttu-id="2a5e7-106">Polecenie cmdlet **New-AzureStorageShare** umożliwia utworzenie udziału plików.</span><span class="sxs-lookup"><span data-stu-id="2a5e7-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="2a5e7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a5e7-107">EXAMPLES</span></span>

### <span data-ttu-id="2a5e7-108">Przykład 1. Tworzenie udziału plików</span><span class="sxs-lookup"><span data-stu-id="2a5e7-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="2a5e7-109">To polecenie tworzy udział plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="2a5e7-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="2a5e7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a5e7-110">PARAMETERS</span></span>

### <span data-ttu-id="2a5e7-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2a5e7-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2a5e7-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="2a5e7-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2a5e7-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="2a5e7-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2a5e7-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="2a5e7-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2a5e7-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2a5e7-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2a5e7-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="2a5e7-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2a5e7-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="2a5e7-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2a5e7-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="2a5e7-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2a5e7-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="2a5e7-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2a5e7-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="2a5e7-120">The default value is 10.</span></span>

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

### <span data-ttu-id="2a5e7-121">-Context</span><span class="sxs-lookup"><span data-stu-id="2a5e7-121">-Context</span></span>
<span data-ttu-id="2a5e7-122">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2a5e7-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2a5e7-123">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="2a5e7-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="2a5e7-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2a5e7-124">-Name</span></span>
<span data-ttu-id="2a5e7-125">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="2a5e7-125">Specifies the name of a file share.</span></span>
<span data-ttu-id="2a5e7-126">To polecenie cmdlet powoduje utworzenie udziału plików o nazwie określającej ten parametr.</span><span class="sxs-lookup"><span data-stu-id="2a5e7-126">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5e7-127">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2a5e7-127">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2a5e7-128">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="2a5e7-128">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="2a5e7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a5e7-129">CommonParameters</span></span>
<span data-ttu-id="2a5e7-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a5e7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a5e7-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a5e7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a5e7-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a5e7-132">INPUTS</span></span>

## <span data-ttu-id="2a5e7-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a5e7-133">OUTPUTS</span></span>

## <span data-ttu-id="2a5e7-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a5e7-134">NOTES</span></span>

## <span data-ttu-id="2a5e7-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a5e7-135">RELATED LINKS</span></span>

[<span data-ttu-id="2a5e7-136">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="2a5e7-136">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="2a5e7-137">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="2a5e7-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="2a5e7-138">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="2a5e7-138">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
