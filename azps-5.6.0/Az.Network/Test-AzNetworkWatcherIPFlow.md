---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 8be10fd630bbc9d4e1952150728d144b5f552fe6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951729"
---
# <span data-ttu-id="b9972-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b9972-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="b9972-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9972-102">SYNOPSIS</span></span>
<span data-ttu-id="b9972-103">Zwraca, czy pakiet jest dozwolony, czy odrzucony z określonego miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="b9972-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="b9972-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b9972-104">SYNTAX</span></span>

### <span data-ttu-id="b9972-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b9972-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9972-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b9972-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9972-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b9972-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9972-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b9972-108">DESCRIPTION</span></span>
<span data-ttu-id="b9972-109">Polecenie Test-AzNetworkWatcherIPFlow cmdlet dla określonego zasobu maszyny wirtualnej i pakietu z określonym kierunkiem przy użyciu lokalnych i zdalnych adresów IP i portów zwraca, czy pakiet jest dozwolony, czy odrzucony.</span><span class="sxs-lookup"><span data-stu-id="b9972-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="b9972-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b9972-110">EXAMPLES</span></span>

### <span data-ttu-id="b9972-111">Przykład 1. Uruchamianie Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b9972-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where-Object { $vm.NetworkProfile.NetworkInterfaces.Id -contains $_.Id }

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="b9972-112">Pobiera dla tej subskrypcji usługę Network Watcher w West Central US, a następnie pobiera maszyny wirtualnej i skojarzone z nią interfejsy sieciowe.</span><span class="sxs-lookup"><span data-stu-id="b9972-112">Gets the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="b9972-113">Następnie dla pierwszego interfejsu sieciowego jest uruchamiany Test-AzNetworkWatcherIPFlow przy użyciu pierwszego adresu IP z pierwszego interfejsu sieciowego dla połączenia wychodzącego do adresu IP w Internecie.</span><span class="sxs-lookup"><span data-stu-id="b9972-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="b9972-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9972-114">PARAMETERS</span></span>

### <span data-ttu-id="b9972-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b9972-115">-AsJob</span></span>
<span data-ttu-id="b9972-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b9972-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9972-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9972-117">-DefaultProfile</span></span>
<span data-ttu-id="b9972-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9972-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9972-119">— Kierunek</span><span class="sxs-lookup"><span data-stu-id="b9972-119">-Direction</span></span>
<span data-ttu-id="b9972-120">Kierunek.</span><span class="sxs-lookup"><span data-stu-id="b9972-120">Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9972-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="b9972-121">-LocalIPAddress</span></span>
<span data-ttu-id="b9972-122">Lokalny adres IP.</span><span class="sxs-lookup"><span data-stu-id="b9972-122">Local IP Address.</span></span>

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

### <span data-ttu-id="b9972-123">- LocalPort</span><span class="sxs-lookup"><span data-stu-id="b9972-123">-LocalPort</span></span>
<span data-ttu-id="b9972-124">Port lokalny.</span><span class="sxs-lookup"><span data-stu-id="b9972-124">Local Port.</span></span>

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

### <span data-ttu-id="b9972-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b9972-125">-Location</span></span>
<span data-ttu-id="b9972-126">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="b9972-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b9972-127">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b9972-127">-NetworkWatcher</span></span>
<span data-ttu-id="b9972-128">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="b9972-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="b9972-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b9972-129">-NetworkWatcherName</span></span>
<span data-ttu-id="b9972-130">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="b9972-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="b9972-131">— Protokół</span><span class="sxs-lookup"><span data-stu-id="b9972-131">-Protocol</span></span>
<span data-ttu-id="b9972-132">Protocol (Protokół).</span><span class="sxs-lookup"><span data-stu-id="b9972-132">Protocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9972-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="b9972-133">-RemoteIPAddress</span></span>
<span data-ttu-id="b9972-134">Zdalny adres IP.</span><span class="sxs-lookup"><span data-stu-id="b9972-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="b9972-135">— RemotePort</span><span class="sxs-lookup"><span data-stu-id="b9972-135">-RemotePort</span></span>
<span data-ttu-id="b9972-136">Port zdalny.</span><span class="sxs-lookup"><span data-stu-id="b9972-136">Remote port.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9972-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9972-137">-ResourceGroupName</span></span>
<span data-ttu-id="b9972-138">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="b9972-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b9972-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="b9972-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="b9972-140">Docelowy identyfikator interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="b9972-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="b9972-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="b9972-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="b9972-142">Docelowy identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b9972-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="b9972-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9972-143">CommonParameters</span></span>
<span data-ttu-id="b9972-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9972-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9972-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9972-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9972-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9972-146">INPUTS</span></span>

### <span data-ttu-id="b9972-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b9972-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b9972-148">System.String</span><span class="sxs-lookup"><span data-stu-id="b9972-148">System.String</span></span>

## <span data-ttu-id="b9972-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9972-149">OUTPUTS</span></span>

### <span data-ttu-id="b9972-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="b9972-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="b9972-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b9972-151">NOTES</span></span>
<span data-ttu-id="b9972-152">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span><span class="sxs-lookup"><span data-stu-id="b9972-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="b9972-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9972-153">RELATED LINKS</span></span>

[<span data-ttu-id="b9972-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b9972-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b9972-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b9972-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b9972-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b9972-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b9972-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b9972-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b9972-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b9972-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b9972-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b9972-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b9972-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b9972-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b9972-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b9972-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b9972-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b9972-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b9972-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b9972-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b9972-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b9972-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b9972-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b9972-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b9972-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9972-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b9972-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b9972-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b9972-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b9972-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b9972-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9972-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b9972-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9972-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b9972-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9972-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b9972-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b9972-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b9972-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9972-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b9972-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9972-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b9972-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b9972-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b9972-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b9972-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b9972-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b9972-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b9972-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b9972-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b9972-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b9972-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="b9972-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9972-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
