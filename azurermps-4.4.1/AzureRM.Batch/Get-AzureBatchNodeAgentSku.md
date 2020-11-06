---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
ms.openlocfilehash: e29b5df4a72ff21dbacb0928b298306eb585b493
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551940"
---
# <span data-ttu-id="eaa06-101">Get-AzureBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="eaa06-101">Get-AzureBatchNodeAgentSku</span></span>

## <span data-ttu-id="eaa06-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eaa06-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa06-103">Pobiera jednostki SKU agenta węzła partii dostępne na koncie wsadowym.</span><span class="sxs-lookup"><span data-stu-id="eaa06-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaa06-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eaa06-104">SYNTAX</span></span>

```
Get-AzureBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaa06-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eaa06-105">DESCRIPTION</span></span>
<span data-ttu-id="eaa06-106">Polecenie cmdlet **Get-AzureBatchNodeAgentSku** Pobiera jednostki SKU agenta węzłów dostępne na koncie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="eaa06-106">The **Get-AzureBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="eaa06-107">Określ konto przy użyciu parametru *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="eaa06-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="eaa06-108">Wyszukiwanie można zawęzić do jednostek SKU zgodnych z filtrem Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="eaa06-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="eaa06-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eaa06-109">EXAMPLES</span></span>

### <span data-ttu-id="eaa06-110">Przykład 1. Pobierz wszystkie dostępne jednostki SKU agenta węzłów</span><span class="sxs-lookup"><span data-stu-id="eaa06-110">Example 1: Get all available node agent SKUs</span></span>
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

<span data-ttu-id="eaa06-111">Pierwsze polecenie pobiera kontekst konta wsadowego zawierający klucze dostępu dla subskrypcji przy użyciu polecenia **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="eaa06-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="eaa06-112">Polecenie zapisuje kontekst w zmiennej $Context do użycia w następnym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="eaa06-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="eaa06-113">Drugie polecenie pobiera wszystkie dostępne jednostki SKU agenta, które obsługują partię.</span><span class="sxs-lookup"><span data-stu-id="eaa06-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="eaa06-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eaa06-114">PARAMETERS</span></span>

### <span data-ttu-id="eaa06-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="eaa06-115">-BatchContext</span></span>
<span data-ttu-id="eaa06-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="eaa06-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="eaa06-117">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="eaa06-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="eaa06-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="eaa06-118">-Filter</span></span>
<span data-ttu-id="eaa06-119">Określa klauzulę filtru OData dla jednostek SKU agenta węzła.</span><span class="sxs-lookup"><span data-stu-id="eaa06-119">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="eaa06-120">Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie jednostki SKU agenta, które obsługują partię.</span><span class="sxs-lookup"><span data-stu-id="eaa06-120">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

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

### <span data-ttu-id="eaa06-121">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="eaa06-121">-MaxCount</span></span>
<span data-ttu-id="eaa06-122">Określa maksymalną liczbę jednostek SKU agenta węzła, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="eaa06-122">Specifies the maximum number of node agent SKUs to return.</span></span>

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

### <span data-ttu-id="eaa06-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaa06-123">-DefaultProfile</span></span>
<span data-ttu-id="eaa06-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eaa06-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaa06-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa06-125">CommonParameters</span></span>
<span data-ttu-id="eaa06-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaa06-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa06-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaa06-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa06-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eaa06-128">INPUTS</span></span>

### <span data-ttu-id="eaa06-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="eaa06-129">BatchAccountContext</span></span>
<span data-ttu-id="eaa06-130">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="eaa06-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="eaa06-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eaa06-131">OUTPUTS</span></span>

### <span data-ttu-id="eaa06-132">Microsoft.Azure.Commands.Batch. Modele. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="eaa06-132">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="eaa06-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eaa06-133">NOTES</span></span>

## <span data-ttu-id="eaa06-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eaa06-134">RELATED LINKS</span></span>

[<span data-ttu-id="eaa06-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="eaa06-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


