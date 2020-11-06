---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: 0a31b787b1be6d45caca74d01ee5d15d00071641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547055"
---
# <span data-ttu-id="d0ce8-101">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d0ce8-101">New-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="d0ce8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0ce8-102">SYNOPSIS</span></span>
<span data-ttu-id="d0ce8-103">Tworzy harmonogram zadań w usłudze przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-103">Creates a job schedule in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0ce8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0ce8-104">SYNTAX</span></span>

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0ce8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d0ce8-105">DESCRIPTION</span></span>
<span data-ttu-id="d0ce8-106">Polecenie cmdlet **New-AzureBatchJobSchedule** tworzy harmonogram zadań w usłudze Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-106">The **New-AzureBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="d0ce8-107">Parametr *BatchAccountContext* określa konto, w którym to polecenie cmdlet tworzy harmonogram.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="d0ce8-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0ce8-108">EXAMPLES</span></span>

### <span data-ttu-id="d0ce8-109">Przykład 1. Tworzenie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="d0ce8-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="d0ce8-110">W tym przykładzie jest tworzony harmonogram zadań.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-110">This example creates a job schedule.</span></span>

<span data-ttu-id="d0ce8-111">Pięć pierwszych poleceń tworzenie i modyfikowanie obiektów **PSSchedule** , **PSJobSpecification** i **PSPoolInformation** .</span><span class="sxs-lookup"><span data-stu-id="d0ce8-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="d0ce8-112">W poleceniach użyto New-Object polecenia cmdlet i standardowej składni programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="d0ce8-113">Poniższe polecenia przechowują te obiekty w zmiennych $Schedule i $JobSpecification.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>

<span data-ttu-id="d0ce8-114">Ostatnie polecenie tworzy harmonogram zadań o IDENTYFIKATORze JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="d0ce8-115">Ten harmonogram tworzy zadania z interwałem cyklu o wymiarze jednego dnia.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="d0ce8-116">Zadania są uruchamiane w puli o IDENTYFIKATORze ContosoPool06, jak określono w piątym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="d0ce8-117">Użyj polecenia cmdlet **Get-AzureRmBatchAccountKeys** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-117">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="d0ce8-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0ce8-118">PARAMETERS</span></span>

### <span data-ttu-id="d0ce8-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d0ce8-119">-BatchContext</span></span>
<span data-ttu-id="d0ce8-120">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d0ce8-121">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="d0ce8-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d0ce8-122">-DisplayName</span></span>
<span data-ttu-id="d0ce8-123">Określa nazwę wyświetlaną dla harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-123">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="d0ce8-124">-ID</span><span class="sxs-lookup"><span data-stu-id="d0ce8-124">-Id</span></span>
<span data-ttu-id="d0ce8-125">Określa identyfikator harmonogramu zadań tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-125">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d0ce8-126">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="d0ce8-126">-JobSpecification</span></span>
<span data-ttu-id="d0ce8-127">Określa szczegóły zadań, które obejmuje ten aplet polecenia w harmonogramie zadań.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-127">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

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

### <span data-ttu-id="d0ce8-128">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d0ce8-128">-Metadata</span></span>
<span data-ttu-id="d0ce8-129">Określa metadane, jako pary klucz/wartość, aby dodać je do harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-129">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="d0ce8-130">Klucz to nazwa metadanych.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-130">The key is the metadata name.</span></span>
<span data-ttu-id="d0ce8-131">Wartość jest wartością metadanych.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-131">The value is the metadata value.</span></span>

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

### <span data-ttu-id="d0ce8-132">-Schedule</span><span class="sxs-lookup"><span data-stu-id="d0ce8-132">-Schedule</span></span>
<span data-ttu-id="d0ce8-133">Określa harmonogram, który określa termin tworzenia zadań.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-133">Specifies the schedule that determines when to create jobs.</span></span>

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

### <span data-ttu-id="d0ce8-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0ce8-134">-DefaultProfile</span></span>
<span data-ttu-id="d0ce8-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0ce8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0ce8-136">CommonParameters</span></span>
<span data-ttu-id="d0ce8-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0ce8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0ce8-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0ce8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0ce8-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0ce8-139">INPUTS</span></span>

### <span data-ttu-id="d0ce8-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d0ce8-140">BatchAccountContext</span></span>
<span data-ttu-id="d0ce8-141">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="d0ce8-141">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="d0ce8-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0ce8-142">OUTPUTS</span></span>

## <span data-ttu-id="d0ce8-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0ce8-143">NOTES</span></span>

## <span data-ttu-id="d0ce8-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0ce8-144">RELATED LINKS</span></span>

[<span data-ttu-id="d0ce8-145">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d0ce8-145">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="d0ce8-146">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d0ce8-146">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="d0ce8-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d0ce8-147">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d0ce8-148">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d0ce8-148">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="d0ce8-149">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d0ce8-149">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="d0ce8-150">Zatrzymaj — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d0ce8-150">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="d0ce8-151">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="d0ce8-151">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


