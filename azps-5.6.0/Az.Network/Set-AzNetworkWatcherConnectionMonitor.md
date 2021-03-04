---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: e5f8e8f470570993433858a0aa1c165122c614e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007697"
---
# <span data-ttu-id="29c35-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29c35-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="29c35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29c35-102">SYNOPSIS</span></span>
<span data-ttu-id="29c35-103">Aktualizuje zasób monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="29c35-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="29c35-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="29c35-104">SYNTAX</span></span>

### <span data-ttu-id="29c35-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="29c35-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29c35-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="29c35-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29c35-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="29c35-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c35-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="29c35-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c35-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="29c35-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c35-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="29c35-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c35-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="29c35-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c35-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="29c35-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c35-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="29c35-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29c35-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="29c35-114">DESCRIPTION</span></span>
<span data-ttu-id="29c35-115">Polecenie Set-AzNetworkWatcherConnectionMonitor aktualizuje zasób monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="29c35-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="29c35-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="29c35-116">EXAMPLES</span></span>

### <span data-ttu-id="29c35-117">Przykład 1. Aktualizowanie monitora połączenia</span><span class="sxs-lookup"><span data-stu-id="29c35-117">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="29c35-118">W tym przykładzie aktualizujemy istniejący monitor połączenia, zmieniając adres docelowyAddress i dodając tagi.</span><span class="sxs-lookup"><span data-stu-id="29c35-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="29c35-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29c35-119">PARAMETERS</span></span>

### <span data-ttu-id="29c35-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="29c35-120">-AsJob</span></span>
<span data-ttu-id="29c35-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="29c35-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29c35-122">- ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="29c35-122">-ConfigureOnly</span></span>
<span data-ttu-id="29c35-123">Konfigurowanie monitora połączenia, ale nie jego uruchamianie</span><span class="sxs-lookup"><span data-stu-id="29c35-123">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="29c35-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29c35-124">-DefaultProfile</span></span>
<span data-ttu-id="29c35-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="29c35-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29c35-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="29c35-126">-DestinationAddress</span></span>
<span data-ttu-id="29c35-127">Adres miejsca docelowego monitora połączenia (adres IP lub nazwa domeny).</span><span class="sxs-lookup"><span data-stu-id="29c35-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="29c35-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="29c35-128">-DestinationPort</span></span>
<span data-ttu-id="29c35-129">Port docelowy używany przez monitor połączenia.</span><span class="sxs-lookup"><span data-stu-id="29c35-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="29c35-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="29c35-130">-DestinationResourceId</span></span>
<span data-ttu-id="29c35-131">Identyfikator zasobu używanego jako miejsce docelowe przez monitor połączenia.</span><span class="sxs-lookup"><span data-stu-id="29c35-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="29c35-132">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="29c35-132">-Force</span></span>
<span data-ttu-id="29c35-133">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="29c35-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="29c35-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29c35-134">-InputObject</span></span>
<span data-ttu-id="29c35-135">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="29c35-135">Connection monitor object.</span></span>

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

### <span data-ttu-id="29c35-136">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="29c35-136">-Location</span></span>
<span data-ttu-id="29c35-137">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="29c35-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="29c35-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="29c35-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="29c35-139">Monitorowanie interwału w sekundach.</span><span class="sxs-lookup"><span data-stu-id="29c35-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="29c35-140">Wartość domyślna to 60 sekund.</span><span class="sxs-lookup"><span data-stu-id="29c35-140">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="29c35-141">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="29c35-141">-Name</span></span>
<span data-ttu-id="29c35-142">Nazwa monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="29c35-142">The connection monitor name.</span></span>

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

### <span data-ttu-id="29c35-143">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29c35-143">-NetworkWatcher</span></span>
<span data-ttu-id="29c35-144">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="29c35-144">The network watcher resource.</span></span>

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

### <span data-ttu-id="29c35-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="29c35-145">-NetworkWatcherName</span></span>
<span data-ttu-id="29c35-146">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="29c35-146">The name of network watcher.</span></span>

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

### <span data-ttu-id="29c35-147">— Uwaga</span><span class="sxs-lookup"><span data-stu-id="29c35-147">-Note</span></span>
<span data-ttu-id="29c35-148">Uwagi skojarzone z monitorem połączenia.</span><span class="sxs-lookup"><span data-stu-id="29c35-148">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="29c35-149">— Dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="29c35-149">-Output</span></span>
<span data-ttu-id="29c35-150">W tym artykule opisano miejsca docelowe wyjściowe monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="29c35-150">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="29c35-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29c35-151">-ResourceGroupName</span></span>
<span data-ttu-id="29c35-152">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="29c35-152">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="29c35-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29c35-153">-ResourceId</span></span>
<span data-ttu-id="29c35-154">Identyfikator zasobu ConnectionMonitor.</span><span class="sxs-lookup"><span data-stu-id="29c35-154">ConnectionMonitor resource ID.</span></span>

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

### <span data-ttu-id="29c35-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="29c35-155">-SourcePort</span></span>
<span data-ttu-id="29c35-156">Port źródłowy używany przez monitor połączenia.</span><span class="sxs-lookup"><span data-stu-id="29c35-156">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="29c35-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="29c35-157">-SourceResourceId</span></span>
<span data-ttu-id="29c35-158">Identyfikator zasobu używanego jako źródło za pomocą monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="29c35-158">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="29c35-159">— Tag</span><span class="sxs-lookup"><span data-stu-id="29c35-159">-Tag</span></span>
<span data-ttu-id="29c35-160">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="29c35-160">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="29c35-161">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="29c35-161">-TestGroup</span></span>
<span data-ttu-id="29c35-162">Lista grup testowych.</span><span class="sxs-lookup"><span data-stu-id="29c35-162">The list of test groups.</span></span>

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

### <span data-ttu-id="29c35-163">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29c35-163">-Confirm</span></span>
<span data-ttu-id="29c35-164">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="29c35-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29c35-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29c35-165">-WhatIf</span></span>
<span data-ttu-id="29c35-166">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29c35-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29c35-167">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="29c35-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29c35-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c35-168">CommonParameters</span></span>
<span data-ttu-id="29c35-169">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29c35-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c35-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29c35-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c35-171">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29c35-171">INPUTS</span></span>

### <span data-ttu-id="29c35-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29c35-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="29c35-173">System.String</span><span class="sxs-lookup"><span data-stu-id="29c35-173">System.String</span></span>

### <span data-ttu-id="29c35-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="29c35-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="29c35-175">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29c35-175">OUTPUTS</span></span>

### <span data-ttu-id="29c35-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="29c35-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="29c35-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="29c35-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="29c35-178">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="29c35-178">NOTES</span></span>

## <span data-ttu-id="29c35-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29c35-179">RELATED LINKS</span></span>
