---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7554183d52b263f4eed470295a2574a3d1f487b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554057"
---
# <span data-ttu-id="95ef0-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="95ef0-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="95ef0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="95ef0-103">Umożliwia utworzenie monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="95ef0-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95ef0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95ef0-104">SYNTAX</span></span>

### <span data-ttu-id="95ef0-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="95ef0-105">SetByName (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95ef0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="95ef0-106">SetByResource</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95ef0-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="95ef0-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95ef0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="95ef0-108">DESCRIPTION</span></span>
<span data-ttu-id="95ef0-109">Polecenie cmdlet New-AzureRmNetworkWatcherConnectionMonitor rcreates monitorze połączeń dla określonego źródła i miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="95ef0-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="95ef0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95ef0-110">EXAMPLES</span></span>

### <span data-ttu-id="95ef0-111">Przykład 1. Tworzenie monitora połączeń dla maszyny wirtualnej i lokalizacji docelowej w Internecie</span><span class="sxs-lookup"><span data-stu-id="95ef0-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

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

<span data-ttu-id="95ef0-112">Polecenie cmdlet New-AzureRmNetworkWatcherConnectionMonitor tworzy monitor połączenia dla określonego źródła i miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="95ef0-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="95ef0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95ef0-113">PARAMETERS</span></span>

### <span data-ttu-id="95ef0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95ef0-114">-AsJob</span></span>
<span data-ttu-id="95ef0-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="95ef0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95ef0-116">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="95ef0-116">-ConfigureOnly</span></span>
<span data-ttu-id="95ef0-117">Konfigurowanie monitora połączeń, ale nie Rozpoczynanie go</span><span class="sxs-lookup"><span data-stu-id="95ef0-117">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="95ef0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95ef0-118">-DefaultProfile</span></span>
<span data-ttu-id="95ef0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="95ef0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95ef0-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="95ef0-120">-DestinationAddress</span></span>
<span data-ttu-id="95ef0-121">Adres IP miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="95ef0-121">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="95ef0-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="95ef0-122">-DestinationPort</span></span>
<span data-ttu-id="95ef0-123">Port docelowy.</span><span class="sxs-lookup"><span data-stu-id="95ef0-123">Destination port.</span></span>

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

### <span data-ttu-id="95ef0-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="95ef0-124">-DestinationResourceId</span></span>
<span data-ttu-id="95ef0-125">Identyfikator miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="95ef0-125">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="95ef0-126">-Force</span><span class="sxs-lookup"><span data-stu-id="95ef0-126">-Force</span></span>
<span data-ttu-id="95ef0-127">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="95ef0-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="95ef0-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="95ef0-128">-Location</span></span>
<span data-ttu-id="95ef0-129">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="95ef0-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="95ef0-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="95ef0-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="95ef0-131">Interwał monitorowania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="95ef0-131">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="95ef0-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="95ef0-132">-Name</span></span>
<span data-ttu-id="95ef0-133">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="95ef0-133">The connection monitor name.</span></span>

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

### <span data-ttu-id="95ef0-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95ef0-134">-NetworkWatcher</span></span>
<span data-ttu-id="95ef0-135">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="95ef0-135">The network watcher resource.</span></span>

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

### <span data-ttu-id="95ef0-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="95ef0-136">-NetworkWatcherName</span></span>
<span data-ttu-id="95ef0-137">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="95ef0-137">The name of network watcher.</span></span>

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

### <span data-ttu-id="95ef0-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95ef0-138">-ResourceGroupName</span></span>
<span data-ttu-id="95ef0-139">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="95ef0-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="95ef0-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="95ef0-140">-SourcePort</span></span>
<span data-ttu-id="95ef0-141">Port źródłowy.</span><span class="sxs-lookup"><span data-stu-id="95ef0-141">Source port.</span></span>

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

### <span data-ttu-id="95ef0-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="95ef0-142">-SourceResourceId</span></span>
<span data-ttu-id="95ef0-143">Identyfikator źródła monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="95ef0-143">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="95ef0-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="95ef0-144">-Tag</span></span>
<span data-ttu-id="95ef0-145">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="95ef0-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="95ef0-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="95ef0-146">-Confirm</span></span>
<span data-ttu-id="95ef0-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95ef0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95ef0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95ef0-148">-WhatIf</span></span>
<span data-ttu-id="95ef0-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95ef0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95ef0-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="95ef0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95ef0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ef0-151">CommonParameters</span></span>
<span data-ttu-id="95ef0-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95ef0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ef0-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95ef0-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ef0-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95ef0-154">INPUTS</span></span>

### <span data-ttu-id="95ef0-155">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95ef0-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="95ef0-156">Parametry: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="95ef0-156">Parameters: NetworkWatcher (ByValue)</span></span>

## <span data-ttu-id="95ef0-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95ef0-157">OUTPUTS</span></span>

### <span data-ttu-id="95ef0-158">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="95ef0-158">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="95ef0-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95ef0-159">NOTES</span></span>
<span data-ttu-id="95ef0-160">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="95ef0-160">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="95ef0-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95ef0-161">RELATED LINKS</span></span>

[<span data-ttu-id="95ef0-162">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95ef0-162">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="95ef0-163">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95ef0-163">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="95ef0-164">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95ef0-164">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="95ef0-165">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="95ef0-165">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="95ef0-166">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="95ef0-166">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="95ef0-167">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="95ef0-167">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="95ef0-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="95ef0-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="95ef0-169">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95ef0-169">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="95ef0-170">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="95ef0-170">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="95ef0-171">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95ef0-171">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="95ef0-172">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95ef0-172">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="95ef0-173">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95ef0-173">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="95ef0-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="95ef0-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="95ef0-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="95ef0-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="95ef0-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="95ef0-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="95ef0-177">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="95ef0-177">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="95ef0-178">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="95ef0-178">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="95ef0-179">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="95ef0-179">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="95ef0-180">Nowe — AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="95ef0-180">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="95ef0-181">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="95ef0-181">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="95ef0-182">Test — AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="95ef0-182">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="95ef0-183">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="95ef0-183">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="95ef0-184">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="95ef0-184">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="95ef0-185">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="95ef0-185">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="95ef0-186">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="95ef0-186">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="95ef0-187">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="95ef0-187">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="95ef0-188">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="95ef0-188">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
