---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: 7c8f33d8339bb873b713acabd71ca57fe9107383
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343366"
---
# <span data-ttu-id="5cd22-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5cd22-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="5cd22-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5cd22-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd22-103">Tworzy nowy zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="5cd22-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="5cd22-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5cd22-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cd22-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5cd22-105">DESCRIPTION</span></span>
<span data-ttu-id="5cd22-106">Polecenie cmdlet New-AzNetworkWatcher tworzy nowy zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="5cd22-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="5cd22-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5cd22-107">EXAMPLES</span></span>

### <span data-ttu-id="5cd22-108">Przykład 1. Tworzenie obserwatora sieci</span><span class="sxs-lookup"><span data-stu-id="5cd22-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="5cd22-109">W tym przykładzie utworzono nowy Monitor sieci w nowo utworzonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="5cd22-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="5cd22-110">Należy zauważyć, że dla każdego regionu można utworzyć tylko jeden Monitor sieci dla każdej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5cd22-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="5cd22-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5cd22-111">PARAMETERS</span></span>

### <span data-ttu-id="5cd22-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd22-112">-DefaultProfile</span></span>
<span data-ttu-id="5cd22-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5cd22-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cd22-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5cd22-114">-Location</span></span>
<span data-ttu-id="5cd22-115">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="5cd22-115">Location.</span></span>

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

### <span data-ttu-id="5cd22-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5cd22-116">-Name</span></span>
<span data-ttu-id="5cd22-117">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="5cd22-117">The network watcher name.</span></span>

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

### <span data-ttu-id="5cd22-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cd22-118">-ResourceGroupName</span></span>
<span data-ttu-id="5cd22-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5cd22-119">The resource group name.</span></span>

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

### <span data-ttu-id="5cd22-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="5cd22-120">-Tag</span></span>
<span data-ttu-id="5cd22-121">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="5cd22-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5cd22-122">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="5cd22-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5cd22-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5cd22-123">-Confirm</span></span>
<span data-ttu-id="5cd22-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cd22-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cd22-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cd22-125">-WhatIf</span></span>
<span data-ttu-id="5cd22-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cd22-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cd22-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5cd22-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cd22-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd22-128">CommonParameters</span></span>
<span data-ttu-id="5cd22-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cd22-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd22-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cd22-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd22-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5cd22-131">INPUTS</span></span>

### <span data-ttu-id="5cd22-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5cd22-132">System.String</span></span>

### <span data-ttu-id="5cd22-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5cd22-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5cd22-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5cd22-134">OUTPUTS</span></span>

### <span data-ttu-id="5cd22-135">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5cd22-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="5cd22-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5cd22-136">NOTES</span></span>
<span data-ttu-id="5cd22-137">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, obserwator sieci</span><span class="sxs-lookup"><span data-stu-id="5cd22-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="5cd22-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5cd22-138">RELATED LINKS</span></span>

[<span data-ttu-id="5cd22-139">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5cd22-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="5cd22-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5cd22-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="5cd22-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5cd22-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="5cd22-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5cd22-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="5cd22-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5cd22-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5cd22-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5cd22-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="5cd22-145">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5cd22-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5cd22-146">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5cd22-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5cd22-147">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5cd22-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="5cd22-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5cd22-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5cd22-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5cd22-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5cd22-150">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5cd22-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5cd22-151">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5cd22-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="5cd22-152">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5cd22-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="5cd22-153">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="5cd22-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="5cd22-154">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5cd22-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5cd22-155">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5cd22-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5cd22-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5cd22-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5cd22-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5cd22-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5cd22-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5cd22-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5cd22-159">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5cd22-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5cd22-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5cd22-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5cd22-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="5cd22-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="5cd22-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5cd22-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="5cd22-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5cd22-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="5cd22-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5cd22-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="5cd22-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5cd22-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
