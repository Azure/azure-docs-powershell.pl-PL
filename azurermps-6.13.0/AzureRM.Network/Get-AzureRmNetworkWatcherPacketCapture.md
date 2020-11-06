---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 00adf4abd887c56f4091761a4a2031bb6b033032
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552703"
---
# <span data-ttu-id="2ee73-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2ee73-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="2ee73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ee73-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee73-103">Pobiera informacje i właściwości oraz stan zasobu przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="2ee73-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ee73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ee73-104">SYNTAX</span></span>

### <span data-ttu-id="2ee73-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2ee73-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ee73-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2ee73-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ee73-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2ee73-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ee73-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2ee73-108">DESCRIPTION</span></span>
<span data-ttu-id="2ee73-109">Get-AzureRmNetworkWatcherPacketCapture pobiera właściwości i stan zasobu przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="2ee73-109">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="2ee73-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ee73-110">EXAMPLES</span></span>

### <span data-ttu-id="2ee73-111">Przykład 1. Tworzenie przechwyconych pakietów za pomocą wielu filtrów i pobieranie ich stanu</span><span class="sxs-lookup"><span data-stu-id="2ee73-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="2ee73-112">W tym przykładzie tworzymy przechwycony pakiet o nazwie "PacketCaptureTest" z wieloma filtrami i limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="2ee73-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="2ee73-113">Po zakończeniu sesji zostanie ona zapisana na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="2ee73-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="2ee73-114">Następnie dzwonimy Get-AzureRmNetworkWatcherPacketCapture, aby pobrać stan sesji przechwytywania.</span><span class="sxs-lookup"><span data-stu-id="2ee73-114">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="2ee73-115">Uwaga: aby można było tworzyć przechwycenia pakietów, rozszerzenie obserwatora sieci Azure musi być zainstalowane na docelowej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2ee73-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="2ee73-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ee73-116">PARAMETERS</span></span>

### <span data-ttu-id="2ee73-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ee73-117">-AsJob</span></span>
<span data-ttu-id="2ee73-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2ee73-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ee73-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee73-119">-DefaultProfile</span></span>
<span data-ttu-id="2ee73-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ee73-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ee73-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2ee73-121">-Location</span></span>
<span data-ttu-id="2ee73-122">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="2ee73-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2ee73-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ee73-123">-NetworkWatcher</span></span>
<span data-ttu-id="2ee73-124">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="2ee73-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="2ee73-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2ee73-125">-NetworkWatcherName</span></span>
<span data-ttu-id="2ee73-126">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="2ee73-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="2ee73-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="2ee73-127">-PacketCaptureName</span></span>
<span data-ttu-id="2ee73-128">Nazwa przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="2ee73-128">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee73-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ee73-129">-ResourceGroupName</span></span>
<span data-ttu-id="2ee73-130">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="2ee73-130">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2ee73-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee73-131">CommonParameters</span></span>
<span data-ttu-id="2ee73-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ee73-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee73-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ee73-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee73-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ee73-134">INPUTS</span></span>

### <span data-ttu-id="2ee73-135">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ee73-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2ee73-136">Parametry: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2ee73-136">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="2ee73-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2ee73-137">System.String</span></span>
<span data-ttu-id="2ee73-138">Parametry: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2ee73-138">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="2ee73-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ee73-139">OUTPUTS</span></span>

### <span data-ttu-id="2ee73-140">Microsoft. Azure. Commands. Network. models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="2ee73-140">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="2ee73-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ee73-141">NOTES</span></span>
<span data-ttu-id="2ee73-142">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, pakiet, przechwytywanie, ruch</span><span class="sxs-lookup"><span data-stu-id="2ee73-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="2ee73-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ee73-143">RELATED LINKS</span></span>

[<span data-ttu-id="2ee73-144">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ee73-144">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2ee73-145">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ee73-145">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2ee73-146">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ee73-146">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2ee73-147">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2ee73-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="2ee73-148">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2ee73-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2ee73-149">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2ee73-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="2ee73-150">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2ee73-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2ee73-151">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2ee73-151">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2ee73-152">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2ee73-152">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="2ee73-153">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2ee73-153">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2ee73-154">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2ee73-154">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2ee73-155">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2ee73-155">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2ee73-156">Nowe — AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ee73-156">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2ee73-157">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2ee73-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="2ee73-158">Test — AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2ee73-158">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="2ee73-159">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ee73-159">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2ee73-160">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ee73-160">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2ee73-161">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ee73-161">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2ee73-162">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2ee73-162">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2ee73-163">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ee73-163">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2ee73-164">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ee73-164">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2ee73-165">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2ee73-165">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2ee73-166">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2ee73-166">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2ee73-167">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2ee73-167">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2ee73-168">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2ee73-168">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2ee73-169">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2ee73-169">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="2ee73-170">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ee73-170">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)

