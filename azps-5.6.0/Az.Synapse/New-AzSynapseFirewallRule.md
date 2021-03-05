---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: e630bdba87f345229ffe18e4cf2011f82f78dc73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976090"
---
# <span data-ttu-id="10f4e-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="10f4e-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="10f4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10f4e-102">SYNOPSIS</span></span>
<span data-ttu-id="10f4e-103">Tworzy regułę zapory analizy synapse.</span><span class="sxs-lookup"><span data-stu-id="10f4e-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="10f4e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10f4e-104">SYNTAX</span></span>

### <span data-ttu-id="10f4e-105">CreateByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="10f4e-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10f4e-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="10f4e-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10f4e-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10f4e-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10f4e-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="10f4e-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10f4e-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="10f4e-109">DESCRIPTION</span></span>
<span data-ttu-id="10f4e-110">Polecenie **cmdlet New-AzSynapseFirewallRule** tworzy regułę zapory analizy Synapse platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="10f4e-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="10f4e-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10f4e-111">EXAMPLES</span></span>

### <span data-ttu-id="10f4e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="10f4e-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="10f4e-113">To polecenie tworzy regułę zapory o nazwie ContosoFirewallRule w obszarze obszaru roboczego ContosoWorkspace o nazwie ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="10f4e-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="10f4e-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="10f4e-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="10f4e-115">To polecenie tworzy regułę zapory o nazwie ContosoFirewallRule w obszarze roboczym za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="10f4e-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="10f4e-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="10f4e-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="10f4e-117">To polecenie tworzy regułę zapory, która zezwala na wszystkie adresy IP platformy Azure w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="10f4e-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="10f4e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10f4e-118">PARAMETERS</span></span>

### <span data-ttu-id="10f4e-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="10f4e-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="10f4e-120">Tworzy specjalną regułę zapory, która zezwala wszystkim ip platformy Azure na uzyskiwanie dostępu.</span><span class="sxs-lookup"><span data-stu-id="10f4e-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateByNameAllowAllIpParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10f4e-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="10f4e-121">-AsJob</span></span>
<span data-ttu-id="10f4e-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="10f4e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10f4e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10f4e-123">-DefaultProfile</span></span>
<span data-ttu-id="10f4e-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="10f4e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10f4e-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="10f4e-125">-EndIpAddress</span></span>
<span data-ttu-id="10f4e-126">Końcowy adres IP reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="10f4e-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="10f4e-127">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="10f4e-127">Must be IPv4 format.</span></span>
<span data-ttu-id="10f4e-128">Musi być większy lub równy wartości startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="10f4e-128">Must be greater than or equal to startIpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10f4e-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="10f4e-129">-Name</span></span>
<span data-ttu-id="10f4e-130">Nazwa reguły firerwall dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="10f4e-130">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10f4e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10f4e-131">-ResourceGroupName</span></span>
<span data-ttu-id="10f4e-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10f4e-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10f4e-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="10f4e-133">-StartIpAddress</span></span>
<span data-ttu-id="10f4e-134">Pierwszy adres IP reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="10f4e-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="10f4e-135">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="10f4e-135">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10f4e-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="10f4e-136">-WorkspaceName</span></span>
<span data-ttu-id="10f4e-137">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="10f4e-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10f4e-138">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="10f4e-138">-WorkspaceObject</span></span>
<span data-ttu-id="10f4e-139">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="10f4e-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10f4e-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10f4e-140">-Confirm</span></span>
<span data-ttu-id="10f4e-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="10f4e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10f4e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10f4e-142">-WhatIf</span></span>
<span data-ttu-id="10f4e-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10f4e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10f4e-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="10f4e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10f4e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10f4e-145">CommonParameters</span></span>
<span data-ttu-id="10f4e-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10f4e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10f4e-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10f4e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10f4e-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10f4e-148">INPUTS</span></span>

### <span data-ttu-id="10f4e-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="10f4e-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="10f4e-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10f4e-150">OUTPUTS</span></span>

### <span data-ttu-id="10f4e-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="10f4e-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="10f4e-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10f4e-152">NOTES</span></span>

## <span data-ttu-id="10f4e-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10f4e-153">RELATED LINKS</span></span>
