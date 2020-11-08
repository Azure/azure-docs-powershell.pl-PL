---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 37da72dd26df32dddee0ea28d2378418e9e4922e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234429"
---
# <span data-ttu-id="18d0d-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="18d0d-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="18d0d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18d0d-102">SYNOPSIS</span></span>
<span data-ttu-id="18d0d-103">Wyświetl skonfigurowane i efektywne reguły grupowych zabezpieczeń sieci stosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18d0d-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="18d0d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18d0d-104">SYNTAX</span></span>

### <span data-ttu-id="18d0d-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="18d0d-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18d0d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="18d0d-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18d0d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="18d0d-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18d0d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="18d0d-108">DESCRIPTION</span></span>
<span data-ttu-id="18d0d-109">Get-AzNetworkWatcherSecurityGroupView pozwala wyświetlić skonfigurowane i efektywne reguły grupowych zabezpieczeń sieci stosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18d0d-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="18d0d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18d0d-110">EXAMPLES</span></span>

### <span data-ttu-id="18d0d-111">Przykład 1. Tworzenie grup zabezpieczeń w celu wyświetlania połączeń na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="18d0d-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="18d0d-112">W powyższym przykładzie najpierw jest wyświetlany regionalny Monitor sieci, a następnie maszyna wirtualna w regionie.</span><span class="sxs-lookup"><span data-stu-id="18d0d-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="18d0d-113">Następnie nawiązanie połączenia z grupą zabezpieczeń na określonej maszynie wirtualnej jest włączone.</span><span class="sxs-lookup"><span data-stu-id="18d0d-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="18d0d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18d0d-114">PARAMETERS</span></span>

### <span data-ttu-id="18d0d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18d0d-115">-AsJob</span></span>
<span data-ttu-id="18d0d-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="18d0d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18d0d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18d0d-117">-DefaultProfile</span></span>
<span data-ttu-id="18d0d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18d0d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18d0d-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="18d0d-119">-Location</span></span>
<span data-ttu-id="18d0d-120">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="18d0d-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="18d0d-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="18d0d-121">-NetworkWatcher</span></span>
<span data-ttu-id="18d0d-122">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="18d0d-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="18d0d-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="18d0d-123">-NetworkWatcherName</span></span>
<span data-ttu-id="18d0d-124">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="18d0d-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="18d0d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18d0d-125">-ResourceGroupName</span></span>
<span data-ttu-id="18d0d-126">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="18d0d-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="18d0d-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="18d0d-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="18d0d-128">Docelowy Identyfikator maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="18d0d-128">The target VM Id</span></span>

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

### <span data-ttu-id="18d0d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18d0d-129">CommonParameters</span></span>
<span data-ttu-id="18d0d-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18d0d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18d0d-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18d0d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18d0d-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18d0d-132">INPUTS</span></span>

### <span data-ttu-id="18d0d-133">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="18d0d-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="18d0d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="18d0d-134">System.String</span></span>

## <span data-ttu-id="18d0d-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18d0d-135">OUTPUTS</span></span>

### <span data-ttu-id="18d0d-136">Microsoft. Azure. Commands. Network. models. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="18d0d-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="18d0d-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18d0d-137">NOTES</span></span>
<span data-ttu-id="18d0d-138">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor sieciowy, przepływ, IP</span><span class="sxs-lookup"><span data-stu-id="18d0d-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="18d0d-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18d0d-139">RELATED LINKS</span></span>

[<span data-ttu-id="18d0d-140">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="18d0d-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="18d0d-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="18d0d-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="18d0d-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="18d0d-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="18d0d-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="18d0d-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="18d0d-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="18d0d-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="18d0d-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="18d0d-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="18d0d-146">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="18d0d-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="18d0d-147">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="18d0d-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="18d0d-148">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="18d0d-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="18d0d-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="18d0d-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="18d0d-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="18d0d-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="18d0d-151">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="18d0d-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="18d0d-152">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="18d0d-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="18d0d-153">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="18d0d-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="18d0d-154">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="18d0d-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="18d0d-155">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18d0d-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="18d0d-156">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18d0d-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="18d0d-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18d0d-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="18d0d-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="18d0d-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="18d0d-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18d0d-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="18d0d-160">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18d0d-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="18d0d-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="18d0d-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="18d0d-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="18d0d-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="18d0d-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="18d0d-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="18d0d-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="18d0d-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="18d0d-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="18d0d-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="18d0d-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="18d0d-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
