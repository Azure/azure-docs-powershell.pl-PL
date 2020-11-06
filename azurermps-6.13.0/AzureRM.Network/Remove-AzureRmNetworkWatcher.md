---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
ms.openlocfilehash: a242c1cbeda2a110f7bb58e8c320f2e9b4d60ac8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552679"
---
# <span data-ttu-id="fae30-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fae30-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="fae30-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fae30-102">SYNOPSIS</span></span>
<span data-ttu-id="fae30-103">Usuwa Monitor sieci.</span><span class="sxs-lookup"><span data-stu-id="fae30-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fae30-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fae30-104">SYNTAX</span></span>

### <span data-ttu-id="fae30-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fae30-105">SetByResource</span></span>
```
Remove-AzureRmNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fae30-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="fae30-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fae30-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="fae30-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fae30-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fae30-108">DESCRIPTION</span></span>
<span data-ttu-id="fae30-109">Polecenie cmdlet Remove-AzureRmNetworkWatcher usuwa zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="fae30-109">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="fae30-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fae30-110">EXAMPLES</span></span>

### <span data-ttu-id="fae30-111">Przykład 1. Tworzenie i usuwanie obserwatora sieci</span><span class="sxs-lookup"><span data-stu-id="fae30-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="fae30-112">W tym przykładzie przedstawiono tworzenie obserwatora sieci w grupie zasobów, a następnie natychmiastowe usunięcie go.</span><span class="sxs-lookup"><span data-stu-id="fae30-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="fae30-113">Należy zauważyć, że dla każdego regionu można utworzyć tylko jeden Monitor sieci dla każdej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fae30-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="fae30-114">Aby zapobiec wyświetlaniu monitu podczas usuwania sieci wirtualnej, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="fae30-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="fae30-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fae30-115">PARAMETERS</span></span>

### <span data-ttu-id="fae30-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fae30-116">-AsJob</span></span>
<span data-ttu-id="fae30-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fae30-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fae30-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae30-118">-DefaultProfile</span></span>
<span data-ttu-id="fae30-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fae30-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae30-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fae30-120">-Location</span></span>
<span data-ttu-id="fae30-121">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="fae30-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="fae30-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fae30-122">-Name</span></span>
<span data-ttu-id="fae30-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="fae30-123">The resource name.</span></span>

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

### <span data-ttu-id="fae30-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fae30-124">-NetworkWatcher</span></span>
<span data-ttu-id="fae30-125">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="fae30-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="fae30-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fae30-126">-PassThru</span></span>
<span data-ttu-id="fae30-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fae30-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fae30-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fae30-128">-ResourceGroupName</span></span>
<span data-ttu-id="fae30-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fae30-129">The resource group name.</span></span>

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

### <span data-ttu-id="fae30-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fae30-130">-Confirm</span></span>
<span data-ttu-id="fae30-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fae30-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fae30-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fae30-132">-WhatIf</span></span>
<span data-ttu-id="fae30-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fae30-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fae30-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fae30-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fae30-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae30-135">CommonParameters</span></span>
<span data-ttu-id="fae30-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fae30-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae30-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fae30-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae30-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fae30-138">INPUTS</span></span>

### <span data-ttu-id="fae30-139">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fae30-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="fae30-140">Parametry: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fae30-140">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="fae30-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fae30-141">System.String</span></span>
<span data-ttu-id="fae30-142">Parametry: Name (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fae30-142">Parameters: Name (ByValue)</span></span>

## <span data-ttu-id="fae30-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fae30-143">OUTPUTS</span></span>

### <span data-ttu-id="fae30-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fae30-144">System.Boolean</span></span>

## <span data-ttu-id="fae30-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fae30-145">NOTES</span></span>
<span data-ttu-id="fae30-146">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, obserwator sieci</span><span class="sxs-lookup"><span data-stu-id="fae30-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="fae30-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fae30-147">RELATED LINKS</span></span>

[<span data-ttu-id="fae30-148">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fae30-148">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="fae30-149">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fae30-149">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="fae30-150">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fae30-150">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="fae30-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="fae30-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="fae30-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="fae30-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="fae30-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="fae30-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="fae30-154">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="fae30-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="fae30-155">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fae30-155">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fae30-156">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="fae30-156">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="fae30-157">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fae30-157">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fae30-158">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fae30-158">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fae30-159">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fae30-159">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fae30-160">Nowe — AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="fae30-160">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="fae30-161">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="fae30-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="fae30-162">Test — AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="fae30-162">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="fae30-163">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fae30-163">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fae30-164">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fae30-164">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fae30-165">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fae30-165">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fae30-166">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="fae30-166">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="fae30-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fae30-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fae30-168">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fae30-168">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fae30-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="fae30-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="fae30-170">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="fae30-170">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="fae30-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="fae30-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="fae30-172">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="fae30-172">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="fae30-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="fae30-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="fae30-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fae30-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
