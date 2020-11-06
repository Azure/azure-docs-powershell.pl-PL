---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc7268d3d7d233f6a3fafeb92540e23ae3eaa6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523998"
---
# <span data-ttu-id="aeeff-101">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aeeff-101">Get-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="aeeff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aeeff-102">SYNOPSIS</span></span>
<span data-ttu-id="aeeff-103">Pobiera zasady dostępu do udziału w magazynie.</span><span class="sxs-lookup"><span data-stu-id="aeeff-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="aeeff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aeeff-104">SYNTAX</span></span>

```
Get-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="aeeff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aeeff-105">DESCRIPTION</span></span>
<span data-ttu-id="aeeff-106">Polecenie cmdlet **Get-AzureStorageShareStoredAccessPolicy** pobiera zasady dostępu do udziału w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="aeeff-106">The **Get-AzureStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="aeeff-107">Aby uzyskać określoną zasadę, określ ją według nazwy.</span><span class="sxs-lookup"><span data-stu-id="aeeff-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="aeeff-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aeeff-108">EXAMPLES</span></span>

### <span data-ttu-id="aeeff-109">Przykład 1: uzyskiwanie zapisanych zasad dostępu w udziale</span><span class="sxs-lookup"><span data-stu-id="aeeff-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="aeeff-110">To polecenie pobiera zapisane zasady dostępu o nazwie GeneralPolicy w ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="aeeff-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="aeeff-111">Przykład 2: uzyskiwanie wszystkich przechowywanych zasad dostępu w obszarze Udostępnianie</span><span class="sxs-lookup"><span data-stu-id="aeeff-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="aeeff-112">To polecenie pobiera wszystkie zapisane zasady dostępu w ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="aeeff-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="aeeff-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aeeff-113">PARAMETERS</span></span>

### <span data-ttu-id="aeeff-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="aeeff-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="aeeff-115">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="aeeff-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="aeeff-116">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="aeeff-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="aeeff-117">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="aeeff-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="aeeff-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="aeeff-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="aeeff-119">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="aeeff-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="aeeff-120">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="aeeff-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="aeeff-121">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="aeeff-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="aeeff-122">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="aeeff-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="aeeff-123">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="aeeff-123">The default value is 10.</span></span>

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

### <span data-ttu-id="aeeff-124">-Context</span><span class="sxs-lookup"><span data-stu-id="aeeff-124">-Context</span></span>
<span data-ttu-id="aeeff-125">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="aeeff-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="aeeff-126">Aby uzyskać kontekst, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="aeeff-126">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="aeeff-127">-Policy</span><span class="sxs-lookup"><span data-stu-id="aeeff-127">-Policy</span></span>
<span data-ttu-id="aeeff-128">Określa nazwę zasad dostępu przechowywanych w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aeeff-128">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeeff-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="aeeff-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="aeeff-130">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="aeeff-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="aeeff-131">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="aeeff-131">-ShareName</span></span>
<span data-ttu-id="aeeff-132">Określa nazwę udziału w magazynie, dla którego to polecenie cmdlet pobiera zasady.</span><span class="sxs-lookup"><span data-stu-id="aeeff-132">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aeeff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeeff-133">CommonParameters</span></span>
<span data-ttu-id="aeeff-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeeff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeeff-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeeff-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeeff-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aeeff-136">INPUTS</span></span>

## <span data-ttu-id="aeeff-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aeeff-137">OUTPUTS</span></span>

## <span data-ttu-id="aeeff-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aeeff-138">NOTES</span></span>

## <span data-ttu-id="aeeff-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aeeff-139">RELATED LINKS</span></span>

[<span data-ttu-id="aeeff-140">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="aeeff-140">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="aeeff-141">Nowe — AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aeeff-141">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="aeeff-142">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aeeff-142">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="aeeff-143">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aeeff-143">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
