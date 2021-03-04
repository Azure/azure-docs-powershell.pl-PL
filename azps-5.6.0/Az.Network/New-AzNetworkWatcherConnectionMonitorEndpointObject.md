---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 385301bf9cab32474aea59937de09003356a5798
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958529"
---
# <span data-ttu-id="0e4fb-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="0e4fb-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="0e4fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e4fb-102">SYNOPSIS</span></span>
<span data-ttu-id="0e4fb-103">Tworzy punkt końcowy monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="0e4fb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0e4fb-104">SYNTAX</span></span>

### <span data-ttu-id="0e4fb-105">AzureVM</span><span class="sxs-lookup"><span data-stu-id="0e4fb-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e4fb-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="0e4fb-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e4fb-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="0e4fb-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e4fb-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="0e4fb-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e4fb-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="0e4fb-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e4fb-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="0e4fb-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e4fb-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="0e4fb-111">DESCRIPTION</span></span>
<span data-ttu-id="0e4fb-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet tworzy punkt końcowy monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="0e4fb-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0e4fb-113">EXAMPLES</span></span>

### <span data-ttu-id="0e4fb-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0e4fb-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="0e4fb-115">Nazwa: workspaceEndpoint Typ: MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-0000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address: Scope : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span><span class="sxs-lookup"><span data-stu-id="0e4fb-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="0e4fb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e4fb-116">PARAMETERS</span></span>

### <span data-ttu-id="0e4fb-117">— Adres</span><span class="sxs-lookup"><span data-stu-id="0e4fb-117">-Address</span></span>
<span data-ttu-id="0e4fb-118">Adres punktu końcowego monitora połączenia (adres IP lub nazwa domeny).</span><span class="sxs-lookup"><span data-stu-id="0e4fb-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExternalAddress, MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e4fb-119">- AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="0e4fb-119">-AzureSubnet</span></span>
<span data-ttu-id="0e4fb-120">Przełącznik punktu końcowego podsieci platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-120">Azure Subnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e4fb-121">— AzureVM</span><span class="sxs-lookup"><span data-stu-id="0e4fb-121">-AzureVM</span></span>
<span data-ttu-id="0e4fb-122">Przełącznik punktu końcowego maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-122">Azure VM endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e4fb-123">— AzureVNet</span><span class="sxs-lookup"><span data-stu-id="0e4fb-123">-AzureVNet</span></span>
<span data-ttu-id="0e4fb-124">Przełącznik punktu końcowego sieci Vnet platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-124">Azure Vnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVNet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e4fb-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="0e4fb-125">-CoverageLevel</span></span>
<span data-ttu-id="0e4fb-126">Zakres testów dla punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="0e4fb-127">Obsługiwane wartości to Domyślne, Niskie, Średnia, Średnia, NadAvergae, Pełne.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e4fb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e4fb-128">-DefaultProfile</span></span>
<span data-ttu-id="0e4fb-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e4fb-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="0e4fb-130">-ExcludeItem</span></span>
<span data-ttu-id="0e4fb-131">Lista elementów, które należy wykluczyć z zakresu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-131">List of items which need to be excluded from endpoint scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e4fb-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="0e4fb-132">-ExternalAddress</span></span>
<span data-ttu-id="0e4fb-133">Przełącznik punktu końcowego adresu zewnętrznego.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-133">External Address endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExternalAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e4fb-134">- IncludeItem</span><span class="sxs-lookup"><span data-stu-id="0e4fb-134">-IncludeItem</span></span>
<span data-ttu-id="0e4fb-135">Lista elementów, które należy ujmować w zakres końcowejponty.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-135">List of items which need to be included into endpont scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, MMAWorkspaceMachine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e4fb-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="0e4fb-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="0e4fb-137">Przełącznik punktu końcowego programu MMA Workspace Machine.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-137">MMA Workspace Machine endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e4fb-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="0e4fb-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="0e4fb-139">Przełącznik punktu końcowego sieci obszarów roboczych programu MMA.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-139">MMA Workspace Network endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e4fb-140">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0e4fb-140">-Name</span></span>
<span data-ttu-id="0e4fb-141">Nazwa punktu końcowego monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-141">The name of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e4fb-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e4fb-142">-ResourceId</span></span>
<span data-ttu-id="0e4fb-143">Identyfikator zasobu punktu końcowego monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-143">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM, AzureVNet, AzureSubnet, MMAWorkspaceMachine, MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e4fb-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e4fb-144">-Confirm</span></span>
<span data-ttu-id="0e4fb-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e4fb-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e4fb-146">-WhatIf</span></span>
<span data-ttu-id="0e4fb-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e4fb-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e4fb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e4fb-149">CommonParameters</span></span>
<span data-ttu-id="0e4fb-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e4fb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e4fb-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e4fb-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e4fb-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e4fb-152">INPUTS</span></span>

### <span data-ttu-id="0e4fb-153">Brak</span><span class="sxs-lookup"><span data-stu-id="0e4fb-153">None</span></span>

## <span data-ttu-id="0e4fb-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e4fb-154">OUTPUTS</span></span>

### <span data-ttu-id="0e4fb-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="0e4fb-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="0e4fb-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0e4fb-156">NOTES</span></span>

## <span data-ttu-id="0e4fb-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e4fb-157">RELATED LINKS</span></span>
