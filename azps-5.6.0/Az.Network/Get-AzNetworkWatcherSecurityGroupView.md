---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 3d2fa4a0d5c98ae468466780cffc2ea6439343f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954369"
---
# <span data-ttu-id="b4a94-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b4a94-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="b4a94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4a94-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a94-103">Wyświetl skonfigurowane i efektywne reguły grupy zabezpieczeń sieciowych zastosowane do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4a94-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="b4a94-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b4a94-104">SYNTAX</span></span>

### <span data-ttu-id="b4a94-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b4a94-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4a94-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b4a94-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4a94-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b4a94-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4a94-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b4a94-108">DESCRIPTION</span></span>
<span data-ttu-id="b4a94-109">Ta Get-AzNetworkWatcherSecurityGroupView umożliwia wyświetlenie skonfigurowanych i efektywnych reguł grupy zabezpieczeń sieciowych zastosowanych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4a94-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="b4a94-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b4a94-110">EXAMPLES</span></span>

### <span data-ttu-id="b4a94-111">Przykład 1. Wywołanie widoku grupy zabezpieczeń na maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b4a94-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="b4a94-112">W powyższym przykładzie najpierw używamy regionalnego urządzenia Network Watcher, a następnie maszyny wirtualnej w regionie.</span><span class="sxs-lookup"><span data-stu-id="b4a94-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="b4a94-113">Następnie wywołamy widok grupy zabezpieczeń dla określonej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4a94-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="b4a94-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4a94-114">PARAMETERS</span></span>

### <span data-ttu-id="b4a94-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b4a94-115">-AsJob</span></span>
<span data-ttu-id="b4a94-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b4a94-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4a94-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a94-117">-DefaultProfile</span></span>
<span data-ttu-id="b4a94-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4a94-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4a94-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b4a94-119">-Location</span></span>
<span data-ttu-id="b4a94-120">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="b4a94-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b4a94-121">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4a94-121">-NetworkWatcher</span></span>
<span data-ttu-id="b4a94-122">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="b4a94-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="b4a94-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b4a94-123">-NetworkWatcherName</span></span>
<span data-ttu-id="b4a94-124">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="b4a94-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="b4a94-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a94-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4a94-126">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="b4a94-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b4a94-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="b4a94-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="b4a94-128">Docelowy identyfikator maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b4a94-128">The target VM Id</span></span>

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

### <span data-ttu-id="b4a94-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a94-129">CommonParameters</span></span>
<span data-ttu-id="b4a94-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4a94-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a94-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4a94-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a94-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4a94-132">INPUTS</span></span>

### <span data-ttu-id="b4a94-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4a94-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b4a94-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b4a94-134">System.String</span></span>

## <span data-ttu-id="b4a94-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4a94-135">OUTPUTS</span></span>

### <span data-ttu-id="b4a94-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="b4a94-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="b4a94-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b4a94-137">NOTES</span></span>
<span data-ttu-id="b4a94-138">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span><span class="sxs-lookup"><span data-stu-id="b4a94-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="b4a94-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4a94-139">RELATED LINKS</span></span>

[<span data-ttu-id="b4a94-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4a94-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b4a94-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4a94-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b4a94-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4a94-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b4a94-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b4a94-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b4a94-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b4a94-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b4a94-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b4a94-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b4a94-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b4a94-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b4a94-147">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b4a94-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b4a94-148">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b4a94-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b4a94-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b4a94-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b4a94-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b4a94-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b4a94-151">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b4a94-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b4a94-152">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4a94-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b4a94-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b4a94-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b4a94-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b4a94-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b4a94-155">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4a94-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4a94-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4a94-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4a94-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4a94-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4a94-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b4a94-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b4a94-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4a94-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4a94-160">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4a94-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4a94-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b4a94-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b4a94-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b4a94-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b4a94-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b4a94-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b4a94-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b4a94-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b4a94-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b4a94-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="b4a94-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4a94-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
