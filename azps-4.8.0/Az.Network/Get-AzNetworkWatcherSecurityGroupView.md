---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 37da72dd26df32dddee0ea28d2378418e9e4922e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220036"
---
# <span data-ttu-id="cbc17-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cbc17-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="cbc17-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cbc17-102">SYNOPSIS</span></span>
<span data-ttu-id="cbc17-103">Wyświetl skonfigurowane i efektywne reguły grupowych zabezpieczeń sieci stosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cbc17-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="cbc17-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cbc17-104">SYNTAX</span></span>

### <span data-ttu-id="cbc17-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cbc17-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbc17-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="cbc17-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbc17-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="cbc17-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbc17-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cbc17-108">DESCRIPTION</span></span>
<span data-ttu-id="cbc17-109">Get-AzNetworkWatcherSecurityGroupView pozwala wyświetlić skonfigurowane i efektywne reguły grupowych zabezpieczeń sieci stosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cbc17-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="cbc17-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cbc17-110">EXAMPLES</span></span>

### <span data-ttu-id="cbc17-111">Przykład 1. Tworzenie grup zabezpieczeń w celu wyświetlania połączeń na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="cbc17-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="cbc17-112">W powyższym przykładzie najpierw jest wyświetlany regionalny Monitor sieci, a następnie maszyna wirtualna w regionie.</span><span class="sxs-lookup"><span data-stu-id="cbc17-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="cbc17-113">Następnie nawiązanie połączenia z grupą zabezpieczeń na określonej maszynie wirtualnej jest włączone.</span><span class="sxs-lookup"><span data-stu-id="cbc17-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="cbc17-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cbc17-114">PARAMETERS</span></span>

### <span data-ttu-id="cbc17-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbc17-115">-AsJob</span></span>
<span data-ttu-id="cbc17-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cbc17-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbc17-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbc17-117">-DefaultProfile</span></span>
<span data-ttu-id="cbc17-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cbc17-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbc17-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cbc17-119">-Location</span></span>
<span data-ttu-id="cbc17-120">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="cbc17-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="cbc17-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cbc17-121">-NetworkWatcher</span></span>
<span data-ttu-id="cbc17-122">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="cbc17-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="cbc17-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cbc17-123">-NetworkWatcherName</span></span>
<span data-ttu-id="cbc17-124">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="cbc17-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="cbc17-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbc17-125">-ResourceGroupName</span></span>
<span data-ttu-id="cbc17-126">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="cbc17-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="cbc17-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="cbc17-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="cbc17-128">Docelowy Identyfikator maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="cbc17-128">The target VM Id</span></span>

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

### <span data-ttu-id="cbc17-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbc17-129">CommonParameters</span></span>
<span data-ttu-id="cbc17-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbc17-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbc17-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbc17-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbc17-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbc17-132">INPUTS</span></span>

### <span data-ttu-id="cbc17-133">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cbc17-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="cbc17-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cbc17-134">System.String</span></span>

## <span data-ttu-id="cbc17-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cbc17-135">OUTPUTS</span></span>

### <span data-ttu-id="cbc17-136">Microsoft. Azure. Commands. Network. models. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="cbc17-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="cbc17-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cbc17-137">NOTES</span></span>
<span data-ttu-id="cbc17-138">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor sieciowy, przepływ, IP</span><span class="sxs-lookup"><span data-stu-id="cbc17-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="cbc17-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cbc17-139">RELATED LINKS</span></span>

[<span data-ttu-id="cbc17-140">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cbc17-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="cbc17-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cbc17-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="cbc17-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cbc17-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="cbc17-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cbc17-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="cbc17-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cbc17-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="cbc17-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cbc17-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="cbc17-146">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cbc17-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="cbc17-147">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cbc17-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cbc17-148">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cbc17-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="cbc17-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cbc17-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cbc17-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cbc17-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cbc17-151">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cbc17-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cbc17-152">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbc17-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="cbc17-153">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="cbc17-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="cbc17-154">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="cbc17-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="cbc17-155">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbc17-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cbc17-156">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbc17-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cbc17-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbc17-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cbc17-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="cbc17-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="cbc17-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbc17-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cbc17-160">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbc17-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cbc17-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cbc17-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="cbc17-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="cbc17-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="cbc17-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="cbc17-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="cbc17-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="cbc17-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="cbc17-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="cbc17-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="cbc17-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbc17-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
