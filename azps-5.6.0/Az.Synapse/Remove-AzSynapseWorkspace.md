---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: f8fc68c94142f9c215a6662e7bf41423c1b5de40
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993140"
---
# <span data-ttu-id="1e93f-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1e93f-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="1e93f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e93f-102">SYNOPSIS</span></span>
<span data-ttu-id="1e93f-103">Usuwa obszar roboczy analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="1e93f-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="1e93f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1e93f-104">SYNTAX</span></span>

### <span data-ttu-id="1e93f-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="1e93f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e93f-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e93f-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e93f-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e93f-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e93f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1e93f-108">DESCRIPTION</span></span>
<span data-ttu-id="1e93f-109">Polecenie **cmdlet Remove-AzSynapseWorkspace** trwale usuwa obszar roboczy usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1e93f-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="1e93f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1e93f-110">EXAMPLES</span></span>

### <span data-ttu-id="1e93f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1e93f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="1e93f-112">To polecenie powoduje usunięcie obszaru roboczego usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1e93f-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="1e93f-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1e93f-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="1e93f-114">To polecenie usuwa obszar roboczy usługi Azure Synapse Analytics w potoku.</span><span class="sxs-lookup"><span data-stu-id="1e93f-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="1e93f-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="1e93f-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="1e93f-116">To polecenie usuwa obszar roboczy usługi Azure Synapse Analytics za pośrednictwem potoku z określonym identyfikatorem zasobu.</span><span class="sxs-lookup"><span data-stu-id="1e93f-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="1e93f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e93f-117">PARAMETERS</span></span>

### <span data-ttu-id="1e93f-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1e93f-118">-AsJob</span></span>
<span data-ttu-id="1e93f-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1e93f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e93f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e93f-120">-DefaultProfile</span></span>
<span data-ttu-id="1e93f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e93f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e93f-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="1e93f-122">-Force</span></span>
<span data-ttu-id="1e93f-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1e93f-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1e93f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e93f-124">-InputObject</span></span>
<span data-ttu-id="1e93f-125">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="1e93f-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e93f-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1e93f-126">-Name</span></span>
<span data-ttu-id="1e93f-127">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="1e93f-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e93f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e93f-128">-PassThru</span></span>
<span data-ttu-id="1e93f-129">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="1e93f-129">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="1e93f-130">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="1e93f-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1e93f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e93f-131">-ResourceGroupName</span></span>
<span data-ttu-id="1e93f-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1e93f-132">Resource group name.</span></span>

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

### <span data-ttu-id="1e93f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e93f-133">-ResourceId</span></span>
<span data-ttu-id="1e93f-134">Identyfikator zasobu obszaru roboczego programu Synapse.</span><span class="sxs-lookup"><span data-stu-id="1e93f-134">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="1e93f-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1e93f-135">-Confirm</span></span>
<span data-ttu-id="1e93f-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1e93f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e93f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e93f-137">-WhatIf</span></span>
<span data-ttu-id="1e93f-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e93f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e93f-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1e93f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e93f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e93f-140">CommonParameters</span></span>
<span data-ttu-id="1e93f-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e93f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e93f-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e93f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e93f-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e93f-143">INPUTS</span></span>

### <span data-ttu-id="1e93f-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1e93f-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1e93f-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e93f-145">OUTPUTS</span></span>

### <span data-ttu-id="1e93f-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1e93f-146">System.Boolean</span></span>

## <span data-ttu-id="1e93f-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1e93f-147">NOTES</span></span>

## <span data-ttu-id="1e93f-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e93f-148">RELATED LINKS</span></span>
