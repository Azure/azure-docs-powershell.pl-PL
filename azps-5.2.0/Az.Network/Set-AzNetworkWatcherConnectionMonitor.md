---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344182"
---
# <span data-ttu-id="d2270-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d2270-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="d2270-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2270-102">SYNOPSIS</span></span>
<span data-ttu-id="d2270-103">Aktualizuje zasób monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="d2270-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="d2270-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2270-104">SYNTAX</span></span>

### <span data-ttu-id="d2270-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d2270-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2270-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d2270-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2270-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="d2270-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2270-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="d2270-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2270-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d2270-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2270-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="d2270-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2270-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d2270-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2270-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="d2270-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2270-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="d2270-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2270-114">Opis</span><span class="sxs-lookup"><span data-stu-id="d2270-114">DESCRIPTION</span></span>
<span data-ttu-id="d2270-115">Polecenie Set-AzNetworkWatcherConnectionMonitor polecenia cmdlet aktualizuje zasób monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="d2270-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="d2270-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2270-116">EXAMPLES</span></span>

### <span data-ttu-id="d2270-117">Przykład 1: aktualizowanie monitora połączeń</span><span class="sxs-lookup"><span data-stu-id="d2270-117">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm
-DestinationAddress google.com -DestinationPort 80 -Tag @{"key1" = "value1"}

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"5b2b20e8-0ce0-417e-9607-76208149bb67"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMach
                                ines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="d2270-118">W tym przykładzie Zaktualizowano istniejący monitor połączenia, zmieniając destinationAddress i dodając Tagi.</span><span class="sxs-lookup"><span data-stu-id="d2270-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="d2270-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2270-119">PARAMETERS</span></span>

### <span data-ttu-id="d2270-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2270-120">-AsJob</span></span>
<span data-ttu-id="d2270-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d2270-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2270-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="d2270-122">-ConfigureOnly</span></span>
<span data-ttu-id="d2270-123">Konfigurowanie monitora połączeń, ale nie Rozpoczynanie go</span><span class="sxs-lookup"><span data-stu-id="d2270-123">Configure connection monitor, but do not start it</span></span>

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

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2270-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2270-124">-DefaultProfile</span></span>
<span data-ttu-id="d2270-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2270-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2270-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="d2270-126">-DestinationAddress</span></span>
<span data-ttu-id="d2270-127">Adres lokalizacji docelowej monitora połączeń (adres IP lub nazwa domeny).</span><span class="sxs-lookup"><span data-stu-id="d2270-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2270-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="d2270-128">-DestinationPort</span></span>
<span data-ttu-id="d2270-129">Port docelowy wykorzystywany przez Monitor połączeń.</span><span class="sxs-lookup"><span data-stu-id="d2270-129">The destination port used by connection monitor.</span></span>

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

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2270-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="d2270-130">-DestinationResourceId</span></span>
<span data-ttu-id="d2270-131">Identyfikator zasobu, który jest wykorzystywany jako miejsce docelowe przez Monitor połączenia.</span><span class="sxs-lookup"><span data-stu-id="d2270-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2270-132">-Force</span><span class="sxs-lookup"><span data-stu-id="d2270-132">-Force</span></span>
<span data-ttu-id="d2270-133">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="d2270-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d2270-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d2270-134">-InputObject</span></span>
<span data-ttu-id="d2270-135">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="d2270-135">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2270-136">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d2270-136">-Location</span></span>
<span data-ttu-id="d2270-137">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d2270-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d2270-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d2270-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="d2270-139">Interwał monitorowania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="d2270-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="d2270-140">Wartość domyślna to 60 sekund.</span><span class="sxs-lookup"><span data-stu-id="d2270-140">Default value is 60 seconds.</span></span>

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

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2270-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d2270-141">-Name</span></span>
<span data-ttu-id="d2270-142">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="d2270-142">The connection monitor name.</span></span>

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

### <span data-ttu-id="d2270-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d2270-143">-NetworkWatcher</span></span>
<span data-ttu-id="d2270-144">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d2270-144">The network watcher resource.</span></span>

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

### <span data-ttu-id="d2270-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d2270-145">-NetworkWatcherName</span></span>
<span data-ttu-id="d2270-146">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d2270-146">The name of network watcher.</span></span>

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

### <span data-ttu-id="d2270-147">-Uwaga</span><span class="sxs-lookup"><span data-stu-id="d2270-147">-Note</span></span>
<span data-ttu-id="d2270-148">Notatki związane z monitorem połączeń.</span><span class="sxs-lookup"><span data-stu-id="d2270-148">Notes associated with connection monitor.</span></span>

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

```yaml
Type: System.String
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2270-149">— Dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="d2270-149">-Output</span></span>
<span data-ttu-id="d2270-150">Zawiera opis docelowych lokalizacji wyjściowych monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="d2270-150">Describes a connection monitor output destinations.</span></span>

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

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2270-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2270-151">-ResourceGroupName</span></span>
<span data-ttu-id="d2270-152">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d2270-152">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d2270-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2270-153">-ResourceId</span></span>
<span data-ttu-id="d2270-154">Identyfikator zasobu ConnectionMonitor.</span><span class="sxs-lookup"><span data-stu-id="d2270-154">ConnectionMonitor resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2270-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="d2270-155">-SourcePort</span></span>
<span data-ttu-id="d2270-156">Port źródłowy wykorzystywany przez Monitor połączeń.</span><span class="sxs-lookup"><span data-stu-id="d2270-156">The source port used by connection monitor.</span></span>

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

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2270-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="d2270-157">-SourceResourceId</span></span>
<span data-ttu-id="d2270-158">Identyfikator zasobu, który został wykorzystany jako źródło przez Monitor połączenia.</span><span class="sxs-lookup"><span data-stu-id="d2270-158">The ID of the resource used as the source by connection monitor.</span></span>

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

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2270-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="d2270-159">-Tag</span></span>
<span data-ttu-id="d2270-160">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2270-160">A hashtable which represents resource tags.</span></span>

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

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2270-161">-Tester</span><span class="sxs-lookup"><span data-stu-id="d2270-161">-TestGroup</span></span>
<span data-ttu-id="d2270-162">Lista grup testowych.</span><span class="sxs-lookup"><span data-stu-id="d2270-162">The list of test groups.</span></span>

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

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2270-163">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2270-163">-Confirm</span></span>
<span data-ttu-id="d2270-164">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2270-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2270-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2270-165">-WhatIf</span></span>
<span data-ttu-id="d2270-166">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2270-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2270-167">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d2270-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2270-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2270-168">CommonParameters</span></span>
<span data-ttu-id="d2270-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2270-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2270-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2270-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2270-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2270-171">INPUTS</span></span>

### <span data-ttu-id="d2270-172">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d2270-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d2270-173">System. String</span><span class="sxs-lookup"><span data-stu-id="d2270-173">System.String</span></span>

### <span data-ttu-id="d2270-174">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="d2270-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="d2270-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2270-175">OUTPUTS</span></span>

### <span data-ttu-id="d2270-176">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="d2270-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="d2270-177">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="d2270-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="d2270-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2270-178">NOTES</span></span>

## <span data-ttu-id="d2270-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2270-179">RELATED LINKS</span></span>
