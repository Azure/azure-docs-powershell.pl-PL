---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: ec7f6f910a50f479a923451fb9b893a5cabb5301
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869876"
---
# <span data-ttu-id="d37a6-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d37a6-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="d37a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d37a6-102">SYNOPSIS</span></span>
<span data-ttu-id="d37a6-103">Umożliwia utworzenie monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="d37a6-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="d37a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d37a6-104">SYNTAX</span></span>

### <span data-ttu-id="d37a6-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d37a6-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d37a6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d37a6-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d37a6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d37a6-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d37a6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d37a6-108">DESCRIPTION</span></span>
<span data-ttu-id="d37a6-109">Polecenie cmdlet New-AzNetworkWatcherConnectionMonitor tworzy monitor połączenia dla określonego źródła i miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="d37a6-109">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="d37a6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d37a6-110">EXAMPLES</span></span>

### <span data-ttu-id="d37a6-111">Przykład 1. Tworzenie monitora połączeń dla maszyny wirtualnej i lokalizacji docelowej w Internecie</span><span class="sxs-lookup"><span data-stu-id="d37a6-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/t1
Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft
                                .Compute/virtualMachines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "bing.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:13:11 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {}
```

<span data-ttu-id="d37a6-112">Polecenie cmdlet New-AzNetworkWatcherConnectionMonitor tworzy monitor połączenia dla określonego źródła i miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="d37a6-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="d37a6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d37a6-113">PARAMETERS</span></span>

### <span data-ttu-id="d37a6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d37a6-114">-AsJob</span></span>
<span data-ttu-id="d37a6-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d37a6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d37a6-116">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="d37a6-116">-ConfigureOnly</span></span>
<span data-ttu-id="d37a6-117">Konfigurowanie monitora połączeń, ale nie Rozpoczynanie go</span><span class="sxs-lookup"><span data-stu-id="d37a6-117">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="d37a6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37a6-118">-DefaultProfile</span></span>
<span data-ttu-id="d37a6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d37a6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d37a6-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="d37a6-120">-DestinationAddress</span></span>
<span data-ttu-id="d37a6-121">Adres IP miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="d37a6-121">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="d37a6-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="d37a6-122">-DestinationPort</span></span>
<span data-ttu-id="d37a6-123">Port docelowy.</span><span class="sxs-lookup"><span data-stu-id="d37a6-123">Destination port.</span></span>

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

### <span data-ttu-id="d37a6-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="d37a6-124">-DestinationResourceId</span></span>
<span data-ttu-id="d37a6-125">Identyfikator miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="d37a6-125">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="d37a6-126">-Force</span><span class="sxs-lookup"><span data-stu-id="d37a6-126">-Force</span></span>
<span data-ttu-id="d37a6-127">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="d37a6-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d37a6-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d37a6-128">-Location</span></span>
<span data-ttu-id="d37a6-129">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d37a6-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d37a6-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d37a6-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="d37a6-131">Interwał monitorowania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="d37a6-131">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="d37a6-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d37a6-132">-Name</span></span>
<span data-ttu-id="d37a6-133">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="d37a6-133">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37a6-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d37a6-134">-NetworkWatcher</span></span>
<span data-ttu-id="d37a6-135">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d37a6-135">The network watcher resource.</span></span>

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

### <span data-ttu-id="d37a6-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d37a6-136">-NetworkWatcherName</span></span>
<span data-ttu-id="d37a6-137">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d37a6-137">The name of network watcher.</span></span>

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

### <span data-ttu-id="d37a6-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d37a6-138">-ResourceGroupName</span></span>
<span data-ttu-id="d37a6-139">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d37a6-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d37a6-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="d37a6-140">-SourcePort</span></span>
<span data-ttu-id="d37a6-141">Port źródłowy.</span><span class="sxs-lookup"><span data-stu-id="d37a6-141">Source port.</span></span>

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

### <span data-ttu-id="d37a6-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="d37a6-142">-SourceResourceId</span></span>
<span data-ttu-id="d37a6-143">Identyfikator źródła monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="d37a6-143">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="d37a6-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="d37a6-144">-Tag</span></span>
<span data-ttu-id="d37a6-145">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="d37a6-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d37a6-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d37a6-146">-Confirm</span></span>
<span data-ttu-id="d37a6-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d37a6-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d37a6-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d37a6-148">-WhatIf</span></span>
<span data-ttu-id="d37a6-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d37a6-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d37a6-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d37a6-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d37a6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37a6-151">CommonParameters</span></span>
<span data-ttu-id="d37a6-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d37a6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37a6-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d37a6-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37a6-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d37a6-154">INPUTS</span></span>

### <span data-ttu-id="d37a6-155">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d37a6-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="d37a6-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d37a6-156">OUTPUTS</span></span>

### <span data-ttu-id="d37a6-157">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="d37a6-157">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="d37a6-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d37a6-158">NOTES</span></span>
<span data-ttu-id="d37a6-159">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="d37a6-159">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="d37a6-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d37a6-160">RELATED LINKS</span></span>

[<span data-ttu-id="d37a6-161">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d37a6-161">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d37a6-162">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d37a6-162">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d37a6-163">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d37a6-163">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d37a6-164">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d37a6-164">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d37a6-165">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d37a6-165">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d37a6-166">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d37a6-166">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d37a6-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d37a6-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d37a6-168">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d37a6-168">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d37a6-169">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d37a6-169">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d37a6-170">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d37a6-170">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d37a6-171">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d37a6-171">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d37a6-172">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d37a6-172">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d37a6-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d37a6-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d37a6-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d37a6-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d37a6-175">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d37a6-175">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d37a6-176">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d37a6-176">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d37a6-177">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d37a6-177">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d37a6-178">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d37a6-178">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d37a6-179">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d37a6-179">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d37a6-180">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d37a6-180">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d37a6-181">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d37a6-181">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d37a6-182">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d37a6-182">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d37a6-183">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d37a6-183">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d37a6-184">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d37a6-184">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d37a6-185">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d37a6-185">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d37a6-186">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d37a6-186">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d37a6-187">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d37a6-187">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
