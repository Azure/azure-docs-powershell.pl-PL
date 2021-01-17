---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 75b8d976dc4c7be0544f2445ef991723c692edbf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340705"
---
# <span data-ttu-id="75770-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="75770-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="75770-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75770-102">SYNOPSIS</span></span>
<span data-ttu-id="75770-103">Zwraca możliwość, że pakiet jest dozwolony lub odmówiony lub pochodzi z określonego miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="75770-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="75770-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75770-104">SYNTAX</span></span>

### <span data-ttu-id="75770-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="75770-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75770-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="75770-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75770-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="75770-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75770-108">Opis</span><span class="sxs-lookup"><span data-stu-id="75770-108">DESCRIPTION</span></span>
<span data-ttu-id="75770-109">Polecenie cmdlet Test-AzNetworkWatcherIPFlow dla określonego zasobu maszyny wirtualnej i pakiet o określonym kierunku przy użyciu lokalnych i zdalnych adresów IP oraz portów zwraca wartość, czy pakiet jest dozwolony, czy zabroniony.</span><span class="sxs-lookup"><span data-stu-id="75770-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="75770-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75770-110">EXAMPLES</span></span>

### <span data-ttu-id="75770-111">Przykład 1: Uruchom Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="75770-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where-Object { $vm.NetworkProfile.NetworkInterfaces.Id -contains $_.Id }

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="75770-112">Pobiera Monitor sieci z zachodniego centralnego USA dla tej subskrypcji, a następnie pobiera maszynę wirtualną i skojarzone z nią interfejsy sieciowe.</span><span class="sxs-lookup"><span data-stu-id="75770-112">Gets the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="75770-113">Następnie w pierwszym interfejsie sieciowym zostanie uruchomiona Test-AzNetworkWatcherIPFlow przy użyciu pierwszego adresu IP od pierwszego interfejsu sieciowego w celu połączenia wychodzącego z adresem IP w Internecie.</span><span class="sxs-lookup"><span data-stu-id="75770-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="75770-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75770-114">PARAMETERS</span></span>

### <span data-ttu-id="75770-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75770-115">-AsJob</span></span>
<span data-ttu-id="75770-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="75770-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75770-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75770-117">-DefaultProfile</span></span>
<span data-ttu-id="75770-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="75770-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75770-119">-Direction</span><span class="sxs-lookup"><span data-stu-id="75770-119">-Direction</span></span>
<span data-ttu-id="75770-120">Obszar.</span><span class="sxs-lookup"><span data-stu-id="75770-120">Direction.</span></span>

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

### <span data-ttu-id="75770-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="75770-121">-LocalIPAddress</span></span>
<span data-ttu-id="75770-122">Lokalny adres IP.</span><span class="sxs-lookup"><span data-stu-id="75770-122">Local IP Address.</span></span>

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

### <span data-ttu-id="75770-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="75770-123">-LocalPort</span></span>
<span data-ttu-id="75770-124">Port lokalny.</span><span class="sxs-lookup"><span data-stu-id="75770-124">Local Port.</span></span>

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

### <span data-ttu-id="75770-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="75770-125">-Location</span></span>
<span data-ttu-id="75770-126">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="75770-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="75770-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="75770-127">-NetworkWatcher</span></span>
<span data-ttu-id="75770-128">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="75770-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="75770-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="75770-129">-NetworkWatcherName</span></span>
<span data-ttu-id="75770-130">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="75770-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="75770-131">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="75770-131">-Protocol</span></span>
<span data-ttu-id="75770-132">Sterownika.</span><span class="sxs-lookup"><span data-stu-id="75770-132">Protocol.</span></span>

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

### <span data-ttu-id="75770-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="75770-133">-RemoteIPAddress</span></span>
<span data-ttu-id="75770-134">Zdalny adres IP.</span><span class="sxs-lookup"><span data-stu-id="75770-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="75770-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="75770-135">-RemotePort</span></span>
<span data-ttu-id="75770-136">Port zdalny.</span><span class="sxs-lookup"><span data-stu-id="75770-136">Remote port.</span></span>

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

### <span data-ttu-id="75770-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75770-137">-ResourceGroupName</span></span>
<span data-ttu-id="75770-138">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="75770-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="75770-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="75770-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="75770-140">Identyfikator interfejsu sieci docelowej.</span><span class="sxs-lookup"><span data-stu-id="75770-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="75770-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="75770-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="75770-142">Docelowy Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="75770-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="75770-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75770-143">CommonParameters</span></span>
<span data-ttu-id="75770-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75770-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75770-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75770-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75770-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75770-146">INPUTS</span></span>

### <span data-ttu-id="75770-147">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="75770-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="75770-148">System. String</span><span class="sxs-lookup"><span data-stu-id="75770-148">System.String</span></span>

## <span data-ttu-id="75770-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75770-149">OUTPUTS</span></span>

### <span data-ttu-id="75770-150">Microsoft. Azure. Commands. Network. models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="75770-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="75770-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75770-151">NOTES</span></span>
<span data-ttu-id="75770-152">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor sieciowy, przepływ, IP</span><span class="sxs-lookup"><span data-stu-id="75770-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="75770-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75770-153">RELATED LINKS</span></span>

[<span data-ttu-id="75770-154">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="75770-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="75770-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="75770-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="75770-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="75770-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="75770-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="75770-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="75770-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="75770-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="75770-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="75770-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="75770-160">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="75770-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="75770-161">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="75770-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="75770-162">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="75770-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="75770-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="75770-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="75770-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="75770-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="75770-165">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="75770-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="75770-166">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="75770-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="75770-167">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="75770-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="75770-168">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="75770-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="75770-169">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75770-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="75770-170">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75770-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="75770-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75770-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="75770-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="75770-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="75770-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75770-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="75770-174">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75770-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="75770-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="75770-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="75770-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="75770-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="75770-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="75770-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="75770-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="75770-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="75770-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="75770-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="75770-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75770-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
