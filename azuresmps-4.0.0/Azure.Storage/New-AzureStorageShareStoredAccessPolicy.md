---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f76cd56055e800dc5d7d5ac15e66be23621ffbe2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523325"
---
# <span data-ttu-id="338ef-101">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="338ef-101">New-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="338ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="338ef-102">SYNOPSIS</span></span>
<span data-ttu-id="338ef-103">Tworzy zapisane zasady dostępu w udziale miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="338ef-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="338ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="338ef-104">SYNTAX</span></span>

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="338ef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="338ef-105">DESCRIPTION</span></span>
<span data-ttu-id="338ef-106">Polecenie cmdlet **New-AzureStorageShareStoredAccessPolicy** tworzy zapisane zasady dostępu w udziale magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="338ef-106">The **New-AzureStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="338ef-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="338ef-107">EXAMPLES</span></span>

### <span data-ttu-id="338ef-108">Przykład 1. Tworzenie zapisanych zasad dostępu w udziale</span><span class="sxs-lookup"><span data-stu-id="338ef-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="338ef-109">To polecenie tworzy zapisane zasady dostępu, które mają pełne uprawnienia w udziale.</span><span class="sxs-lookup"><span data-stu-id="338ef-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="338ef-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="338ef-110">PARAMETERS</span></span>

### <span data-ttu-id="338ef-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="338ef-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="338ef-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="338ef-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="338ef-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="338ef-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="338ef-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="338ef-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="338ef-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="338ef-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="338ef-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="338ef-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="338ef-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="338ef-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="338ef-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="338ef-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="338ef-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="338ef-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="338ef-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="338ef-120">The default value is 10.</span></span>

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

### <span data-ttu-id="338ef-121">-Context</span><span class="sxs-lookup"><span data-stu-id="338ef-121">-Context</span></span>
<span data-ttu-id="338ef-122">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="338ef-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="338ef-123">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="338ef-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="338ef-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="338ef-124">-ExpiryTime</span></span>
<span data-ttu-id="338ef-125">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="338ef-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="338ef-126">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="338ef-126">-Permission</span></span>
<span data-ttu-id="338ef-127">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskania dostępu do plików znajdujących się pod nim lub udostępnionych.</span><span class="sxs-lookup"><span data-stu-id="338ef-127">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="338ef-128">-Policy</span><span class="sxs-lookup"><span data-stu-id="338ef-128">-Policy</span></span>
<span data-ttu-id="338ef-129">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="338ef-129">Specifies a name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="338ef-130">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="338ef-130">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="338ef-131">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="338ef-131">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="338ef-132">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="338ef-132">-ShareName</span></span>
<span data-ttu-id="338ef-133">Określa nazwę udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="338ef-133">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="338ef-134">-StartTime</span><span class="sxs-lookup"><span data-stu-id="338ef-134">-StartTime</span></span>
<span data-ttu-id="338ef-135">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="338ef-135">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="338ef-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="338ef-136">CommonParameters</span></span>
<span data-ttu-id="338ef-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="338ef-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="338ef-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="338ef-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="338ef-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="338ef-139">INPUTS</span></span>

## <span data-ttu-id="338ef-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="338ef-140">OUTPUTS</span></span>

## <span data-ttu-id="338ef-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="338ef-141">NOTES</span></span>

## <span data-ttu-id="338ef-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="338ef-142">RELATED LINKS</span></span>

[<span data-ttu-id="338ef-143">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="338ef-143">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="338ef-144">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="338ef-144">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="338ef-145">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="338ef-145">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="338ef-146">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="338ef-146">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)