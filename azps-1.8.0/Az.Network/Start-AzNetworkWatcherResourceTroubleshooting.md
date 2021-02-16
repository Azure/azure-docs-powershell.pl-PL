---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 5c11eecb00aa97fc90aecc770a77285f77be988b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402783"
---
# <span data-ttu-id="cd6dd-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cd6dd-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="cd6dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="cd6dd-103">Rozpoczyna rozwiązywanie problemów w zasobie sieci na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="cd6dd-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="cd6dd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cd6dd-104">SYNTAX</span></span>

### <span data-ttu-id="cd6dd-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="cd6dd-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd6dd-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="cd6dd-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd6dd-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="cd6dd-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd6dd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cd6dd-108">DESCRIPTION</span></span>
<span data-ttu-id="cd6dd-109">Polecenie Start-AzNetworkWatcherResourceTroubleshooting rozpoczyna rozwiązywanie problemów dla zasobu sieciowego na platformie Azure i zwraca informacje o potencjalnych problemach i środki zaradcze.</span><span class="sxs-lookup"><span data-stu-id="cd6dd-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="cd6dd-110">Obecnie bramy i połączenia sieci wirtualnej są obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="cd6dd-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="cd6dd-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cd6dd-111">EXAMPLES</span></span>

### <span data-ttu-id="cd6dd-112">Przykład 1. Rozpoczynanie rozwiązywania problemów z bramą sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="cd6dd-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="cd6dd-113">Powyższy przykład rozpoczyna rozwiązywanie problemów w wirtualnej bramie sieciowej.</span><span class="sxs-lookup"><span data-stu-id="cd6dd-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="cd6dd-114">Operacja może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="cd6dd-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="cd6dd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd6dd-115">PARAMETERS</span></span>

### <span data-ttu-id="cd6dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd6dd-116">-DefaultProfile</span></span>
<span data-ttu-id="cd6dd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd6dd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd6dd-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cd6dd-118">-Location</span></span>
<span data-ttu-id="cd6dd-119">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="cd6dd-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="cd6dd-120">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd6dd-120">-NetworkWatcher</span></span>
<span data-ttu-id="cd6dd-121">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="cd6dd-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="cd6dd-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cd6dd-122">-NetworkWatcherName</span></span>
<span data-ttu-id="cd6dd-123">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="cd6dd-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="cd6dd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd6dd-124">-ResourceGroupName</span></span>
<span data-ttu-id="cd6dd-125">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="cd6dd-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="cd6dd-126">- StorageId</span><span class="sxs-lookup"><span data-stu-id="cd6dd-126">-StorageId</span></span>
<span data-ttu-id="cd6dd-127">Identyfikator magazynu.</span><span class="sxs-lookup"><span data-stu-id="cd6dd-127">The storage ID.</span></span>

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

### <span data-ttu-id="cd6dd-128">— StoragePath</span><span class="sxs-lookup"><span data-stu-id="cd6dd-128">-StoragePath</span></span>
<span data-ttu-id="cd6dd-129">Ścieżka magazynu.</span><span class="sxs-lookup"><span data-stu-id="cd6dd-129">The storage path.</span></span>

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

### <span data-ttu-id="cd6dd-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="cd6dd-130">-TargetResourceId</span></span>
<span data-ttu-id="cd6dd-131">Określa identyfikator zasobu, który ma być rozwiązywany.</span><span class="sxs-lookup"><span data-stu-id="cd6dd-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="cd6dd-132">Przykładowy format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span><span class="sxs-lookup"><span data-stu-id="cd6dd-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="cd6dd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd6dd-133">CommonParameters</span></span>
<span data-ttu-id="cd6dd-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd6dd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd6dd-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd6dd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd6dd-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd6dd-136">INPUTS</span></span>

### <span data-ttu-id="cd6dd-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd6dd-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="cd6dd-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cd6dd-138">System.String</span></span>

## <span data-ttu-id="cd6dd-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd6dd-139">OUTPUTS</span></span>

### <span data-ttu-id="cd6dd-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cd6dd-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="cd6dd-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cd6dd-141">NOTES</span></span>
<span data-ttu-id="cd6dd-142">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span><span class="sxs-lookup"><span data-stu-id="cd6dd-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="cd6dd-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd6dd-143">RELATED LINKS</span></span>

[<span data-ttu-id="cd6dd-144">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd6dd-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="cd6dd-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd6dd-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="cd6dd-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd6dd-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="cd6dd-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cd6dd-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="cd6dd-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cd6dd-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="cd6dd-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cd6dd-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="cd6dd-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cd6dd-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="cd6dd-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd6dd-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd6dd-152">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cd6dd-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="cd6dd-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd6dd-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd6dd-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd6dd-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd6dd-155">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd6dd-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd6dd-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd6dd-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="cd6dd-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="cd6dd-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="cd6dd-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="cd6dd-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="cd6dd-159">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd6dd-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cd6dd-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd6dd-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cd6dd-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd6dd-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cd6dd-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="cd6dd-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="cd6dd-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd6dd-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cd6dd-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd6dd-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cd6dd-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cd6dd-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="cd6dd-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="cd6dd-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="cd6dd-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="cd6dd-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="cd6dd-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="cd6dd-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="cd6dd-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="cd6dd-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="cd6dd-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd6dd-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
