---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: 4c6a1e179cf0c6086035488d092232e85c570637
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543771"
---
# <span data-ttu-id="f1968-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f1968-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="f1968-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f1968-102">SYNOPSIS</span></span>
<span data-ttu-id="f1968-103">Pobiera następny przeskok z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f1968-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1968-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f1968-104">SYNTAX</span></span>

### <span data-ttu-id="f1968-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f1968-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1968-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f1968-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1968-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f1968-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1968-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f1968-108">DESCRIPTION</span></span>
<span data-ttu-id="f1968-109">Polecenie cmdlet Get-AzureRmNetworkWatcherNextHop pobiera następny przeskok z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f1968-109">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="f1968-110">Następny przeskok umożliwia wyświetlenie typu zasobu platformy Azure, skojarzonego adresu IP tego zasobu oraz reguły tabeli routingu odpowiedzialnej za trasę.</span><span class="sxs-lookup"><span data-stu-id="f1968-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="f1968-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f1968-111">EXAMPLES</span></span>

### <span data-ttu-id="f1968-112">Przykład 1. Uzyskiwanie następnego przeskoku podczas komunikowania się z internetowym adresem IP</span><span class="sxs-lookup"><span data-stu-id="f1968-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="f1968-113">Uzyskiwanie następnego przeskoku do komunikacji wychodzącej z podstawowego interfejsu sieciowego w określonym wirtualnym Vachine do 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="f1968-113">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="f1968-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f1968-114">PARAMETERS</span></span>

### <span data-ttu-id="f1968-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1968-115">-AsJob</span></span>
<span data-ttu-id="f1968-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f1968-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1968-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1968-117">-DefaultProfile</span></span>
<span data-ttu-id="f1968-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1968-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1968-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="f1968-119">-DestinationIPAddress</span></span>
<span data-ttu-id="f1968-120">Docelowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="f1968-120">Destination IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1968-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f1968-121">-Location</span></span>
<span data-ttu-id="f1968-122">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="f1968-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f1968-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f1968-123">-NetworkWatcher</span></span>
<span data-ttu-id="f1968-124">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="f1968-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="f1968-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f1968-125">-NetworkWatcherName</span></span>
<span data-ttu-id="f1968-126">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="f1968-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="f1968-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1968-127">-ResourceGroupName</span></span>
<span data-ttu-id="f1968-128">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="f1968-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f1968-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="f1968-129">-SourceIPAddress</span></span>
<span data-ttu-id="f1968-130">Źródłowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="f1968-130">Source IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1968-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="f1968-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="f1968-132">Identyfikator interfejsu sieci docelowej.</span><span class="sxs-lookup"><span data-stu-id="f1968-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="f1968-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="f1968-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="f1968-134">Docelowy Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f1968-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="f1968-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1968-135">CommonParameters</span></span>
<span data-ttu-id="f1968-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1968-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1968-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1968-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1968-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1968-138">INPUTS</span></span>

### <span data-ttu-id="f1968-139">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f1968-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f1968-140">Parametry: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f1968-140">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="f1968-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f1968-141">System.String</span></span>
<span data-ttu-id="f1968-142">Parametry: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f1968-142">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="f1968-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f1968-143">OUTPUTS</span></span>

### <span data-ttu-id="f1968-144">Microsoft. Azure. Commands. Network. models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="f1968-144">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="f1968-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f1968-145">NOTES</span></span>
<span data-ttu-id="f1968-146">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, następny, przeskok</span><span class="sxs-lookup"><span data-stu-id="f1968-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="f1968-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1968-147">RELATED LINKS</span></span>

[<span data-ttu-id="f1968-148">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f1968-148">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f1968-149">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f1968-149">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f1968-150">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f1968-150">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f1968-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f1968-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="f1968-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f1968-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f1968-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f1968-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="f1968-154">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f1968-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f1968-155">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f1968-155">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f1968-156">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f1968-156">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="f1968-157">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f1968-157">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f1968-158">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f1968-158">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f1968-159">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f1968-159">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f1968-160">Nowe — AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1968-160">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f1968-161">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f1968-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="f1968-162">Test — AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f1968-162">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="f1968-163">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f1968-163">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f1968-164">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f1968-164">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f1968-165">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f1968-165">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f1968-166">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f1968-166">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f1968-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f1968-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f1968-168">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f1968-168">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f1968-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f1968-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f1968-170">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f1968-170">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f1968-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f1968-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f1968-172">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f1968-172">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f1968-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f1968-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="f1968-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f1968-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
