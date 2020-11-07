---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 5399c97f076f1402b20b91798d2db215d00af8b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708908"
---
# <span data-ttu-id="d34f9-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d34f9-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="d34f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d34f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d34f9-103">Rozpoczynanie rozwiązywania problemów z zasobem sieciowym na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d34f9-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="d34f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d34f9-104">SYNTAX</span></span>

### <span data-ttu-id="d34f9-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d34f9-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d34f9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d34f9-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d34f9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d34f9-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d34f9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d34f9-108">DESCRIPTION</span></span>
<span data-ttu-id="d34f9-109">Polecenie cmdlet Start-AzNetworkWatcherResourceTroubleshooting uruchamia Rozwiązywanie problemów z zasobem sieciowym na platformie Azure i zwraca informacje o potencjalnych problemach i ograniczeniach.</span><span class="sxs-lookup"><span data-stu-id="d34f9-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="d34f9-110">Obecnie obsługiwane są bramy sieci wirtualnej i połączenia.</span><span class="sxs-lookup"><span data-stu-id="d34f9-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="d34f9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d34f9-111">EXAMPLES</span></span>

### <span data-ttu-id="d34f9-112">Przykład 1. Rozpocznij Rozwiązywanie problemów dotyczących bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d34f9-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="d34f9-113">Powyższy przykład rozpoczyna Rozwiązywanie problemów z bramą sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d34f9-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="d34f9-114">Ukończenie operacji może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="d34f9-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="d34f9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d34f9-115">PARAMETERS</span></span>

### <span data-ttu-id="d34f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d34f9-116">-DefaultProfile</span></span>
<span data-ttu-id="d34f9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d34f9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d34f9-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d34f9-118">-Location</span></span>
<span data-ttu-id="d34f9-119">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d34f9-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d34f9-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d34f9-120">-NetworkWatcher</span></span>
<span data-ttu-id="d34f9-121">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d34f9-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="d34f9-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d34f9-122">-NetworkWatcherName</span></span>
<span data-ttu-id="d34f9-123">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d34f9-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="d34f9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d34f9-124">-ResourceGroupName</span></span>
<span data-ttu-id="d34f9-125">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d34f9-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d34f9-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="d34f9-126">-StorageId</span></span>
<span data-ttu-id="d34f9-127">Identyfikator magazynu.</span><span class="sxs-lookup"><span data-stu-id="d34f9-127">The storage ID.</span></span>

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

### <span data-ttu-id="d34f9-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="d34f9-128">-StoragePath</span></span>
<span data-ttu-id="d34f9-129">Ścieżka do magazynu.</span><span class="sxs-lookup"><span data-stu-id="d34f9-129">The storage path.</span></span>

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

### <span data-ttu-id="d34f9-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d34f9-130">-TargetResourceId</span></span>
<span data-ttu-id="d34f9-131">Określa identyfikator zasobu, którego dotyczy problem.</span><span class="sxs-lookup"><span data-stu-id="d34f9-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="d34f9-132">Przykładowy format: "/subscriptions/$ {Identyfikator subskrypcji}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {ConnectionName}"</span><span class="sxs-lookup"><span data-stu-id="d34f9-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="d34f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d34f9-133">CommonParameters</span></span>
<span data-ttu-id="d34f9-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d34f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d34f9-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d34f9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d34f9-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d34f9-136">INPUTS</span></span>

### <span data-ttu-id="d34f9-137">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d34f9-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d34f9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d34f9-138">System.String</span></span>

## <span data-ttu-id="d34f9-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d34f9-139">OUTPUTS</span></span>

### <span data-ttu-id="d34f9-140">Microsoft. Azure. Commands. Network. models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d34f9-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="d34f9-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d34f9-141">NOTES</span></span>
<span data-ttu-id="d34f9-142">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, rozwiązywanie problemów, VPN, połączenie</span><span class="sxs-lookup"><span data-stu-id="d34f9-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="d34f9-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d34f9-143">RELATED LINKS</span></span>

[<span data-ttu-id="d34f9-144">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d34f9-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d34f9-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d34f9-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d34f9-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d34f9-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d34f9-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d34f9-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d34f9-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d34f9-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d34f9-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d34f9-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d34f9-150">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d34f9-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d34f9-151">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d34f9-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d34f9-152">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d34f9-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d34f9-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d34f9-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d34f9-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d34f9-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d34f9-155">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d34f9-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d34f9-156">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d34f9-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d34f9-157">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d34f9-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d34f9-158">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d34f9-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d34f9-159">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d34f9-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d34f9-160">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d34f9-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d34f9-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d34f9-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d34f9-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d34f9-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d34f9-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d34f9-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d34f9-164">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d34f9-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d34f9-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d34f9-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d34f9-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d34f9-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d34f9-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d34f9-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d34f9-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d34f9-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d34f9-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d34f9-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="d34f9-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d34f9-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)