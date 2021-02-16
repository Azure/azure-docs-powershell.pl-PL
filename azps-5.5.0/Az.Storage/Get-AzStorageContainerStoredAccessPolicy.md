---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 5a0f976d561396bc93facfeedcbb1c89c768e5b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178203"
---
# <span data-ttu-id="ed4d1-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ed4d1-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="ed4d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed4d1-102">SYNOPSIS</span></span>
<span data-ttu-id="ed4d1-103">Pobiera zasady lub zasady dostępu przechowywane dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="ed4d1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ed4d1-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ed4d1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ed4d1-105">DESCRIPTION</span></span>
<span data-ttu-id="ed4d1-106">Polecenie **cmdlet Get-AzStorageContainerStoredAccessPolicy** zawiera listę przechowywanych zasad dostępu dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="ed4d1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ed4d1-107">EXAMPLES</span></span>

### <span data-ttu-id="ed4d1-108">Przykład 1. Uzyskiwanie przechowywanych zasad dostępu w kontenerze magazynu</span><span class="sxs-lookup"><span data-stu-id="ed4d1-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="ed4d1-109">To polecenie pobiera zasady dostępu o nazwie Zasady22 w kontenerze magazynu o nazwie Container07.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="ed4d1-110">Przykład 2. Uzyskiwanie wszystkich przechowywanych zasad dostępu w kontenerze magazynu</span><span class="sxs-lookup"><span data-stu-id="ed4d1-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="ed4d1-111">To polecenie pobiera wszystkie zasady dostępu w kontenerze magazynu o nazwie Container07.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="ed4d1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed4d1-112">PARAMETERS</span></span>

### <span data-ttu-id="ed4d1-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ed4d1-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ed4d1-114">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ed4d1-115">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ed4d1-116">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ed4d1-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ed4d1-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ed4d1-118">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ed4d1-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ed4d1-120">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ed4d1-121">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ed4d1-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-122">The default value is 10.</span></span>

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

### <span data-ttu-id="ed4d1-123">— Kontener</span><span class="sxs-lookup"><span data-stu-id="ed4d1-123">-Container</span></span>
<span data-ttu-id="ed4d1-124">Określa nazwę kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="ed4d1-125">— kontekst</span><span class="sxs-lookup"><span data-stu-id="ed4d1-125">-Context</span></span>
<span data-ttu-id="ed4d1-126">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="ed4d1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed4d1-127">-DefaultProfile</span></span>
<span data-ttu-id="ed4d1-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed4d1-129">— Zasady</span><span class="sxs-lookup"><span data-stu-id="ed4d1-129">-Policy</span></span>
<span data-ttu-id="ed4d1-130">Określa zasady dostępu przechowywanego na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-130">Specifies the Azure stored access policy.</span></span>

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

### <span data-ttu-id="ed4d1-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ed4d1-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ed4d1-132">Określa interwał po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ed4d1-133">Jeśli określony interwał pominie się przed rozpoczęciem przetwarzania żądania przez usługę magazynu, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="ed4d1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed4d1-134">CommonParameters</span></span>
<span data-ttu-id="ed4d1-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed4d1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed4d1-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed4d1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed4d1-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed4d1-137">INPUTS</span></span>

### <span data-ttu-id="ed4d1-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ed4d1-138">System.String</span></span>

### <span data-ttu-id="ed4d1-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ed4d1-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ed4d1-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ed4d1-140">OUTPUTS</span></span>

### <span data-ttu-id="ed4d1-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="ed4d1-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="ed4d1-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ed4d1-142">NOTES</span></span>

## <span data-ttu-id="ed4d1-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed4d1-143">RELATED LINKS</span></span>

[<span data-ttu-id="ed4d1-144">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ed4d1-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="ed4d1-145">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ed4d1-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="ed4d1-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ed4d1-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


