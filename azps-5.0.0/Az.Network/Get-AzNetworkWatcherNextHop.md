---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: cf120e8e9ca9e0dad8f4d430c7f207d40fcfab3b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317244"
---
# <span data-ttu-id="8cba4-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8cba4-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="8cba4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8cba4-102">SYNOPSIS</span></span>
<span data-ttu-id="8cba4-103">Pobiera następny przeskok z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8cba4-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="8cba4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8cba4-104">SYNTAX</span></span>

### <span data-ttu-id="8cba4-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8cba4-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cba4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="8cba4-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cba4-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8cba4-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cba4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8cba4-108">DESCRIPTION</span></span>
<span data-ttu-id="8cba4-109">Polecenie cmdlet Get-AzNetworkWatcherNextHop pobiera następny przeskok z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8cba4-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="8cba4-110">Następny przeskok umożliwia wyświetlenie typu zasobu platformy Azure, skojarzonego adresu IP tego zasobu oraz reguły tabeli routingu odpowiedzialnej za trasę.</span><span class="sxs-lookup"><span data-stu-id="8cba4-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="8cba4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8cba4-111">EXAMPLES</span></span>

### <span data-ttu-id="8cba4-112">Przykład 1. Uzyskiwanie następnego przeskoku podczas komunikowania się z internetowym adresem IP</span><span class="sxs-lookup"><span data-stu-id="8cba4-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="8cba4-113">Pobiera następny przeskok komunikacji wychodzącej z podstawowego interfejsu sieciowego na określonej maszynie wirtualnej na 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="8cba4-113">Gets the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Machine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="8cba4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8cba4-114">PARAMETERS</span></span>

### <span data-ttu-id="8cba4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cba4-115">-AsJob</span></span>
<span data-ttu-id="8cba4-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8cba4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8cba4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cba4-117">-DefaultProfile</span></span>
<span data-ttu-id="8cba4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8cba4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cba4-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="8cba4-119">-DestinationIPAddress</span></span>
<span data-ttu-id="8cba4-120">Docelowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="8cba4-120">Destination IP address.</span></span>

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

### <span data-ttu-id="8cba4-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8cba4-121">-Location</span></span>
<span data-ttu-id="8cba4-122">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="8cba4-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="8cba4-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8cba4-123">-NetworkWatcher</span></span>
<span data-ttu-id="8cba4-124">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="8cba4-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="8cba4-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8cba4-125">-NetworkWatcherName</span></span>
<span data-ttu-id="8cba4-126">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="8cba4-126">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cba4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cba4-127">-ResourceGroupName</span></span>
<span data-ttu-id="8cba4-128">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="8cba4-128">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cba4-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="8cba4-129">-SourceIPAddress</span></span>
<span data-ttu-id="8cba4-130">Źródłowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="8cba4-130">Source IP address.</span></span>

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

### <span data-ttu-id="8cba4-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="8cba4-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="8cba4-132">Identyfikator interfejsu sieci docelowej.</span><span class="sxs-lookup"><span data-stu-id="8cba4-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="8cba4-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="8cba4-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="8cba4-134">Docelowy Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8cba4-134">The target virtual machine ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cba4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cba4-135">CommonParameters</span></span>
<span data-ttu-id="8cba4-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cba4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cba4-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cba4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cba4-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8cba4-138">INPUTS</span></span>

### <span data-ttu-id="8cba4-139">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8cba4-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="8cba4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8cba4-140">System.String</span></span>

## <span data-ttu-id="8cba4-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8cba4-141">OUTPUTS</span></span>

### <span data-ttu-id="8cba4-142">Microsoft. Azure. Commands. Network. models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="8cba4-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="8cba4-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8cba4-143">NOTES</span></span>
<span data-ttu-id="8cba4-144">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, następny, przeskok</span><span class="sxs-lookup"><span data-stu-id="8cba4-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="8cba4-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8cba4-145">RELATED LINKS</span></span>

[<span data-ttu-id="8cba4-146">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8cba4-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8cba4-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8cba4-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8cba4-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8cba4-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8cba4-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8cba4-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8cba4-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8cba4-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8cba4-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8cba4-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8cba4-152">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8cba4-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8cba4-153">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8cba4-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8cba4-154">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8cba4-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8cba4-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8cba4-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8cba4-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8cba4-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8cba4-157">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8cba4-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8cba4-158">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cba4-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8cba4-159">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8cba4-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8cba4-160">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8cba4-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="8cba4-161">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8cba4-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8cba4-162">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8cba4-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8cba4-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8cba4-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8cba4-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8cba4-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8cba4-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8cba4-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8cba4-166">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8cba4-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8cba4-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8cba4-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8cba4-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8cba4-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8cba4-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8cba4-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8cba4-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8cba4-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="8cba4-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8cba4-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="8cba4-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8cba4-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
