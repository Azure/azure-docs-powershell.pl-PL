---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: d26f50768c561e05b4dc27ad829c063b73c5a336
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553815"
---
# <span data-ttu-id="dc9a0-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="dc9a0-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="dc9a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc9a0-102">SYNOPSIS</span></span>
<span data-ttu-id="dc9a0-103">Pobiera następny przeskok z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dc9a0-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc9a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc9a0-104">SYNTAX</span></span>

### <span data-ttu-id="dc9a0-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dc9a0-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc9a0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="dc9a0-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc9a0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dc9a0-107">DESCRIPTION</span></span>
<span data-ttu-id="dc9a0-108">Polecenie cmdlet Get-AzureRmNetworkWatcherNextHop pobiera następny przeskok z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dc9a0-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="dc9a0-109">Następny przeskok umożliwia wyświetlenie typu zasobu platformy Azure, skojarzonego adresu IP tego zasobu oraz reguły tabeli routingu odpowiedzialnej za trasę.</span><span class="sxs-lookup"><span data-stu-id="dc9a0-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="dc9a0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc9a0-110">EXAMPLES</span></span>

### <span data-ttu-id="dc9a0-111">— Przykład 1: uzyskiwanie następnego przeskoku podczas komunikowania się z internetowym adresem IP —</span><span class="sxs-lookup"><span data-stu-id="dc9a0-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="dc9a0-112">Uzyskiwanie następnego przeskoku do komunikacji wychodzącej z podstawowego interfejsu sieciowego w określonym wirtualnym Vachine do 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="dc9a0-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="dc9a0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc9a0-113">PARAMETERS</span></span>

### <span data-ttu-id="dc9a0-114">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="dc9a0-114">-DestinationIPAddress</span></span>
<span data-ttu-id="dc9a0-115">Docelowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="dc9a0-115">Destination IP address.</span></span>

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

### <span data-ttu-id="dc9a0-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dc9a0-116">-NetworkWatcher</span></span>
<span data-ttu-id="dc9a0-117">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="dc9a0-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="dc9a0-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="dc9a0-118">-NetworkWatcherName</span></span>
<span data-ttu-id="dc9a0-119">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="dc9a0-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="dc9a0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc9a0-120">-ResourceGroupName</span></span>
<span data-ttu-id="dc9a0-121">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="dc9a0-121">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="dc9a0-122">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="dc9a0-122">-SourceIPAddress</span></span>
<span data-ttu-id="dc9a0-123">Źródłowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="dc9a0-123">Source IP address.</span></span>

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

### <span data-ttu-id="dc9a0-124">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="dc9a0-124">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="dc9a0-125">Identyfikator interfejsu sieci docelowej.</span><span class="sxs-lookup"><span data-stu-id="dc9a0-125">Target network interface Id.</span></span>

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

### <span data-ttu-id="dc9a0-126">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="dc9a0-126">-TargetVirtualMachineId</span></span>
<span data-ttu-id="dc9a0-127">Docelowy Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dc9a0-127">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="dc9a0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc9a0-128">-DefaultProfile</span></span>
<span data-ttu-id="dc9a0-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc9a0-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc9a0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc9a0-130">CommonParameters</span></span>
<span data-ttu-id="dc9a0-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc9a0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc9a0-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc9a0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc9a0-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc9a0-133">INPUTS</span></span>

### <span data-ttu-id="dc9a0-134">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dc9a0-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="dc9a0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dc9a0-135">System.String</span></span>

## <span data-ttu-id="dc9a0-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc9a0-136">OUTPUTS</span></span>

### <span data-ttu-id="dc9a0-137">Microsoft. Azure. Commands. Network. models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="dc9a0-137">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="dc9a0-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc9a0-138">NOTES</span></span>
<span data-ttu-id="dc9a0-139">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, następny, przeskok</span><span class="sxs-lookup"><span data-stu-id="dc9a0-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="dc9a0-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc9a0-140">RELATED LINKS</span></span>

[<span data-ttu-id="dc9a0-141">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dc9a0-141">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dc9a0-142">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dc9a0-142">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dc9a0-143">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dc9a0-143">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dc9a0-144">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="dc9a0-144">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="dc9a0-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="dc9a0-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="dc9a0-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="dc9a0-146">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="dc9a0-147">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="dc9a0-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="dc9a0-148">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dc9a0-148">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dc9a0-149">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="dc9a0-149">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="dc9a0-150">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dc9a0-150">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dc9a0-151">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dc9a0-151">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dc9a0-152">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dc9a0-152">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

