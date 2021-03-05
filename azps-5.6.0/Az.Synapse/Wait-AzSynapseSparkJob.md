---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: fa658b7727c07b7457c2a10c1ac42e3fdb5fe347
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008209"
---
# <span data-ttu-id="343b5-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="343b5-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="343b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="343b5-102">SYNOPSIS</span></span>
<span data-ttu-id="343b5-103">Czeka na ukończenie zadania analizy Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="343b5-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="343b5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="343b5-104">SYNTAX</span></span>

### <span data-ttu-id="343b5-105">WaitSparkJobByIdParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="343b5-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="343b5-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="343b5-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="343b5-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="343b5-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="343b5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="343b5-108">DESCRIPTION</span></span>
<span data-ttu-id="343b5-109">Polecenie cmdlet **Wait-AzSynapseSparkJob** czeka na ukończenie zadania analizy Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="343b5-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="343b5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="343b5-110">EXAMPLES</span></span>

### <span data-ttu-id="343b5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="343b5-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="343b5-112">To polecenie czeka na ukończenie zadania o określonym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="343b5-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="343b5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="343b5-113">PARAMETERS</span></span>

### <span data-ttu-id="343b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="343b5-114">-DefaultProfile</span></span>
<span data-ttu-id="343b5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="343b5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="343b5-116">- Natłok</span><span class="sxs-lookup"><span data-stu-id="343b5-116">-LivyId</span></span>
<span data-ttu-id="343b5-117">Identyfikator zadania przebiegu w sparku.</span><span class="sxs-lookup"><span data-stu-id="343b5-117">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdParameterSet, WaitSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="343b5-118">— SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="343b5-118">-SparkJobObject</span></span>
<span data-ttu-id="343b5-119">Obiekt wprowadzania zadania przebiegu w przebiegu w przebiegu, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="343b5-119">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="343b5-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="343b5-120">-SparkPoolName</span></span>
<span data-ttu-id="343b5-121">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="343b5-121">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="343b5-122">— SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="343b5-122">-SparkPoolObject</span></span>
<span data-ttu-id="343b5-123">Obiekt wejściowy puli przebiegu w przebiegu w przebiegu, który zwykle przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="343b5-123">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: WaitSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="343b5-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="343b5-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="343b5-125">Maksymalna ilość czasu oczekiwania przed błędem. Wartością domyślną jest nigdy nie przeoczanie limitu czasu.</span><span class="sxs-lookup"><span data-stu-id="343b5-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="343b5-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="343b5-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="343b5-127">Interwał ankiety między sprawdzaniem stanu zadania (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="343b5-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="343b5-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="343b5-128">-WorkspaceName</span></span>
<span data-ttu-id="343b5-129">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="343b5-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="343b5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="343b5-130">CommonParameters</span></span>
<span data-ttu-id="343b5-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="343b5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="343b5-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="343b5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="343b5-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="343b5-133">INPUTS</span></span>

### <span data-ttu-id="343b5-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="343b5-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="343b5-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="343b5-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="343b5-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="343b5-136">OUTPUTS</span></span>

### <span data-ttu-id="343b5-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="343b5-137">System.Boolean</span></span>

## <span data-ttu-id="343b5-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="343b5-138">NOTES</span></span>

## <span data-ttu-id="343b5-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="343b5-139">RELATED LINKS</span></span>
