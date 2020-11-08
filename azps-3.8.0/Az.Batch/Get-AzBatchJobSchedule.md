---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
ms.openlocfilehash: a90f437bc593e1abcb6dc2d92292e04dd9c9f74b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "94061774"
---
# <span data-ttu-id="23505-101">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="23505-101">Get-AzBatchJobSchedule</span></span>

## <span data-ttu-id="23505-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23505-102">SYNOPSIS</span></span>
<span data-ttu-id="23505-103">Pobiera harmonogramy zadań wsadowych.</span><span class="sxs-lookup"><span data-stu-id="23505-103">Gets Batch job schedules.</span></span>

## <span data-ttu-id="23505-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23505-104">SYNTAX</span></span>

### <span data-ttu-id="23505-105">ODataFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="23505-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23505-106">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="23505-106">Id</span></span>
```
Get-AzBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23505-107">Opis</span><span class="sxs-lookup"><span data-stu-id="23505-107">DESCRIPTION</span></span>
<span data-ttu-id="23505-108">Polecenie cmdlet **Get-AzBatchJobSchedule** pobiera harmonogramy zadań wsadowych platformy Azure dla konta wsadowego określonego przez parametr *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="23505-108">The **Get-AzBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="23505-109">Określ identyfikator, aby uzyskać jeden harmonogram zadania.</span><span class="sxs-lookup"><span data-stu-id="23505-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="23505-110">Określ parametr *Filter* , aby pobrać harmonogramy zadań zgodne z filtrem Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="23505-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="23505-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23505-111">EXAMPLES</span></span>

### <span data-ttu-id="23505-112">Przykład 1: uzyskiwanie harmonogramu zadań przez określenie identyfikatora</span><span class="sxs-lookup"><span data-stu-id="23505-112">Example 1: Get a job schedule by specifying an ID</span></span>
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

<span data-ttu-id="23505-113">To polecenie pobiera harmonogram zadań o IDENTYFIKATORze JobSchedule23.</span><span class="sxs-lookup"><span data-stu-id="23505-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="23505-114">Użyj polecenia cmdlet Get-AzBatchAccountKey, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="23505-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="23505-115">Przykład 2: pobieranie harmonogramów zadań przy użyciu filtru</span><span class="sxs-lookup"><span data-stu-id="23505-115">Example 2: Get job schedules by using a filter</span></span>
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

<span data-ttu-id="23505-116">To polecenie pobiera wszystkie harmonogramy zadań, których identyfikatory zaczynają się od zadania, określając parametr *Filter* .</span><span class="sxs-lookup"><span data-stu-id="23505-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="23505-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23505-117">PARAMETERS</span></span>

### <span data-ttu-id="23505-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="23505-118">-BatchContext</span></span>
<span data-ttu-id="23505-119">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="23505-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="23505-120">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="23505-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="23505-121">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="23505-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="23505-122">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="23505-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="23505-123">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="23505-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="23505-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23505-124">-DefaultProfile</span></span>
<span data-ttu-id="23505-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23505-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23505-126">-Expand</span><span class="sxs-lookup"><span data-stu-id="23505-126">-Expand</span></span>
<span data-ttu-id="23505-127">Określa klauzulę expanda Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="23505-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="23505-128">Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównej jednostki.</span><span class="sxs-lookup"><span data-stu-id="23505-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="23505-129">-Filter</span><span class="sxs-lookup"><span data-stu-id="23505-129">-Filter</span></span>
<span data-ttu-id="23505-130">Określa klauzulę filtru OData.</span><span class="sxs-lookup"><span data-stu-id="23505-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="23505-131">To polecenie cmdlet zwraca harmonogramy zadań zgodne z filtrem określanym przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="23505-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="23505-132">Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie harmonogramy zadań dla kontekstu partii.</span><span class="sxs-lookup"><span data-stu-id="23505-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="23505-133">-ID</span><span class="sxs-lookup"><span data-stu-id="23505-133">-Id</span></span>
<span data-ttu-id="23505-134">Określa identyfikator harmonogramu zadań, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23505-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="23505-135">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="23505-135">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="23505-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="23505-136">-MaxCount</span></span>
<span data-ttu-id="23505-137">Określa maksymalną liczbę harmonogramów zadań, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="23505-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="23505-138">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="23505-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="23505-139">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="23505-139">The default value is 1000.</span></span>

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

### <span data-ttu-id="23505-140">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="23505-140">-Select</span></span>
<span data-ttu-id="23505-141">Określa klauzulę SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="23505-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="23505-142">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="23505-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="23505-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23505-143">CommonParameters</span></span>
<span data-ttu-id="23505-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23505-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23505-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23505-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23505-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23505-146">INPUTS</span></span>

### <span data-ttu-id="23505-147">System. String</span><span class="sxs-lookup"><span data-stu-id="23505-147">System.String</span></span>

### <span data-ttu-id="23505-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="23505-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="23505-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23505-149">OUTPUTS</span></span>

### <span data-ttu-id="23505-150">Microsoft.Azure.Commands.Batch. Modele. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="23505-150">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="23505-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23505-151">NOTES</span></span>

## <span data-ttu-id="23505-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23505-152">RELATED LINKS</span></span>

[<span data-ttu-id="23505-153">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="23505-153">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="23505-154">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="23505-154">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="23505-155">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="23505-155">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="23505-156">Nowe — AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="23505-156">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="23505-157">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="23505-157">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="23505-158">Zatrzymaj — AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="23505-158">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="23505-159">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="23505-159">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


