---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
ms.openlocfilehash: f5ed25a663f6f1841c4c2b6ca901d726a047eabd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963466"
---
# <span data-ttu-id="06f07-101">Remove-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="06f07-101">Remove-AzSynapseDataFlow</span></span>

## <span data-ttu-id="06f07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06f07-102">SYNOPSIS</span></span>
<span data-ttu-id="06f07-103">Usuwa przepływ danych z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="06f07-103">Removes a data flow from workspace.</span></span>

## <span data-ttu-id="06f07-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="06f07-104">SYNTAX</span></span>

### <span data-ttu-id="06f07-105">RemoveByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="06f07-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06f07-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="06f07-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06f07-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="06f07-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataFlow -InputObject <PSDataFlowResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06f07-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="06f07-108">DESCRIPTION</span></span>
<span data-ttu-id="06f07-109">Polecenie **cmdlet Remove-AzSynapseDataFlow** usuwa przepływ danych z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="06f07-109">The **Remove-AzSynapseDataFlow** cmdlet removes a data flow from workspace.</span></span>

## <span data-ttu-id="06f07-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="06f07-110">EXAMPLES</span></span>

### <span data-ttu-id="06f07-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="06f07-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="06f07-112">To polecenie usuwa przepływ danych o nazwie ContosoDataFlow z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="06f07-112">This command removes the data flow named ContosoDataFlow from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="06f07-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06f07-113">PARAMETERS</span></span>

### <span data-ttu-id="06f07-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="06f07-114">-AsJob</span></span>
<span data-ttu-id="06f07-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="06f07-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06f07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06f07-116">-DefaultProfile</span></span>
<span data-ttu-id="06f07-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="06f07-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06f07-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="06f07-118">-Force</span></span>
<span data-ttu-id="06f07-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="06f07-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="06f07-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06f07-120">-InputObject</span></span>
<span data-ttu-id="06f07-121">Obiekt przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="06f07-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06f07-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="06f07-122">-Name</span></span>
<span data-ttu-id="06f07-123">Nazwa przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="06f07-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06f07-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06f07-124">-PassThru</span></span>
<span data-ttu-id="06f07-125">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="06f07-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="06f07-126">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="06f07-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="06f07-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="06f07-127">-WorkspaceName</span></span>
<span data-ttu-id="06f07-128">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="06f07-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06f07-129">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="06f07-129">-WorkspaceObject</span></span>
<span data-ttu-id="06f07-130">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="06f07-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06f07-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06f07-131">-Confirm</span></span>
<span data-ttu-id="06f07-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="06f07-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06f07-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06f07-133">-WhatIf</span></span>
<span data-ttu-id="06f07-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06f07-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06f07-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="06f07-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06f07-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06f07-136">CommonParameters</span></span>
<span data-ttu-id="06f07-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06f07-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06f07-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06f07-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06f07-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06f07-139">INPUTS</span></span>

### <span data-ttu-id="06f07-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="06f07-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="06f07-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="06f07-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="06f07-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06f07-142">OUTPUTS</span></span>

### <span data-ttu-id="06f07-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="06f07-143">System.Boolean</span></span>

## <span data-ttu-id="06f07-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="06f07-144">NOTES</span></span>

## <span data-ttu-id="06f07-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06f07-145">RELATED LINKS</span></span>
