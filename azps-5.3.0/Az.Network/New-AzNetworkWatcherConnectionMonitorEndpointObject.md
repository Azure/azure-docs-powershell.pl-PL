---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 5a29c0bbad712d99b03ab1ff5347cba5c07b02aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385427"
---
# <span data-ttu-id="783f3-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="783f3-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="783f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="783f3-102">SYNOPSIS</span></span>
<span data-ttu-id="783f3-103">Tworzy punkt końcowy monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="783f3-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="783f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="783f3-104">SYNTAX</span></span>

### <span data-ttu-id="783f3-105">AzureVM</span><span class="sxs-lookup"><span data-stu-id="783f3-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="783f3-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="783f3-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="783f3-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="783f3-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="783f3-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="783f3-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="783f3-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="783f3-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="783f3-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="783f3-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="783f3-111">Opis</span><span class="sxs-lookup"><span data-stu-id="783f3-111">DESCRIPTION</span></span>
<span data-ttu-id="783f3-112">Polecenie cmdlet New-AzNetworkWatcherConnectionMonitorEndpointObject powoduje utworzenie punktu końcowego monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="783f3-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="783f3-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="783f3-113">EXAMPLES</span></span>

### <span data-ttu-id="783f3-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="783f3-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="783f3-115">Nazwa: workspaceEndpoint: MMAWorkspaceMachine ResourceId:/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace adres: zakres: {"include": [{"adres": "WIN-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="783f3-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="783f3-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="783f3-116">PARAMETERS</span></span>

### <span data-ttu-id="783f3-117">-Address (adres)</span><span class="sxs-lookup"><span data-stu-id="783f3-117">-Address</span></span>
<span data-ttu-id="783f3-118">Adres punktu końcowego monitora połączenia (adres IP lub nazwa domeny).</span><span class="sxs-lookup"><span data-stu-id="783f3-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

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

### <span data-ttu-id="783f3-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="783f3-119">-AzureSubnet</span></span>
<span data-ttu-id="783f3-120">Przełącznik punktu końcowego podsieci platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="783f3-120">Azure Subnet endpoint switch.</span></span>

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

### <span data-ttu-id="783f3-121">-AzureVM</span><span class="sxs-lookup"><span data-stu-id="783f3-121">-AzureVM</span></span>
<span data-ttu-id="783f3-122">Przełącznik punktu końcowego maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="783f3-122">Azure VM endpoint switch.</span></span>

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

### <span data-ttu-id="783f3-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="783f3-123">-AzureVNet</span></span>
<span data-ttu-id="783f3-124">Przełącznik punktu końcowego usługi Azure VNET.</span><span class="sxs-lookup"><span data-stu-id="783f3-124">Azure Vnet endpoint switch.</span></span>

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

### <span data-ttu-id="783f3-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="783f3-125">-CoverageLevel</span></span>
<span data-ttu-id="783f3-126">Testuj pokrycie dla punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="783f3-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="783f3-127">Obsługiwane są wartości domyślne, niskie, BelowAverage, średnia, AboveAvergae i pełne.</span><span class="sxs-lookup"><span data-stu-id="783f3-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

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

### <span data-ttu-id="783f3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="783f3-128">-DefaultProfile</span></span>
<span data-ttu-id="783f3-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="783f3-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="783f3-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="783f3-130">-ExcludeItem</span></span>
<span data-ttu-id="783f3-131">Lista elementów wymagających wykluczenia z zakresu punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="783f3-131">List of items which need to be excluded from endpoint scope.</span></span>

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

### <span data-ttu-id="783f3-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="783f3-132">-ExternalAddress</span></span>
<span data-ttu-id="783f3-133">Przełącznik punktu końcowego adresu zewnętrznego.</span><span class="sxs-lookup"><span data-stu-id="783f3-133">External Address endpoint switch.</span></span>

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

### <span data-ttu-id="783f3-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="783f3-134">-IncludeItem</span></span>
<span data-ttu-id="783f3-135">Lista elementów, które muszą zostać uwzględnione w zakresie ENDPONT.</span><span class="sxs-lookup"><span data-stu-id="783f3-135">List of items which need to be included into endpont scope.</span></span>

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

### <span data-ttu-id="783f3-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="783f3-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="783f3-137">Przełącznik punktu końcowego maszyny MMA w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="783f3-137">MMA Workspace Machine endpoint switch.</span></span>

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

### <span data-ttu-id="783f3-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="783f3-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="783f3-139">Przełącznik punktu końcowego sieci MMA w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="783f3-139">MMA Workspace Network endpoint switch.</span></span>

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

### <span data-ttu-id="783f3-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="783f3-140">-Name</span></span>
<span data-ttu-id="783f3-141">Nazwa punktu końcowego monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="783f3-141">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="783f3-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="783f3-142">-ResourceId</span></span>
<span data-ttu-id="783f3-143">Identyfikator zasobu punktu końcowego monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="783f3-143">Resource ID of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="783f3-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="783f3-144">-Confirm</span></span>
<span data-ttu-id="783f3-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="783f3-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="783f3-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="783f3-146">-WhatIf</span></span>
<span data-ttu-id="783f3-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="783f3-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="783f3-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="783f3-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="783f3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="783f3-149">CommonParameters</span></span>
<span data-ttu-id="783f3-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="783f3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="783f3-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="783f3-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="783f3-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="783f3-152">INPUTS</span></span>

### <span data-ttu-id="783f3-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="783f3-153">None</span></span>

## <span data-ttu-id="783f3-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="783f3-154">OUTPUTS</span></span>

### <span data-ttu-id="783f3-155">Microsoft. Azure. Commands. Network. models. PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="783f3-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="783f3-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="783f3-156">NOTES</span></span>

## <span data-ttu-id="783f3-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="783f3-157">RELATED LINKS</span></span>
