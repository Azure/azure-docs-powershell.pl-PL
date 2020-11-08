---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: e06b9957b8e9b58e25b52b69d4064aca1a69035a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233696"
---
# <span data-ttu-id="9ae41-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="9ae41-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="9ae41-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ae41-102">SYNOPSIS</span></span>
<span data-ttu-id="9ae41-103">Pobiera obrazy obsługiwane przez partię dla konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9ae41-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="9ae41-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ae41-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ae41-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9ae41-105">DESCRIPTION</span></span>
<span data-ttu-id="9ae41-106">Polecenie cmdlet **Get-AzBatchSupportedImage** umożliwia pobieranie obsługiwanych obrazów maszyny wirtualnej dostępnych na koncie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="9ae41-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="9ae41-107">Określ konto przy użyciu parametru *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="9ae41-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="9ae41-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ae41-108">EXAMPLES</span></span>

### <span data-ttu-id="9ae41-109">Przykład 1: pobieranie wszystkich dostępnych obsługiwanych obrazów</span><span class="sxs-lookup"><span data-stu-id="9ae41-109">Example 1: Get all available supported images</span></span>

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

<span data-ttu-id="9ae41-110">Pierwsze polecenie pobiera kontekst konta wsadowego zawierający klucze dostępu dla subskrypcji przy użyciu polecenia **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="9ae41-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="9ae41-111">Polecenie zapisuje kontekst w zmiennej $Context do użycia w następnym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="9ae41-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="9ae41-112">Drugie polecenie pobiera wszystkie dostępne obrazy dla tego konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9ae41-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="9ae41-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ae41-113">PARAMETERS</span></span>

### <span data-ttu-id="9ae41-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9ae41-114">-BatchContext</span></span>
<span data-ttu-id="9ae41-115">Wystąpienie BatchAccountContext, które ma być używane podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9ae41-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="9ae41-116">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9ae41-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="9ae41-117">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="9ae41-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="9ae41-118">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="9ae41-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="9ae41-119">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="9ae41-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9ae41-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ae41-120">-DefaultProfile</span></span>
<span data-ttu-id="9ae41-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae41-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ae41-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="9ae41-122">-Filter</span></span>
<span data-ttu-id="9ae41-123">Określa klauzulę filtru OData dla obsługiwanych obrazów.</span><span class="sxs-lookup"><span data-stu-id="9ae41-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="9ae41-124">Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie obrazy obsługiwane przez konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="9ae41-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

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

### <span data-ttu-id="9ae41-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="9ae41-125">-MaxCount</span></span>
<span data-ttu-id="9ae41-126">Określa maksymalną liczbę obsługiwanych obrazów, które należy zwrócić.</span><span class="sxs-lookup"><span data-stu-id="9ae41-126">Specifies the maximum number of supported images to return.</span></span>

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

### <span data-ttu-id="9ae41-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ae41-127">CommonParameters</span></span>
<span data-ttu-id="9ae41-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ae41-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ae41-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ae41-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ae41-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ae41-130">INPUTS</span></span>

### <span data-ttu-id="9ae41-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9ae41-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9ae41-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ae41-132">OUTPUTS</span></span>

### <span data-ttu-id="9ae41-133">Microsoft.Azure.Commands.Batch. Modele. PSImageInformation</span><span class="sxs-lookup"><span data-stu-id="9ae41-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="9ae41-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ae41-134">NOTES</span></span>

## <span data-ttu-id="9ae41-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ae41-135">RELATED LINKS</span></span>

[<span data-ttu-id="9ae41-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9ae41-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)