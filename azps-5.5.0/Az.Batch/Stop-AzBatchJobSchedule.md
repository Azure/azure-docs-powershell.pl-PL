---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: b236f163a6c5c849fcbfcea0a19dac955e15c798
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195219"
---
# <span data-ttu-id="6e1c3-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6e1c3-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="6e1c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e1c3-102">SYNOPSIS</span></span>
<span data-ttu-id="6e1c3-103">Zatrzymuje harmonogram zadań wsadowych.</span><span class="sxs-lookup"><span data-stu-id="6e1c3-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="6e1c3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6e1c3-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e1c3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6e1c3-105">DESCRIPTION</span></span>
<span data-ttu-id="6e1c3-106">Polecenie **cmdlet Stop-AzBatchJobSchedule** zatrzymuje harmonogram zadań partii platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6e1c3-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="6e1c3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6e1c3-107">EXAMPLES</span></span>

### <span data-ttu-id="6e1c3-108">Przykład 1. Zatrzymywanie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="6e1c3-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="6e1c3-109">To polecenie zatrzymuje harmonogram zadań z identyfikatorem Harmonogram zadań17.</span><span class="sxs-lookup"><span data-stu-id="6e1c3-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="6e1c3-110">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="6e1c3-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="6e1c3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e1c3-111">PARAMETERS</span></span>

### <span data-ttu-id="6e1c3-112">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="6e1c3-112">-BatchContext</span></span>
<span data-ttu-id="6e1c3-113">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="6e1c3-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6e1c3-114">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6e1c3-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6e1c3-115">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="6e1c3-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6e1c3-116">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="6e1c3-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6e1c3-117">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6e1c3-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6e1c3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e1c3-118">-DefaultProfile</span></span>
<span data-ttu-id="6e1c3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e1c3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e1c3-120">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="6e1c3-120">-Id</span></span>
<span data-ttu-id="6e1c3-121">Określa identyfikator harmonogramu zadań, który ma być stopowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e1c3-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="6e1c3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e1c3-122">CommonParameters</span></span>
<span data-ttu-id="6e1c3-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e1c3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e1c3-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e1c3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e1c3-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e1c3-125">INPUTS</span></span>

### <span data-ttu-id="6e1c3-126">System.String</span><span class="sxs-lookup"><span data-stu-id="6e1c3-126">System.String</span></span>

### <span data-ttu-id="6e1c3-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6e1c3-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6e1c3-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e1c3-128">OUTPUTS</span></span>

### <span data-ttu-id="6e1c3-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="6e1c3-129">System.Void</span></span>

## <span data-ttu-id="6e1c3-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6e1c3-130">NOTES</span></span>

## <span data-ttu-id="6e1c3-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e1c3-131">RELATED LINKS</span></span>

[<span data-ttu-id="6e1c3-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6e1c3-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="6e1c3-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6e1c3-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="6e1c3-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6e1c3-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6e1c3-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6e1c3-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="6e1c3-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6e1c3-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="6e1c3-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6e1c3-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="6e1c3-138">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="6e1c3-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
