---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 0c59de4b0c6dfd7da196b4ec67999406a14e0d1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870136"
---
# <span data-ttu-id="21424-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="21424-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="21424-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21424-102">SYNOPSIS</span></span>
<span data-ttu-id="21424-103">Zwraca monitor połączenia z określoną nazwą lub z listą monitorów połączeń.</span><span class="sxs-lookup"><span data-stu-id="21424-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="21424-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21424-104">SYNTAX</span></span>

### <span data-ttu-id="21424-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="21424-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21424-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="21424-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21424-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="21424-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21424-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="21424-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21424-109">Opis</span><span class="sxs-lookup"><span data-stu-id="21424-109">DESCRIPTION</span></span>
<span data-ttu-id="21424-110">Polecenie cmdlet Get-AzNetworkWatcherConnectionMonitor zwraca monitor połączenia z określoną nazwą/identyfikatorem zasobu lub listą monitorów połączeń odpowiadającą określonemu obserwatorowi/lokalizacji sieci.</span><span class="sxs-lookup"><span data-stu-id="21424-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="21424-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21424-111">EXAMPLES</span></span>

### <span data-ttu-id="21424-112">Przykład 1: uzyskiwanie monitora połączeń według nazwy w określonej lokalizacji</span><span class="sxs-lookup"><span data-stu-id="21424-112">Example 1: Get connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="21424-113">W tym przykładzie monitor połączenia jest wyświetlany według nazwy w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="21424-113">In this example we get connection monitor by name in the specified location.</span></span>

### <span data-ttu-id="21424-114">Przykład 2: uzyskiwanie monitorów połączeń przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="21424-114">Example 2: Get connection monitors using filtering</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitor -ResourceGroupName NetworkWatcherRG -NetworkWatcherName NetworkWatcher_centraluseuap -Name cm*


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="21424-115">W tym przykładzie są odbierane wszystkie monitory połączeń w NetworkWatcher_centraluseuap rozpoczynające się od "cm"</span><span class="sxs-lookup"><span data-stu-id="21424-115">In this example we get all connection monitors in NetworkWatcher_centraluseuap that start with "cm"</span></span>

## <span data-ttu-id="21424-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21424-116">PARAMETERS</span></span>

### <span data-ttu-id="21424-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21424-117">-DefaultProfile</span></span>
<span data-ttu-id="21424-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21424-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21424-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="21424-119">-Location</span></span>
<span data-ttu-id="21424-120">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="21424-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="21424-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21424-121">-Name</span></span>
<span data-ttu-id="21424-122">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="21424-122">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="21424-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="21424-123">-NetworkWatcher</span></span>
<span data-ttu-id="21424-124">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="21424-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="21424-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="21424-125">-NetworkWatcherName</span></span>
<span data-ttu-id="21424-126">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="21424-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="21424-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21424-127">-ResourceGroupName</span></span>
<span data-ttu-id="21424-128">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="21424-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="21424-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21424-129">-ResourceId</span></span>
<span data-ttu-id="21424-130">Identyfikator zasobu monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="21424-130">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="21424-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21424-131">CommonParameters</span></span>
<span data-ttu-id="21424-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21424-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21424-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21424-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21424-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21424-134">INPUTS</span></span>

### <span data-ttu-id="21424-135">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="21424-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="21424-136">System. String</span><span class="sxs-lookup"><span data-stu-id="21424-136">System.String</span></span>

## <span data-ttu-id="21424-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21424-137">OUTPUTS</span></span>

### <span data-ttu-id="21424-138">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="21424-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="21424-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21424-139">NOTES</span></span>
<span data-ttu-id="21424-140">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="21424-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="21424-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21424-141">RELATED LINKS</span></span>

[<span data-ttu-id="21424-142">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="21424-142">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="21424-143">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="21424-143">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="21424-144">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="21424-144">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="21424-145">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="21424-145">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="21424-146">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="21424-146">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="21424-147">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="21424-147">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="21424-148">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="21424-148">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="21424-149">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="21424-149">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="21424-150">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="21424-150">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="21424-151">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="21424-151">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="21424-152">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="21424-152">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="21424-153">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="21424-153">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="21424-154">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="21424-154">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="21424-155">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="21424-155">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="21424-156">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="21424-156">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="21424-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="21424-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="21424-158">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="21424-158">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="21424-159">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="21424-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="21424-160">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="21424-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="21424-161">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="21424-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="21424-162">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="21424-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="21424-163">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="21424-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="21424-164">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="21424-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="21424-165">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="21424-165">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="21424-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="21424-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="21424-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="21424-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="21424-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="21424-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
