---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: c916b5a7a7d56c241e3cd346c5b7386c0f36ddb1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339118"
---
# <span data-ttu-id="535ed-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="535ed-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="535ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="535ed-102">SYNOPSIS</span></span>
<span data-ttu-id="535ed-103">Anuluje zadanie Synapse analiza Spark.</span><span class="sxs-lookup"><span data-stu-id="535ed-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="535ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="535ed-104">SYNTAX</span></span>

### <span data-ttu-id="535ed-105">StopSparkJobByIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="535ed-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="535ed-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="535ed-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="535ed-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="535ed-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="535ed-108">Opis</span><span class="sxs-lookup"><span data-stu-id="535ed-108">DESCRIPTION</span></span>
<span data-ttu-id="535ed-109">Polecenie cmdlet **stop-AzSynapseSparkJob** anuluje zadanie usługi Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="535ed-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="535ed-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="535ed-110">EXAMPLES</span></span>

### <span data-ttu-id="535ed-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="535ed-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="535ed-112">To polecenie anuluje zadanie programu Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="535ed-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="535ed-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="535ed-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="535ed-114">To polecenie anuluje zadanie Synapse analiza zapłonu za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="535ed-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="535ed-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="535ed-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="535ed-116">To polecenie anuluje zadanie Synapse analiza zapłonu za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="535ed-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="535ed-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="535ed-117">PARAMETERS</span></span>

### <span data-ttu-id="535ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="535ed-118">-DefaultProfile</span></span>
<span data-ttu-id="535ed-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="535ed-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="535ed-120">-Force</span><span class="sxs-lookup"><span data-stu-id="535ed-120">-Force</span></span>
<span data-ttu-id="535ed-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="535ed-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535ed-122">-LivyId</span><span class="sxs-lookup"><span data-stu-id="535ed-122">-LivyId</span></span>
<span data-ttu-id="535ed-123">Identyfikator zadania usługi Spark.</span><span class="sxs-lookup"><span data-stu-id="535ed-123">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdParameterSet, StopSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535ed-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="535ed-124">-PassThru</span></span>
<span data-ttu-id="535ed-125">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="535ed-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="535ed-126">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="535ed-126">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535ed-127">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="535ed-127">-SparkJobObject</span></span>
<span data-ttu-id="535ed-128">Obiekt wejściowy programu Spark, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="535ed-128">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="535ed-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="535ed-129">-SparkPoolName</span></span>
<span data-ttu-id="535ed-130">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="535ed-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535ed-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="535ed-131">-SparkPoolObject</span></span>
<span data-ttu-id="535ed-132">Obiekt wejściowy usługi Spark Pool, zazwyczaj przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="535ed-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: StopSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="535ed-133">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="535ed-133">-WorkspaceName</span></span>
<span data-ttu-id="535ed-134">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="535ed-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535ed-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="535ed-135">-Confirm</span></span>
<span data-ttu-id="535ed-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="535ed-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535ed-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="535ed-137">-WhatIf</span></span>
<span data-ttu-id="535ed-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="535ed-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="535ed-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="535ed-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535ed-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="535ed-140">CommonParameters</span></span>
<span data-ttu-id="535ed-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="535ed-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="535ed-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="535ed-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="535ed-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="535ed-143">INPUTS</span></span>

### <span data-ttu-id="535ed-144">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="535ed-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="535ed-145">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="535ed-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="535ed-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="535ed-146">OUTPUTS</span></span>

### <span data-ttu-id="535ed-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="535ed-147">System.Boolean</span></span>

## <span data-ttu-id="535ed-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="535ed-148">NOTES</span></span>

## <span data-ttu-id="535ed-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="535ed-149">RELATED LINKS</span></span>
