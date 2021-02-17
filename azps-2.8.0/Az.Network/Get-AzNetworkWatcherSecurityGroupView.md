---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: e1b6b0339b093a048d6d74998ac6b0eb276e81cd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411011"
---
# <span data-ttu-id="c89b9-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c89b9-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="c89b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c89b9-102">SYNOPSIS</span></span>
<span data-ttu-id="c89b9-103">Wyświetl skonfigurowane i efektywne reguły grupy zabezpieczeń sieciowych zastosowane do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c89b9-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="c89b9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c89b9-104">SYNTAX</span></span>

### <span data-ttu-id="c89b9-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="c89b9-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c89b9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c89b9-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c89b9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c89b9-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c89b9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c89b9-108">DESCRIPTION</span></span>
<span data-ttu-id="c89b9-109">Ta Get-AzNetworkWatcherSecurityGroupView umożliwia wyświetlenie skonfigurowanych i efektywnych reguł grupy zabezpieczeń sieciowych zastosowanych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c89b9-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="c89b9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c89b9-110">EXAMPLES</span></span>

### <span data-ttu-id="c89b9-111">Przykład 1. Wywołanie widoku grupy zabezpieczeń na maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c89b9-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="c89b9-112">W powyższym przykładzie najpierw używamy regionalnego urządzenia Network Watcher, a następnie maszyny wirtualnej w regionie.</span><span class="sxs-lookup"><span data-stu-id="c89b9-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="c89b9-113">Następnie wywołamy widok grupy zabezpieczeń dla określonej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c89b9-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="c89b9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c89b9-114">PARAMETERS</span></span>

### <span data-ttu-id="c89b9-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c89b9-115">-AsJob</span></span>
<span data-ttu-id="c89b9-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c89b9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c89b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c89b9-117">-DefaultProfile</span></span>
<span data-ttu-id="c89b9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c89b9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c89b9-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c89b9-119">-Location</span></span>
<span data-ttu-id="c89b9-120">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="c89b9-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c89b9-121">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c89b9-121">-NetworkWatcher</span></span>
<span data-ttu-id="c89b9-122">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="c89b9-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="c89b9-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c89b9-123">-NetworkWatcherName</span></span>
<span data-ttu-id="c89b9-124">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="c89b9-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="c89b9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c89b9-125">-ResourceGroupName</span></span>
<span data-ttu-id="c89b9-126">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="c89b9-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c89b9-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="c89b9-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="c89b9-128">Docelowy identyfikator maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c89b9-128">The target VM Id</span></span>

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

### <span data-ttu-id="c89b9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c89b9-129">CommonParameters</span></span>
<span data-ttu-id="c89b9-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c89b9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c89b9-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c89b9-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c89b9-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c89b9-132">INPUTS</span></span>

### <span data-ttu-id="c89b9-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c89b9-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c89b9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c89b9-134">System.String</span></span>

## <span data-ttu-id="c89b9-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c89b9-135">OUTPUTS</span></span>

### <span data-ttu-id="c89b9-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="c89b9-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="c89b9-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c89b9-137">NOTES</span></span>
<span data-ttu-id="c89b9-138">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span><span class="sxs-lookup"><span data-stu-id="c89b9-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="c89b9-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c89b9-139">RELATED LINKS</span></span>

[<span data-ttu-id="c89b9-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c89b9-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c89b9-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c89b9-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c89b9-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c89b9-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c89b9-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c89b9-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c89b9-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c89b9-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c89b9-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c89b9-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c89b9-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c89b9-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c89b9-147">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c89b9-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c89b9-148">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c89b9-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c89b9-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c89b9-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c89b9-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c89b9-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c89b9-151">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c89b9-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c89b9-152">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c89b9-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c89b9-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c89b9-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c89b9-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c89b9-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c89b9-155">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c89b9-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c89b9-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c89b9-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c89b9-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c89b9-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c89b9-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c89b9-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c89b9-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c89b9-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c89b9-160">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c89b9-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c89b9-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c89b9-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c89b9-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c89b9-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c89b9-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c89b9-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c89b9-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c89b9-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c89b9-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c89b9-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c89b9-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c89b9-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
