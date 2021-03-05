---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: 54b9f9b60c1d424e6fd62ede85e517b40df1d062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014017"
---
# <span data-ttu-id="a7d0b-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a7d0b-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="a7d0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7d0b-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d0b-103">Wyłącza harmonogram zadań wsadowych.</span><span class="sxs-lookup"><span data-stu-id="a7d0b-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="a7d0b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a7d0b-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7d0b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a7d0b-105">DESCRIPTION</span></span>
<span data-ttu-id="a7d0b-106">Polecenie **cmdlet Disable-AzBatchJobSchedule** wyłącza harmonogram zadań partii platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d0b-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="a7d0b-107">Jeśli wyłączysz harmonogram, zadania nie będą tworzone zgodnie z tym harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="a7d0b-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="a7d0b-108">Wyłączony harmonogram można włączyć później.</span><span class="sxs-lookup"><span data-stu-id="a7d0b-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="a7d0b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a7d0b-109">EXAMPLES</span></span>

### <span data-ttu-id="a7d0b-110">Przykład 1. Wyłączanie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="a7d0b-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="a7d0b-111">To polecenie wyłącza harmonogram zadań z identyfikatorem Harmonogram zadań17.</span><span class="sxs-lookup"><span data-stu-id="a7d0b-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="a7d0b-112">Użyj polecenia **cmdlet Get-AzBatchAccountKey,** aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="a7d0b-112">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a7d0b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7d0b-113">PARAMETERS</span></span>

### <span data-ttu-id="a7d0b-114">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="a7d0b-114">-BatchContext</span></span>
<span data-ttu-id="a7d0b-115">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="a7d0b-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a7d0b-116">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a7d0b-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a7d0b-117">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="a7d0b-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a7d0b-118">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="a7d0b-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a7d0b-119">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a7d0b-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a7d0b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d0b-120">-DefaultProfile</span></span>
<span data-ttu-id="a7d0b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d0b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7d0b-122">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="a7d0b-122">-Id</span></span>
<span data-ttu-id="a7d0b-123">Określa identyfikator harmonogramu zadań, który to polecenie cmdlet wyłącza.</span><span class="sxs-lookup"><span data-stu-id="a7d0b-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="a7d0b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d0b-124">CommonParameters</span></span>
<span data-ttu-id="a7d0b-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7d0b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d0b-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7d0b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d0b-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7d0b-127">INPUTS</span></span>

### <span data-ttu-id="a7d0b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a7d0b-128">System.String</span></span>

### <span data-ttu-id="a7d0b-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a7d0b-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a7d0b-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7d0b-130">OUTPUTS</span></span>

### <span data-ttu-id="a7d0b-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="a7d0b-131">System.Void</span></span>

## <span data-ttu-id="a7d0b-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a7d0b-132">NOTES</span></span>

## <span data-ttu-id="a7d0b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7d0b-133">RELATED LINKS</span></span>

[<span data-ttu-id="a7d0b-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a7d0b-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="a7d0b-135">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a7d0b-135">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a7d0b-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a7d0b-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="a7d0b-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a7d0b-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="a7d0b-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a7d0b-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="a7d0b-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a7d0b-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="a7d0b-140">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a7d0b-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
