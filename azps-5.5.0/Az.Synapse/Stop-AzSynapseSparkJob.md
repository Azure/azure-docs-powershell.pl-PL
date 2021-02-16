---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: c916b5a7a7d56c241e3cd346c5b7386c0f36ddb1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195539"
---
# <span data-ttu-id="0b914-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="0b914-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="0b914-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b914-102">SYNOPSIS</span></span>
<span data-ttu-id="0b914-103">Anulowanie zadania analizy Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="0b914-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="0b914-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0b914-104">SYNTAX</span></span>

### <span data-ttu-id="0b914-105">StopSparkJobByIdParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="0b914-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b914-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b914-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b914-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b914-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b914-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0b914-108">DESCRIPTION</span></span>
<span data-ttu-id="0b914-109">Polecenie **cmdlet Stop-AzSynapseSparkJob** anuluje zadanie analizy Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="0b914-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="0b914-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0b914-110">EXAMPLES</span></span>

### <span data-ttu-id="0b914-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0b914-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="0b914-112">To polecenie anuluje zadanie analizy Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="0b914-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="0b914-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0b914-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="0b914-114">To polecenie anuluje zadanie analizy Synapse Analytics w potoku.</span><span class="sxs-lookup"><span data-stu-id="0b914-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="0b914-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0b914-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="0b914-116">To polecenie anuluje zadanie analizy Synapse Analytics w potoku.</span><span class="sxs-lookup"><span data-stu-id="0b914-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="0b914-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b914-117">PARAMETERS</span></span>

### <span data-ttu-id="0b914-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b914-118">-DefaultProfile</span></span>
<span data-ttu-id="0b914-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b914-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b914-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0b914-120">-Force</span></span>
<span data-ttu-id="0b914-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0b914-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0b914-122">- Natłok</span><span class="sxs-lookup"><span data-stu-id="0b914-122">-LivyId</span></span>
<span data-ttu-id="0b914-123">Identyfikator zadania przebiegu w sparku.</span><span class="sxs-lookup"><span data-stu-id="0b914-123">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="0b914-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b914-124">-PassThru</span></span>
<span data-ttu-id="0b914-125">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="0b914-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="0b914-126">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="0b914-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0b914-127">— SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="0b914-127">-SparkJobObject</span></span>
<span data-ttu-id="0b914-128">Obiekt wprowadzania zadania przebiegu w uścisce, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="0b914-128">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0b914-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="0b914-129">-SparkPoolName</span></span>
<span data-ttu-id="0b914-130">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="0b914-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="0b914-131">— SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="0b914-131">-SparkPoolObject</span></span>
<span data-ttu-id="0b914-132">Obiekt wejściowy puli przebiegu w przebiegu w przebiegu w uścisce, który zwykle przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="0b914-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0b914-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0b914-133">-WorkspaceName</span></span>
<span data-ttu-id="0b914-134">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="0b914-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0b914-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0b914-135">-Confirm</span></span>
<span data-ttu-id="0b914-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0b914-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b914-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b914-137">-WhatIf</span></span>
<span data-ttu-id="0b914-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b914-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b914-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0b914-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b914-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b914-140">CommonParameters</span></span>
<span data-ttu-id="0b914-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b914-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b914-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b914-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b914-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b914-143">INPUTS</span></span>

### <span data-ttu-id="0b914-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="0b914-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="0b914-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="0b914-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="0b914-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b914-146">OUTPUTS</span></span>

### <span data-ttu-id="0b914-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0b914-147">System.Boolean</span></span>

## <span data-ttu-id="0b914-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0b914-148">NOTES</span></span>

## <span data-ttu-id="0b914-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b914-149">RELATED LINKS</span></span>
