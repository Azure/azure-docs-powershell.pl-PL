---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 6dadd92955c325120b67d8faae99c7f8ae90dc5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547792"
---
# <span data-ttu-id="b6954-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b6954-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="b6954-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6954-102">SYNOPSIS</span></span>
<span data-ttu-id="b6954-103">Tworzy zapisane zasady dostępu dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b6954-103">Creates a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6954-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6954-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b6954-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6954-105">DESCRIPTION</span></span>
<span data-ttu-id="b6954-106">Polecenie cmdlet **New-AzureStorageContainerStoredAccessPolicy** tworzy zapisane zasady dostępu dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b6954-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="b6954-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6954-107">EXAMPLES</span></span>

### <span data-ttu-id="b6954-108">Przykład 1. Tworzenie zapisanych zasad dostępu w kontenerze magazynu</span><span class="sxs-lookup"><span data-stu-id="b6954-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="b6954-109">To polecenie tworzy zasady dostępu o nazwie Policy01 w kontenerze magazynu o nazwie.</span><span class="sxs-lookup"><span data-stu-id="b6954-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="b6954-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6954-110">PARAMETERS</span></span>

### <span data-ttu-id="b6954-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b6954-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b6954-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="b6954-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b6954-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="b6954-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b6954-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="b6954-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b6954-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b6954-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b6954-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b6954-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b6954-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b6954-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b6954-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="b6954-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b6954-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="b6954-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b6954-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="b6954-120">The default value is 10.</span></span>

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

### <span data-ttu-id="b6954-121">-Kontener</span><span class="sxs-lookup"><span data-stu-id="b6954-121">-Container</span></span>
<span data-ttu-id="b6954-122">Określa nazwę kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b6954-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6954-123">-Context</span><span class="sxs-lookup"><span data-stu-id="b6954-123">-Context</span></span>
<span data-ttu-id="b6954-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b6954-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b6954-125">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b6954-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b6954-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6954-126">-DefaultProfile</span></span>
<span data-ttu-id="b6954-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6954-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6954-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b6954-128">-ExpiryTime</span></span>
<span data-ttu-id="b6954-129">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="b6954-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6954-130">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="b6954-130">-Permission</span></span>
<span data-ttu-id="b6954-131">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskiwania dostępu do kontenera.</span><span class="sxs-lookup"><span data-stu-id="b6954-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="b6954-132">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="b6954-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6954-133">-Policy</span><span class="sxs-lookup"><span data-stu-id="b6954-133">-Policy</span></span>
<span data-ttu-id="b6954-134">Określa zapisane zasady dostępu, które zawierają uprawnienia dla tego tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="b6954-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6954-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b6954-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b6954-136">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="b6954-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b6954-137">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="b6954-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b6954-138">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="b6954-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b6954-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b6954-139">-StartTime</span></span>
<span data-ttu-id="b6954-140">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="b6954-140">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6954-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6954-141">CommonParameters</span></span>
<span data-ttu-id="b6954-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6954-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6954-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6954-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6954-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6954-144">INPUTS</span></span>

### <span data-ttu-id="b6954-145">System. String</span><span class="sxs-lookup"><span data-stu-id="b6954-145">System.String</span></span>

### <span data-ttu-id="b6954-146">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b6954-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b6954-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6954-147">OUTPUTS</span></span>

### <span data-ttu-id="b6954-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b6954-148">System.String</span></span>

## <span data-ttu-id="b6954-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6954-149">NOTES</span></span>

## <span data-ttu-id="b6954-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6954-150">RELATED LINKS</span></span>

[<span data-ttu-id="b6954-151">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b6954-151">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="b6954-152">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b6954-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b6954-153">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b6954-153">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="b6954-154">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b6954-154">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


