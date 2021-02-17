---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: ffaac0bdd4a144cc3979da052c0c40cb824862f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239219"
---
# <span data-ttu-id="4a98f-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4a98f-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="4a98f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a98f-102">SYNOPSIS</span></span>
<span data-ttu-id="4a98f-103">Zatrzymuje zadanie wsadowe.</span><span class="sxs-lookup"><span data-stu-id="4a98f-103">Stops a Batch job.</span></span>

## <span data-ttu-id="4a98f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4a98f-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a98f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4a98f-105">DESCRIPTION</span></span>
<span data-ttu-id="4a98f-106">Polecenie **cmdlet Stop-AzBatchJob** zatrzymuje zadanie partii platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4a98f-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="4a98f-107">To polecenie oznacza zadanie jako ukończone.</span><span class="sxs-lookup"><span data-stu-id="4a98f-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="4a98f-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4a98f-108">EXAMPLES</span></span>

### <span data-ttu-id="4a98f-109">Przykład 1. Zatrzymywanie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="4a98f-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="4a98f-110">To polecenie zatrzymuje zadanie o identyfikatorze Zadanie 000001.</span><span class="sxs-lookup"><span data-stu-id="4a98f-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="4a98f-111">To polecenie określa przyczynę zatrzymania zadania.</span><span class="sxs-lookup"><span data-stu-id="4a98f-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="4a98f-112">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="4a98f-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="4a98f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a98f-113">PARAMETERS</span></span>

### <span data-ttu-id="4a98f-114">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="4a98f-114">-BatchContext</span></span>
<span data-ttu-id="4a98f-115">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="4a98f-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4a98f-116">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4a98f-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4a98f-117">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="4a98f-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4a98f-118">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="4a98f-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4a98f-119">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4a98f-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4a98f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a98f-120">-DefaultProfile</span></span>
<span data-ttu-id="4a98f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a98f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a98f-122">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="4a98f-122">-Id</span></span>
<span data-ttu-id="4a98f-123">Określa identyfikator zadania, które ma być zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a98f-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="4a98f-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="4a98f-124">-TerminateReason</span></span>
<span data-ttu-id="4a98f-125">Określa przyczynę decyzji o zatrzymaniu zadania.</span><span class="sxs-lookup"><span data-stu-id="4a98f-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="4a98f-126">To polecenie cmdlet przechowuje ten tekst jako właściwość **TerminateReason** zadania.</span><span class="sxs-lookup"><span data-stu-id="4a98f-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a98f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a98f-127">CommonParameters</span></span>
<span data-ttu-id="4a98f-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a98f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a98f-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a98f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a98f-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a98f-130">INPUTS</span></span>

### <span data-ttu-id="4a98f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="4a98f-131">System.String</span></span>

### <span data-ttu-id="4a98f-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4a98f-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4a98f-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a98f-133">OUTPUTS</span></span>

### <span data-ttu-id="4a98f-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="4a98f-134">System.Void</span></span>

## <span data-ttu-id="4a98f-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4a98f-135">NOTES</span></span>

## <span data-ttu-id="4a98f-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a98f-136">RELATED LINKS</span></span>

[<span data-ttu-id="4a98f-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4a98f-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="4a98f-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4a98f-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="4a98f-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4a98f-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4a98f-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4a98f-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="4a98f-141">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4a98f-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="4a98f-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="4a98f-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="4a98f-143">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="4a98f-143">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
