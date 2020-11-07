---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
ms.openlocfilehash: bf96b5930895332de2e78ffdee71f9f6a2654b83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554162"
---
# <span data-ttu-id="04eb6-101">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="04eb6-101">New-AzureBatchJob</span></span>

## <span data-ttu-id="04eb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="04eb6-103">Tworzy zadanie w usłudze przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="04eb6-103">Creates a job in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04eb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04eb6-104">SYNTAX</span></span>

```
New-AzureBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04eb6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="04eb6-105">DESCRIPTION</span></span>
<span data-ttu-id="04eb6-106">Polecenie cmdlet **New-AzureBatchJob** tworzy zadanie w usłudze Azure Batch na koncie określonym przez parametr *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="04eb6-106">The **New-AzureBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="04eb6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04eb6-107">EXAMPLES</span></span>

### <span data-ttu-id="04eb6-108">Przykład 1. Tworzenie zadania</span><span class="sxs-lookup"><span data-stu-id="04eb6-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzureBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="04eb6-109">Pierwsze polecenie tworzy obiekt **PSPoolInformation** przy użyciu polecenia cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="04eb6-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="04eb6-110">Polecenie zapisuje ten obiekt w zmiennej $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="04eb6-110">The command stores that object in the $PoolInformation variable.</span></span>

<span data-ttu-id="04eb6-111">Drugie polecenie przypisuje identyfikator Pool22 do właściwości **PoolId** obiektu w $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="04eb6-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>

<span data-ttu-id="04eb6-112">Ostatnie polecenie tworzy zadanie o IDENTYFIKATORze ContosoJob35.</span><span class="sxs-lookup"><span data-stu-id="04eb6-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="04eb6-113">Zadania dodane do zadania uruchomionego w puli o IDENTYFIKATORze Pool22.</span><span class="sxs-lookup"><span data-stu-id="04eb6-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="04eb6-114">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="04eb6-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="04eb6-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04eb6-115">PARAMETERS</span></span>

### <span data-ttu-id="04eb6-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="04eb6-116">-BatchContext</span></span>
<span data-ttu-id="04eb6-117">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="04eb6-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="04eb6-118">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="04eb6-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="04eb6-119">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="04eb6-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="04eb6-120">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="04eb6-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="04eb6-121">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="04eb6-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04eb6-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="04eb6-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="04eb6-123">Określa typowe zmienne środowiskowe jako pary klucz/wartość, które to polecenie cmdlet ustawia dla wszystkich zadań w zadaniu.</span><span class="sxs-lookup"><span data-stu-id="04eb6-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="04eb6-124">Klucz jest nazwą zmiennej środowiskowej.</span><span class="sxs-lookup"><span data-stu-id="04eb6-124">The key is the environment variable name.</span></span>
<span data-ttu-id="04eb6-125">Wartość jest wartością zmiennej środowiskowej.</span><span class="sxs-lookup"><span data-stu-id="04eb6-125">The value is the environment variable value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eb6-126">-Ograniczenia</span><span class="sxs-lookup"><span data-stu-id="04eb6-126">-Constraints</span></span>
<span data-ttu-id="04eb6-127">Określa ograniczenia wykonania zadania.</span><span class="sxs-lookup"><span data-stu-id="04eb6-127">Specifies the execution constraints for the job.</span></span>

```yaml
Type: PSJobConstraints
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eb6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04eb6-128">-DefaultProfile</span></span>
<span data-ttu-id="04eb6-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="04eb6-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eb6-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="04eb6-130">-DisplayName</span></span>
<span data-ttu-id="04eb6-131">Określa nazwę wyświetlaną zadania.</span><span class="sxs-lookup"><span data-stu-id="04eb6-131">Specifies the display name for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eb6-132">-ID</span><span class="sxs-lookup"><span data-stu-id="04eb6-132">-Id</span></span>
<span data-ttu-id="04eb6-133">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="04eb6-133">Specifies an ID for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04eb6-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="04eb6-134">-JobManagerTask</span></span>
<span data-ttu-id="04eb6-135">Umożliwia określenie zadania w Menedżerze zadań.</span><span class="sxs-lookup"><span data-stu-id="04eb6-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="04eb6-136">Usługa przetwarzania wsadowego uruchamia zadanie Menedżera zadań po uruchomieniu zadania.</span><span class="sxs-lookup"><span data-stu-id="04eb6-136">The Batch service runs the Job Manager task when the job is started.</span></span>

```yaml
Type: PSJobManagerTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eb6-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="04eb6-137">-JobPreparationTask</span></span>
<span data-ttu-id="04eb6-138">Określa zadanie przygotowywania zadań.</span><span class="sxs-lookup"><span data-stu-id="04eb6-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="04eb6-139">Usługa przetwarzania wsadowego uruchamia zadanie przygotowywania zadań w węźle obliczeniowym przed rozpoczęciem wykonywania zadań tego zadania w tym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="04eb6-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

```yaml
Type: PSJobPreparationTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eb6-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="04eb6-140">-JobReleaseTask</span></span>
<span data-ttu-id="04eb6-141">Określa zadanie wydania zlecenia.</span><span class="sxs-lookup"><span data-stu-id="04eb6-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="04eb6-142">Po zakończeniu zadania usługa przetwarzania wsadowego wykonuje zadanie wydania zadania.</span><span class="sxs-lookup"><span data-stu-id="04eb6-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="04eb6-143">Usługa przetwarzania wsadowego wykonuje zadanie wydania zadania w każdym węźle obliczeniowym, na którym zostało uruchomione jakieś zadanie.</span><span class="sxs-lookup"><span data-stu-id="04eb6-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

```yaml
Type: PSJobReleaseTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eb6-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="04eb6-144">-Metadata</span></span>
<span data-ttu-id="04eb6-145">Określa metadane, jako pary klucz/wartość, aby dodać je do zadania.</span><span class="sxs-lookup"><span data-stu-id="04eb6-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="04eb6-146">Klucz to nazwa metadanych.</span><span class="sxs-lookup"><span data-stu-id="04eb6-146">The key is the metadata name.</span></span>
<span data-ttu-id="04eb6-147">Wartość jest wartością metadanych.</span><span class="sxs-lookup"><span data-stu-id="04eb6-147">The value is the metadata value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eb6-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="04eb6-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="04eb6-149">Określa akcję, jaką usługa wsadowa przyjmuje, jeśli wszystkie zadania w tym zadaniu są w stanie ukończenia.</span><span class="sxs-lookup"><span data-stu-id="04eb6-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

```yaml
Type: OnAllTasksComplete
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eb6-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="04eb6-150">-OnTaskFailure</span></span>
<span data-ttu-id="04eb6-151">Określa akcję, jaką usługa wsadowa przyjmuje, jeśli jakieś zadanie w zadaniu nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="04eb6-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

```yaml
Type: OnTaskFailure
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eb6-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="04eb6-152">-PoolInformation</span></span>
<span data-ttu-id="04eb6-153">Określa szczegóły puli, w której usługa przetwarzania wsadowego uruchamia zadania zadania.</span><span class="sxs-lookup"><span data-stu-id="04eb6-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

```yaml
Type: PSPoolInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eb6-154">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="04eb6-154">-Priority</span></span>
<span data-ttu-id="04eb6-155">Określa priorytet zadania.</span><span class="sxs-lookup"><span data-stu-id="04eb6-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="04eb6-156">Prawidłowe wartości to: liczba całkowita z zakresu od-1000 do 1000.</span><span class="sxs-lookup"><span data-stu-id="04eb6-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="04eb6-157">Wartość-1000 jest najniższym priorytetem.</span><span class="sxs-lookup"><span data-stu-id="04eb6-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="04eb6-158">Wartość 1000 jest najwyższym priorytetem.</span><span class="sxs-lookup"><span data-stu-id="04eb6-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="04eb6-159">Wartość domyślna to 0.</span><span class="sxs-lookup"><span data-stu-id="04eb6-159">The default value is 0.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eb6-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="04eb6-160">-UsesTaskDependencies</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eb6-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04eb6-161">CommonParameters</span></span>
<span data-ttu-id="04eb6-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04eb6-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04eb6-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04eb6-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04eb6-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04eb6-164">INPUTS</span></span>

### <span data-ttu-id="04eb6-165">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="04eb6-165">BatchAccountContext</span></span>
<span data-ttu-id="04eb6-166">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="04eb6-166">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="04eb6-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04eb6-167">OUTPUTS</span></span>

## <span data-ttu-id="04eb6-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04eb6-168">NOTES</span></span>

## <span data-ttu-id="04eb6-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04eb6-169">RELATED LINKS</span></span>

[<span data-ttu-id="04eb6-170">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="04eb6-170">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="04eb6-171">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="04eb6-171">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="04eb6-172">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="04eb6-172">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="04eb6-173">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="04eb6-173">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="04eb6-174">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="04eb6-174">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="04eb6-175">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="04eb6-175">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="04eb6-176">Zatrzymaj — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="04eb6-176">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="04eb6-177">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="04eb6-177">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

