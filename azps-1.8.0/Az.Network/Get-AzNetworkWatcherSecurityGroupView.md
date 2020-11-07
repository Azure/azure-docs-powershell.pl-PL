---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: f40b7e28bce34ef9e4cc289bed7f8c4524ef49d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709483"
---
# <span data-ttu-id="889ab-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="889ab-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="889ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="889ab-102">SYNOPSIS</span></span>
<span data-ttu-id="889ab-103">Wyświetl skonfigurowane i efektywne reguły grupowych zabezpieczeń sieci stosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="889ab-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="889ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="889ab-104">SYNTAX</span></span>

### <span data-ttu-id="889ab-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="889ab-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="889ab-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="889ab-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="889ab-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="889ab-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="889ab-108">Opis</span><span class="sxs-lookup"><span data-stu-id="889ab-108">DESCRIPTION</span></span>
<span data-ttu-id="889ab-109">Get-AzNetworkWatcherSecurityGroupView pozwala wyświetlić skonfigurowane i efektywne reguły grupowych zabezpieczeń sieci stosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="889ab-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="889ab-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="889ab-110">EXAMPLES</span></span>

### <span data-ttu-id="889ab-111">Przykład 1. Tworzenie grup zabezpieczeń w celu wyświetlania połączeń na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="889ab-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="889ab-112">W powyższym przykładzie najpierw jest wyświetlany regionalny Monitor sieci, a następnie maszyna wirtualna w regionie.</span><span class="sxs-lookup"><span data-stu-id="889ab-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="889ab-113">Następnie nawiązanie połączenia z grupą zabezpieczeń na określonej maszynie wirtualnej jest włączone.</span><span class="sxs-lookup"><span data-stu-id="889ab-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="889ab-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="889ab-114">PARAMETERS</span></span>

### <span data-ttu-id="889ab-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="889ab-115">-AsJob</span></span>
<span data-ttu-id="889ab-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="889ab-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="889ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="889ab-117">-DefaultProfile</span></span>
<span data-ttu-id="889ab-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="889ab-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="889ab-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="889ab-119">-Location</span></span>
<span data-ttu-id="889ab-120">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="889ab-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="889ab-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="889ab-121">-NetworkWatcher</span></span>
<span data-ttu-id="889ab-122">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="889ab-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="889ab-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="889ab-123">-NetworkWatcherName</span></span>
<span data-ttu-id="889ab-124">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="889ab-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="889ab-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="889ab-125">-ResourceGroupName</span></span>
<span data-ttu-id="889ab-126">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="889ab-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="889ab-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="889ab-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="889ab-128">Docelowy Identyfikator maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="889ab-128">The target VM Id</span></span>

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

### <span data-ttu-id="889ab-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="889ab-129">CommonParameters</span></span>
<span data-ttu-id="889ab-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="889ab-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="889ab-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="889ab-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="889ab-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="889ab-132">INPUTS</span></span>

### <span data-ttu-id="889ab-133">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="889ab-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="889ab-134">System. String</span><span class="sxs-lookup"><span data-stu-id="889ab-134">System.String</span></span>

## <span data-ttu-id="889ab-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="889ab-135">OUTPUTS</span></span>

### <span data-ttu-id="889ab-136">Microsoft. Azure. Commands. Network. models. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="889ab-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="889ab-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="889ab-137">NOTES</span></span>
<span data-ttu-id="889ab-138">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor sieciowy, przepływ, IP</span><span class="sxs-lookup"><span data-stu-id="889ab-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="889ab-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="889ab-139">RELATED LINKS</span></span>

[<span data-ttu-id="889ab-140">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="889ab-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="889ab-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="889ab-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="889ab-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="889ab-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="889ab-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="889ab-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="889ab-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="889ab-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="889ab-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="889ab-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="889ab-146">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="889ab-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="889ab-147">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="889ab-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="889ab-148">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="889ab-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="889ab-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="889ab-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="889ab-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="889ab-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="889ab-151">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="889ab-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="889ab-152">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="889ab-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="889ab-153">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="889ab-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="889ab-154">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="889ab-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="889ab-155">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="889ab-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="889ab-156">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="889ab-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="889ab-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="889ab-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="889ab-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="889ab-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="889ab-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="889ab-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="889ab-160">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="889ab-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="889ab-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="889ab-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="889ab-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="889ab-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="889ab-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="889ab-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="889ab-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="889ab-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="889ab-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="889ab-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="889ab-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="889ab-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)