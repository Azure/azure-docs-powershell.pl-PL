---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: c7137e9fda6c947755c8bd2e0091dd33347027fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222420"
---
# <span data-ttu-id="b0275-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="b0275-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="b0275-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0275-102">SYNOPSIS</span></span>
<span data-ttu-id="b0275-103">Oczekuje na ukończenie zadania usługi Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="b0275-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="b0275-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0275-104">SYNTAX</span></span>

### <span data-ttu-id="b0275-105">WaitSparkJobByIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b0275-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0275-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0275-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0275-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0275-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0275-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b0275-108">DESCRIPTION</span></span>
<span data-ttu-id="b0275-109">Polecenie cmdlet **wait-AzSynapseSparkJob** oczekuje na ukończenie zadania funkcji Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b0275-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="b0275-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0275-110">EXAMPLES</span></span>

### <span data-ttu-id="b0275-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b0275-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="b0275-112">To polecenie oczekuje na zakończenie zadania o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="b0275-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="b0275-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0275-113">PARAMETERS</span></span>

### <span data-ttu-id="b0275-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0275-114">-DefaultProfile</span></span>
<span data-ttu-id="b0275-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0275-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0275-116">-LivyId</span><span class="sxs-lookup"><span data-stu-id="b0275-116">-LivyId</span></span>
<span data-ttu-id="b0275-117">Identyfikator zadania usługi Spark.</span><span class="sxs-lookup"><span data-stu-id="b0275-117">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="b0275-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="b0275-118">-SparkJobObject</span></span>
<span data-ttu-id="b0275-119">Obiekt wejściowy programu Spark, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="b0275-119">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b0275-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="b0275-120">-SparkPoolName</span></span>
<span data-ttu-id="b0275-121">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="b0275-121">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="b0275-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="b0275-122">-SparkPoolObject</span></span>
<span data-ttu-id="b0275-123">Obiekt wejściowy usługi Spark Pool, zazwyczaj przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="b0275-123">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b0275-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="b0275-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="b0275-125">Maksymalny czas oczekiwania przed błędem. Wartość domyślna to nigdy nie przekroczyć limitu czasu.</span><span class="sxs-lookup"><span data-stu-id="b0275-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="b0275-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b0275-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="b0275-127">Interwał sondowania między sprawdzaniem stanu zadania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="b0275-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="b0275-128">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="b0275-128">-WorkspaceName</span></span>
<span data-ttu-id="b0275-129">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="b0275-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b0275-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0275-130">CommonParameters</span></span>
<span data-ttu-id="b0275-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0275-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0275-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0275-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0275-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0275-133">INPUTS</span></span>

### <span data-ttu-id="b0275-134">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="b0275-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="b0275-135">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="b0275-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="b0275-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0275-136">OUTPUTS</span></span>

### <span data-ttu-id="b0275-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0275-137">System.Boolean</span></span>

## <span data-ttu-id="b0275-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0275-138">NOTES</span></span>

## <span data-ttu-id="b0275-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0275-139">RELATED LINKS</span></span>
