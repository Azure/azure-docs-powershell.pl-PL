---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: c7137e9fda6c947755c8bd2e0091dd33347027fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182626"
---
# <span data-ttu-id="b0a51-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="b0a51-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="b0a51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0a51-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a51-103">Czeka na ukończenie zadania analizy Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b0a51-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="b0a51-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b0a51-104">SYNTAX</span></span>

### <span data-ttu-id="b0a51-105">WaitSparkJobByIdParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b0a51-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0a51-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0a51-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0a51-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0a51-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0a51-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b0a51-108">DESCRIPTION</span></span>
<span data-ttu-id="b0a51-109">Polecenie cmdlet **Wait-AzSynapseSparkJob** czeka na ukończenie zadania analizy Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b0a51-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="b0a51-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b0a51-110">EXAMPLES</span></span>

### <span data-ttu-id="b0a51-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b0a51-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="b0a51-112">To polecenie czeka na ukończenie zadania o określonym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="b0a51-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="b0a51-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0a51-113">PARAMETERS</span></span>

### <span data-ttu-id="b0a51-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a51-114">-DefaultProfile</span></span>
<span data-ttu-id="b0a51-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0a51-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0a51-116">- Natłok</span><span class="sxs-lookup"><span data-stu-id="b0a51-116">-LivyId</span></span>
<span data-ttu-id="b0a51-117">Identyfikator zadania przebiegu w sparku.</span><span class="sxs-lookup"><span data-stu-id="b0a51-117">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="b0a51-118">— SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="b0a51-118">-SparkJobObject</span></span>
<span data-ttu-id="b0a51-119">Obiekt wprowadzania zadania przebiegu w uścisce, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="b0a51-119">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b0a51-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="b0a51-120">-SparkPoolName</span></span>
<span data-ttu-id="b0a51-121">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="b0a51-121">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="b0a51-122">— SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="b0a51-122">-SparkPoolObject</span></span>
<span data-ttu-id="b0a51-123">Obiekt wejściowy puli przebiegu w przebiegu w przebiegu w uścisce, który zwykle przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="b0a51-123">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b0a51-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="b0a51-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="b0a51-125">Maksymalny czas oczekiwania przed błędem. Wartość domyślna to nigdy nie przeoczanie limitu czasu.</span><span class="sxs-lookup"><span data-stu-id="b0a51-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="b0a51-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b0a51-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="b0a51-127">Interwał ankiety między sprawdzaniem stanu zadania (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="b0a51-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="b0a51-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b0a51-128">-WorkspaceName</span></span>
<span data-ttu-id="b0a51-129">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="b0a51-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b0a51-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a51-130">CommonParameters</span></span>
<span data-ttu-id="b0a51-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0a51-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a51-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0a51-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a51-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0a51-133">INPUTS</span></span>

### <span data-ttu-id="b0a51-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="b0a51-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="b0a51-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="b0a51-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="b0a51-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0a51-136">OUTPUTS</span></span>

### <span data-ttu-id="b0a51-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b0a51-137">System.Boolean</span></span>

## <span data-ttu-id="b0a51-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b0a51-138">NOTES</span></span>

## <span data-ttu-id="b0a51-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0a51-139">RELATED LINKS</span></span>
