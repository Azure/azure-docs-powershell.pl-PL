---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
ms.openlocfilehash: c8b51f3822ce52fd21aa1d2b8df45d11108d713a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543936"
---
# <span data-ttu-id="c3711-101">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c3711-101">Get-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="c3711-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3711-102">SYNOPSIS</span></span>
<span data-ttu-id="c3711-103">Pobiera harmonogramy zadań wsadowych.</span><span class="sxs-lookup"><span data-stu-id="c3711-103">Gets Batch job schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3711-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3711-104">SYNTAX</span></span>

### <span data-ttu-id="c3711-105">ODataFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c3711-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3711-106">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="c3711-106">Id</span></span>
```
Get-AzureBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3711-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c3711-107">DESCRIPTION</span></span>
<span data-ttu-id="c3711-108">Polecenie cmdlet **Get-AzureBatchJobSchedule** pobiera harmonogramy zadań wsadowych platformy Azure dla konta wsadowego określonego przez parametr *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="c3711-108">The **Get-AzureBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="c3711-109">Określ identyfikator, aby uzyskać jeden harmonogram zadania.</span><span class="sxs-lookup"><span data-stu-id="c3711-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="c3711-110">Określ parametr *Filter* , aby pobrać harmonogramy zadań zgodne z filtrem Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="c3711-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="c3711-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3711-111">EXAMPLES</span></span>

### <span data-ttu-id="c3711-112">Przykład 1: uzyskiwanie harmonogramu zadań przez określenie identyfikatora</span><span class="sxs-lookup"><span data-stu-id="c3711-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
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

<span data-ttu-id="c3711-113">To polecenie pobiera harmonogram zadań o IDENTYFIKATORze JobSchedule23.</span><span class="sxs-lookup"><span data-stu-id="c3711-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="c3711-114">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="c3711-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c3711-115">Przykład 2: pobieranie harmonogramów zadań przy użyciu filtru</span><span class="sxs-lookup"><span data-stu-id="c3711-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
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

<span data-ttu-id="c3711-116">To polecenie pobiera wszystkie harmonogramy zadań, których identyfikatory zaczynają się od zadania, określając parametr *Filter* .</span><span class="sxs-lookup"><span data-stu-id="c3711-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="c3711-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3711-117">PARAMETERS</span></span>

### <span data-ttu-id="c3711-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c3711-118">-BatchContext</span></span>
<span data-ttu-id="c3711-119">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="c3711-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c3711-120">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="c3711-120">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c3711-121">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="c3711-121">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c3711-122">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="c3711-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c3711-123">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c3711-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c3711-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3711-124">-DefaultProfile</span></span>
<span data-ttu-id="c3711-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3711-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3711-126">-Expand</span><span class="sxs-lookup"><span data-stu-id="c3711-126">-Expand</span></span>
<span data-ttu-id="c3711-127">Określa klauzulę expanda Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="c3711-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="c3711-128">Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównej jednostki.</span><span class="sxs-lookup"><span data-stu-id="c3711-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="c3711-129">-Filter</span><span class="sxs-lookup"><span data-stu-id="c3711-129">-Filter</span></span>
<span data-ttu-id="c3711-130">Określa klauzulę filtru OData.</span><span class="sxs-lookup"><span data-stu-id="c3711-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="c3711-131">To polecenie cmdlet zwraca harmonogramy zadań zgodne z filtrem określanym przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c3711-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="c3711-132">Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie harmonogramy zadań dla kontekstu partii.</span><span class="sxs-lookup"><span data-stu-id="c3711-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="c3711-133">-ID</span><span class="sxs-lookup"><span data-stu-id="c3711-133">-Id</span></span>
<span data-ttu-id="c3711-134">Określa identyfikator harmonogramu zadań, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3711-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="c3711-135">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="c3711-135">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="c3711-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c3711-136">-MaxCount</span></span>
<span data-ttu-id="c3711-137">Określa maksymalną liczbę harmonogramów zadań, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="c3711-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="c3711-138">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="c3711-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="c3711-139">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="c3711-139">The default value is 1000.</span></span>

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

### <span data-ttu-id="c3711-140">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="c3711-140">-Select</span></span>
<span data-ttu-id="c3711-141">Określa klauzulę SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="c3711-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="c3711-142">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="c3711-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="c3711-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3711-143">CommonParameters</span></span>
<span data-ttu-id="c3711-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3711-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3711-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3711-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3711-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3711-146">INPUTS</span></span>

### <span data-ttu-id="c3711-147">System. String</span><span class="sxs-lookup"><span data-stu-id="c3711-147">System.String</span></span>

### <span data-ttu-id="c3711-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c3711-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="c3711-149">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c3711-149">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="c3711-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3711-150">OUTPUTS</span></span>

### <span data-ttu-id="c3711-151">Microsoft.Azure.Commands.Batch. Modele. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c3711-151">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="c3711-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3711-152">NOTES</span></span>

## <span data-ttu-id="c3711-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3711-153">RELATED LINKS</span></span>

[<span data-ttu-id="c3711-154">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c3711-154">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="c3711-155">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c3711-155">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="c3711-156">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c3711-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c3711-157">Nowe — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c3711-157">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="c3711-158">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c3711-158">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="c3711-159">Zatrzymaj — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c3711-159">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="c3711-160">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="c3711-160">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


