---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 48f2ea831470482a91e9ff78dc8b70472e2f556a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011162"
---
# <span data-ttu-id="7147e-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7147e-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="7147e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7147e-102">SYNOPSIS</span></span>
<span data-ttu-id="7147e-103">Aktualizuje regułę zapory analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="7147e-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="7147e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7147e-104">SYNTAX</span></span>

### <span data-ttu-id="7147e-105">UpdateByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7147e-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7147e-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7147e-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7147e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7147e-107">DESCRIPTION</span></span>
<span data-ttu-id="7147e-108">Polecenie **cmdlet Update-AzSynapseFirewallRule** modyfikuje regułę zapory analizy Synapse platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7147e-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="7147e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7147e-109">EXAMPLES</span></span>

### <span data-ttu-id="7147e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7147e-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="7147e-111">To polecenie aktualizuje regułę zapory o nazwie ContosoFirewallRule w obszarze roboczym ContosoWorkspace o nazwie ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="7147e-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="7147e-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7147e-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="7147e-113">To polecenie aktualizuje regułę zapory o nazwie ContosoFirewallRule w obszarze roboczym za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="7147e-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="7147e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7147e-114">PARAMETERS</span></span>

### <span data-ttu-id="7147e-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7147e-115">-AsJob</span></span>
<span data-ttu-id="7147e-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7147e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7147e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7147e-117">-DefaultProfile</span></span>
<span data-ttu-id="7147e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7147e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7147e-119">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="7147e-119">-EndIpAddress</span></span>
<span data-ttu-id="7147e-120">Końcowy adres IP reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="7147e-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="7147e-121">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="7147e-121">Must be IPv4 format.</span></span>
<span data-ttu-id="7147e-122">Musi być większy lub równy wartości startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="7147e-122">Must be greater than or equal to startIpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7147e-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7147e-123">-Name</span></span>
<span data-ttu-id="7147e-124">Nazwa reguły firerwall dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="7147e-124">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="7147e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7147e-125">-ResourceGroupName</span></span>
<span data-ttu-id="7147e-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7147e-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7147e-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="7147e-127">-StartIpAddress</span></span>
<span data-ttu-id="7147e-128">Pierwszy adres IP reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="7147e-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="7147e-129">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="7147e-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7147e-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7147e-130">-WorkspaceName</span></span>
<span data-ttu-id="7147e-131">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="7147e-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7147e-132">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7147e-132">-WorkspaceObject</span></span>
<span data-ttu-id="7147e-133">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="7147e-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7147e-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7147e-134">-Confirm</span></span>
<span data-ttu-id="7147e-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7147e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7147e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7147e-136">-WhatIf</span></span>
<span data-ttu-id="7147e-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7147e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7147e-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7147e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7147e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7147e-139">CommonParameters</span></span>
<span data-ttu-id="7147e-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7147e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7147e-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7147e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7147e-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7147e-142">INPUTS</span></span>

### <span data-ttu-id="7147e-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7147e-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7147e-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7147e-144">OUTPUTS</span></span>

### <span data-ttu-id="7147e-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7147e-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="7147e-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7147e-146">NOTES</span></span>

## <span data-ttu-id="7147e-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7147e-147">RELATED LINKS</span></span>
