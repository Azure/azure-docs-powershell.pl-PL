---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 2de9b483e6458278da7fcccc942fd7bf0e0e796c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408155"
---
# <span data-ttu-id="01b90-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="01b90-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="01b90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01b90-102">SYNOPSIS</span></span>
<span data-ttu-id="01b90-103">Pobiera następny przeskok z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="01b90-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="01b90-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="01b90-104">SYNTAX</span></span>

### <span data-ttu-id="01b90-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="01b90-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01b90-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="01b90-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01b90-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="01b90-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01b90-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="01b90-108">DESCRIPTION</span></span>
<span data-ttu-id="01b90-109">Polecenie Get-AzNetworkWatcherNextHop cmdlet pobiera następny przeskok z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="01b90-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="01b90-110">Następny przeskok umożliwia wyświetlenie typu zasobu Azure, skojarzonego adresu IP tego zasobu i reguły tabeli routingu, która jest odpowiedzialna za trasę.</span><span class="sxs-lookup"><span data-stu-id="01b90-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="01b90-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="01b90-111">EXAMPLES</span></span>

### <span data-ttu-id="01b90-112">Przykład 1. Uzyskiwanie następnego przeskoku podczas komunikowania się za pomocą internetowego adresu IP</span><span class="sxs-lookup"><span data-stu-id="01b90-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
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

<span data-ttu-id="01b90-113">Pobiera następny przeskok dla komunikacji wychodzącej z podstawowego interfejsu sieciowego na określonej maszyny wirtualnej do programu 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="01b90-113">Gets the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Machine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="01b90-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01b90-114">PARAMETERS</span></span>

### <span data-ttu-id="01b90-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="01b90-115">-AsJob</span></span>
<span data-ttu-id="01b90-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="01b90-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01b90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01b90-117">-DefaultProfile</span></span>
<span data-ttu-id="01b90-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="01b90-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01b90-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="01b90-119">-DestinationIPAddress</span></span>
<span data-ttu-id="01b90-120">Docelowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="01b90-120">Destination IP address.</span></span>

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

### <span data-ttu-id="01b90-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="01b90-121">-Location</span></span>
<span data-ttu-id="01b90-122">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="01b90-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="01b90-123">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="01b90-123">-NetworkWatcher</span></span>
<span data-ttu-id="01b90-124">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="01b90-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="01b90-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="01b90-125">-NetworkWatcherName</span></span>
<span data-ttu-id="01b90-126">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="01b90-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="01b90-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01b90-127">-ResourceGroupName</span></span>
<span data-ttu-id="01b90-128">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="01b90-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="01b90-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="01b90-129">-SourceIPAddress</span></span>
<span data-ttu-id="01b90-130">Źródłowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="01b90-130">Source IP address.</span></span>

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

### <span data-ttu-id="01b90-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="01b90-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="01b90-132">Docelowy identyfikator interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="01b90-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="01b90-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="01b90-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="01b90-134">Docelowy identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="01b90-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="01b90-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01b90-135">CommonParameters</span></span>
<span data-ttu-id="01b90-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01b90-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01b90-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01b90-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01b90-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01b90-138">INPUTS</span></span>

### <span data-ttu-id="01b90-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="01b90-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="01b90-140">System.String</span><span class="sxs-lookup"><span data-stu-id="01b90-140">System.String</span></span>

## <span data-ttu-id="01b90-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01b90-141">OUTPUTS</span></span>

### <span data-ttu-id="01b90-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="01b90-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="01b90-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="01b90-143">NOTES</span></span>
<span data-ttu-id="01b90-144">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span><span class="sxs-lookup"><span data-stu-id="01b90-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="01b90-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01b90-145">RELATED LINKS</span></span>

[<span data-ttu-id="01b90-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="01b90-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="01b90-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="01b90-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="01b90-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="01b90-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="01b90-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="01b90-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="01b90-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="01b90-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="01b90-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="01b90-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="01b90-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="01b90-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="01b90-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="01b90-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="01b90-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="01b90-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="01b90-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="01b90-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="01b90-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="01b90-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="01b90-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="01b90-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="01b90-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="01b90-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="01b90-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="01b90-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="01b90-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="01b90-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="01b90-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="01b90-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="01b90-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="01b90-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="01b90-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="01b90-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="01b90-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="01b90-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="01b90-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="01b90-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="01b90-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="01b90-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="01b90-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="01b90-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="01b90-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="01b90-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="01b90-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="01b90-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="01b90-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="01b90-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="01b90-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="01b90-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="01b90-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="01b90-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
