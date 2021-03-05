---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: 80fc0c530904717561aa34ca98844fede75e747e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992951"
---
# <span data-ttu-id="54cf4-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="54cf4-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="54cf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="54cf4-103">Aktualizuje właściwości zadania.</span><span class="sxs-lookup"><span data-stu-id="54cf4-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="54cf4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="54cf4-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54cf4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="54cf4-105">DESCRIPTION</span></span>
<span data-ttu-id="54cf4-106">Polecenie **cmdlet Set-AzBatchTask** aktualizuje właściwości zadania w usłudze wsadowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="54cf4-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="54cf4-107">Użyj Get-AzBatchTask cmdlet, aby uzyskać **obiekt PSCloudTask.**</span><span class="sxs-lookup"><span data-stu-id="54cf4-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="54cf4-108">Zmodyfikuj właściwości tego obiektu, a następnie użyj bieżącego polecenia cmdlet w celu zatwierdzenia zmian w usłudze wsadowej.</span><span class="sxs-lookup"><span data-stu-id="54cf4-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="54cf4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="54cf4-109">EXAMPLES</span></span>

### <span data-ttu-id="54cf4-110">Przykład 1. Aktualizowanie zadania</span><span class="sxs-lookup"><span data-stu-id="54cf4-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="54cf4-111">Pierwsze polecenie pobiera zadanie za pomocą polecenia **Get-AzBatchTask,** a następnie przechowuje je w $Task zmienną.</span><span class="sxs-lookup"><span data-stu-id="54cf4-111">The first command gets a task by using **Get-AzBatchTask**, and then stores it in the $Task variable.</span></span>
<span data-ttu-id="54cf4-112">Kolejne dwa polecenia modyfikują ograniczenia zadania w $Task.</span><span class="sxs-lookup"><span data-stu-id="54cf4-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="54cf4-113">Ostatnie polecenie aktualizuje usługę wsadową, aby dopasować obiekt lokalny w $Task.</span><span class="sxs-lookup"><span data-stu-id="54cf4-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="54cf4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54cf4-114">PARAMETERS</span></span>

### <span data-ttu-id="54cf4-115">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="54cf4-115">-BatchContext</span></span>
<span data-ttu-id="54cf4-116">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="54cf4-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="54cf4-117">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="54cf4-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="54cf4-118">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="54cf4-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="54cf4-119">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="54cf4-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="54cf4-120">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="54cf4-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="54cf4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54cf4-121">-DefaultProfile</span></span>
<span data-ttu-id="54cf4-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="54cf4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54cf4-123">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="54cf4-123">-Task</span></span>
<span data-ttu-id="54cf4-124">Określa **usługę PSCloudTask,** dla której to polecenie cmdlet aktualizuje usługę batch.</span><span class="sxs-lookup"><span data-stu-id="54cf4-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54cf4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54cf4-125">CommonParameters</span></span>
<span data-ttu-id="54cf4-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54cf4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54cf4-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54cf4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54cf4-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54cf4-128">INPUTS</span></span>

### <span data-ttu-id="54cf4-129">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="54cf4-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="54cf4-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="54cf4-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="54cf4-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54cf4-131">OUTPUTS</span></span>

### <span data-ttu-id="54cf4-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="54cf4-132">System.Void</span></span>

## <span data-ttu-id="54cf4-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="54cf4-133">NOTES</span></span>

## <span data-ttu-id="54cf4-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54cf4-134">RELATED LINKS</span></span>

[<span data-ttu-id="54cf4-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="54cf4-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="54cf4-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="54cf4-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="54cf4-137">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="54cf4-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="54cf4-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="54cf4-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="54cf4-139">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="54cf4-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="54cf4-140">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="54cf4-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
