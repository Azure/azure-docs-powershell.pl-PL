---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 18db8d01bd9c6c54b1fdf3957f25e12848e309ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958538"
---
# <span data-ttu-id="9d7fe-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9d7fe-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="9d7fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d7fe-102">SYNOPSIS</span></span>
<span data-ttu-id="9d7fe-103">Tworzy zasób monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="9d7fe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9d7fe-104">SYNTAX</span></span>

### <span data-ttu-id="9d7fe-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="9d7fe-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d7fe-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9d7fe-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d7fe-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="9d7fe-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d7fe-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="9d7fe-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d7fe-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9d7fe-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d7fe-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="9d7fe-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d7fe-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="9d7fe-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d7fe-112">OPIS</span><span class="sxs-lookup"><span data-stu-id="9d7fe-112">DESCRIPTION</span></span>
<span data-ttu-id="9d7fe-113">Polecenie New-AzNetworkWatcherConnectionMonitor cmdlet tworzy zasób monitora połączenia dla określonego źródła i miejsca docelowego (monitor połączenia SingleSourcedestination) lub zestaw grup testowych (MultiEndpointConnectionMonitor).</span><span class="sxs-lookup"><span data-stu-id="9d7fe-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="9d7fe-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9d7fe-114">EXAMPLES</span></span>

### <span data-ttu-id="9d7fe-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9d7fe-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="9d7fe-116">Nazwa: cm Id : /subscriptions/00000000-0000-0000-00000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag : W/"e86b28cf-b907-14475-a8b7-34d310367694" ProvisioningState: Succeeded Source: { "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft. Compute/virtualMachines/virtualMachines/virtualMachines", "Port": 0 } Miejsce docelowe: { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds: 60 AutoStart: True StartTime: 2018-01-12 7:13:11 PM MonitoringStatus: Bieżąca lokalizacja: centraluseuap Typ: Microsoft.Network/networkWatchers/connectionMonitors Tags: {}</span><span class="sxs-lookup"><span data-stu-id="9d7fe-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="9d7fe-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d7fe-117">PARAMETERS</span></span>

### <span data-ttu-id="9d7fe-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9d7fe-118">-AsJob</span></span>
<span data-ttu-id="9d7fe-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9d7fe-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d7fe-120">- ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="9d7fe-120">-ConfigureOnly</span></span>
<span data-ttu-id="9d7fe-121">Konfigurowanie monitora połączenia, ale nie jego uruchamianie</span><span class="sxs-lookup"><span data-stu-id="9d7fe-121">Configure connection monitor, but do not start it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7fe-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9d7fe-122">-ConnectionMonitor</span></span>
<span data-ttu-id="9d7fe-123">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-123">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject
Parameter Sets: SetByConnectionMonitorV2Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7fe-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d7fe-124">-DefaultProfile</span></span>
<span data-ttu-id="9d7fe-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d7fe-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="9d7fe-126">-DestinationAddress</span></span>
<span data-ttu-id="9d7fe-127">Adres miejsca docelowego monitora połączenia (adres IP lub nazwa domeny).</span><span class="sxs-lookup"><span data-stu-id="9d7fe-127">Address of the connection monitor destination (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7fe-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="9d7fe-128">-DestinationPort</span></span>
<span data-ttu-id="9d7fe-129">Port docelowy używany przez monitor połączenia.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-129">The destination port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7fe-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="9d7fe-130">-DestinationResourceId</span></span>
<span data-ttu-id="9d7fe-131">Identyfikator zasobu używanego jako miejsce docelowe przez monitor połączenia.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-131">The ID of the resource used as the destination by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7fe-132">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9d7fe-132">-Force</span></span>
<span data-ttu-id="9d7fe-133">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="9d7fe-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9d7fe-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9d7fe-134">-Location</span></span>
<span data-ttu-id="9d7fe-135">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-135">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation, SetByLocationV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7fe-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9d7fe-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="9d7fe-137">Monitorowanie interwału w sekundach.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="9d7fe-138">Wartość domyślna to 60 sekund.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-138">Default value is 60 seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7fe-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9d7fe-139">-Name</span></span>
<span data-ttu-id="9d7fe-140">Nazwa monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-140">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7fe-141">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9d7fe-141">-NetworkWatcher</span></span>
<span data-ttu-id="9d7fe-142">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-142">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7fe-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9d7fe-143">-NetworkWatcherName</span></span>
<span data-ttu-id="9d7fe-144">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-144">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7fe-145">— Uwaga</span><span class="sxs-lookup"><span data-stu-id="9d7fe-145">-Note</span></span>
<span data-ttu-id="9d7fe-146">Uwagi skojarzone z monitorem połączenia.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-146">Notes associated with connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7fe-147">— Dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="9d7fe-147">-Output</span></span>
<span data-ttu-id="9d7fe-148">W tym artykule opisano miejsca docelowe wyjściowe monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-148">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7fe-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d7fe-149">-ResourceGroupName</span></span>
<span data-ttu-id="9d7fe-150">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-150">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7fe-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="9d7fe-151">-SourcePort</span></span>
<span data-ttu-id="9d7fe-152">Port źródłowy używany przez monitor połączenia.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-152">The source port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7fe-153">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="9d7fe-153">-SourceResourceId</span></span>
<span data-ttu-id="9d7fe-154">Identyfikator zasobu używanego jako źródło za pomocą monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-154">The ID of the resource used as the source by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7fe-155">— Tag</span><span class="sxs-lookup"><span data-stu-id="9d7fe-155">-Tag</span></span>
<span data-ttu-id="9d7fe-156">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-156">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7fe-157">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="9d7fe-157">-TestGroup</span></span>
<span data-ttu-id="9d7fe-158">Lista grup testowych.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-158">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7fe-159">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d7fe-159">-Confirm</span></span>
<span data-ttu-id="9d7fe-160">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d7fe-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d7fe-161">-WhatIf</span></span>
<span data-ttu-id="9d7fe-162">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d7fe-163">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d7fe-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d7fe-164">CommonParameters</span></span>
<span data-ttu-id="9d7fe-165">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d7fe-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d7fe-166">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d7fe-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d7fe-167">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d7fe-167">INPUTS</span></span>

### <span data-ttu-id="9d7fe-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9d7fe-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="9d7fe-169">System.String</span><span class="sxs-lookup"><span data-stu-id="9d7fe-169">System.String</span></span>

### <span data-ttu-id="9d7fe-170">System.Collections.generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlet.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="9d7fe-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9d7fe-171">System.Collections.generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlet.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="9d7fe-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9d7fe-172">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d7fe-172">OUTPUTS</span></span>

### <span data-ttu-id="9d7fe-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="9d7fe-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="9d7fe-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="9d7fe-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="9d7fe-175">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9d7fe-175">NOTES</span></span>

## <span data-ttu-id="9d7fe-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d7fe-176">RELATED LINKS</span></span>
