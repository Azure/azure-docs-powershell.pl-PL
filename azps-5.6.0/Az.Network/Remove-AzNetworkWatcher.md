---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: be611f42d07f354bbcd0d98b55a2ae8cfbd27344
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976634"
---
# <span data-ttu-id="64d97-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64d97-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="64d97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64d97-102">SYNOPSIS</span></span>
<span data-ttu-id="64d97-103">Usuwa czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="64d97-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="64d97-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="64d97-104">SYNTAX</span></span>

### <span data-ttu-id="64d97-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="64d97-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64d97-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="64d97-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64d97-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="64d97-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64d97-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="64d97-108">DESCRIPTION</span></span>
<span data-ttu-id="64d97-109">Polecenie Remove-AzNetworkWatcher cmdlet usuwa zasób usługi Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="64d97-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="64d97-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="64d97-110">EXAMPLES</span></span>

### <span data-ttu-id="64d97-111">Przykład 1. Tworzenie i usuwanie czujki sieci</span><span class="sxs-lookup"><span data-stu-id="64d97-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="64d97-112">W tym przykładzie w grupie zasobów jest kreślarz sieciowy, a następnie natychmiast usuwany.</span><span class="sxs-lookup"><span data-stu-id="64d97-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="64d97-113">Pamiętaj, że dla każdego regionu na subskrypcję można utworzyć tylko jednego czujki sieciowej.</span><span class="sxs-lookup"><span data-stu-id="64d97-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="64d97-114">Aby pominąć monit podczas usuwania sieci wirtualnej, użyj flagi -Force.</span><span class="sxs-lookup"><span data-stu-id="64d97-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="64d97-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64d97-115">PARAMETERS</span></span>

### <span data-ttu-id="64d97-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="64d97-116">-AsJob</span></span>
<span data-ttu-id="64d97-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="64d97-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64d97-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d97-118">-DefaultProfile</span></span>
<span data-ttu-id="64d97-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="64d97-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64d97-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="64d97-120">-Location</span></span>
<span data-ttu-id="64d97-121">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="64d97-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="64d97-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="64d97-122">-Name</span></span>
<span data-ttu-id="64d97-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="64d97-123">The resource name.</span></span>

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

### <span data-ttu-id="64d97-124">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64d97-124">-NetworkWatcher</span></span>
<span data-ttu-id="64d97-125">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="64d97-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="64d97-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64d97-126">-PassThru</span></span>
<span data-ttu-id="64d97-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="64d97-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="64d97-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64d97-128">-ResourceGroupName</span></span>
<span data-ttu-id="64d97-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="64d97-129">The resource group name.</span></span>

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

### <span data-ttu-id="64d97-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64d97-130">-Confirm</span></span>
<span data-ttu-id="64d97-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="64d97-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64d97-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64d97-132">-WhatIf</span></span>
<span data-ttu-id="64d97-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64d97-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64d97-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="64d97-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64d97-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d97-135">CommonParameters</span></span>
<span data-ttu-id="64d97-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64d97-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d97-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64d97-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d97-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64d97-138">INPUTS</span></span>

### <span data-ttu-id="64d97-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64d97-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="64d97-140">System.String</span><span class="sxs-lookup"><span data-stu-id="64d97-140">System.String</span></span>

## <span data-ttu-id="64d97-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64d97-141">OUTPUTS</span></span>

### <span data-ttu-id="64d97-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="64d97-142">System.Boolean</span></span>

## <span data-ttu-id="64d97-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="64d97-143">NOTES</span></span>
<span data-ttu-id="64d97-144">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span><span class="sxs-lookup"><span data-stu-id="64d97-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="64d97-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64d97-145">RELATED LINKS</span></span>

[<span data-ttu-id="64d97-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64d97-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="64d97-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64d97-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="64d97-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64d97-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="64d97-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="64d97-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="64d97-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="64d97-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="64d97-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="64d97-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="64d97-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="64d97-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="64d97-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64d97-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64d97-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="64d97-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="64d97-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64d97-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64d97-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64d97-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64d97-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64d97-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64d97-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="64d97-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="64d97-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="64d97-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="64d97-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="64d97-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="64d97-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64d97-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64d97-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64d97-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64d97-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64d97-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64d97-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="64d97-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="64d97-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64d97-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64d97-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64d97-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64d97-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="64d97-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="64d97-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="64d97-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="64d97-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="64d97-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="64d97-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="64d97-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="64d97-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="64d97-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="64d97-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64d97-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
