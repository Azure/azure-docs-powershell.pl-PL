---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: c4190508a50a8267108b428f4bf993be226cec2b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892245"
---
# <span data-ttu-id="e1e34-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e1e34-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="e1e34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1e34-102">SYNOPSIS</span></span>
<span data-ttu-id="e1e34-103">Pobiera zasady programu Access lub zasady dotyczące kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e1e34-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="e1e34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1e34-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="e1e34-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e1e34-105">DESCRIPTION</span></span>
<span data-ttu-id="e1e34-106">Polecenie cmdlet **Get-AzStorageContainerStoredAccessPolicy** zawiera listę przechowywanych zasad dostępu lub zasad dotyczących kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e1e34-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="e1e34-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1e34-107">EXAMPLES</span></span>

### <span data-ttu-id="e1e34-108">Przykład 1: uzyskiwanie zapisanych zasad dostępu w kontenerze magazynu</span><span class="sxs-lookup"><span data-stu-id="e1e34-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="e1e34-109">To polecenie pobiera zasady dostępu o nazwie Policy22 w kontenerze magazynu o nazwie Container07.</span><span class="sxs-lookup"><span data-stu-id="e1e34-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="e1e34-110">Przykład 2: uzyskiwanie wszystkich przechowywanych zasad dostępu w kontenerze magazynu</span><span class="sxs-lookup"><span data-stu-id="e1e34-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="e1e34-111">To polecenie pobiera wszystkie zasady dostępu w kontenerze magazynu o nazwie Container07.</span><span class="sxs-lookup"><span data-stu-id="e1e34-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="e1e34-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1e34-112">PARAMETERS</span></span>

### <span data-ttu-id="e1e34-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e1e34-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e1e34-114">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="e1e34-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e1e34-115">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="e1e34-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e1e34-116">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="e1e34-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e1e34-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e1e34-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e1e34-118">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="e1e34-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e1e34-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="e1e34-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e1e34-120">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="e1e34-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e1e34-121">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="e1e34-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e1e34-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="e1e34-122">The default value is 10.</span></span>

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

### <span data-ttu-id="e1e34-123">-Kontener</span><span class="sxs-lookup"><span data-stu-id="e1e34-123">-Container</span></span>
<span data-ttu-id="e1e34-124">Określa nazwę kontenera usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e1e34-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="e1e34-125">-Context</span><span class="sxs-lookup"><span data-stu-id="e1e34-125">-Context</span></span>
<span data-ttu-id="e1e34-126">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e1e34-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="e1e34-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1e34-127">-DefaultProfile</span></span>
<span data-ttu-id="e1e34-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1e34-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1e34-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="e1e34-129">-Policy</span></span>
<span data-ttu-id="e1e34-130">Określa zasady dostępu przechowywane na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e1e34-130">Specifies the Azure stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1e34-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e1e34-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e1e34-132">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="e1e34-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="e1e34-133">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="e1e34-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="e1e34-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1e34-134">CommonParameters</span></span>
<span data-ttu-id="e1e34-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1e34-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1e34-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1e34-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1e34-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1e34-137">INPUTS</span></span>

### <span data-ttu-id="e1e34-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e1e34-138">System.String</span></span>

### <span data-ttu-id="e1e34-139">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e1e34-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e1e34-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1e34-140">OUTPUTS</span></span>

### <span data-ttu-id="e1e34-141">Microsoft. WindowsAz. Storage. blob. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="e1e34-141">Microsoft.WindowsAz.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="e1e34-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1e34-142">NOTES</span></span>

## <span data-ttu-id="e1e34-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1e34-143">RELATED LINKS</span></span>

[<span data-ttu-id="e1e34-144">Nowe — AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e1e34-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="e1e34-145">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e1e34-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="e1e34-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e1e34-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


