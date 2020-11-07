---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7e3836f2c546c5ba3ad2ee4a2845e7c813601dda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872191"
---
# <span data-ttu-id="3b4ee-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3b4ee-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="3b4ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b4ee-102">SYNOPSIS</span></span>
<span data-ttu-id="3b4ee-103">Aktualizowanie monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-103">Update a connection monitor.</span></span>

## <span data-ttu-id="3b4ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b4ee-104">SYNTAX</span></span>

### <span data-ttu-id="3b4ee-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3b4ee-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b4ee-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3b4ee-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b4ee-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3b4ee-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b4ee-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3b4ee-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b4ee-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="3b4ee-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b4ee-110">Opis</span><span class="sxs-lookup"><span data-stu-id="3b4ee-110">DESCRIPTION</span></span>
<span data-ttu-id="3b4ee-111">Polecenie cmdlet Set-AzNetworkWatcherConnectionMonitor aktualizuje określony monitor połączeń.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="3b4ee-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b4ee-112">EXAMPLES</span></span>

### <span data-ttu-id="3b4ee-113">Przykład 1: aktualizowanie monitora połączeń</span><span class="sxs-lookup"><span data-stu-id="3b4ee-113">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="3b4ee-114">W tym przykładzie Zaktualizowano istniejący monitor połączenia, zmieniając destinationAddress i dodając Tagi.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="3b4ee-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b4ee-115">PARAMETERS</span></span>

### <span data-ttu-id="3b4ee-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b4ee-116">-AsJob</span></span>
<span data-ttu-id="3b4ee-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3b4ee-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b4ee-118">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="3b4ee-118">-ConfigureOnly</span></span>
<span data-ttu-id="3b4ee-119">Konfigurowanie monitora połączeń, ale nie Rozpoczynanie go</span><span class="sxs-lookup"><span data-stu-id="3b4ee-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="3b4ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b4ee-120">-DefaultProfile</span></span>
<span data-ttu-id="3b4ee-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b4ee-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="3b4ee-122">-DestinationAddress</span></span>
<span data-ttu-id="3b4ee-123">Adres IP miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="3b4ee-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="3b4ee-124">-DestinationPort</span></span>
<span data-ttu-id="3b4ee-125">Port docelowy.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-125">Destination port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b4ee-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="3b4ee-126">-DestinationResourceId</span></span>
<span data-ttu-id="3b4ee-127">Identyfikator miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="3b4ee-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3b4ee-128">-InputObject</span></span>
<span data-ttu-id="3b4ee-129">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-129">Connection monitor object.</span></span>

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

### <span data-ttu-id="3b4ee-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3b4ee-130">-Location</span></span>
<span data-ttu-id="3b4ee-131">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-131">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b4ee-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="3b4ee-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="3b4ee-133">Interwał monitorowania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-133">Monitoring interval in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b4ee-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3b4ee-134">-Name</span></span>
<span data-ttu-id="3b4ee-135">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-135">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b4ee-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3b4ee-136">-NetworkWatcher</span></span>
<span data-ttu-id="3b4ee-137">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-137">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b4ee-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3b4ee-138">-NetworkWatcherName</span></span>
<span data-ttu-id="3b4ee-139">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-139">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b4ee-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b4ee-140">-ResourceGroupName</span></span>
<span data-ttu-id="3b4ee-141">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-141">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b4ee-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b4ee-142">-ResourceId</span></span>
<span data-ttu-id="3b4ee-143">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-143">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b4ee-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="3b4ee-144">-SourcePort</span></span>
<span data-ttu-id="3b4ee-145">Port źródłowy.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-145">Source port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b4ee-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="3b4ee-146">-SourceResourceId</span></span>
<span data-ttu-id="3b4ee-147">Identyfikator źródła monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="3b4ee-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b4ee-148">-Tag</span></span>
<span data-ttu-id="3b4ee-149">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-149">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b4ee-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b4ee-150">-Confirm</span></span>
<span data-ttu-id="3b4ee-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b4ee-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b4ee-152">-WhatIf</span></span>
<span data-ttu-id="3b4ee-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b4ee-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b4ee-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b4ee-155">CommonParameters</span></span>
<span data-ttu-id="3b4ee-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b4ee-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b4ee-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b4ee-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b4ee-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b4ee-158">INPUTS</span></span>

### <span data-ttu-id="3b4ee-159">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3b4ee-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3b4ee-160">System. String</span><span class="sxs-lookup"><span data-stu-id="3b4ee-160">System.String</span></span>

### <span data-ttu-id="3b4ee-161">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="3b4ee-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="3b4ee-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b4ee-162">OUTPUTS</span></span>

### <span data-ttu-id="3b4ee-163">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="3b4ee-163">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="3b4ee-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b4ee-164">NOTES</span></span>
<span data-ttu-id="3b4ee-165">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="3b4ee-165">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="3b4ee-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b4ee-166">RELATED LINKS</span></span>

[<span data-ttu-id="3b4ee-167">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3b4ee-167">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3b4ee-168">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3b4ee-168">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3b4ee-169">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3b4ee-169">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3b4ee-170">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3b4ee-170">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3b4ee-171">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3b4ee-171">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3b4ee-172">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3b4ee-172">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3b4ee-173">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3b4ee-173">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3b4ee-174">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3b4ee-174">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3b4ee-175">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3b4ee-175">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3b4ee-176">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3b4ee-176">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3b4ee-177">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3b4ee-177">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3b4ee-178">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3b4ee-178">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3b4ee-179">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3b4ee-179">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3b4ee-180">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3b4ee-180">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="3b4ee-181">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3b4ee-181">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3b4ee-182">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3b4ee-182">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3b4ee-183">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3b4ee-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3b4ee-184">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3b4ee-184">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3b4ee-185">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b4ee-185">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3b4ee-186">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3b4ee-186">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3b4ee-187">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3b4ee-187">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="3b4ee-188">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3b4ee-188">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3b4ee-189">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3b4ee-189">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3b4ee-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3b4ee-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3b4ee-191">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3b4ee-191">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3b4ee-192">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3b4ee-192">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3b4ee-193">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3b4ee-193">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
