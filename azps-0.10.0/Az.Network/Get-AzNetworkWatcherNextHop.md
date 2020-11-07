---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 02e24fd35fbe2e5aec5fc8b6ed73d3608d07c5b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890721"
---
# <span data-ttu-id="6d228-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6d228-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="6d228-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d228-102">SYNOPSIS</span></span>
<span data-ttu-id="6d228-103">Pobiera następny przeskok z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6d228-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="6d228-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d228-104">SYNTAX</span></span>

### <span data-ttu-id="6d228-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6d228-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d228-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6d228-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d228-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6d228-107">DESCRIPTION</span></span>
<span data-ttu-id="6d228-108">Polecenie cmdlet Get-AzNetworkWatcherNextHop pobiera następny przeskok z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6d228-108">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="6d228-109">Następny przeskok umożliwia wyświetlenie typu zasobu platformy Azure, skojarzonego adresu IP tego zasobu oraz reguły tabeli routingu odpowiedzialnej za trasę.</span><span class="sxs-lookup"><span data-stu-id="6d228-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="6d228-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d228-110">EXAMPLES</span></span>

### <span data-ttu-id="6d228-111">— Przykład 1: uzyskiwanie następnego przeskoku podczas komunikowania się z internetowym adresem IP —</span><span class="sxs-lookup"><span data-stu-id="6d228-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="6d228-112">Uzyskiwanie następnego przeskoku do komunikacji wychodzącej z podstawowego interfejsu sieciowego w określonym wirtualnym Vachine do 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="6d228-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="6d228-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d228-113">PARAMETERS</span></span>

### <span data-ttu-id="6d228-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d228-114">-AsJob</span></span>
<span data-ttu-id="6d228-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6d228-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d228-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d228-116">-DefaultProfile</span></span>
<span data-ttu-id="6d228-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d228-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d228-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="6d228-118">-DestinationIPAddress</span></span>
<span data-ttu-id="6d228-119">Docelowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="6d228-119">Destination IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d228-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6d228-120">-NetworkWatcher</span></span>
<span data-ttu-id="6d228-121">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="6d228-121">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d228-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6d228-122">-NetworkWatcherName</span></span>
<span data-ttu-id="6d228-123">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="6d228-123">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d228-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d228-124">-ResourceGroupName</span></span>
<span data-ttu-id="6d228-125">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="6d228-125">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d228-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="6d228-126">-SourceIPAddress</span></span>
<span data-ttu-id="6d228-127">Źródłowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="6d228-127">Source IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d228-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="6d228-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="6d228-129">Identyfikator interfejsu sieci docelowej.</span><span class="sxs-lookup"><span data-stu-id="6d228-129">Target network interface Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d228-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="6d228-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="6d228-131">Docelowy Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6d228-131">The target virtual machine ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d228-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d228-132">CommonParameters</span></span>
<span data-ttu-id="6d228-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d228-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d228-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d228-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d228-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d228-135">INPUTS</span></span>

### <span data-ttu-id="6d228-136">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6d228-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6d228-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6d228-137">System.String</span></span>

## <span data-ttu-id="6d228-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d228-138">OUTPUTS</span></span>

### <span data-ttu-id="6d228-139">Microsoft. Azure. Commands. Network. models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="6d228-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="6d228-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d228-140">NOTES</span></span>
<span data-ttu-id="6d228-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, następny, przeskok</span><span class="sxs-lookup"><span data-stu-id="6d228-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="6d228-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d228-142">RELATED LINKS</span></span>

[<span data-ttu-id="6d228-143">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6d228-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="6d228-144">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6d228-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="6d228-145">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6d228-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="6d228-146">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6d228-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="6d228-147">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6d228-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6d228-148">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6d228-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="6d228-149">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6d228-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6d228-150">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d228-150">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6d228-151">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6d228-151">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="6d228-152">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d228-152">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6d228-153">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d228-153">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6d228-154">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d228-154">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

