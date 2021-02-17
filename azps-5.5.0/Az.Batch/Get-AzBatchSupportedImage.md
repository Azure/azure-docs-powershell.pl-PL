---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: e06b9957b8e9b58e25b52b69d4064aca1a69035a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239299"
---
# <span data-ttu-id="6a7bc-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="6a7bc-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="6a7bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a7bc-102">SYNOPSIS</span></span>
<span data-ttu-id="6a7bc-103">Pobiera obrazy obsługiwane przez partię dla konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="6a7bc-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="6a7bc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6a7bc-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a7bc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6a7bc-105">DESCRIPTION</span></span>
<span data-ttu-id="6a7bc-106">Polecenie **cmdlet Get-AzBatchSupportedImage** jest obsługiwane przez obrazy maszyn wirtualnych dostępne na koncie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="6a7bc-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="6a7bc-107">Określ konto, używając *parametru BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="6a7bc-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="6a7bc-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6a7bc-108">EXAMPLES</span></span>

### <span data-ttu-id="6a7bc-109">Przykład 1. Uzyskiwanie wszystkich obsługiwanych obrazów</span><span class="sxs-lookup"><span data-stu-id="6a7bc-109">Example 1: Get all available supported images</span></span>

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

<span data-ttu-id="6a7bc-110">Pierwsze polecenie uzyskuje kontekst konta wsadowego zawierający klucze dostępu dla Twojej subskrypcji przy użyciu klucza **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="6a7bc-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="6a7bc-111">Polecenie przechowuje kontekst w zmiennej $Context do użycia w następnym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="6a7bc-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="6a7bc-112">Drugie polecenie pobiera wszystkie obrazy obsługiwane dla tego konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="6a7bc-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="6a7bc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a7bc-113">PARAMETERS</span></span>

### <span data-ttu-id="6a7bc-114">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="6a7bc-114">-BatchContext</span></span>
<span data-ttu-id="6a7bc-115">Wystąpienie BatchAccountContext do użycia podczas interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="6a7bc-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="6a7bc-116">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6a7bc-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="6a7bc-117">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="6a7bc-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="6a7bc-118">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="6a7bc-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="6a7bc-119">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6a7bc-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6a7bc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a7bc-120">-DefaultProfile</span></span>
<span data-ttu-id="6a7bc-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a7bc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a7bc-122">— Filtr</span><span class="sxs-lookup"><span data-stu-id="6a7bc-122">-Filter</span></span>
<span data-ttu-id="6a7bc-123">Określa klauzulę filtru OData dla obsługiwanych obrazów.</span><span class="sxs-lookup"><span data-stu-id="6a7bc-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="6a7bc-124">Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie obrazy, które obsługuje konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="6a7bc-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

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

### <span data-ttu-id="6a7bc-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6a7bc-125">-MaxCount</span></span>
<span data-ttu-id="6a7bc-126">Określa maksymalną liczbę obsługiwanych obrazów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="6a7bc-126">Specifies the maximum number of supported images to return.</span></span>

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

### <span data-ttu-id="6a7bc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a7bc-127">CommonParameters</span></span>
<span data-ttu-id="6a7bc-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a7bc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a7bc-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a7bc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a7bc-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a7bc-130">INPUTS</span></span>

### <span data-ttu-id="6a7bc-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6a7bc-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6a7bc-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6a7bc-132">OUTPUTS</span></span>

### <span data-ttu-id="6a7bc-133">Microsoft.Azure.Commands.Batch. Models.PSImageInformation</span><span class="sxs-lookup"><span data-stu-id="6a7bc-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="6a7bc-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6a7bc-134">NOTES</span></span>

## <span data-ttu-id="6a7bc-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a7bc-135">RELATED LINKS</span></span>

[<span data-ttu-id="6a7bc-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6a7bc-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)