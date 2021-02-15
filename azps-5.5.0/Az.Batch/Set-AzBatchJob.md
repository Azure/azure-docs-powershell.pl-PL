---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 1104eed4d60405226cdc6dad351ae418b84142e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244235"
---
# <span data-ttu-id="0e280-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="0e280-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="0e280-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e280-102">SYNOPSIS</span></span>
<span data-ttu-id="0e280-103">Aktualizuje zadanie wsadowe.</span><span class="sxs-lookup"><span data-stu-id="0e280-103">Updates a Batch job.</span></span>

## <span data-ttu-id="0e280-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0e280-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e280-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0e280-105">DESCRIPTION</span></span>
<span data-ttu-id="0e280-106">Polecenie **cmdlet Set-AzBatchJob** aktualizuje zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="0e280-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="0e280-107">Użyj Get-AzBatchJob cmdlet, aby uzyskać **obiekt PSCloudJob.**</span><span class="sxs-lookup"><span data-stu-id="0e280-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="0e280-108">Zmodyfikuj właściwości tego obiektu, a następnie użyj bieżącego polecenia cmdlet w celu zatwierdzenia zmian w usłudze wsadowej.</span><span class="sxs-lookup"><span data-stu-id="0e280-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="0e280-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0e280-109">EXAMPLES</span></span>

### <span data-ttu-id="0e280-110">Przykład 1. Aktualizowanie zadania</span><span class="sxs-lookup"><span data-stu-id="0e280-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="0e280-111">Pierwsze polecenie uzyskuje zadanie za pomocą polecenia **Get-AzBatchJob,** a następnie przechowuje je w $Job zmienną.</span><span class="sxs-lookup"><span data-stu-id="0e280-111">The first command gets a job by using **Get-AzBatchJob**, and then stores it in the $Job variable.</span></span>
<span data-ttu-id="0e280-112">Drugie polecenie modyfikuje specyfikację priorytetu dla $Job obiektu.</span><span class="sxs-lookup"><span data-stu-id="0e280-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="0e280-113">Ostatnie polecenie aktualizuje usługę Batch, aby dopasować obiekt lokalny w $Job.</span><span class="sxs-lookup"><span data-stu-id="0e280-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="0e280-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e280-114">PARAMETERS</span></span>

### <span data-ttu-id="0e280-115">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="0e280-115">-BatchContext</span></span>
<span data-ttu-id="0e280-116">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="0e280-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0e280-117">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0e280-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0e280-118">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="0e280-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0e280-119">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="0e280-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0e280-120">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0e280-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0e280-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e280-121">-DefaultProfile</span></span>
<span data-ttu-id="0e280-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e280-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e280-123">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="0e280-123">-Job</span></span>
<span data-ttu-id="0e280-124">Określa polecenie **PSCloudJob,** którego to polecenie cmdlet aktualizuje usługę Batch.</span><span class="sxs-lookup"><span data-stu-id="0e280-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e280-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e280-125">CommonParameters</span></span>
<span data-ttu-id="0e280-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e280-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e280-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e280-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e280-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e280-128">INPUTS</span></span>

### <span data-ttu-id="0e280-129">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="0e280-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="0e280-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0e280-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0e280-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e280-131">OUTPUTS</span></span>

### <span data-ttu-id="0e280-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="0e280-132">System.Void</span></span>

## <span data-ttu-id="0e280-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0e280-133">NOTES</span></span>

## <span data-ttu-id="0e280-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e280-134">RELATED LINKS</span></span>

[<span data-ttu-id="0e280-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="0e280-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="0e280-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="0e280-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="0e280-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="0e280-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="0e280-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0e280-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="0e280-139">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="0e280-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="0e280-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="0e280-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="0e280-141">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="0e280-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="0e280-142">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0e280-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
