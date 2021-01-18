---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: cce361870f6dc65f644264e52b331c209177668f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503212"
---
# <span data-ttu-id="bfe2c-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bfe2c-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="bfe2c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bfe2c-102">SYNOPSIS</span></span>
<span data-ttu-id="bfe2c-103">Usuwa Monitor sieci.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="bfe2c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bfe2c-104">SYNTAX</span></span>

### <span data-ttu-id="bfe2c-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bfe2c-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfe2c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="bfe2c-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfe2c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="bfe2c-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfe2c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bfe2c-108">DESCRIPTION</span></span>
<span data-ttu-id="bfe2c-109">Polecenie cmdlet Remove-AzNetworkWatcher usuwa zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="bfe2c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bfe2c-110">EXAMPLES</span></span>

### <span data-ttu-id="bfe2c-111">Przykład 1. Tworzenie i usuwanie obserwatora sieci</span><span class="sxs-lookup"><span data-stu-id="bfe2c-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="bfe2c-112">W tym przykładzie przedstawiono tworzenie obserwatora sieci w grupie zasobów, a następnie natychmiastowe usunięcie go.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="bfe2c-113">Należy zauważyć, że dla każdego regionu można utworzyć tylko jeden Monitor sieci dla każdej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="bfe2c-114">Aby zapobiec wyświetlaniu monitu podczas usuwania sieci wirtualnej, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="bfe2c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bfe2c-115">PARAMETERS</span></span>

### <span data-ttu-id="bfe2c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bfe2c-116">-AsJob</span></span>
<span data-ttu-id="bfe2c-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bfe2c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bfe2c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfe2c-118">-DefaultProfile</span></span>
<span data-ttu-id="bfe2c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfe2c-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bfe2c-120">-Location</span></span>
<span data-ttu-id="bfe2c-121">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="bfe2c-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bfe2c-122">-Name</span></span>
<span data-ttu-id="bfe2c-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe2c-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bfe2c-124">-NetworkWatcher</span></span>
<span data-ttu-id="bfe2c-125">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="bfe2c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfe2c-126">-PassThru</span></span>
<span data-ttu-id="bfe2c-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-127">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfe2c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfe2c-128">-ResourceGroupName</span></span>
<span data-ttu-id="bfe2c-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-129">The resource group name.</span></span>

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

### <span data-ttu-id="bfe2c-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bfe2c-130">-Confirm</span></span>
<span data-ttu-id="bfe2c-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfe2c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfe2c-132">-WhatIf</span></span>
<span data-ttu-id="bfe2c-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfe2c-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfe2c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfe2c-135">CommonParameters</span></span>
<span data-ttu-id="bfe2c-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfe2c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfe2c-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfe2c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfe2c-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfe2c-138">INPUTS</span></span>

### <span data-ttu-id="bfe2c-139">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bfe2c-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="bfe2c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bfe2c-140">System.String</span></span>

## <span data-ttu-id="bfe2c-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bfe2c-141">OUTPUTS</span></span>

### <span data-ttu-id="bfe2c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bfe2c-142">System.Boolean</span></span>

## <span data-ttu-id="bfe2c-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bfe2c-143">NOTES</span></span>
<span data-ttu-id="bfe2c-144">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, obserwator sieci</span><span class="sxs-lookup"><span data-stu-id="bfe2c-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="bfe2c-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfe2c-145">RELATED LINKS</span></span>

[<span data-ttu-id="bfe2c-146">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bfe2c-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="bfe2c-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bfe2c-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="bfe2c-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bfe2c-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="bfe2c-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="bfe2c-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="bfe2c-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="bfe2c-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="bfe2c-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="bfe2c-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="bfe2c-152">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="bfe2c-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="bfe2c-153">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bfe2c-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bfe2c-154">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="bfe2c-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="bfe2c-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bfe2c-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bfe2c-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bfe2c-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bfe2c-157">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bfe2c-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bfe2c-158">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfe2c-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="bfe2c-159">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="bfe2c-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="bfe2c-160">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="bfe2c-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="bfe2c-161">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bfe2c-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bfe2c-162">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bfe2c-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bfe2c-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bfe2c-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bfe2c-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="bfe2c-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="bfe2c-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bfe2c-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bfe2c-166">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bfe2c-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bfe2c-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="bfe2c-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="bfe2c-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="bfe2c-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="bfe2c-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="bfe2c-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="bfe2c-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="bfe2c-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="bfe2c-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="bfe2c-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="bfe2c-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bfe2c-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
