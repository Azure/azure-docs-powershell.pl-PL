---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: 8db1f11cfd434beb52eb32e4b175b2dab67ecbdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717645"
---
# <span data-ttu-id="bedd3-101">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="bedd3-101">Stop-AzureBatchPoolResize</span></span>

## <span data-ttu-id="bedd3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bedd3-102">SYNOPSIS</span></span>
<span data-ttu-id="bedd3-103">Zatrzymuje operację zmiany rozmiaru puli.</span><span class="sxs-lookup"><span data-stu-id="bedd3-103">Stops a pool resize operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bedd3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bedd3-104">SYNTAX</span></span>

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bedd3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bedd3-105">DESCRIPTION</span></span>
<span data-ttu-id="bedd3-106">Polecenie cmdlet **stop-AzureBatchPoolResize** zatrzymuje operację zmiany rozmiaru wsadu Azure Part na puli.</span><span class="sxs-lookup"><span data-stu-id="bedd3-106">The **Stop-AzureBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="bedd3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bedd3-107">EXAMPLES</span></span>

### <span data-ttu-id="bedd3-108">Przykład 1. Zatrzymaj zmianę rozmiaru puli</span><span class="sxs-lookup"><span data-stu-id="bedd3-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="bedd3-109">To polecenie zatrzymuje operację zmiany rozmiaru puli o IDENTYFIKATORze ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="bedd3-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="bedd3-110">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="bedd3-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="bedd3-111">Przykład 2: zatrzymywanie zmiany rozmiaru puli za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="bedd3-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="bedd3-112">To polecenie zatrzymuje zmianę rozmiaru puli za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="bedd3-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="bedd3-113">Polecenie pobiera pulę o IDENTYFIKATORze ContosoPool06 przy użyciu polecenia cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="bedd3-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="bedd3-114">Polecenie przekazuje ten obiekt puli do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bedd3-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="bedd3-115">Polecenie zatrzyma operację zmiany rozmiaru w tej puli.</span><span class="sxs-lookup"><span data-stu-id="bedd3-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="bedd3-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bedd3-116">PARAMETERS</span></span>

### <span data-ttu-id="bedd3-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bedd3-117">-BatchContext</span></span>
<span data-ttu-id="bedd3-118">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="bedd3-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bedd3-119">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="bedd3-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bedd3-120">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="bedd3-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bedd3-121">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="bedd3-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bedd3-122">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="bedd3-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bedd3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bedd3-123">-DefaultProfile</span></span>
<span data-ttu-id="bedd3-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bedd3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bedd3-125">-ID</span><span class="sxs-lookup"><span data-stu-id="bedd3-125">-Id</span></span>
<span data-ttu-id="bedd3-126">Określa identyfikator puli, dla którego to polecenie cmdlet zatrzyma operację zmiany rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="bedd3-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bedd3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bedd3-127">CommonParameters</span></span>
<span data-ttu-id="bedd3-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bedd3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bedd3-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bedd3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bedd3-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bedd3-130">INPUTS</span></span>

### <span data-ttu-id="bedd3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bedd3-131">System.String</span></span>

### <span data-ttu-id="bedd3-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bedd3-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="bedd3-133">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bedd3-133">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="bedd3-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bedd3-134">OUTPUTS</span></span>

### <span data-ttu-id="bedd3-135">System. void</span><span class="sxs-lookup"><span data-stu-id="bedd3-135">System.Void</span></span>

## <span data-ttu-id="bedd3-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bedd3-136">NOTES</span></span>

## <span data-ttu-id="bedd3-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bedd3-137">RELATED LINKS</span></span>

[<span data-ttu-id="bedd3-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bedd3-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bedd3-139">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="bedd3-139">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="bedd3-140">Start — AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="bedd3-140">Start-AzureBatchPoolResize</span></span>](./Start-AzureBatchPoolResize.md)

[<span data-ttu-id="bedd3-141">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="bedd3-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


