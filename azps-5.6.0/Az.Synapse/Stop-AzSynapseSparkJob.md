---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: 601ab4b0602a83b708418c626eb48695e18eb7c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991992"
---
# <span data-ttu-id="801b1-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="801b1-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="801b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="801b1-102">SYNOPSIS</span></span>
<span data-ttu-id="801b1-103">Anulowanie zadania analizy Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="801b1-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="801b1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="801b1-104">SYNTAX</span></span>

### <span data-ttu-id="801b1-105">StopSparkJobByIdParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="801b1-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="801b1-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="801b1-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="801b1-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="801b1-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="801b1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="801b1-108">DESCRIPTION</span></span>
<span data-ttu-id="801b1-109">Polecenie **cmdlet Stop-AzSynapseSparkJob** anuluje zadanie analizy Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="801b1-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="801b1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="801b1-110">EXAMPLES</span></span>

### <span data-ttu-id="801b1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="801b1-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="801b1-112">To polecenie anuluje zadanie analizy Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="801b1-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="801b1-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="801b1-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="801b1-114">To polecenie anuluje zadanie analizy Synapse Analytics w potoku.</span><span class="sxs-lookup"><span data-stu-id="801b1-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="801b1-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="801b1-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="801b1-116">To polecenie anuluje zadanie analizy Synapse Analytics w potoku.</span><span class="sxs-lookup"><span data-stu-id="801b1-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="801b1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="801b1-117">PARAMETERS</span></span>

### <span data-ttu-id="801b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="801b1-118">-DefaultProfile</span></span>
<span data-ttu-id="801b1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="801b1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="801b1-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="801b1-120">-Force</span></span>
<span data-ttu-id="801b1-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="801b1-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="801b1-122">- Natłok</span><span class="sxs-lookup"><span data-stu-id="801b1-122">-LivyId</span></span>
<span data-ttu-id="801b1-123">Identyfikator zadania przebiegu w sparku.</span><span class="sxs-lookup"><span data-stu-id="801b1-123">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="801b1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="801b1-124">-PassThru</span></span>
<span data-ttu-id="801b1-125">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="801b1-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="801b1-126">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="801b1-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="801b1-127">— SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="801b1-127">-SparkJobObject</span></span>
<span data-ttu-id="801b1-128">Obiekt wprowadzania zadania przebiegu w przebiegu w przebiegu, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="801b1-128">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="801b1-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="801b1-129">-SparkPoolName</span></span>
<span data-ttu-id="801b1-130">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="801b1-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="801b1-131">— SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="801b1-131">-SparkPoolObject</span></span>
<span data-ttu-id="801b1-132">Obiekt wejściowy puli przebiegu w przebiegu w przebiegu, który zwykle przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="801b1-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="801b1-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="801b1-133">-WorkspaceName</span></span>
<span data-ttu-id="801b1-134">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="801b1-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="801b1-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="801b1-135">-Confirm</span></span>
<span data-ttu-id="801b1-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="801b1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="801b1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="801b1-137">-WhatIf</span></span>
<span data-ttu-id="801b1-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="801b1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="801b1-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="801b1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="801b1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="801b1-140">CommonParameters</span></span>
<span data-ttu-id="801b1-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="801b1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="801b1-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="801b1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="801b1-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="801b1-143">INPUTS</span></span>

### <span data-ttu-id="801b1-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="801b1-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="801b1-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="801b1-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="801b1-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="801b1-146">OUTPUTS</span></span>

### <span data-ttu-id="801b1-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="801b1-147">System.Boolean</span></span>

## <span data-ttu-id="801b1-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="801b1-148">NOTES</span></span>

## <span data-ttu-id="801b1-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="801b1-149">RELATED LINKS</span></span>
