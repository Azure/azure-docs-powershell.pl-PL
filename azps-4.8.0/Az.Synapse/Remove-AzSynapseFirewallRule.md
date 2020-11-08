---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 6094c8d7e75136c9a9abf220ccfcb8775bda5dd7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064384"
---
# <span data-ttu-id="8c68d-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8c68d-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="8c68d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c68d-102">SYNOPSIS</span></span>
<span data-ttu-id="8c68d-103">Usuwa regułę zapory Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8c68d-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="8c68d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c68d-104">SYNTAX</span></span>

### <span data-ttu-id="8c68d-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8c68d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c68d-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c68d-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c68d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8c68d-107">DESCRIPTION</span></span>
<span data-ttu-id="8c68d-108">Polecenie cmdlet **Remove-AzSynapseFirewallRule** powoduje trwałe usunięcie reguły zapory usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8c68d-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="8c68d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c68d-109">EXAMPLES</span></span>

### <span data-ttu-id="8c68d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8c68d-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="8c68d-111">To polecenie usuwa regułę zapory o nazwie ContosoFirewallRule w obszarze roboczym ContosoWorkspace z nazwą ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="8c68d-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="8c68d-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8c68d-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="8c68d-113">To polecenie usuwa regułę zapory o nazwie ContosoFirewallRule w obszarze roboczym za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="8c68d-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="8c68d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c68d-114">PARAMETERS</span></span>

### <span data-ttu-id="8c68d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c68d-115">-AsJob</span></span>
<span data-ttu-id="8c68d-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8c68d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c68d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c68d-117">-DefaultProfile</span></span>
<span data-ttu-id="8c68d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c68d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c68d-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8c68d-119">-Name</span></span>
<span data-ttu-id="8c68d-120">Nazwa reguły firerwall dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="8c68d-120">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="8c68d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c68d-121">-PassThru</span></span>
<span data-ttu-id="8c68d-122">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="8c68d-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8c68d-123">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="8c68d-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8c68d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c68d-124">-ResourceGroupName</span></span>
<span data-ttu-id="8c68d-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c68d-125">Resource group name.</span></span>

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

### <span data-ttu-id="8c68d-126">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="8c68d-126">-WorkspaceName</span></span>
<span data-ttu-id="8c68d-127">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="8c68d-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8c68d-128">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="8c68d-128">-WorkspaceObject</span></span>
<span data-ttu-id="8c68d-129">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="8c68d-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8c68d-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c68d-130">-Confirm</span></span>
<span data-ttu-id="8c68d-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c68d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c68d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c68d-132">-WhatIf</span></span>
<span data-ttu-id="8c68d-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c68d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c68d-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8c68d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c68d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c68d-135">CommonParameters</span></span>
<span data-ttu-id="8c68d-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c68d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c68d-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c68d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c68d-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c68d-138">INPUTS</span></span>

### <span data-ttu-id="8c68d-139">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8c68d-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8c68d-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c68d-140">OUTPUTS</span></span>

### <span data-ttu-id="8c68d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8c68d-141">System.Boolean</span></span>

## <span data-ttu-id="8c68d-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c68d-142">NOTES</span></span>

## <span data-ttu-id="8c68d-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c68d-143">RELATED LINKS</span></span>
