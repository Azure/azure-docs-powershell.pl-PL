---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: 0524a55284d5c93db006248c12aa5a44f40deee7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541936"
---
# <span data-ttu-id="5ac0e-101">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5ac0e-101">New-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="5ac0e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ac0e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac0e-103">Tworzy harmonogram zadań w usłudze przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-103">Creates a job schedule in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ac0e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ac0e-104">SYNTAX</span></span>

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ac0e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ac0e-105">DESCRIPTION</span></span>
<span data-ttu-id="5ac0e-106">Polecenie cmdlet **New-AzureBatchJobSchedule** tworzy harmonogram zadań w usłudze Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-106">The **New-AzureBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="5ac0e-107">Parametr *BatchAccountContext* określa konto, w którym to polecenie cmdlet tworzy harmonogram.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="5ac0e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ac0e-108">EXAMPLES</span></span>

### <span data-ttu-id="5ac0e-109">Przykład 1. Tworzenie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="5ac0e-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="5ac0e-110">W tym przykładzie jest tworzony harmonogram zadań.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-110">This example creates a job schedule.</span></span>
<span data-ttu-id="5ac0e-111">Pięć pierwszych poleceń tworzenie i modyfikowanie obiektów **PSSchedule** , **PSJobSpecification** i **PSPoolInformation** .</span><span class="sxs-lookup"><span data-stu-id="5ac0e-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="5ac0e-112">W poleceniach użyto New-Object polecenia cmdlet i standardowej składni programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="5ac0e-113">Poniższe polecenia przechowują te obiekty w zmiennych $Schedule i $JobSpecification.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>
<span data-ttu-id="5ac0e-114">Ostatnie polecenie tworzy harmonogram zadań o IDENTYFIKATORze JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="5ac0e-115">Ten harmonogram tworzy zadania z interwałem cyklu o wymiarze jednego dnia.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="5ac0e-116">Zadania są uruchamiane w puli o IDENTYFIKATORze ContosoPool06, jak określono w piątym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="5ac0e-117">Użyj polecenia cmdlet **Get-AzureRmBatchAccountKeys** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-117">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="5ac0e-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ac0e-118">PARAMETERS</span></span>

### <span data-ttu-id="5ac0e-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5ac0e-119">-BatchContext</span></span>
<span data-ttu-id="5ac0e-120">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5ac0e-121">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5ac0e-122">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5ac0e-123">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5ac0e-124">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5ac0e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac0e-125">-DefaultProfile</span></span>
<span data-ttu-id="5ac0e-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ac0e-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5ac0e-127">-DisplayName</span></span>
<span data-ttu-id="5ac0e-128">Określa nazwę wyświetlaną dla harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-128">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="5ac0e-129">-ID</span><span class="sxs-lookup"><span data-stu-id="5ac0e-129">-Id</span></span>
<span data-ttu-id="5ac0e-130">Określa identyfikator harmonogramu zadań tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5ac0e-131">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="5ac0e-131">-JobSpecification</span></span>
<span data-ttu-id="5ac0e-132">Określa szczegóły zadań, które obejmuje ten aplet polecenia w harmonogramie zadań.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

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

### <span data-ttu-id="5ac0e-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="5ac0e-133">-Metadata</span></span>
<span data-ttu-id="5ac0e-134">Określa metadane, jako pary klucz/wartość, aby dodać je do harmonogramu zadań.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="5ac0e-135">Klucz to nazwa metadanych.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-135">The key is the metadata name.</span></span>
<span data-ttu-id="5ac0e-136">Wartość jest wartością metadanych.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-136">The value is the metadata value.</span></span>

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

### <span data-ttu-id="5ac0e-137">-Schedule</span><span class="sxs-lookup"><span data-stu-id="5ac0e-137">-Schedule</span></span>
<span data-ttu-id="5ac0e-138">Określa harmonogram, który określa termin tworzenia zadań.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-138">Specifies the schedule that determines when to create jobs.</span></span>

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

### <span data-ttu-id="5ac0e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac0e-139">CommonParameters</span></span>
<span data-ttu-id="5ac0e-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ac0e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac0e-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ac0e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac0e-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ac0e-142">INPUTS</span></span>

### <span data-ttu-id="5ac0e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5ac0e-143">System.String</span></span>

### <span data-ttu-id="5ac0e-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5ac0e-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="5ac0e-145">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5ac0e-145">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="5ac0e-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ac0e-146">OUTPUTS</span></span>

### <span data-ttu-id="5ac0e-147">System. void</span><span class="sxs-lookup"><span data-stu-id="5ac0e-147">System.Void</span></span>

## <span data-ttu-id="5ac0e-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ac0e-148">NOTES</span></span>

## <span data-ttu-id="5ac0e-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ac0e-149">RELATED LINKS</span></span>

[<span data-ttu-id="5ac0e-150">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5ac0e-150">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="5ac0e-151">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5ac0e-151">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="5ac0e-152">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5ac0e-152">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5ac0e-153">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5ac0e-153">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="5ac0e-154">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5ac0e-154">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="5ac0e-155">Zatrzymaj — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5ac0e-155">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="5ac0e-156">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="5ac0e-156">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

