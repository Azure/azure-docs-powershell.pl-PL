---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95d5afafbed6ab6e3ba81cbfd509fd7b531217e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710774"
---
# <span data-ttu-id="9be71-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9be71-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="9be71-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9be71-102">SYNOPSIS</span></span>
<span data-ttu-id="9be71-103">Tworzy zapisane zasady dostępu dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9be71-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="9be71-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9be71-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="9be71-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9be71-105">DESCRIPTION</span></span>
<span data-ttu-id="9be71-106">Polecenie cmdlet **New-AzureStorageContainerStoredAccessPolicy** tworzy zapisane zasady dostępu dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9be71-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="9be71-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9be71-107">EXAMPLES</span></span>

### <span data-ttu-id="9be71-108">Przykład 1. Tworzenie zapisanych zasad dostępu w kontenerze magazynu</span><span class="sxs-lookup"><span data-stu-id="9be71-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="9be71-109">To polecenie tworzy zasady dostępu o nazwie Policy01 w kontenerze magazynu o nazwie.</span><span class="sxs-lookup"><span data-stu-id="9be71-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="9be71-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9be71-110">PARAMETERS</span></span>

### <span data-ttu-id="9be71-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9be71-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9be71-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="9be71-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9be71-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="9be71-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9be71-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="9be71-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9be71-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9be71-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9be71-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="9be71-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9be71-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="9be71-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9be71-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="9be71-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9be71-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="9be71-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9be71-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="9be71-120">The default value is 10.</span></span>

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

### <span data-ttu-id="9be71-121">-Kontener</span><span class="sxs-lookup"><span data-stu-id="9be71-121">-Container</span></span>
<span data-ttu-id="9be71-122">Określa nazwę kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9be71-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="9be71-123">-Context</span><span class="sxs-lookup"><span data-stu-id="9be71-123">-Context</span></span>
<span data-ttu-id="9be71-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9be71-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9be71-125">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="9be71-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9be71-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9be71-126">-ExpiryTime</span></span>
<span data-ttu-id="9be71-127">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="9be71-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="9be71-128">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="9be71-128">-Permission</span></span>
<span data-ttu-id="9be71-129">Określa poziom dostępu publicznego do tego kontenera.</span><span class="sxs-lookup"><span data-stu-id="9be71-129">Specifies the level of public access to this container.</span></span>

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

### <span data-ttu-id="9be71-130">-Policy</span><span class="sxs-lookup"><span data-stu-id="9be71-130">-Policy</span></span>
<span data-ttu-id="9be71-131">Określa zapisane zasady dostępu, które zawierają uprawnienia dla tego tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="9be71-131">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="9be71-132">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9be71-132">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9be71-133">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="9be71-133">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9be71-134">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="9be71-134">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9be71-135">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="9be71-135">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9be71-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9be71-136">-StartTime</span></span>
<span data-ttu-id="9be71-137">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="9be71-137">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="9be71-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9be71-138">CommonParameters</span></span>
<span data-ttu-id="9be71-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9be71-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9be71-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9be71-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9be71-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9be71-141">INPUTS</span></span>

## <span data-ttu-id="9be71-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9be71-142">OUTPUTS</span></span>

## <span data-ttu-id="9be71-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9be71-143">NOTES</span></span>

## <span data-ttu-id="9be71-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9be71-144">RELATED LINKS</span></span>

[<span data-ttu-id="9be71-145">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9be71-145">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="9be71-146">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9be71-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="9be71-147">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9be71-147">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="9be71-148">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9be71-148">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


