---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 871509fc03a7cb80735b6f011a7103350fd945ac
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401236"
---
# <span data-ttu-id="afaad-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="afaad-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="afaad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afaad-102">SYNOPSIS</span></span>
<span data-ttu-id="afaad-103">Uzyskuje wynik rozwiązywania problemów z wcześniej uruchomionej lub obecnie uruchomionej operacji rozwiązywania problemów.</span><span class="sxs-lookup"><span data-stu-id="afaad-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="afaad-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="afaad-104">SYNTAX</span></span>

### <span data-ttu-id="afaad-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="afaad-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afaad-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="afaad-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afaad-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="afaad-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afaad-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="afaad-108">DESCRIPTION</span></span>
<span data-ttu-id="afaad-109">Polecenie Get-AzNetworkWatcherTroubleshootingResult cmdlet pobiera wynik rozwiązywania problemów z wcześniej uruchomionej lub Start-AzNetworkWatcherResourceTroubleshooting operacji.</span><span class="sxs-lookup"><span data-stu-id="afaad-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="afaad-110">Jeśli operacja rozwiązywania problemów jest obecnie w toku, jej ukończenie może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="afaad-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="afaad-111">Obecnie bramy i połączenia sieci wirtualnej są obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="afaad-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="afaad-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="afaad-112">EXAMPLES</span></span>

### <span data-ttu-id="afaad-113">Przykład 1. Rozpoczynanie rozwiązywania problemów z bramą sieci wirtualnej i pobieranie wyników</span><span class="sxs-lookup"><span data-stu-id="afaad-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="afaad-114">Powyższy przykład rozpoczyna rozwiązywanie problemów w wirtualnej bramie sieciowej.</span><span class="sxs-lookup"><span data-stu-id="afaad-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="afaad-115">Operacja może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="afaad-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="afaad-116">Po zakończeniu rozwiązywania problemów Get-AzNetworkWatcherTroubleshootingResult do zasobu jest dzwonienie w celu pobrania wyniku tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="afaad-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="afaad-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afaad-117">PARAMETERS</span></span>

### <span data-ttu-id="afaad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afaad-118">-DefaultProfile</span></span>
<span data-ttu-id="afaad-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="afaad-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afaad-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="afaad-120">-Location</span></span>
<span data-ttu-id="afaad-121">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="afaad-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="afaad-122">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="afaad-122">-NetworkWatcher</span></span>
<span data-ttu-id="afaad-123">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="afaad-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="afaad-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="afaad-124">-NetworkWatcherName</span></span>
<span data-ttu-id="afaad-125">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="afaad-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="afaad-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afaad-126">-ResourceGroupName</span></span>
<span data-ttu-id="afaad-127">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="afaad-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="afaad-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="afaad-128">-TargetResourceId</span></span>
<span data-ttu-id="afaad-129">Identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="afaad-129">The target resource ID.</span></span>

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

### <span data-ttu-id="afaad-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afaad-130">CommonParameters</span></span>
<span data-ttu-id="afaad-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afaad-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afaad-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afaad-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afaad-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afaad-133">INPUTS</span></span>

### <span data-ttu-id="afaad-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="afaad-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="afaad-135">System.String</span><span class="sxs-lookup"><span data-stu-id="afaad-135">System.String</span></span>

## <span data-ttu-id="afaad-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="afaad-136">OUTPUTS</span></span>

### <span data-ttu-id="afaad-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="afaad-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="afaad-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="afaad-138">NOTES</span></span>
<span data-ttu-id="afaad-139">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span><span class="sxs-lookup"><span data-stu-id="afaad-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="afaad-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="afaad-140">RELATED LINKS</span></span>

[<span data-ttu-id="afaad-141">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="afaad-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="afaad-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="afaad-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="afaad-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="afaad-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="afaad-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="afaad-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="afaad-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="afaad-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="afaad-146">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="afaad-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="afaad-147">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="afaad-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="afaad-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="afaad-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="afaad-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="afaad-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="afaad-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="afaad-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="afaad-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="afaad-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="afaad-152">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="afaad-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="afaad-153">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="afaad-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="afaad-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="afaad-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="afaad-155">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="afaad-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="afaad-156">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="afaad-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="afaad-157">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="afaad-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="afaad-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="afaad-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="afaad-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="afaad-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="afaad-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="afaad-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="afaad-161">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="afaad-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="afaad-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="afaad-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="afaad-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="afaad-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="afaad-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="afaad-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="afaad-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="afaad-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="afaad-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="afaad-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="afaad-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="afaad-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
