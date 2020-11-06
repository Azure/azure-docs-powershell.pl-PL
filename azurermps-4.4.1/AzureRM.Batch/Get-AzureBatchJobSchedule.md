---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
ms.openlocfilehash: 139282332fb1c5d0ace02ddd7b998c1875af931a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546288"
---
# <span data-ttu-id="ec0f0-101">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ec0f0-101">Get-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="ec0f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec0f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ec0f0-103">Pobiera harmonogramy zadań wsadowych.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-103">Gets Batch job schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec0f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec0f0-104">SYNTAX</span></span>

### <span data-ttu-id="ec0f0-105">ODataFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ec0f0-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec0f0-106">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="ec0f0-106">Id</span></span>
```
Get-AzureBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec0f0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ec0f0-107">DESCRIPTION</span></span>
<span data-ttu-id="ec0f0-108">Polecenie cmdlet **Get-AzureBatchJobSchedule** pobiera harmonogramy zadań wsadowych platformy Azure dla konta wsadowego określonego przez parametr *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="ec0f0-108">The **Get-AzureBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="ec0f0-109">Określ identyfikator, aby uzyskać jeden harmonogram zadania.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="ec0f0-110">Określ parametr *Filter* , aby pobrać harmonogramy zadań zgodne z filtrem Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="ec0f0-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="ec0f0-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec0f0-111">EXAMPLES</span></span>

### <span data-ttu-id="ec0f0-112">Przykład 1: uzyskiwanie harmonogramu zadań przez określenie identyfikatora</span><span class="sxs-lookup"><span data-stu-id="ec0f0-112">Example 1: Get a job schedule by specifying an ID</span></span>
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

<span data-ttu-id="ec0f0-113">To polecenie pobiera harmonogram zadań o IDENTYFIKATORze JobSchedule23.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="ec0f0-114">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ec0f0-115">Przykład 2: pobieranie harmonogramów zadań przy użyciu filtru</span><span class="sxs-lookup"><span data-stu-id="ec0f0-115">Example 2: Get job schedules by using a filter</span></span>
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

<span data-ttu-id="ec0f0-116">To polecenie pobiera wszystkie harmonogramy zadań, których identyfikatory zaczynają się od zadania, określając parametr *Filter* .</span><span class="sxs-lookup"><span data-stu-id="ec0f0-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="ec0f0-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec0f0-117">PARAMETERS</span></span>

### <span data-ttu-id="ec0f0-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ec0f0-118">-BatchContext</span></span>
<span data-ttu-id="ec0f0-119">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ec0f0-120">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="ec0f0-121">-Expand</span><span class="sxs-lookup"><span data-stu-id="ec0f0-121">-Expand</span></span>
<span data-ttu-id="ec0f0-122">Określa klauzulę expanda Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="ec0f0-122">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="ec0f0-123">Określ wartość dla tego parametru, aby uzyskać skojarzone jednostki głównej jednostki.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-123">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="ec0f0-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="ec0f0-124">-Filter</span></span>
<span data-ttu-id="ec0f0-125">Określa klauzulę filtru OData.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-125">Specifies an OData filter clause.</span></span>
<span data-ttu-id="ec0f0-126">To polecenie cmdlet zwraca harmonogramy zadań zgodne z filtrem określanym przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-126">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="ec0f0-127">Jeśli nie określisz filtru, to polecenie cmdlet zwróci wszystkie harmonogramy zadań dla kontekstu partii.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-127">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="ec0f0-128">-ID</span><span class="sxs-lookup"><span data-stu-id="ec0f0-128">-Id</span></span>
<span data-ttu-id="ec0f0-129">Określa identyfikator harmonogramu zadań, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-129">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="ec0f0-130">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-130">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="ec0f0-131">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ec0f0-131">-MaxCount</span></span>
<span data-ttu-id="ec0f0-132">Określa maksymalną liczbę harmonogramów zadań, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-132">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="ec0f0-133">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-133">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="ec0f0-134">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-134">The default value is 1000.</span></span>

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

### <span data-ttu-id="ec0f0-135">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="ec0f0-135">-Select</span></span>
<span data-ttu-id="ec0f0-136">Określa klauzulę SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-136">Specifies an OData select clause.</span></span>
<span data-ttu-id="ec0f0-137">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-137">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="ec0f0-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec0f0-138">-DefaultProfile</span></span>
<span data-ttu-id="ec0f0-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec0f0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec0f0-140">CommonParameters</span></span>
<span data-ttu-id="ec0f0-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec0f0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec0f0-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec0f0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec0f0-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec0f0-143">INPUTS</span></span>

### <span data-ttu-id="ec0f0-144">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ec0f0-144">BatchAccountContext</span></span>
<span data-ttu-id="ec0f0-145">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ec0f0-145">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ec0f0-146">Ciąg</span><span class="sxs-lookup"><span data-stu-id="ec0f0-146">String</span></span>
<span data-ttu-id="ec0f0-147">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="ec0f0-147">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ec0f0-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec0f0-148">OUTPUTS</span></span>

### <span data-ttu-id="ec0f0-149">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ec0f0-149">PSCloudJobSchedule</span></span>

## <span data-ttu-id="ec0f0-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec0f0-150">NOTES</span></span>

## <span data-ttu-id="ec0f0-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec0f0-151">RELATED LINKS</span></span>

[<span data-ttu-id="ec0f0-152">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ec0f0-152">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="ec0f0-153">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ec0f0-153">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="ec0f0-154">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ec0f0-154">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ec0f0-155">Nowe — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ec0f0-155">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="ec0f0-156">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ec0f0-156">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="ec0f0-157">Zatrzymaj — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ec0f0-157">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="ec0f0-158">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="ec0f0-158">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


