---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184186"
---
# <span data-ttu-id="1673a-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1673a-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="1673a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1673a-102">SYNOPSIS</span></span>
<span data-ttu-id="1673a-103">Aktualizuje zasób monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="1673a-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="1673a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1673a-104">SYNTAX</span></span>

### <span data-ttu-id="1673a-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="1673a-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1673a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1673a-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1673a-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="1673a-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1673a-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="1673a-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1673a-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1673a-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1673a-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="1673a-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1673a-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1673a-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1673a-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="1673a-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1673a-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="1673a-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1673a-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="1673a-114">DESCRIPTION</span></span>
<span data-ttu-id="1673a-115">Polecenie Set-AzNetworkWatcherConnectionMonitor aktualizuje zasób monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="1673a-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="1673a-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1673a-116">EXAMPLES</span></span>

### <span data-ttu-id="1673a-117">Przykład 1. Aktualizowanie monitora połączenia</span><span class="sxs-lookup"><span data-stu-id="1673a-117">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="1673a-118">W tym przykładzie aktualizujemy istniejący monitor połączenia, zmieniając adres docelowyAddress i dodając tagi.</span><span class="sxs-lookup"><span data-stu-id="1673a-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="1673a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1673a-119">PARAMETERS</span></span>

### <span data-ttu-id="1673a-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1673a-120">-AsJob</span></span>
<span data-ttu-id="1673a-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1673a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1673a-122">- ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="1673a-122">-ConfigureOnly</span></span>
<span data-ttu-id="1673a-123">Konfigurowanie monitora połączenia, ale nie jego uruchamianie</span><span class="sxs-lookup"><span data-stu-id="1673a-123">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="1673a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1673a-124">-DefaultProfile</span></span>
<span data-ttu-id="1673a-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1673a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1673a-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="1673a-126">-DestinationAddress</span></span>
<span data-ttu-id="1673a-127">Adres miejsca docelowego monitora połączenia (adres IP lub nazwa domeny).</span><span class="sxs-lookup"><span data-stu-id="1673a-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="1673a-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="1673a-128">-DestinationPort</span></span>
<span data-ttu-id="1673a-129">Port docelowy używany przez monitor połączenia.</span><span class="sxs-lookup"><span data-stu-id="1673a-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="1673a-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="1673a-130">-DestinationResourceId</span></span>
<span data-ttu-id="1673a-131">Identyfikator zasobu używanego jako miejsce docelowe przez monitor połączenia.</span><span class="sxs-lookup"><span data-stu-id="1673a-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="1673a-132">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="1673a-132">-Force</span></span>
<span data-ttu-id="1673a-133">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="1673a-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1673a-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1673a-134">-InputObject</span></span>
<span data-ttu-id="1673a-135">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="1673a-135">Connection monitor object.</span></span>

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

### <span data-ttu-id="1673a-136">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1673a-136">-Location</span></span>
<span data-ttu-id="1673a-137">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="1673a-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1673a-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="1673a-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="1673a-139">Interwał monitorowania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="1673a-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="1673a-140">Wartość domyślna to 60 sekund.</span><span class="sxs-lookup"><span data-stu-id="1673a-140">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="1673a-141">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1673a-141">-Name</span></span>
<span data-ttu-id="1673a-142">Nazwa monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="1673a-142">The connection monitor name.</span></span>

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

### <span data-ttu-id="1673a-143">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1673a-143">-NetworkWatcher</span></span>
<span data-ttu-id="1673a-144">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="1673a-144">The network watcher resource.</span></span>

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

### <span data-ttu-id="1673a-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1673a-145">-NetworkWatcherName</span></span>
<span data-ttu-id="1673a-146">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="1673a-146">The name of network watcher.</span></span>

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

### <span data-ttu-id="1673a-147">— Uwaga</span><span class="sxs-lookup"><span data-stu-id="1673a-147">-Note</span></span>
<span data-ttu-id="1673a-148">Uwagi skojarzone z monitorem połączenia.</span><span class="sxs-lookup"><span data-stu-id="1673a-148">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="1673a-149">— Dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="1673a-149">-Output</span></span>
<span data-ttu-id="1673a-150">W tym artykule opisano miejsca docelowe wyjściowe monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="1673a-150">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="1673a-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1673a-151">-ResourceGroupName</span></span>
<span data-ttu-id="1673a-152">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="1673a-152">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1673a-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1673a-153">-ResourceId</span></span>
<span data-ttu-id="1673a-154">Identyfikator zasobu ConnectionMonitor.</span><span class="sxs-lookup"><span data-stu-id="1673a-154">ConnectionMonitor resource ID.</span></span>

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

### <span data-ttu-id="1673a-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="1673a-155">-SourcePort</span></span>
<span data-ttu-id="1673a-156">Port źródłowy używany przez monitor połączenia.</span><span class="sxs-lookup"><span data-stu-id="1673a-156">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="1673a-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="1673a-157">-SourceResourceId</span></span>
<span data-ttu-id="1673a-158">Identyfikator zasobu używanego jako źródło za pomocą monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="1673a-158">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="1673a-159">— Tag</span><span class="sxs-lookup"><span data-stu-id="1673a-159">-Tag</span></span>
<span data-ttu-id="1673a-160">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="1673a-160">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1673a-161">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="1673a-161">-TestGroup</span></span>
<span data-ttu-id="1673a-162">Lista grup testowych.</span><span class="sxs-lookup"><span data-stu-id="1673a-162">The list of test groups.</span></span>

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

### <span data-ttu-id="1673a-163">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1673a-163">-Confirm</span></span>
<span data-ttu-id="1673a-164">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1673a-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1673a-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1673a-165">-WhatIf</span></span>
<span data-ttu-id="1673a-166">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1673a-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1673a-167">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1673a-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1673a-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1673a-168">CommonParameters</span></span>
<span data-ttu-id="1673a-169">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1673a-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1673a-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1673a-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1673a-171">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1673a-171">INPUTS</span></span>

### <span data-ttu-id="1673a-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1673a-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1673a-173">System.String</span><span class="sxs-lookup"><span data-stu-id="1673a-173">System.String</span></span>

### <span data-ttu-id="1673a-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="1673a-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="1673a-175">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1673a-175">OUTPUTS</span></span>

### <span data-ttu-id="1673a-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="1673a-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="1673a-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="1673a-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="1673a-178">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1673a-178">NOTES</span></span>

## <span data-ttu-id="1673a-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1673a-179">RELATED LINKS</span></span>
