---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: f38250a4beed7eb05f758e17a1d3d17f1d76f86e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400199"
---
# <span data-ttu-id="a1b1b-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a1b1b-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="a1b1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b1b-103">Tworzy nowy zasób Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="a1b1b-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="a1b1b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a1b1b-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1b1b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a1b1b-105">DESCRIPTION</span></span>
<span data-ttu-id="a1b1b-106">Polecenie New-AzNetworkWatcher cmdlet tworzy nowy zasób usługi Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="a1b1b-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="a1b1b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a1b1b-107">EXAMPLES</span></span>

### <span data-ttu-id="a1b1b-108">Przykład 1. Tworzenie czujki sieci</span><span class="sxs-lookup"><span data-stu-id="a1b1b-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="a1b1b-109">W tym przykładzie jest tworzona nowa czujka sieci w nowo utworzonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a1b1b-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="a1b1b-110">Pamiętaj, że w ramach jednej subskrypcji można utworzyć tylko jednego czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="a1b1b-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="a1b1b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1b1b-111">PARAMETERS</span></span>

### <span data-ttu-id="a1b1b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b1b-112">-DefaultProfile</span></span>
<span data-ttu-id="a1b1b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b1b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1b1b-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a1b1b-114">-Location</span></span>
<span data-ttu-id="a1b1b-115">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="a1b1b-115">Location.</span></span>

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

### <span data-ttu-id="a1b1b-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a1b1b-116">-Name</span></span>
<span data-ttu-id="a1b1b-117">Nazwa sieciowego czujki.</span><span class="sxs-lookup"><span data-stu-id="a1b1b-117">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b1b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b1b-118">-ResourceGroupName</span></span>
<span data-ttu-id="a1b1b-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a1b1b-119">The resource group name.</span></span>

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

### <span data-ttu-id="a1b1b-120">— Tag</span><span class="sxs-lookup"><span data-stu-id="a1b1b-120">-Tag</span></span>
<span data-ttu-id="a1b1b-121">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="a1b1b-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a1b1b-122">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="a1b1b-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b1b-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1b1b-123">-Confirm</span></span>
<span data-ttu-id="a1b1b-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a1b1b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1b1b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1b1b-125">-WhatIf</span></span>
<span data-ttu-id="a1b1b-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1b1b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1b1b-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a1b1b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1b1b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b1b-128">CommonParameters</span></span>
<span data-ttu-id="a1b1b-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b1b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b1b-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1b1b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b1b-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1b1b-131">INPUTS</span></span>

### <span data-ttu-id="a1b1b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a1b1b-132">System.String</span></span>

### <span data-ttu-id="a1b1b-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a1b1b-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a1b1b-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a1b1b-134">OUTPUTS</span></span>

### <span data-ttu-id="a1b1b-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a1b1b-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="a1b1b-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a1b1b-136">NOTES</span></span>
<span data-ttu-id="a1b1b-137">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span><span class="sxs-lookup"><span data-stu-id="a1b1b-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="a1b1b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1b1b-138">RELATED LINKS</span></span>

[<span data-ttu-id="a1b1b-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a1b1b-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a1b1b-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a1b1b-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a1b1b-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a1b1b-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a1b1b-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a1b1b-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a1b1b-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a1b1b-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a1b1b-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a1b1b-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a1b1b-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a1b1b-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a1b1b-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a1b1b-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a1b1b-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a1b1b-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a1b1b-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a1b1b-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a1b1b-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a1b1b-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a1b1b-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a1b1b-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a1b1b-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1b1b-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a1b1b-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a1b1b-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a1b1b-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a1b1b-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a1b1b-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a1b1b-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a1b1b-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a1b1b-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a1b1b-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a1b1b-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a1b1b-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a1b1b-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a1b1b-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a1b1b-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a1b1b-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a1b1b-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a1b1b-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a1b1b-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a1b1b-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a1b1b-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a1b1b-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a1b1b-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a1b1b-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a1b1b-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a1b1b-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a1b1b-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a1b1b-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a1b1b-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
