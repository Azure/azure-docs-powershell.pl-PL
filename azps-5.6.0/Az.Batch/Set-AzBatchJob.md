---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: cc084f276f379013125693e3314ff1eab8a7b123
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965185"
---
# <span data-ttu-id="4b47b-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4b47b-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="4b47b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b47b-102">SYNOPSIS</span></span>
<span data-ttu-id="4b47b-103">Aktualizuje zadanie wsadowe.</span><span class="sxs-lookup"><span data-stu-id="4b47b-103">Updates a Batch job.</span></span>

## <span data-ttu-id="4b47b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4b47b-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b47b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4b47b-105">DESCRIPTION</span></span>
<span data-ttu-id="4b47b-106">Polecenie **cmdlet Set-AzBatchJob** aktualizuje zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="4b47b-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="4b47b-107">Użyj Get-AzBatchJob cmdlet, aby uzyskać **obiekt PSCloudJob.**</span><span class="sxs-lookup"><span data-stu-id="4b47b-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="4b47b-108">Zmodyfikuj właściwości tego obiektu, a następnie użyj bieżącego polecenia cmdlet w celu zatwierdzenia zmian w usłudze wsadowej.</span><span class="sxs-lookup"><span data-stu-id="4b47b-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="4b47b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4b47b-109">EXAMPLES</span></span>

### <span data-ttu-id="4b47b-110">Przykład 1. Aktualizowanie zadania</span><span class="sxs-lookup"><span data-stu-id="4b47b-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="4b47b-111">Pierwsze polecenie otrzymuje zadanie za pomocą polecenia **Get-AzBatchJob,** a następnie zapisuje je w $Job zmienną.</span><span class="sxs-lookup"><span data-stu-id="4b47b-111">The first command gets a job by using **Get-AzBatchJob**, and then stores it in the $Job variable.</span></span>
<span data-ttu-id="4b47b-112">Drugie polecenie modyfikuje specyfikację priorytetu dla $Job obiektu.</span><span class="sxs-lookup"><span data-stu-id="4b47b-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="4b47b-113">Ostatnie polecenie aktualizuje usługę wsadową, aby dopasować obiekt lokalny w $Job.</span><span class="sxs-lookup"><span data-stu-id="4b47b-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="4b47b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b47b-114">PARAMETERS</span></span>

### <span data-ttu-id="4b47b-115">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="4b47b-115">-BatchContext</span></span>
<span data-ttu-id="4b47b-116">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="4b47b-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4b47b-117">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4b47b-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4b47b-118">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="4b47b-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4b47b-119">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="4b47b-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4b47b-120">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4b47b-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4b47b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b47b-121">-DefaultProfile</span></span>
<span data-ttu-id="4b47b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4b47b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b47b-123">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="4b47b-123">-Job</span></span>
<span data-ttu-id="4b47b-124">Określa polecenie **PSCloudJob,** którego to polecenie cmdlet aktualizuje usługę Batch.</span><span class="sxs-lookup"><span data-stu-id="4b47b-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="4b47b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b47b-125">CommonParameters</span></span>
<span data-ttu-id="4b47b-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b47b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b47b-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b47b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b47b-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b47b-128">INPUTS</span></span>

### <span data-ttu-id="4b47b-129">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="4b47b-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="4b47b-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4b47b-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4b47b-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b47b-131">OUTPUTS</span></span>

### <span data-ttu-id="4b47b-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="4b47b-132">System.Void</span></span>

## <span data-ttu-id="4b47b-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4b47b-133">NOTES</span></span>

## <span data-ttu-id="4b47b-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b47b-134">RELATED LINKS</span></span>

[<span data-ttu-id="4b47b-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4b47b-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="4b47b-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4b47b-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="4b47b-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4b47b-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="4b47b-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4b47b-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4b47b-139">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4b47b-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="4b47b-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4b47b-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="4b47b-141">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4b47b-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="4b47b-142">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="4b47b-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
