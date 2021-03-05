---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
ms.openlocfilehash: 0d33ce7e41fb8058acb36a4668eeb337d54f187e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972977"
---
# <span data-ttu-id="bf0dd-101">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bf0dd-101">Get-AzBatchJobSchedule</span></span>

## <span data-ttu-id="bf0dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf0dd-102">SYNOPSIS</span></span>
<span data-ttu-id="bf0dd-103">Pobiera harmonogramy zadań wsadowych.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-103">Gets Batch job schedules.</span></span>

## <span data-ttu-id="bf0dd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bf0dd-104">SYNTAX</span></span>

### <span data-ttu-id="bf0dd-105">FiltrDanych OData (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bf0dd-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf0dd-106">Identyfikator</span><span class="sxs-lookup"><span data-stu-id="bf0dd-106">Id</span></span>
```
Get-AzBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf0dd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bf0dd-107">DESCRIPTION</span></span>
<span data-ttu-id="bf0dd-108">Polecenie **cmdlet Get-AzBatchJobSchedule** pobiera harmonogramy zadań partii platformy Azure dla konta batch określonego przez *parametr BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="bf0dd-108">The **Get-AzBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="bf0dd-109">Określ identyfikator, aby uzyskać pojedynczy harmonogram zadań.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="bf0dd-110">Określ parametr *filtru,* aby uzyskać harmonogramy zadań zgodne z filtrem protokołu Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="bf0dd-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="bf0dd-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bf0dd-111">EXAMPLES</span></span>

### <span data-ttu-id="bf0dd-112">Przykład 1. Uzyskiwanie harmonogramu zadań przez podanie identyfikatora</span><span class="sxs-lookup"><span data-stu-id="bf0dd-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 :
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    :
PreviousState               : Invalid
PreviousStateTransitionTime :
Schedule                    :
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23
```

<span data-ttu-id="bf0dd-113">To polecenie pobiera harmonogram zadań z identyfikatorem Harmonogram zadań23.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="bf0dd-114">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="bf0dd-115">Przykład 2. Uzyskiwanie harmonogramów zadań przy użyciu filtru</span><span class="sxs-lookup"><span data-stu-id="bf0dd-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 :
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    :
PreviousState               : Invalid
PreviousStateTransitionTime :
Schedule                    :
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23

CreationTime                : 7/26/2015 5:39:33 PM
DisplayName                 :
ETag                        : 0x8D295E12B1084B4
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule26
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/26/2015 5:39:33 PM
Metadata                    :
PreviousState               : Invalid
PreviousStateTransitionTime :
Schedule                    :
State                       : Active
StateTransitionTime         : 7/26/2015 5:39:33 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule26
```

<span data-ttu-id="bf0dd-116">To polecenie pobiera wszystkie harmonogramy zadań, które mają identyfikatory, których nazwy zaczynają się od zadania, przez określenie *parametru* Filtruj.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="bf0dd-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf0dd-117">PARAMETERS</span></span>

### <span data-ttu-id="bf0dd-118">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="bf0dd-118">-BatchContext</span></span>
<span data-ttu-id="bf0dd-119">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bf0dd-120">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bf0dd-121">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bf0dd-122">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bf0dd-123">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bf0dd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf0dd-124">-DefaultProfile</span></span>
<span data-ttu-id="bf0dd-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf0dd-126">— Rozwiń</span><span class="sxs-lookup"><span data-stu-id="bf0dd-126">-Expand</span></span>
<span data-ttu-id="bf0dd-127">Określa klauzulę rozwijania protokołu Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="bf0dd-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="bf0dd-128">Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównej o otrzymuję.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="bf0dd-129">— Filtr</span><span class="sxs-lookup"><span data-stu-id="bf0dd-129">-Filter</span></span>
<span data-ttu-id="bf0dd-130">Określa klauzulę filtru OData.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="bf0dd-131">To polecenie cmdlet zwraca harmonogramy zadań zgodne z filtrem, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="bf0dd-132">Jeśli filtr nie zostanie określony, to polecenie cmdlet zwróci wszystkie harmonogramy zadań dla kontekstu partii.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0dd-133">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="bf0dd-133">-Id</span></span>
<span data-ttu-id="bf0dd-134">Określa identyfikator harmonogramu zadań, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="bf0dd-135">Nie można określić symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-135">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf0dd-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bf0dd-136">-MaxCount</span></span>
<span data-ttu-id="bf0dd-137">Określa maksymalną liczbę harmonogramów zadań do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="bf0dd-138">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie użyje górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="bf0dd-139">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-139">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0dd-140">— Wybierz</span><span class="sxs-lookup"><span data-stu-id="bf0dd-140">-Select</span></span>
<span data-ttu-id="bf0dd-141">Określa klauzulę wybierania danych OData.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="bf0dd-142">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="bf0dd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf0dd-143">CommonParameters</span></span>
<span data-ttu-id="bf0dd-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf0dd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf0dd-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf0dd-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf0dd-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf0dd-146">INPUTS</span></span>

### <span data-ttu-id="bf0dd-147">System.String</span><span class="sxs-lookup"><span data-stu-id="bf0dd-147">System.String</span></span>

### <span data-ttu-id="bf0dd-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bf0dd-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bf0dd-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf0dd-149">OUTPUTS</span></span>

### <span data-ttu-id="bf0dd-150">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bf0dd-150">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="bf0dd-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bf0dd-151">NOTES</span></span>

## <span data-ttu-id="bf0dd-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf0dd-152">RELATED LINKS</span></span>

[<span data-ttu-id="bf0dd-153">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bf0dd-153">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="bf0dd-154">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bf0dd-154">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="bf0dd-155">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="bf0dd-155">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="bf0dd-156">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bf0dd-156">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="bf0dd-157">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bf0dd-157">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="bf0dd-158">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bf0dd-158">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="bf0dd-159">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bf0dd-159">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
