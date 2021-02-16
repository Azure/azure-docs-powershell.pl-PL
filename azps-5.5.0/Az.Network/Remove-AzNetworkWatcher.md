---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: fb2dfd74e4807aab76fb48a4593a8a46c4fe6f3f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406676"
---
# <span data-ttu-id="47086-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47086-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="47086-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47086-102">SYNOPSIS</span></span>
<span data-ttu-id="47086-103">Usuwa czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="47086-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="47086-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="47086-104">SYNTAX</span></span>

### <span data-ttu-id="47086-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="47086-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47086-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="47086-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47086-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="47086-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47086-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="47086-108">DESCRIPTION</span></span>
<span data-ttu-id="47086-109">Polecenie Remove-AzNetworkWatcher cmdlet usuwa zasób usługi Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="47086-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="47086-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="47086-110">EXAMPLES</span></span>

### <span data-ttu-id="47086-111">Przykład 1. Tworzenie i usuwanie czujki sieci</span><span class="sxs-lookup"><span data-stu-id="47086-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="47086-112">W tym przykładzie w grupie zasobów jest kreślarz sieciowy, a następnie natychmiast usuwany.</span><span class="sxs-lookup"><span data-stu-id="47086-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="47086-113">Pamiętaj, że dla każdego regionu na subskrypcję można utworzyć tylko jednego czujki sieciowej.</span><span class="sxs-lookup"><span data-stu-id="47086-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="47086-114">Aby pominąć monit podczas usuwania sieci wirtualnej, użyj flagi -Force.</span><span class="sxs-lookup"><span data-stu-id="47086-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="47086-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47086-115">PARAMETERS</span></span>

### <span data-ttu-id="47086-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="47086-116">-AsJob</span></span>
<span data-ttu-id="47086-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="47086-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47086-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47086-118">-DefaultProfile</span></span>
<span data-ttu-id="47086-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="47086-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47086-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="47086-120">-Location</span></span>
<span data-ttu-id="47086-121">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="47086-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="47086-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="47086-122">-Name</span></span>
<span data-ttu-id="47086-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="47086-123">The resource name.</span></span>

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

### <span data-ttu-id="47086-124">- NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47086-124">-NetworkWatcher</span></span>
<span data-ttu-id="47086-125">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="47086-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="47086-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47086-126">-PassThru</span></span>
<span data-ttu-id="47086-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="47086-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="47086-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47086-128">-ResourceGroupName</span></span>
<span data-ttu-id="47086-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="47086-129">The resource group name.</span></span>

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

### <span data-ttu-id="47086-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="47086-130">-Confirm</span></span>
<span data-ttu-id="47086-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="47086-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47086-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47086-132">-WhatIf</span></span>
<span data-ttu-id="47086-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47086-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47086-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="47086-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47086-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47086-135">CommonParameters</span></span>
<span data-ttu-id="47086-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47086-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47086-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47086-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47086-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47086-138">INPUTS</span></span>

### <span data-ttu-id="47086-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47086-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="47086-140">System.String</span><span class="sxs-lookup"><span data-stu-id="47086-140">System.String</span></span>

## <span data-ttu-id="47086-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47086-141">OUTPUTS</span></span>

### <span data-ttu-id="47086-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="47086-142">System.Boolean</span></span>

## <span data-ttu-id="47086-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="47086-143">NOTES</span></span>
<span data-ttu-id="47086-144">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span><span class="sxs-lookup"><span data-stu-id="47086-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="47086-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47086-145">RELATED LINKS</span></span>

[<span data-ttu-id="47086-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47086-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="47086-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47086-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="47086-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47086-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="47086-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="47086-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="47086-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="47086-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="47086-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="47086-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="47086-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="47086-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="47086-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="47086-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="47086-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="47086-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="47086-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="47086-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="47086-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="47086-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="47086-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="47086-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="47086-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="47086-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="47086-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="47086-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="47086-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="47086-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="47086-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47086-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47086-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47086-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47086-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47086-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47086-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="47086-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="47086-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47086-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47086-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47086-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47086-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="47086-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="47086-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="47086-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="47086-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="47086-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="47086-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="47086-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="47086-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="47086-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="47086-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47086-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
