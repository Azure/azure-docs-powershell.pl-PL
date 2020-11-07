---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 71f00e9e1842eef237a7128d5e20e2ac2116e8a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887889"
---
# <span data-ttu-id="8e47d-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8e47d-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="8e47d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e47d-102">SYNOPSIS</span></span>
<span data-ttu-id="8e47d-103">Pobiera zasady programu Access lub zasady dotyczące kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8e47d-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="8e47d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e47d-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="8e47d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8e47d-105">DESCRIPTION</span></span>
<span data-ttu-id="8e47d-106">Polecenie cmdlet **Get-AzStorageContainerStoredAccessPolicy** zawiera listę przechowywanych zasad dostępu lub zasad dotyczących kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8e47d-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="8e47d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e47d-107">EXAMPLES</span></span>

### <span data-ttu-id="8e47d-108">Przykład 1: uzyskiwanie zapisanych zasad dostępu w kontenerze magazynu</span><span class="sxs-lookup"><span data-stu-id="8e47d-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="8e47d-109">To polecenie pobiera zasady dostępu o nazwie Policy22 w kontenerze magazynu o nazwie Container07.</span><span class="sxs-lookup"><span data-stu-id="8e47d-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="8e47d-110">Przykład 2: uzyskiwanie wszystkich przechowywanych zasad dostępu w kontenerze magazynu</span><span class="sxs-lookup"><span data-stu-id="8e47d-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="8e47d-111">To polecenie pobiera wszystkie zasady dostępu w kontenerze magazynu o nazwie Container07.</span><span class="sxs-lookup"><span data-stu-id="8e47d-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="8e47d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e47d-112">PARAMETERS</span></span>

### <span data-ttu-id="8e47d-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8e47d-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8e47d-114">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="8e47d-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8e47d-115">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="8e47d-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8e47d-116">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="8e47d-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e47d-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8e47d-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8e47d-118">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8e47d-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8e47d-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8e47d-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8e47d-120">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="8e47d-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8e47d-121">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="8e47d-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8e47d-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="8e47d-122">The default value is 10.</span></span>

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

### <span data-ttu-id="8e47d-123">-Kontener</span><span class="sxs-lookup"><span data-stu-id="8e47d-123">-Container</span></span>
<span data-ttu-id="8e47d-124">Określa nazwę kontenera usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8e47d-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="8e47d-125">-Context</span><span class="sxs-lookup"><span data-stu-id="8e47d-125">-Context</span></span>
<span data-ttu-id="8e47d-126">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8e47d-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="8e47d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e47d-127">-DefaultProfile</span></span>
<span data-ttu-id="8e47d-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e47d-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e47d-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="8e47d-129">-Policy</span></span>
<span data-ttu-id="8e47d-130">Określa zasady dostępu przechowywane na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="8e47d-130">Specifies the Azure stored access policy.</span></span>

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

### <span data-ttu-id="8e47d-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8e47d-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8e47d-132">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="8e47d-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="8e47d-133">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="8e47d-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e47d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e47d-134">CommonParameters</span></span>
<span data-ttu-id="8e47d-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e47d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e47d-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e47d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e47d-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e47d-137">INPUTS</span></span>

### <span data-ttu-id="8e47d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8e47d-138">System.String</span></span>

### <span data-ttu-id="8e47d-139">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8e47d-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8e47d-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e47d-140">OUTPUTS</span></span>

### <span data-ttu-id="8e47d-141">Microsoft. Azure. Storage. blob. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="8e47d-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="8e47d-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e47d-142">NOTES</span></span>

## <span data-ttu-id="8e47d-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e47d-143">RELATED LINKS</span></span>

[<span data-ttu-id="8e47d-144">Nowe — AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8e47d-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="8e47d-145">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8e47d-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="8e47d-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8e47d-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


