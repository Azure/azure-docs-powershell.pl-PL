---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: c0f1dc4972e3b71dce74bffb7a72e782774a2734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524574"
---
# <span data-ttu-id="c7bbf-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c7bbf-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="c7bbf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="c7bbf-103">Aktualizuje właściwości puli.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7bbf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7bbf-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7bbf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c7bbf-105">DESCRIPTION</span></span>
<span data-ttu-id="c7bbf-106">Polecenie cmdlet **Set-AzureBatchPool** aktualizuje właściwości puli w usłudze Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="c7bbf-107">Użyj polecenia cmdlet Get-AzureBatchPool, aby uzyskać obiekt **PSCloudPool** .</span><span class="sxs-lookup"><span data-stu-id="c7bbf-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="c7bbf-108">Zmodyfikuj właściwości tego obiektu, a następnie użyj bieżącego polecenia cmdlet, aby zatwierdzić zmiany w usłudze przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="c7bbf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7bbf-109">EXAMPLES</span></span>

### <span data-ttu-id="c7bbf-110">Przykład 1: aktualizowanie puli</span><span class="sxs-lookup"><span data-stu-id="c7bbf-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="c7bbf-111">Pierwsze polecenie uzyskuje pulę przy użyciu polecenia **Get-AzureBatchPool** , a następnie zapisuje ją w zmiennej $Pool.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="c7bbf-112">Kolejne trzy polecenia modyfikują specyfikację zadania rozpoczęcia dla obiektu $Pool.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="c7bbf-113">Polecenie ostatnie aktualizuje usługę wsadu tak, aby odpowiadała obiektowi lokalnemu w $Pool.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="c7bbf-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7bbf-114">PARAMETERS</span></span>

### <span data-ttu-id="c7bbf-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c7bbf-115">-BatchContext</span></span>
<span data-ttu-id="c7bbf-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c7bbf-117">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c7bbf-118">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c7bbf-119">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c7bbf-120">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c7bbf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7bbf-121">-DefaultProfile</span></span>
<span data-ttu-id="c7bbf-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7bbf-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="c7bbf-123">-Pool</span></span>
<span data-ttu-id="c7bbf-124">Określa **PSCloudPool** , do którego to polecenie cmdlet aktualizuje usługę wsadową.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7bbf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7bbf-125">CommonParameters</span></span>
<span data-ttu-id="c7bbf-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7bbf-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7bbf-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7bbf-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7bbf-128">INPUTS</span></span>

### <span data-ttu-id="c7bbf-129">Microsoft.Azure.Commands.Batch. Modele. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="c7bbf-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>
<span data-ttu-id="c7bbf-130">Parametry: Pool (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c7bbf-130">Parameters: Pool (ByValue)</span></span>

### <span data-ttu-id="c7bbf-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c7bbf-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="c7bbf-132">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c7bbf-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="c7bbf-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7bbf-133">OUTPUTS</span></span>

### <span data-ttu-id="c7bbf-134">System. void</span><span class="sxs-lookup"><span data-stu-id="c7bbf-134">System.Void</span></span>

## <span data-ttu-id="c7bbf-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7bbf-135">NOTES</span></span>

## <span data-ttu-id="c7bbf-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7bbf-136">RELATED LINKS</span></span>

[<span data-ttu-id="c7bbf-137">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c7bbf-137">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="c7bbf-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c7bbf-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c7bbf-139">Nowe — AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c7bbf-139">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="c7bbf-140">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c7bbf-140">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="c7bbf-141">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="c7bbf-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


