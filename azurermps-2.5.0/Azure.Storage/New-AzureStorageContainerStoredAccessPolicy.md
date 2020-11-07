---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 0610e4ca8bf520bc9812599747968a583641dd76
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898832"
---
# <span data-ttu-id="c3419-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c3419-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="c3419-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3419-102">SYNOPSIS</span></span>
<span data-ttu-id="c3419-103">Tworzy zapisane zasady dostępu dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c3419-103">Creates a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3419-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3419-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c3419-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c3419-105">DESCRIPTION</span></span>
<span data-ttu-id="c3419-106">Polecenie cmdlet **New-AzureStorageContainerStoredAccessPolicy** tworzy zapisane zasady dostępu dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c3419-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="c3419-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3419-107">EXAMPLES</span></span>

### <span data-ttu-id="c3419-108">Przykład 1. Tworzenie zapisanych zasad dostępu w kontenerze magazynu</span><span class="sxs-lookup"><span data-stu-id="c3419-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="c3419-109">To polecenie tworzy zasady dostępu o nazwie Policy01 w kontenerze magazynu o nazwie.</span><span class="sxs-lookup"><span data-stu-id="c3419-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="c3419-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3419-110">PARAMETERS</span></span>

### <span data-ttu-id="c3419-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c3419-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c3419-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="c3419-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c3419-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="c3419-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c3419-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="c3419-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c3419-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c3419-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c3419-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c3419-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c3419-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c3419-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c3419-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="c3419-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c3419-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="c3419-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c3419-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="c3419-120">The default value is 10.</span></span>

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

### <span data-ttu-id="c3419-121">-Kontener</span><span class="sxs-lookup"><span data-stu-id="c3419-121">-Container</span></span>
<span data-ttu-id="c3419-122">Określa nazwę kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c3419-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="c3419-123">-Context</span><span class="sxs-lookup"><span data-stu-id="c3419-123">-Context</span></span>
<span data-ttu-id="c3419-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c3419-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c3419-125">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c3419-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c3419-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3419-126">-DefaultProfile</span></span>
<span data-ttu-id="c3419-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3419-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3419-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c3419-128">-ExpiryTime</span></span>
<span data-ttu-id="c3419-129">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="c3419-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="c3419-130">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="c3419-130">-Permission</span></span>
<span data-ttu-id="c3419-131">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskiwania dostępu do kontenera.</span><span class="sxs-lookup"><span data-stu-id="c3419-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="c3419-132">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="c3419-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="c3419-133">-Policy</span><span class="sxs-lookup"><span data-stu-id="c3419-133">-Policy</span></span>
<span data-ttu-id="c3419-134">Określa zapisane zasady dostępu, które zawierają uprawnienia dla tego tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="c3419-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="c3419-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c3419-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c3419-136">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="c3419-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c3419-137">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="c3419-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c3419-138">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="c3419-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c3419-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c3419-139">-StartTime</span></span>
<span data-ttu-id="c3419-140">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="c3419-140">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="c3419-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3419-141">CommonParameters</span></span>
<span data-ttu-id="c3419-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3419-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3419-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3419-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3419-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3419-144">INPUTS</span></span>

### <span data-ttu-id="c3419-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c3419-145">System.String</span></span>

### <span data-ttu-id="c3419-146">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c3419-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c3419-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3419-147">OUTPUTS</span></span>

### <span data-ttu-id="c3419-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c3419-148">System.String</span></span>

## <span data-ttu-id="c3419-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3419-149">NOTES</span></span>

## <span data-ttu-id="c3419-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3419-150">RELATED LINKS</span></span>

[<span data-ttu-id="c3419-151">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c3419-151">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="c3419-152">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c3419-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="c3419-153">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c3419-153">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="c3419-154">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c3419-154">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


