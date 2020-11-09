---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317479"
---
# <span data-ttu-id="cc428-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cc428-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="cc428-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc428-102">SYNOPSIS</span></span>
<span data-ttu-id="cc428-103">Umożliwia utworzenie reguły zapory Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="cc428-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="cc428-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc428-104">SYNTAX</span></span>

### <span data-ttu-id="cc428-105">CreateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cc428-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc428-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc428-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc428-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc428-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc428-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc428-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc428-109">Opis</span><span class="sxs-lookup"><span data-stu-id="cc428-109">DESCRIPTION</span></span>
<span data-ttu-id="cc428-110">Polecenie cmdlet **New-AzSynapseFirewallRule** tworzy regułę zapory Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="cc428-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="cc428-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc428-111">EXAMPLES</span></span>

### <span data-ttu-id="cc428-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cc428-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="cc428-113">To polecenie tworzy regułę zapory o nazwie ContosoFirewallRule w obszarze roboczym ContosoWorkspace z nazwą ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="cc428-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="cc428-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cc428-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="cc428-115">To polecenie tworzy regułę zapory o nazwie ContosoFirewallRule w obszarze roboczym za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="cc428-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="cc428-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="cc428-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="cc428-117">To polecenie tworzy regułę zapory zezwalającą na wszystkie adresy IP usługi Azure w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="cc428-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="cc428-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc428-118">PARAMETERS</span></span>

### <span data-ttu-id="cc428-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="cc428-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="cc428-120">Umożliwia utworzenie specjalnej reguły zapory, która umożliwia dostęp do wszystkich adresów IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cc428-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

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

### <span data-ttu-id="cc428-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc428-121">-AsJob</span></span>
<span data-ttu-id="cc428-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cc428-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc428-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc428-123">-DefaultProfile</span></span>
<span data-ttu-id="cc428-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc428-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc428-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="cc428-125">-EndIpAddress</span></span>
<span data-ttu-id="cc428-126">Końcowy adres IP reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="cc428-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="cc428-127">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="cc428-127">Must be IPv4 format.</span></span>
<span data-ttu-id="cc428-128">Musi być większe lub równe startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="cc428-128">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="cc428-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cc428-129">-Name</span></span>
<span data-ttu-id="cc428-130">Nazwa reguły firerwall dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="cc428-130">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="cc428-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc428-131">-ResourceGroupName</span></span>
<span data-ttu-id="cc428-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc428-132">Resource group name.</span></span>

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

### <span data-ttu-id="cc428-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="cc428-133">-StartIpAddress</span></span>
<span data-ttu-id="cc428-134">Początkowy adres IP reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="cc428-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="cc428-135">Musi to być format IPv4.</span><span class="sxs-lookup"><span data-stu-id="cc428-135">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="cc428-136">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="cc428-136">-WorkspaceName</span></span>
<span data-ttu-id="cc428-137">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="cc428-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cc428-138">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="cc428-138">-WorkspaceObject</span></span>
<span data-ttu-id="cc428-139">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="cc428-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cc428-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cc428-140">-Confirm</span></span>
<span data-ttu-id="cc428-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc428-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc428-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc428-142">-WhatIf</span></span>
<span data-ttu-id="cc428-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc428-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc428-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cc428-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc428-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc428-145">CommonParameters</span></span>
<span data-ttu-id="cc428-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc428-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc428-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc428-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc428-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc428-148">INPUTS</span></span>

### <span data-ttu-id="cc428-149">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cc428-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cc428-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc428-150">OUTPUTS</span></span>

### <span data-ttu-id="cc428-151">Microsoft. Azure. Commands. Synapse. models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cc428-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="cc428-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc428-152">NOTES</span></span>

## <span data-ttu-id="cc428-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc428-153">RELATED LINKS</span></span>
