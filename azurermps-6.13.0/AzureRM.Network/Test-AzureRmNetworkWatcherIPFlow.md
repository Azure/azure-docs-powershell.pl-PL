---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 6fc406d0af3ed451fbbf2f14c9ca8943256df744
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554038"
---
# <span data-ttu-id="a2e11-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a2e11-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="a2e11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2e11-102">SYNOPSIS</span></span>
<span data-ttu-id="a2e11-103">Zwraca możliwość, że pakiet jest dozwolony lub odmówiony lub pochodzi z określonego miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="a2e11-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2e11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2e11-104">SYNTAX</span></span>

### <span data-ttu-id="a2e11-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a2e11-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2e11-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a2e11-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2e11-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a2e11-107">SetByLocation</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2e11-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a2e11-108">DESCRIPTION</span></span>
<span data-ttu-id="a2e11-109">Polecenie cmdlet Test-AzureRmNetworkWatcherIPFlow dla określonego zasobu maszyny wirtualnej i pakiet o określonym kierunku przy użyciu lokalnych i zdalnych adresów IP oraz portów zwraca wartość, czy pakiet jest dozwolony, czy zabroniony.</span><span class="sxs-lookup"><span data-stu-id="a2e11-109">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="a2e11-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2e11-110">EXAMPLES</span></span>

### <span data-ttu-id="a2e11-111">Przykład 1: Uruchom Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a2e11-111">Example 1: Run Test-AzureRmNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="a2e11-112">W przypadku tej subskrypcji jest wyświetlany Monitor sieci na zachodnich centralach w USA, a następnie jest pobierana ta maszyna wirtualna i skojarzone z nią interfejsy sieciowe.</span><span class="sxs-lookup"><span data-stu-id="a2e11-112">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="a2e11-113">Następnie w pierwszym interfejsie sieciowym zostanie uruchomiona Test-AzureRmNetworkWatcherIPFlow przy użyciu pierwszego adresu IP od pierwszego interfejsu sieciowego w celu połączenia wychodzącego z adresem IP w Internecie.</span><span class="sxs-lookup"><span data-stu-id="a2e11-113">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="a2e11-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2e11-114">PARAMETERS</span></span>

### <span data-ttu-id="a2e11-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2e11-115">-AsJob</span></span>
<span data-ttu-id="a2e11-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a2e11-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2e11-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2e11-117">-DefaultProfile</span></span>
<span data-ttu-id="a2e11-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2e11-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2e11-119">-Direction</span><span class="sxs-lookup"><span data-stu-id="a2e11-119">-Direction</span></span>
<span data-ttu-id="a2e11-120">Obszar.</span><span class="sxs-lookup"><span data-stu-id="a2e11-120">Direction.</span></span>

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

### <span data-ttu-id="a2e11-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="a2e11-121">-LocalIPAddress</span></span>
<span data-ttu-id="a2e11-122">Lokalny adres IP.</span><span class="sxs-lookup"><span data-stu-id="a2e11-122">Local IP Address.</span></span>

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

### <span data-ttu-id="a2e11-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="a2e11-123">-LocalPort</span></span>
<span data-ttu-id="a2e11-124">Port lokalny.</span><span class="sxs-lookup"><span data-stu-id="a2e11-124">Local Port.</span></span>

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

### <span data-ttu-id="a2e11-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a2e11-125">-Location</span></span>
<span data-ttu-id="a2e11-126">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="a2e11-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a2e11-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2e11-127">-NetworkWatcher</span></span>
<span data-ttu-id="a2e11-128">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="a2e11-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="a2e11-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a2e11-129">-NetworkWatcherName</span></span>
<span data-ttu-id="a2e11-130">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="a2e11-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="a2e11-131">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="a2e11-131">-Protocol</span></span>
<span data-ttu-id="a2e11-132">Sterownika.</span><span class="sxs-lookup"><span data-stu-id="a2e11-132">Protocol.</span></span>

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

### <span data-ttu-id="a2e11-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="a2e11-133">-RemoteIPAddress</span></span>
<span data-ttu-id="a2e11-134">Zdalny adres IP.</span><span class="sxs-lookup"><span data-stu-id="a2e11-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="a2e11-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="a2e11-135">-RemotePort</span></span>
<span data-ttu-id="a2e11-136">Port zdalny.</span><span class="sxs-lookup"><span data-stu-id="a2e11-136">Remote port.</span></span>

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

### <span data-ttu-id="a2e11-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2e11-137">-ResourceGroupName</span></span>
<span data-ttu-id="a2e11-138">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="a2e11-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a2e11-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="a2e11-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="a2e11-140">Identyfikator interfejsu sieci docelowej.</span><span class="sxs-lookup"><span data-stu-id="a2e11-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="a2e11-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="a2e11-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="a2e11-142">Docelowy Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a2e11-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="a2e11-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2e11-143">CommonParameters</span></span>
<span data-ttu-id="a2e11-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2e11-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2e11-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2e11-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2e11-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2e11-146">INPUTS</span></span>

### <span data-ttu-id="a2e11-147">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2e11-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a2e11-148">Parametry: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a2e11-148">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="a2e11-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a2e11-149">System.String</span></span>
<span data-ttu-id="a2e11-150">Parametry: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a2e11-150">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="a2e11-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2e11-151">OUTPUTS</span></span>

### <span data-ttu-id="a2e11-152">Microsoft. Azure. Commands. Network. models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="a2e11-152">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="a2e11-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2e11-153">NOTES</span></span>
<span data-ttu-id="a2e11-154">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor sieciowy, przepływ, IP</span><span class="sxs-lookup"><span data-stu-id="a2e11-154">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="a2e11-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2e11-155">RELATED LINKS</span></span>

[<span data-ttu-id="a2e11-156">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2e11-156">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a2e11-157">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2e11-157">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a2e11-158">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2e11-158">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a2e11-159">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a2e11-159">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="a2e11-160">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a2e11-160">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a2e11-161">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a2e11-161">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="a2e11-162">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a2e11-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a2e11-163">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2e11-163">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2e11-164">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a2e11-164">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="a2e11-165">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2e11-165">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2e11-166">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2e11-166">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2e11-167">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2e11-167">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2e11-168">Nowe — AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2e11-168">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a2e11-169">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a2e11-169">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="a2e11-170">Test — AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a2e11-170">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="a2e11-171">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2e11-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a2e11-172">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2e11-172">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a2e11-173">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2e11-173">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a2e11-174">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a2e11-174">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a2e11-175">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2e11-175">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a2e11-176">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2e11-176">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a2e11-177">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a2e11-177">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a2e11-178">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a2e11-178">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a2e11-179">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a2e11-179">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a2e11-180">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a2e11-180">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a2e11-181">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a2e11-181">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="a2e11-182">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2e11-182">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
