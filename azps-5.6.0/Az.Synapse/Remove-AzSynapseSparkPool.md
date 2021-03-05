---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: 22b006d096d1ab2457d53a97a6265bf950c4658e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963450"
---
# <span data-ttu-id="758e8-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="758e8-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="758e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="758e8-102">SYNOPSIS</span></span>
<span data-ttu-id="758e8-103">Usuwa pulę przebiegu w czasie analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="758e8-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="758e8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="758e8-104">SYNTAX</span></span>

### <span data-ttu-id="758e8-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="758e8-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="758e8-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="758e8-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="758e8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="758e8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="758e8-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="758e8-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="758e8-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="758e8-109">DESCRIPTION</span></span>
<span data-ttu-id="758e8-110">Polecenie **cmdlet Remove-AzSynapseSparkPool** trwale usuwa pulę przebiegu w czasie analizy Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="758e8-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="758e8-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="758e8-111">EXAMPLES</span></span>

### <span data-ttu-id="758e8-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="758e8-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="758e8-113">To polecenie usuwa pulę przebiegu w czasie analizy Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="758e8-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="758e8-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="758e8-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="758e8-115">To polecenie usuwa pulę przebiegu w czasie analizy Azure Synapse Analytics w potoku.</span><span class="sxs-lookup"><span data-stu-id="758e8-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="758e8-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="758e8-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="758e8-117">To polecenie usuwa pulę przebiegu w czasie analizy Azure Synapse Analytics w potoku.</span><span class="sxs-lookup"><span data-stu-id="758e8-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="758e8-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="758e8-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="758e8-119">To polecenie usuwa pulę przebiegu w czasie analizy Azure Synapse Analytics z identyfikatorem zasobu.</span><span class="sxs-lookup"><span data-stu-id="758e8-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="758e8-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="758e8-120">PARAMETERS</span></span>

### <span data-ttu-id="758e8-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="758e8-121">-AsJob</span></span>
<span data-ttu-id="758e8-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="758e8-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="758e8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="758e8-123">-DefaultProfile</span></span>
<span data-ttu-id="758e8-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="758e8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="758e8-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="758e8-125">-Force</span></span>
<span data-ttu-id="758e8-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="758e8-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="758e8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="758e8-127">-InputObject</span></span>
<span data-ttu-id="758e8-128">Obiekt wejściowy puli przebiegu w przebiegu w przebiegu, który zwykle przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="758e8-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="758e8-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="758e8-129">-Name</span></span>
<span data-ttu-id="758e8-130">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="758e8-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758e8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="758e8-131">-PassThru</span></span>
<span data-ttu-id="758e8-132">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="758e8-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="758e8-133">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="758e8-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="758e8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="758e8-134">-ResourceGroupName</span></span>
<span data-ttu-id="758e8-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="758e8-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758e8-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="758e8-136">-ResourceId</span></span>
<span data-ttu-id="758e8-137">Identyfikator zasobu puli synpsy przebiegu w czasie.</span><span class="sxs-lookup"><span data-stu-id="758e8-137">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758e8-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="758e8-138">-WorkspaceName</span></span>
<span data-ttu-id="758e8-139">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="758e8-139">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758e8-140">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="758e8-140">-WorkspaceObject</span></span>
<span data-ttu-id="758e8-141">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="758e8-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="758e8-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="758e8-142">-Confirm</span></span>
<span data-ttu-id="758e8-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="758e8-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="758e8-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="758e8-144">-WhatIf</span></span>
<span data-ttu-id="758e8-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="758e8-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="758e8-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="758e8-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="758e8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="758e8-147">CommonParameters</span></span>
<span data-ttu-id="758e8-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="758e8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="758e8-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="758e8-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="758e8-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="758e8-150">INPUTS</span></span>

### <span data-ttu-id="758e8-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="758e8-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="758e8-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="758e8-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="758e8-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="758e8-153">OUTPUTS</span></span>

### <span data-ttu-id="758e8-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="758e8-154">System.Boolean</span></span>

## <span data-ttu-id="758e8-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="758e8-155">NOTES</span></span>

## <span data-ttu-id="758e8-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="758e8-156">RELATED LINKS</span></span>
