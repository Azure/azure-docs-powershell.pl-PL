---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: 1afa4776aa82dcfddab1709cf08dcfe8cd0ff71b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323120"
---
# <span data-ttu-id="96966-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="96966-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="96966-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="96966-102">SYNOPSIS</span></span>
<span data-ttu-id="96966-103">Usuwa pulę Synapse analizy Spark.</span><span class="sxs-lookup"><span data-stu-id="96966-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="96966-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="96966-104">SYNTAX</span></span>

### <span data-ttu-id="96966-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="96966-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96966-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96966-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96966-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96966-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96966-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96966-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96966-109">Opis</span><span class="sxs-lookup"><span data-stu-id="96966-109">DESCRIPTION</span></span>
<span data-ttu-id="96966-110">Polecenie cmdlet **Remove-AzSynapseSparkPool** umożliwia trwałe usunięcie puli platformy Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="96966-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="96966-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="96966-111">EXAMPLES</span></span>

### <span data-ttu-id="96966-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="96966-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="96966-113">To polecenie usuwa pulę platformy Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="96966-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="96966-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="96966-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="96966-115">To polecenie usuwa pulę usługi Azure Synapse Analytics Spark za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="96966-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="96966-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="96966-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="96966-117">To polecenie usuwa pulę usługi Azure Synapse Analytics Spark za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="96966-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="96966-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="96966-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="96966-119">To polecenie usuwa pulę usługi Azure Synapse Analytics Spark z IDENTYFIKATORem zasobu.</span><span class="sxs-lookup"><span data-stu-id="96966-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="96966-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="96966-120">PARAMETERS</span></span>

### <span data-ttu-id="96966-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96966-121">-AsJob</span></span>
<span data-ttu-id="96966-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="96966-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96966-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96966-123">-DefaultProfile</span></span>
<span data-ttu-id="96966-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="96966-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96966-125">-Force</span><span class="sxs-lookup"><span data-stu-id="96966-125">-Force</span></span>
<span data-ttu-id="96966-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="96966-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="96966-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="96966-127">-InputObject</span></span>
<span data-ttu-id="96966-128">Obiekt wejściowy usługi Spark Pool, zazwyczaj przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="96966-128">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="96966-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="96966-129">-Name</span></span>
<span data-ttu-id="96966-130">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="96966-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="96966-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96966-131">-PassThru</span></span>
<span data-ttu-id="96966-132">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="96966-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="96966-133">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="96966-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="96966-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96966-134">-ResourceGroupName</span></span>
<span data-ttu-id="96966-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="96966-135">Resource group name.</span></span>

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

### <span data-ttu-id="96966-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96966-136">-ResourceId</span></span>
<span data-ttu-id="96966-137">Identyfikator zasobu puli usługi Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="96966-137">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="96966-138">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="96966-138">-WorkspaceName</span></span>
<span data-ttu-id="96966-139">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="96966-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="96966-140">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="96966-140">-WorkspaceObject</span></span>
<span data-ttu-id="96966-141">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="96966-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="96966-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="96966-142">-Confirm</span></span>
<span data-ttu-id="96966-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96966-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96966-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96966-144">-WhatIf</span></span>
<span data-ttu-id="96966-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96966-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96966-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="96966-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96966-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96966-147">CommonParameters</span></span>
<span data-ttu-id="96966-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96966-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96966-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96966-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96966-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96966-150">INPUTS</span></span>

### <span data-ttu-id="96966-151">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="96966-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="96966-152">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="96966-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="96966-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="96966-153">OUTPUTS</span></span>

### <span data-ttu-id="96966-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96966-154">System.Boolean</span></span>

## <span data-ttu-id="96966-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="96966-155">NOTES</span></span>

## <span data-ttu-id="96966-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96966-156">RELATED LINKS</span></span>
