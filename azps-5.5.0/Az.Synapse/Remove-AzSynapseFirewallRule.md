---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 8dd3321804afb2f7901a8acd22cfdab3dd990c41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198362"
---
# <span data-ttu-id="ab397-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ab397-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="ab397-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab397-102">SYNOPSIS</span></span>
<span data-ttu-id="ab397-103">Usuwa regułę zapory analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="ab397-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="ab397-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ab397-104">SYNTAX</span></span>

### <span data-ttu-id="ab397-105">DeleteByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ab397-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab397-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab397-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab397-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ab397-107">DESCRIPTION</span></span>
<span data-ttu-id="ab397-108">Polecenie **cmdlet Remove-AzSynapseFirewallRule** trwale usuwa regułę zapory usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ab397-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="ab397-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ab397-109">EXAMPLES</span></span>

### <span data-ttu-id="ab397-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ab397-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="ab397-111">To polecenie usuwa regułę zapory o nazwie ContosoFirewallRule w obszarze obszaru roboczego ContosoWorkspace o nazwie ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="ab397-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="ab397-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ab397-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="ab397-113">To polecenie usuwa regułę zapory o nazwie ContosoFirewallRule w obszarze roboczym z potoku.</span><span class="sxs-lookup"><span data-stu-id="ab397-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="ab397-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab397-114">PARAMETERS</span></span>

### <span data-ttu-id="ab397-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ab397-115">-AsJob</span></span>
<span data-ttu-id="ab397-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ab397-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab397-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab397-117">-DefaultProfile</span></span>
<span data-ttu-id="ab397-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab397-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab397-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ab397-119">-Force</span></span>
<span data-ttu-id="ab397-120">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ab397-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ab397-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ab397-121">-Name</span></span>
<span data-ttu-id="ab397-122">Nazwa reguły firerwall dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="ab397-122">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab397-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab397-123">-PassThru</span></span>
<span data-ttu-id="ab397-124">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="ab397-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ab397-125">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="ab397-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ab397-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab397-126">-ResourceGroupName</span></span>
<span data-ttu-id="ab397-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ab397-127">Resource group name.</span></span>

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

### <span data-ttu-id="ab397-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ab397-128">-WorkspaceName</span></span>
<span data-ttu-id="ab397-129">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="ab397-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ab397-130">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ab397-130">-WorkspaceObject</span></span>
<span data-ttu-id="ab397-131">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="ab397-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ab397-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab397-132">-Confirm</span></span>
<span data-ttu-id="ab397-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ab397-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab397-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab397-134">-WhatIf</span></span>
<span data-ttu-id="ab397-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab397-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab397-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ab397-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab397-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab397-137">CommonParameters</span></span>
<span data-ttu-id="ab397-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab397-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab397-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab397-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab397-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab397-140">INPUTS</span></span>

### <span data-ttu-id="ab397-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ab397-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ab397-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab397-142">OUTPUTS</span></span>

### <span data-ttu-id="ab397-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ab397-143">System.Boolean</span></span>

## <span data-ttu-id="ab397-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ab397-144">NOTES</span></span>

## <span data-ttu-id="ab397-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab397-145">RELATED LINKS</span></span>
