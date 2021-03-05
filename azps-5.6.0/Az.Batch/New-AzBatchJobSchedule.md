---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
ms.openlocfilehash: 63a8ba2d98bd81cbeca3286259920debc10723a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986987"
---
# <span data-ttu-id="0115e-101">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0115e-101">New-AzBatchJobSchedule</span></span>

## <span data-ttu-id="0115e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0115e-102">SYNOPSIS</span></span>
<span data-ttu-id="0115e-103">Tworzy harmonogram zadań w usłudze wsadowej.</span><span class="sxs-lookup"><span data-stu-id="0115e-103">Creates a job schedule in the Batch service.</span></span>

## <span data-ttu-id="0115e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0115e-104">SYNTAX</span></span>

```
New-AzBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0115e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0115e-105">DESCRIPTION</span></span>
<span data-ttu-id="0115e-106">Polecenie **cmdlet New-AzBatchJobSchedule** tworzy harmonogram zadań w usłudze wsadowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0115e-106">The **New-AzBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="0115e-107">Parametr *BatchAccountContext* określa konto, na którym to polecenie cmdlet tworzy harmonogram.</span><span class="sxs-lookup"><span data-stu-id="0115e-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="0115e-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0115e-108">EXAMPLES</span></span>

### <span data-ttu-id="0115e-109">Przykład 1. Tworzenie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="0115e-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="0115e-110">W tym przykładzie jest tworzenie harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="0115e-110">This example creates a job schedule.</span></span>
<span data-ttu-id="0115e-111">Pierwsze pięć poleceń tworzy i modyfikuje obiekty **PSSchedule,** **PSJobSpecification** i **PSPoolInformation.**</span><span class="sxs-lookup"><span data-stu-id="0115e-111">The first five commands create and modify **PSSchedule**, **PSJobSpecification**, and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="0115e-112">W poleceniach jest używany New-Object cmdlet i standardowa składnia programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0115e-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="0115e-113">Polecenia przechowują te obiekty w $Schedule i $JobSpecification zmiennych.</span><span class="sxs-lookup"><span data-stu-id="0115e-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>
<span data-ttu-id="0115e-114">Ostatnie polecenie tworzy harmonogram zadań z identyfikatorem Harmonogram zadań17.</span><span class="sxs-lookup"><span data-stu-id="0115e-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="0115e-115">Ten harmonogram tworzy zadania z interwałem cyklu jednego dnia.</span><span class="sxs-lookup"><span data-stu-id="0115e-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="0115e-116">Zadania są uruchamiane w puli o identyfikatorze ContosoPool06 określonym w piątym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="0115e-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="0115e-117">Użyj polecenia **cmdlet Get-AzBatchAccountKey,** aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="0115e-117">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="0115e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0115e-118">PARAMETERS</span></span>

### <span data-ttu-id="0115e-119">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="0115e-119">-BatchContext</span></span>
<span data-ttu-id="0115e-120">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="0115e-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0115e-121">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0115e-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0115e-122">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="0115e-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0115e-123">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="0115e-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0115e-124">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0115e-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0115e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0115e-125">-DefaultProfile</span></span>
<span data-ttu-id="0115e-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0115e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0115e-127">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="0115e-127">-DisplayName</span></span>
<span data-ttu-id="0115e-128">Określa nazwę wyświetlaną harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="0115e-128">Specifies a display name for the job schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0115e-129">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="0115e-129">-Id</span></span>
<span data-ttu-id="0115e-130">Określa identyfikator harmonogramu zadania, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0115e-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0115e-131">— określone zadanie</span><span class="sxs-lookup"><span data-stu-id="0115e-131">-JobSpecification</span></span>
<span data-ttu-id="0115e-132">Określa szczegóły zadań, które to polecenie cmdlet uwzględnia w harmonogramie zadań.</span><span class="sxs-lookup"><span data-stu-id="0115e-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0115e-133">— Metadane</span><span class="sxs-lookup"><span data-stu-id="0115e-133">-Metadata</span></span>
<span data-ttu-id="0115e-134">Określa metadane (jako pary klucz/wartość), które mają być dodane do harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="0115e-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="0115e-135">Kluczem jest nazwa metadanych.</span><span class="sxs-lookup"><span data-stu-id="0115e-135">The key is the metadata name.</span></span>
<span data-ttu-id="0115e-136">Wartość jest wartością metadanych.</span><span class="sxs-lookup"><span data-stu-id="0115e-136">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0115e-137">— Planowanie</span><span class="sxs-lookup"><span data-stu-id="0115e-137">-Schedule</span></span>
<span data-ttu-id="0115e-138">Określa harmonogram określający czas tworzenia zadań.</span><span class="sxs-lookup"><span data-stu-id="0115e-138">Specifies the schedule that determines when to create jobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0115e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0115e-139">CommonParameters</span></span>
<span data-ttu-id="0115e-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0115e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0115e-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0115e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0115e-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0115e-142">INPUTS</span></span>

### <span data-ttu-id="0115e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="0115e-143">System.String</span></span>

### <span data-ttu-id="0115e-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0115e-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0115e-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0115e-145">OUTPUTS</span></span>

### <span data-ttu-id="0115e-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="0115e-146">System.Void</span></span>

## <span data-ttu-id="0115e-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0115e-147">NOTES</span></span>

## <span data-ttu-id="0115e-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0115e-148">RELATED LINKS</span></span>

[<span data-ttu-id="0115e-149">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0115e-149">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="0115e-150">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0115e-150">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="0115e-151">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0115e-151">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="0115e-152">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0115e-152">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="0115e-153">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0115e-153">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="0115e-154">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0115e-154">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="0115e-155">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0115e-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
