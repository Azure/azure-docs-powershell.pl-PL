---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 423f249a7971883cbe47d8f499fdd780980362f3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347521"
---
# <span data-ttu-id="539ee-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="539ee-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="539ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="539ee-102">SYNOPSIS</span></span>
<span data-ttu-id="539ee-103">Aktualizuje właściwości puli.</span><span class="sxs-lookup"><span data-stu-id="539ee-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="539ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="539ee-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="539ee-105">Opis</span><span class="sxs-lookup"><span data-stu-id="539ee-105">DESCRIPTION</span></span>
<span data-ttu-id="539ee-106">Polecenie cmdlet **Set-AzBatchPool** aktualizuje właściwości puli w usłudze Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="539ee-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="539ee-107">Użyj polecenia cmdlet Get-AzBatchPool, aby uzyskać obiekt **PSCloudPool** .</span><span class="sxs-lookup"><span data-stu-id="539ee-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="539ee-108">Zmodyfikuj właściwości tego obiektu, a następnie użyj bieżącego polecenia cmdlet, aby zatwierdzić zmiany w usłudze przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="539ee-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="539ee-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="539ee-109">EXAMPLES</span></span>

### <span data-ttu-id="539ee-110">Przykład 1: aktualizowanie puli</span><span class="sxs-lookup"><span data-stu-id="539ee-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="539ee-111">Pierwsze polecenie uzyskuje pulę przy użyciu polecenia **Get-AzBatchPool**, a następnie zapisuje ją w zmiennej $Pool.</span><span class="sxs-lookup"><span data-stu-id="539ee-111">The first command gets a pool by using **Get-AzBatchPool**, and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="539ee-112">Kolejne trzy polecenia modyfikują specyfikację zadania rozpoczęcia dla obiektu $Pool.</span><span class="sxs-lookup"><span data-stu-id="539ee-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="539ee-113">Polecenie ostatnie aktualizuje usługę wsadu tak, aby odpowiadała obiektowi lokalnemu w $Pool.</span><span class="sxs-lookup"><span data-stu-id="539ee-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="539ee-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="539ee-114">PARAMETERS</span></span>

### <span data-ttu-id="539ee-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="539ee-115">-BatchContext</span></span>
<span data-ttu-id="539ee-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="539ee-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="539ee-117">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="539ee-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="539ee-118">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="539ee-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="539ee-119">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="539ee-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="539ee-120">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="539ee-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="539ee-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="539ee-121">-DefaultProfile</span></span>
<span data-ttu-id="539ee-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="539ee-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="539ee-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="539ee-123">-Pool</span></span>
<span data-ttu-id="539ee-124">Określa **PSCloudPool** , do którego to polecenie cmdlet aktualizuje usługę wsadową.</span><span class="sxs-lookup"><span data-stu-id="539ee-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="539ee-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="539ee-125">CommonParameters</span></span>
<span data-ttu-id="539ee-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="539ee-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="539ee-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="539ee-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="539ee-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="539ee-128">INPUTS</span></span>

### <span data-ttu-id="539ee-129">Microsoft.Azure.Commands.Batch. Modele. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="539ee-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="539ee-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="539ee-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="539ee-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="539ee-131">OUTPUTS</span></span>

### <span data-ttu-id="539ee-132">System. void</span><span class="sxs-lookup"><span data-stu-id="539ee-132">System.Void</span></span>

## <span data-ttu-id="539ee-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="539ee-133">NOTES</span></span>

## <span data-ttu-id="539ee-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="539ee-134">RELATED LINKS</span></span>

[<span data-ttu-id="539ee-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="539ee-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="539ee-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="539ee-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="539ee-137">Nowe — AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="539ee-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="539ee-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="539ee-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="539ee-139">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="539ee-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
