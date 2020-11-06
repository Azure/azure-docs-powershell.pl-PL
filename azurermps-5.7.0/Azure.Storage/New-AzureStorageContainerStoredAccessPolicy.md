---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 072e9b16bec9709808cd3da7c90d60a6055f0363
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545896"
---
# <span data-ttu-id="b8b9c-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b8b9c-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="b8b9c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b9c-103">Tworzy zapisane zasady dostępu dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-103">Creates a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8b9c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8b9c-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8b9c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b8b9c-105">DESCRIPTION</span></span>
<span data-ttu-id="b8b9c-106">Polecenie cmdlet **New-AzureStorageContainerStoredAccessPolicy** tworzy zapisane zasady dostępu dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="b8b9c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8b9c-107">EXAMPLES</span></span>

### <span data-ttu-id="b8b9c-108">Przykład 1. Tworzenie zapisanych zasad dostępu w kontenerze magazynu</span><span class="sxs-lookup"><span data-stu-id="b8b9c-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="b8b9c-109">To polecenie tworzy zasady dostępu o nazwie Policy01 w kontenerze magazynu o nazwie.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="b8b9c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8b9c-110">PARAMETERS</span></span>

### <span data-ttu-id="b8b9c-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8b9c-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b8b9c-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b8b9c-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b8b9c-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b8b9c-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b8b9c-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b8b9c-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b8b9c-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b8b9c-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b8b9c-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b8b9c-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-120">The default value is 10.</span></span>

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

### <span data-ttu-id="b8b9c-121">-Kontener</span><span class="sxs-lookup"><span data-stu-id="b8b9c-121">-Container</span></span>
<span data-ttu-id="b8b9c-122">Określa nazwę kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="b8b9c-123">-Context</span><span class="sxs-lookup"><span data-stu-id="b8b9c-123">-Context</span></span>
<span data-ttu-id="b8b9c-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b8b9c-125">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b8b9c-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b8b9c-126">-ExpiryTime</span></span>
<span data-ttu-id="b8b9c-127">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="b8b9c-128">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="b8b9c-128">-Permission</span></span>
<span data-ttu-id="b8b9c-129">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskiwania dostępu do kontenera.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-129">Specifies permissions in the stored access policy to access the container.</span></span>

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

### <span data-ttu-id="b8b9c-130">-Policy</span><span class="sxs-lookup"><span data-stu-id="b8b9c-130">-Policy</span></span>
<span data-ttu-id="b8b9c-131">Określa zapisane zasady dostępu, które zawierają uprawnienia dla tego tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-131">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="b8b9c-132">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8b9c-132">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b8b9c-133">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-133">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b8b9c-134">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-134">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b8b9c-135">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-135">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b8b9c-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b8b9c-136">-StartTime</span></span>
<span data-ttu-id="b8b9c-137">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-137">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="b8b9c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b9c-138">CommonParameters</span></span>
<span data-ttu-id="b8b9c-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8b9c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b9c-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8b9c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b9c-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8b9c-141">INPUTS</span></span>

### <span data-ttu-id="b8b9c-142">Ciąg</span><span class="sxs-lookup"><span data-stu-id="b8b9c-142">String</span></span>

<span data-ttu-id="b8b9c-143">Parametr "Container" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="b8b9c-143">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="b8b9c-144">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b8b9c-144">IStorageContext</span></span>

<span data-ttu-id="b8b9c-145">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="b8b9c-145">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="b8b9c-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8b9c-146">OUTPUTS</span></span>

### <span data-ttu-id="b8b9c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b8b9c-147">System.String</span></span>

## <span data-ttu-id="b8b9c-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8b9c-148">NOTES</span></span>

## <span data-ttu-id="b8b9c-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8b9c-149">RELATED LINKS</span></span>

[<span data-ttu-id="b8b9c-150">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b8b9c-150">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="b8b9c-151">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b8b9c-151">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b8b9c-152">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b8b9c-152">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="b8b9c-153">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b8b9c-153">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


