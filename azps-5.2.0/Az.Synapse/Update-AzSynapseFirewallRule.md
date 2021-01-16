---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 9188a1cc8dde39db4d755fb2059f3633fc85ead8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334333"
---
# <span data-ttu-id="13842-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="13842-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="13842-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13842-102">SYNOPSIS</span></span>
<span data-ttu-id="13842-103">Umożliwia zaktualizowanie reguły zapory Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="13842-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="13842-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13842-104">SYNTAX</span></span>

### <span data-ttu-id="13842-105">UpdateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="13842-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13842-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13842-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13842-107">Opis</span><span class="sxs-lookup"><span data-stu-id="13842-107">DESCRIPTION</span></span>
<span data-ttu-id="13842-108">Polecenie cmdlet **Update-AzSynapseFirewallRule** modyfikuje regułę zapory Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="13842-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="13842-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13842-109">EXAMPLES</span></span>

### <span data-ttu-id="13842-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13842-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="13842-111">To polecenie aktualizuje regułę zapory o nazwie ContosoFirewallRule w obszarze roboczym ContosoWorkspace z nazwą ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="13842-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="13842-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="13842-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="13842-113">To polecenie aktualizuje regułę zapory o nazwie ContosoFirewallRule w obszarze roboczym za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="13842-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="13842-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13842-114">PARAMETERS</span></span>

### <span data-ttu-id="13842-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13842-115">-AsJob</span></span>
<span data-ttu-id="13842-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="13842-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13842-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13842-117">-DefaultProfile</span></span>
<span data-ttu-id="13842-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13842-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13842-119">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="13842-119">-EndIpAddress</span></span>
<span data-ttu-id="13842-120">Końcowy adres IP reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="13842-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="13842-121">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="13842-121">Must be IPv4 format.</span></span>
<span data-ttu-id="13842-122">Musi być większe lub równe startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="13842-122">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="13842-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13842-123">-Name</span></span>
<span data-ttu-id="13842-124">Nazwa reguły firerwall dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="13842-124">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="13842-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13842-125">-ResourceGroupName</span></span>
<span data-ttu-id="13842-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="13842-126">Resource group name.</span></span>

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

### <span data-ttu-id="13842-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="13842-127">-StartIpAddress</span></span>
<span data-ttu-id="13842-128">Początkowy adres IP reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="13842-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="13842-129">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="13842-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="13842-130">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="13842-130">-WorkspaceName</span></span>
<span data-ttu-id="13842-131">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="13842-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="13842-132">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="13842-132">-WorkspaceObject</span></span>
<span data-ttu-id="13842-133">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="13842-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="13842-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13842-134">-Confirm</span></span>
<span data-ttu-id="13842-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13842-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13842-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13842-136">-WhatIf</span></span>
<span data-ttu-id="13842-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13842-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13842-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13842-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13842-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13842-139">CommonParameters</span></span>
<span data-ttu-id="13842-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13842-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13842-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13842-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13842-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13842-142">INPUTS</span></span>

### <span data-ttu-id="13842-143">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="13842-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="13842-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13842-144">OUTPUTS</span></span>

### <span data-ttu-id="13842-145">Microsoft. Azure. Commands. Synapse. models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="13842-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="13842-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13842-146">NOTES</span></span>

## <span data-ttu-id="13842-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13842-147">RELATED LINKS</span></span>
