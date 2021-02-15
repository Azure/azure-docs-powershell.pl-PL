---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 423f249a7971883cbe47d8f499fdd780980362f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197010"
---
# <span data-ttu-id="24636-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="24636-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="24636-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24636-102">SYNOPSIS</span></span>
<span data-ttu-id="24636-103">Aktualizuje właściwości puli.</span><span class="sxs-lookup"><span data-stu-id="24636-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="24636-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="24636-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24636-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="24636-105">DESCRIPTION</span></span>
<span data-ttu-id="24636-106">Polecenie **cmdlet Set-AzBatchPool** aktualizuje właściwości puli w usłudze Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="24636-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="24636-107">Użyj Get-AzBatchPool cmdlet, aby uzyskać **obiekt PSCloudPool.**</span><span class="sxs-lookup"><span data-stu-id="24636-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="24636-108">Zmodyfikuj właściwości tego obiektu, a następnie użyj bieżącego polecenia cmdlet w celu zatwierdzenia zmian w usłudze wsadowej.</span><span class="sxs-lookup"><span data-stu-id="24636-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="24636-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="24636-109">EXAMPLES</span></span>

### <span data-ttu-id="24636-110">Przykład 1. Aktualizowanie puli</span><span class="sxs-lookup"><span data-stu-id="24636-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="24636-111">Pierwsze polecenie uzyskuje pulę przy użyciu **get-AzBatchPool,** a następnie przechowuje ją w $Pool zmienną.</span><span class="sxs-lookup"><span data-stu-id="24636-111">The first command gets a pool by using **Get-AzBatchPool**, and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="24636-112">Następne trzy polecenia modyfikują specyfikację zadania rozpoczęcia na $Pool obiekt.</span><span class="sxs-lookup"><span data-stu-id="24636-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="24636-113">Ostatnie polecenie aktualizuje usługę wsadową, aby dopasować obiekt lokalny w $Pool.</span><span class="sxs-lookup"><span data-stu-id="24636-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="24636-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24636-114">PARAMETERS</span></span>

### <span data-ttu-id="24636-115">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="24636-115">-BatchContext</span></span>
<span data-ttu-id="24636-116">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="24636-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="24636-117">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="24636-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="24636-118">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="24636-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="24636-119">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="24636-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="24636-120">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="24636-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="24636-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24636-121">-DefaultProfile</span></span>
<span data-ttu-id="24636-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="24636-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24636-123">— Pula</span><span class="sxs-lookup"><span data-stu-id="24636-123">-Pool</span></span>
<span data-ttu-id="24636-124">Określa **usługę PSCloudPool,** do której to polecenie cmdlet aktualizuje usługę Batch.</span><span class="sxs-lookup"><span data-stu-id="24636-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="24636-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24636-125">CommonParameters</span></span>
<span data-ttu-id="24636-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24636-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24636-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24636-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24636-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24636-128">INPUTS</span></span>

### <span data-ttu-id="24636-129">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="24636-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="24636-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="24636-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="24636-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24636-131">OUTPUTS</span></span>

### <span data-ttu-id="24636-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="24636-132">System.Void</span></span>

## <span data-ttu-id="24636-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="24636-133">NOTES</span></span>

## <span data-ttu-id="24636-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24636-134">RELATED LINKS</span></span>

[<span data-ttu-id="24636-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="24636-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="24636-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="24636-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="24636-137">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="24636-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="24636-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="24636-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="24636-139">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="24636-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
