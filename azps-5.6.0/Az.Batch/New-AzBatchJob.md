---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
ms.openlocfilehash: 97b6d2c332b4bc59df165599fe49d38fe496008c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987001"
---
# <span data-ttu-id="6a11d-101">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6a11d-101">New-AzBatchJob</span></span>

## <span data-ttu-id="6a11d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a11d-102">SYNOPSIS</span></span>
<span data-ttu-id="6a11d-103">Tworzy zadanie w usłudze wsadowej.</span><span class="sxs-lookup"><span data-stu-id="6a11d-103">Creates a job in the Batch service.</span></span>

## <span data-ttu-id="6a11d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6a11d-104">SYNTAX</span></span>

```
New-AzBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a11d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6a11d-105">DESCRIPTION</span></span>
<span data-ttu-id="6a11d-106">Polecenie **cmdlet New-AzBatchJob** tworzy zadanie w usłudze Azure Batch na koncie określonym przez *parametr BatchAccountContext.*</span><span class="sxs-lookup"><span data-stu-id="6a11d-106">The **New-AzBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="6a11d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6a11d-107">EXAMPLES</span></span>

### <span data-ttu-id="6a11d-108">Przykład 1. Tworzenie zadania</span><span class="sxs-lookup"><span data-stu-id="6a11d-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $PoolInformation.PoolId = "Pool22"
PS C:\> New-AzBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="6a11d-109">Pierwsze polecenie tworzy obiekt **PSPoolInformation** przy użyciu New-Object cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a11d-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="6a11d-110">Polecenie przechowuje ten obiekt w $PoolInformation zmienną.</span><span class="sxs-lookup"><span data-stu-id="6a11d-110">The command stores that object in the $PoolInformation variable.</span></span>
<span data-ttu-id="6a11d-111">Drugie polecenie przypisuje identyfikator Pool22 właściwości **PoolId** obiektu w $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="6a11d-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>
<span data-ttu-id="6a11d-112">Ostatnie polecenie tworzy zadanie o identyfikatorze ContosoJob35.</span><span class="sxs-lookup"><span data-stu-id="6a11d-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="6a11d-113">Zadania dodane do zadania są uruchamiane w puli o puli identyfikatorów 22.</span><span class="sxs-lookup"><span data-stu-id="6a11d-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="6a11d-114">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="6a11d-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="6a11d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a11d-115">PARAMETERS</span></span>

### <span data-ttu-id="6a11d-116">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="6a11d-116">-BatchContext</span></span>
<span data-ttu-id="6a11d-117">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="6a11d-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6a11d-118">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6a11d-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6a11d-119">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="6a11d-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6a11d-120">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="6a11d-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6a11d-121">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6a11d-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6a11d-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="6a11d-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="6a11d-123">Określa typowe zmienne środowiskowe, jako pary klucz/wartość, ustawiane przez to polecenie cmdlet dla wszystkich zadań w zadaniu.</span><span class="sxs-lookup"><span data-stu-id="6a11d-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="6a11d-124">Kluczem jest nazwa zmiennej środowiskowej.</span><span class="sxs-lookup"><span data-stu-id="6a11d-124">The key is the environment variable name.</span></span>
<span data-ttu-id="6a11d-125">Wartość jest wartością zmiennej środowiskowej.</span><span class="sxs-lookup"><span data-stu-id="6a11d-125">The value is the environment variable value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a11d-126">— Ograniczenia</span><span class="sxs-lookup"><span data-stu-id="6a11d-126">-Constraints</span></span>
<span data-ttu-id="6a11d-127">Określa ograniczenia wykonywania zadania.</span><span class="sxs-lookup"><span data-stu-id="6a11d-127">Specifies the execution constraints for the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a11d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a11d-128">-DefaultProfile</span></span>
<span data-ttu-id="6a11d-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a11d-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a11d-130">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="6a11d-130">-DisplayName</span></span>
<span data-ttu-id="6a11d-131">Określa nazwę wyświetlaną zadania.</span><span class="sxs-lookup"><span data-stu-id="6a11d-131">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="6a11d-132">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="6a11d-132">-Id</span></span>
<span data-ttu-id="6a11d-133">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="6a11d-133">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="6a11d-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="6a11d-134">-JobManagerTask</span></span>
<span data-ttu-id="6a11d-135">Określa zadanie Menedżera zadań.</span><span class="sxs-lookup"><span data-stu-id="6a11d-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="6a11d-136">Usługa wsadowa uruchamia zadanie Menedżera zadań po jego uruchamianiu.</span><span class="sxs-lookup"><span data-stu-id="6a11d-136">The Batch service runs the Job Manager task when the job is started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobManagerTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a11d-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="6a11d-137">-JobPreparationTask</span></span>
<span data-ttu-id="6a11d-138">Określa zadanie przygotowanie zadania.</span><span class="sxs-lookup"><span data-stu-id="6a11d-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="6a11d-139">Usługa wsadowa uruchamia zadanie Przygotowanie zadania w węźle obliczeniowym przed rozpoczęciem jakichkolwiek zadań tego zadania w tym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="6a11d-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a11d-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="6a11d-140">-JobReleaseTask</span></span>
<span data-ttu-id="6a11d-141">Określa zadanie Zwolnij zadanie.</span><span class="sxs-lookup"><span data-stu-id="6a11d-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="6a11d-142">Po zakończeniu zadania usługa wsadowa uruchamia zadanie zwolnienia zadania.</span><span class="sxs-lookup"><span data-stu-id="6a11d-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="6a11d-143">Usługa wsadowa uruchamia zadanie zwalniania zadania w każdym węźle obliczeniowym, w którym uruchomiła dowolne zadanie.</span><span class="sxs-lookup"><span data-stu-id="6a11d-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobReleaseTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a11d-144">— Metadane</span><span class="sxs-lookup"><span data-stu-id="6a11d-144">-Metadata</span></span>
<span data-ttu-id="6a11d-145">Określa metadane (jako pary klucz/wartość), które mają być dodane do zadania.</span><span class="sxs-lookup"><span data-stu-id="6a11d-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="6a11d-146">Kluczem jest nazwa metadanych.</span><span class="sxs-lookup"><span data-stu-id="6a11d-146">The key is the metadata name.</span></span>
<span data-ttu-id="6a11d-147">Wartość jest wartością metadanych.</span><span class="sxs-lookup"><span data-stu-id="6a11d-147">The value is the metadata value.</span></span>

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

### <span data-ttu-id="6a11d-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="6a11d-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="6a11d-149">Określa akcję, która ma zostać wykonane przez usługę wsadową, jeśli wszystkie zadania w zadaniu znajdują się w stanie ukończonym.</span><span class="sxs-lookup"><span data-stu-id="6a11d-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnAllTasksComplete]
Parameter Sets: (All)
Aliases:
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a11d-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="6a11d-150">-OnTaskFailure</span></span>
<span data-ttu-id="6a11d-151">Określa akcję, która podejmuje usługa wsadowa, jeśli jakiekolwiek zadanie w zadaniu kończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="6a11d-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnTaskFailure]
Parameter Sets: (All)
Aliases:
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a11d-152">- PoolInformation</span><span class="sxs-lookup"><span data-stu-id="6a11d-152">-PoolInformation</span></span>
<span data-ttu-id="6a11d-153">Określa szczegóły puli, w której usługa Batch uruchamia zadania zadania.</span><span class="sxs-lookup"><span data-stu-id="6a11d-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a11d-154">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="6a11d-154">-Priority</span></span>
<span data-ttu-id="6a11d-155">Określa priorytet zadania.</span><span class="sxs-lookup"><span data-stu-id="6a11d-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="6a11d-156">Prawidłowe wartości to liczby całkowite z od -1000 do 1000.</span><span class="sxs-lookup"><span data-stu-id="6a11d-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="6a11d-157">Wartość -1000 ma najniższy priorytet.</span><span class="sxs-lookup"><span data-stu-id="6a11d-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="6a11d-158">Najwyższy priorytet ma wartość 1000.</span><span class="sxs-lookup"><span data-stu-id="6a11d-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="6a11d-159">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="6a11d-159">The default value is 0.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a11d-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="6a11d-160">-UsesTaskDependencies</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a11d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a11d-161">CommonParameters</span></span>
<span data-ttu-id="6a11d-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a11d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a11d-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a11d-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a11d-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a11d-164">INPUTS</span></span>

### <span data-ttu-id="6a11d-165">System.String</span><span class="sxs-lookup"><span data-stu-id="6a11d-165">System.String</span></span>

### <span data-ttu-id="6a11d-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6a11d-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6a11d-167">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a11d-167">OUTPUTS</span></span>

### <span data-ttu-id="6a11d-168">System.Void</span><span class="sxs-lookup"><span data-stu-id="6a11d-168">System.Void</span></span>

## <span data-ttu-id="6a11d-169">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6a11d-169">NOTES</span></span>

## <span data-ttu-id="6a11d-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a11d-170">RELATED LINKS</span></span>

[<span data-ttu-id="6a11d-171">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6a11d-171">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="6a11d-172">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6a11d-172">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="6a11d-173">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6a11d-173">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6a11d-174">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6a11d-174">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="6a11d-175">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6a11d-175">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="6a11d-176">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6a11d-176">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="6a11d-177">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6a11d-177">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="6a11d-178">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="6a11d-178">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
