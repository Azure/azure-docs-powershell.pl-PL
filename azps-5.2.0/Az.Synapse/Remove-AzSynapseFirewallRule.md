---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 8dd3321804afb2f7901a8acd22cfdab3dd990c41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369210"
---
# <span data-ttu-id="452bd-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="452bd-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="452bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="452bd-102">SYNOPSIS</span></span>
<span data-ttu-id="452bd-103">Usuwa regułę zapory Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="452bd-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="452bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="452bd-104">SYNTAX</span></span>

### <span data-ttu-id="452bd-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="452bd-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="452bd-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="452bd-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="452bd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="452bd-107">DESCRIPTION</span></span>
<span data-ttu-id="452bd-108">Polecenie cmdlet **Remove-AzSynapseFirewallRule** powoduje trwałe usunięcie reguły zapory usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="452bd-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="452bd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="452bd-109">EXAMPLES</span></span>

### <span data-ttu-id="452bd-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="452bd-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="452bd-111">To polecenie usuwa regułę zapory o nazwie ContosoFirewallRule w obszarze roboczym ContosoWorkspace z nazwą ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="452bd-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="452bd-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="452bd-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="452bd-113">To polecenie usuwa regułę zapory o nazwie ContosoFirewallRule w obszarze roboczym za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="452bd-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="452bd-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="452bd-114">PARAMETERS</span></span>

### <span data-ttu-id="452bd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="452bd-115">-AsJob</span></span>
<span data-ttu-id="452bd-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="452bd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="452bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="452bd-117">-DefaultProfile</span></span>
<span data-ttu-id="452bd-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="452bd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="452bd-119">-Force</span><span class="sxs-lookup"><span data-stu-id="452bd-119">-Force</span></span>
<span data-ttu-id="452bd-120">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="452bd-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="452bd-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="452bd-121">-Name</span></span>
<span data-ttu-id="452bd-122">Nazwa reguły firerwall dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="452bd-122">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="452bd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="452bd-123">-PassThru</span></span>
<span data-ttu-id="452bd-124">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="452bd-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="452bd-125">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="452bd-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="452bd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="452bd-126">-ResourceGroupName</span></span>
<span data-ttu-id="452bd-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="452bd-127">Resource group name.</span></span>

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

### <span data-ttu-id="452bd-128">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="452bd-128">-WorkspaceName</span></span>
<span data-ttu-id="452bd-129">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="452bd-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="452bd-130">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="452bd-130">-WorkspaceObject</span></span>
<span data-ttu-id="452bd-131">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="452bd-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="452bd-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="452bd-132">-Confirm</span></span>
<span data-ttu-id="452bd-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="452bd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="452bd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="452bd-134">-WhatIf</span></span>
<span data-ttu-id="452bd-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="452bd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="452bd-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="452bd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="452bd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="452bd-137">CommonParameters</span></span>
<span data-ttu-id="452bd-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="452bd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="452bd-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="452bd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="452bd-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="452bd-140">INPUTS</span></span>

### <span data-ttu-id="452bd-141">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="452bd-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="452bd-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="452bd-142">OUTPUTS</span></span>

### <span data-ttu-id="452bd-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="452bd-143">System.Boolean</span></span>

## <span data-ttu-id="452bd-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="452bd-144">NOTES</span></span>

## <span data-ttu-id="452bd-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="452bd-145">RELATED LINKS</span></span>
