---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: e5d177776e288a855c35def8d45310a6f6849c27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990466"
---
# <span data-ttu-id="23a4a-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="23a4a-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="23a4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23a4a-102">SYNOPSIS</span></span>
<span data-ttu-id="23a4a-103">Pobiera obrazy obsługiwane przez partię dla konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="23a4a-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="23a4a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="23a4a-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23a4a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="23a4a-105">DESCRIPTION</span></span>
<span data-ttu-id="23a4a-106">Polecenie **cmdlet Get-AzBatchSupportedImage** jest obsługiwane przez obrazy maszyn wirtualnych dostępne na koncie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="23a4a-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="23a4a-107">Określ konto, używając *parametru BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="23a4a-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="23a4a-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="23a4a-108">EXAMPLES</span></span>

### <span data-ttu-id="23a4a-109">Przykład 1. Uzyskiwanie wszystkich obsługiwanych obrazów</span><span class="sxs-lookup"><span data-stu-id="23a4a-109">Example 1: Get all available supported images</span></span>

```powershell
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchSupportedImage -BatchContext $Context
BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:16.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 16.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:18.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 18.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : credativ:debian:8:latest
NodeAgentSkuId        : batch.node.debian 8
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : microsoftwindowsserver:windowsserver:2016-datacenter:latest
NodeAgentSkuId        : batch.node.windows amd64
OSType                : Windows
VerificationType      : Verified

...
```

<span data-ttu-id="23a4a-110">Pierwsze polecenie uzyskuje kontekst konta wsadowego zawierający klucze dostępu dla Twojej subskrypcji przy użyciu klucza **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="23a4a-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="23a4a-111">Polecenie przechowuje kontekst w zmiennej $Context do użycia w następnym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="23a4a-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="23a4a-112">Drugie polecenie pobiera wszystkie obrazy obsługiwane dla tego konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="23a4a-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="23a4a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23a4a-113">PARAMETERS</span></span>

### <span data-ttu-id="23a4a-114">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="23a4a-114">-BatchContext</span></span>
<span data-ttu-id="23a4a-115">Wystąpienie BatchAccountContext do użycia podczas interakcji z usługą batch.</span><span class="sxs-lookup"><span data-stu-id="23a4a-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="23a4a-116">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="23a4a-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="23a4a-117">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="23a4a-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="23a4a-118">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="23a4a-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="23a4a-119">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="23a4a-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23a4a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23a4a-120">-DefaultProfile</span></span>
<span data-ttu-id="23a4a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="23a4a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23a4a-122">— Filtr</span><span class="sxs-lookup"><span data-stu-id="23a4a-122">-Filter</span></span>
<span data-ttu-id="23a4a-123">Określa klauzulę filtru OData dla obsługiwanych obrazów.</span><span class="sxs-lookup"><span data-stu-id="23a4a-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="23a4a-124">Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie obrazy, które obsługuje konto batch.</span><span class="sxs-lookup"><span data-stu-id="23a4a-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

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

### <span data-ttu-id="23a4a-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="23a4a-125">-MaxCount</span></span>
<span data-ttu-id="23a4a-126">Określa maksymalną liczbę obsługiwanych obrazów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="23a4a-126">Specifies the maximum number of supported images to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23a4a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23a4a-127">CommonParameters</span></span>
<span data-ttu-id="23a4a-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23a4a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23a4a-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23a4a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23a4a-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23a4a-130">INPUTS</span></span>

### <span data-ttu-id="23a4a-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="23a4a-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="23a4a-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23a4a-132">OUTPUTS</span></span>

### <span data-ttu-id="23a4a-133">Microsoft.Azure.Commands.Batch. Models.PSImageInformation</span><span class="sxs-lookup"><span data-stu-id="23a4a-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="23a4a-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="23a4a-134">NOTES</span></span>

## <span data-ttu-id="23a4a-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23a4a-135">RELATED LINKS</span></span>

[<span data-ttu-id="23a4a-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="23a4a-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)