---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197339"
---
# <span data-ttu-id="e6215-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e6215-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="e6215-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6215-102">SYNOPSIS</span></span>
<span data-ttu-id="e6215-103">Tworzy regułę zapory analizy synapse.</span><span class="sxs-lookup"><span data-stu-id="e6215-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="e6215-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e6215-104">SYNTAX</span></span>

### <span data-ttu-id="e6215-105">CreateByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e6215-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6215-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6215-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6215-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6215-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6215-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6215-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6215-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="e6215-109">DESCRIPTION</span></span>
<span data-ttu-id="e6215-110">Polecenie **cmdlet New-AzSynapseFirewallRule** tworzy regułę zapory analizy Synapse platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e6215-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="e6215-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e6215-111">EXAMPLES</span></span>

### <span data-ttu-id="e6215-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e6215-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="e6215-113">To polecenie tworzy regułę zapory o nazwie ContosoFirewallRule w obszarze obszaru roboczego ContosoWorkspace o nazwie ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="e6215-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="e6215-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e6215-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="e6215-115">To polecenie tworzy regułę zapory o nazwie ContosoFirewallRule w obszarze roboczym za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="e6215-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="e6215-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e6215-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="e6215-117">To polecenie tworzy regułę zapory, która zezwala na wszystkie adresy IP platformy Azure w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="e6215-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="e6215-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6215-118">PARAMETERS</span></span>

### <span data-ttu-id="e6215-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="e6215-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="e6215-120">Tworzy specjalną regułę zapory, która zezwala wszystkim ip platformy Azure na uzyskiwanie dostępu.</span><span class="sxs-lookup"><span data-stu-id="e6215-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

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

### <span data-ttu-id="e6215-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e6215-121">-AsJob</span></span>
<span data-ttu-id="e6215-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e6215-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6215-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6215-123">-DefaultProfile</span></span>
<span data-ttu-id="e6215-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6215-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6215-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="e6215-125">-EndIpAddress</span></span>
<span data-ttu-id="e6215-126">Końcowy adres IP reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="e6215-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="e6215-127">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="e6215-127">Must be IPv4 format.</span></span>
<span data-ttu-id="e6215-128">Musi być większy lub równy wartości startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="e6215-128">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="e6215-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e6215-129">-Name</span></span>
<span data-ttu-id="e6215-130">Nazwa reguły firerwall dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="e6215-130">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="e6215-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6215-131">-ResourceGroupName</span></span>
<span data-ttu-id="e6215-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e6215-132">Resource group name.</span></span>

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

### <span data-ttu-id="e6215-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="e6215-133">-StartIpAddress</span></span>
<span data-ttu-id="e6215-134">Adres IP początku reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="e6215-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="e6215-135">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="e6215-135">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="e6215-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e6215-136">-WorkspaceName</span></span>
<span data-ttu-id="e6215-137">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="e6215-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e6215-138">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e6215-138">-WorkspaceObject</span></span>
<span data-ttu-id="e6215-139">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="e6215-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e6215-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e6215-140">-Confirm</span></span>
<span data-ttu-id="e6215-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e6215-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6215-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6215-142">-WhatIf</span></span>
<span data-ttu-id="e6215-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6215-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6215-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e6215-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6215-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6215-145">CommonParameters</span></span>
<span data-ttu-id="e6215-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6215-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6215-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6215-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6215-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6215-148">INPUTS</span></span>

### <span data-ttu-id="e6215-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e6215-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e6215-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e6215-150">OUTPUTS</span></span>

### <span data-ttu-id="e6215-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e6215-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="e6215-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e6215-152">NOTES</span></span>

## <span data-ttu-id="e6215-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6215-153">RELATED LINKS</span></span>
