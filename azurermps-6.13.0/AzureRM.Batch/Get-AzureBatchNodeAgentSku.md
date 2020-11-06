---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodeagentsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
ms.openlocfilehash: 86451c1ac7ba52c9b013b3724d9c706caaa961ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524582"
---
# <span data-ttu-id="4e641-101">Get-AzureBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="4e641-101">Get-AzureBatchNodeAgentSku</span></span>

## <span data-ttu-id="4e641-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e641-102">SYNOPSIS</span></span>
<span data-ttu-id="4e641-103">Pobiera jednostki SKU agenta węzła partii dostępne na koncie wsadowym.</span><span class="sxs-lookup"><span data-stu-id="4e641-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e641-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e641-104">SYNTAX</span></span>

```
Get-AzureBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e641-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4e641-105">DESCRIPTION</span></span>
<span data-ttu-id="4e641-106">Polecenie cmdlet **Get-AzureBatchNodeAgentSku** Pobiera jednostki SKU agenta węzłów dostępne na koncie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="4e641-106">The **Get-AzureBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="4e641-107">Określ konto przy użyciu parametru *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="4e641-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="4e641-108">Wyszukiwanie można zawęzić do jednostek SKU zgodnych z filtrem Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="4e641-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="4e641-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e641-109">EXAMPLES</span></span>

### <span data-ttu-id="4e641-110">Przykład 1. Pobierz wszystkie dostępne jednostki SKU agenta węzłów</span><span class="sxs-lookup"><span data-stu-id="4e641-110">Example 1: Get all available node agent SKUs</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

<span data-ttu-id="4e641-111">Pierwsze polecenie pobiera kontekst konta wsadowego zawierający klucze dostępu dla subskrypcji przy użyciu polecenia **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="4e641-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="4e641-112">Polecenie zapisuje kontekst w zmiennej $Context do użycia w następnym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="4e641-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="4e641-113">Drugie polecenie pobiera wszystkie dostępne jednostki SKU agenta, które obsługują partię.</span><span class="sxs-lookup"><span data-stu-id="4e641-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="4e641-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e641-114">PARAMETERS</span></span>

### <span data-ttu-id="4e641-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4e641-115">-BatchContext</span></span>
<span data-ttu-id="4e641-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="4e641-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4e641-117">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="4e641-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4e641-118">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="4e641-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4e641-119">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="4e641-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4e641-120">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4e641-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4e641-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e641-121">-DefaultProfile</span></span>
<span data-ttu-id="4e641-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e641-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e641-123">-Filter</span><span class="sxs-lookup"><span data-stu-id="4e641-123">-Filter</span></span>
<span data-ttu-id="4e641-124">Określa klauzulę filtru OData dla jednostek SKU agenta węzła.</span><span class="sxs-lookup"><span data-stu-id="4e641-124">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="4e641-125">Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie jednostki SKU agenta, które obsługują partię.</span><span class="sxs-lookup"><span data-stu-id="4e641-125">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

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

### <span data-ttu-id="4e641-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4e641-126">-MaxCount</span></span>
<span data-ttu-id="4e641-127">Określa maksymalną liczbę jednostek SKU agenta węzła, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="4e641-127">Specifies the maximum number of node agent SKUs to return.</span></span>

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

### <span data-ttu-id="4e641-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e641-128">CommonParameters</span></span>
<span data-ttu-id="4e641-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e641-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e641-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e641-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e641-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e641-131">INPUTS</span></span>

### <span data-ttu-id="4e641-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4e641-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="4e641-133">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4e641-133">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="4e641-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e641-134">OUTPUTS</span></span>

### <span data-ttu-id="4e641-135">Microsoft.Azure.Commands.Batch. Modele. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="4e641-135">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="4e641-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e641-136">NOTES</span></span>

## <span data-ttu-id="4e641-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e641-137">RELATED LINKS</span></span>

[<span data-ttu-id="4e641-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="4e641-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


