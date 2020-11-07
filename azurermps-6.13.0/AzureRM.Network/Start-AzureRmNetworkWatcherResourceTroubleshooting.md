---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermnetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: d0f4661a2b4814fc1c4b5692de6c56865cfa6be9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717259"
---
# <span data-ttu-id="d9cf9-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d9cf9-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="d9cf9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="d9cf9-103">Rozpoczynanie rozwiązywania problemów z zasobem sieciowym na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d9cf9-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9cf9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9cf9-104">SYNTAX</span></span>

### <span data-ttu-id="d9cf9-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d9cf9-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9cf9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d9cf9-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9cf9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d9cf9-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9cf9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d9cf9-108">DESCRIPTION</span></span>
<span data-ttu-id="d9cf9-109">Polecenie cmdlet Start-AzureRmNetworkWatcherResourceTroubleshooting uruchamia Rozwiązywanie problemów z zasobem sieciowym na platformie Azure i zwraca informacje o potencjalnych problemach i ograniczeniach.</span><span class="sxs-lookup"><span data-stu-id="d9cf9-109">The Start-AzureRmNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="d9cf9-110">Obecnie obsługiwane są bramy sieci wirtualnej i połączenia.</span><span class="sxs-lookup"><span data-stu-id="d9cf9-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="d9cf9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9cf9-111">EXAMPLES</span></span>

### <span data-ttu-id="d9cf9-112">Przykład 1. Rozpocznij Rozwiązywanie problemów dotyczących bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d9cf9-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="d9cf9-113">Powyższy przykład rozpoczyna Rozwiązywanie problemów z bramą sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d9cf9-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="d9cf9-114">Ukończenie operacji może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="d9cf9-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="d9cf9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9cf9-115">PARAMETERS</span></span>

### <span data-ttu-id="d9cf9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9cf9-116">-DefaultProfile</span></span>
<span data-ttu-id="d9cf9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9cf9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9cf9-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d9cf9-118">-Location</span></span>
<span data-ttu-id="d9cf9-119">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d9cf9-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d9cf9-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d9cf9-120">-NetworkWatcher</span></span>
<span data-ttu-id="d9cf9-121">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d9cf9-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="d9cf9-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d9cf9-122">-NetworkWatcherName</span></span>
<span data-ttu-id="d9cf9-123">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d9cf9-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="d9cf9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9cf9-124">-ResourceGroupName</span></span>
<span data-ttu-id="d9cf9-125">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d9cf9-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d9cf9-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="d9cf9-126">-StorageId</span></span>
<span data-ttu-id="d9cf9-127">Identyfikator magazynu.</span><span class="sxs-lookup"><span data-stu-id="d9cf9-127">The storage ID.</span></span>

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

### <span data-ttu-id="d9cf9-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="d9cf9-128">-StoragePath</span></span>
<span data-ttu-id="d9cf9-129">Ścieżka do magazynu.</span><span class="sxs-lookup"><span data-stu-id="d9cf9-129">The storage path.</span></span>

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

### <span data-ttu-id="d9cf9-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d9cf9-130">-TargetResourceId</span></span>
<span data-ttu-id="d9cf9-131">Określa identyfikator zasobu, którego dotyczy problem.</span><span class="sxs-lookup"><span data-stu-id="d9cf9-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="d9cf9-132">Przykładowy format: "/subscriptions/$ {Identyfikator subskrypcji}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {ConnectionName}"</span><span class="sxs-lookup"><span data-stu-id="d9cf9-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="d9cf9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9cf9-133">CommonParameters</span></span>
<span data-ttu-id="d9cf9-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9cf9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9cf9-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9cf9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9cf9-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9cf9-136">INPUTS</span></span>

### <span data-ttu-id="d9cf9-137">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d9cf9-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d9cf9-138">Parametry: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d9cf9-138">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="d9cf9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d9cf9-139">System.String</span></span>
<span data-ttu-id="d9cf9-140">Parametry: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d9cf9-140">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="d9cf9-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9cf9-141">OUTPUTS</span></span>

### <span data-ttu-id="d9cf9-142">Microsoft. Azure. Commands. Network. models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d9cf9-142">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="d9cf9-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9cf9-143">NOTES</span></span>
<span data-ttu-id="d9cf9-144">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, rozwiązywanie problemów, VPN, połączenie</span><span class="sxs-lookup"><span data-stu-id="d9cf9-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="d9cf9-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9cf9-145">RELATED LINKS</span></span>

[<span data-ttu-id="d9cf9-146">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d9cf9-146">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d9cf9-147">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d9cf9-147">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d9cf9-148">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d9cf9-148">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d9cf9-149">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d9cf9-149">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="d9cf9-150">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d9cf9-150">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d9cf9-151">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d9cf9-151">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="d9cf9-152">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d9cf9-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d9cf9-153">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d9cf9-153">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d9cf9-154">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d9cf9-154">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="d9cf9-155">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d9cf9-155">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d9cf9-156">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d9cf9-156">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d9cf9-157">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d9cf9-157">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d9cf9-158">Nowe — AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9cf9-158">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d9cf9-159">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d9cf9-159">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="d9cf9-160">Test — AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d9cf9-160">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="d9cf9-161">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d9cf9-161">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d9cf9-162">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d9cf9-162">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d9cf9-163">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d9cf9-163">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d9cf9-164">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d9cf9-164">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d9cf9-165">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d9cf9-165">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d9cf9-166">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d9cf9-166">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d9cf9-167">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d9cf9-167">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d9cf9-168">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d9cf9-168">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d9cf9-169">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d9cf9-169">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d9cf9-170">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d9cf9-170">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d9cf9-171">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d9cf9-171">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="d9cf9-172">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d9cf9-172">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
