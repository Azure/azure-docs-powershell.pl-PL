---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 577f883affc772c01343a57a533c5ae06eccf31c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718885"
---
# <span data-ttu-id="3f91f-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3f91f-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="3f91f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f91f-102">SYNOPSIS</span></span>
<span data-ttu-id="3f91f-103">Zwraca możliwość, że pakiet jest dozwolony lub odmówiony lub pochodzi z określonego miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="3f91f-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f91f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f91f-104">SYNTAX</span></span>

### <span data-ttu-id="3f91f-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3f91f-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f91f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3f91f-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f91f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3f91f-107">DESCRIPTION</span></span>
<span data-ttu-id="3f91f-108">Polecenie cmdlet Test-AzureRmNetworkWatcherIPFlow dla określonego zasobu maszyny wirtualnej i pakiet o określonym kierunku przy użyciu lokalnych i zdalnych adresów IP oraz portów zwraca wartość, czy pakiet jest dozwolony, czy zabroniony.</span><span class="sxs-lookup"><span data-stu-id="3f91f-108">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="3f91f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f91f-109">EXAMPLES</span></span>

### <span data-ttu-id="3f91f-110">---Przykład 1: Uruchom Test-AzureRmNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="3f91f-110">--- Example 1: Run Test-AzureRmNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="3f91f-111">W przypadku tej subskrypcji jest wyświetlany Monitor sieci na zachodnich centralach w USA, a następnie jest pobierana ta maszyna wirtualna i skojarzone z nią interfejsy sieciowe.</span><span class="sxs-lookup"><span data-stu-id="3f91f-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="3f91f-112">Następnie w pierwszym interfejsie sieciowym zostanie uruchomiona Test-AzureRmNetworkWatcherIPFlow przy użyciu pierwszego adresu IP od pierwszego interfejsu sieciowego w celu połączenia wychodzącego z adresem IP w Internecie.</span><span class="sxs-lookup"><span data-stu-id="3f91f-112">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="3f91f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f91f-113">PARAMETERS</span></span>

### <span data-ttu-id="3f91f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f91f-114">-AsJob</span></span>
<span data-ttu-id="3f91f-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3f91f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f91f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f91f-116">-DefaultProfile</span></span>
<span data-ttu-id="3f91f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f91f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f91f-118">-Direction</span><span class="sxs-lookup"><span data-stu-id="3f91f-118">-Direction</span></span>
<span data-ttu-id="3f91f-119">Obszar.</span><span class="sxs-lookup"><span data-stu-id="3f91f-119">Direction.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f91f-120">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="3f91f-120">-LocalIPAddress</span></span>
<span data-ttu-id="3f91f-121">Lokalny adres IP.</span><span class="sxs-lookup"><span data-stu-id="3f91f-121">Local IP Address.</span></span>

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

### <span data-ttu-id="3f91f-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="3f91f-122">-LocalPort</span></span>
<span data-ttu-id="3f91f-123">Port lokalny.</span><span class="sxs-lookup"><span data-stu-id="3f91f-123">Local Port.</span></span>

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

### <span data-ttu-id="3f91f-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3f91f-124">-NetworkWatcher</span></span>
<span data-ttu-id="3f91f-125">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="3f91f-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="3f91f-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3f91f-126">-NetworkWatcherName</span></span>
<span data-ttu-id="3f91f-127">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="3f91f-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="3f91f-128">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="3f91f-128">-Protocol</span></span>
<span data-ttu-id="3f91f-129">Sterownika.</span><span class="sxs-lookup"><span data-stu-id="3f91f-129">Protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f91f-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="3f91f-130">-RemoteIPAddress</span></span>
<span data-ttu-id="3f91f-131">Zdalny adres IP.</span><span class="sxs-lookup"><span data-stu-id="3f91f-131">Remote IP Address.</span></span>

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

### <span data-ttu-id="3f91f-132">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="3f91f-132">-RemotePort</span></span>
<span data-ttu-id="3f91f-133">Port zdalny.</span><span class="sxs-lookup"><span data-stu-id="3f91f-133">Remote port.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f91f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f91f-134">-ResourceGroupName</span></span>
<span data-ttu-id="3f91f-135">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="3f91f-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3f91f-136">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="3f91f-136">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="3f91f-137">Identyfikator interfejsu sieci docelowej.</span><span class="sxs-lookup"><span data-stu-id="3f91f-137">Target network interface Id.</span></span>

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

### <span data-ttu-id="3f91f-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="3f91f-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="3f91f-139">Docelowy Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3f91f-139">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="3f91f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f91f-140">CommonParameters</span></span>
<span data-ttu-id="3f91f-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f91f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f91f-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f91f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f91f-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f91f-143">INPUTS</span></span>

### <span data-ttu-id="3f91f-144">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3f91f-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3f91f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="3f91f-145">System.String</span></span>

## <span data-ttu-id="3f91f-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f91f-146">OUTPUTS</span></span>

### <span data-ttu-id="3f91f-147">Microsoft. Azure. Commands. Network. models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="3f91f-147">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="3f91f-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f91f-148">NOTES</span></span>
<span data-ttu-id="3f91f-149">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor sieciowy, przepływ, IP</span><span class="sxs-lookup"><span data-stu-id="3f91f-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="3f91f-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f91f-150">RELATED LINKS</span></span>

[<span data-ttu-id="3f91f-151">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3f91f-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3f91f-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3f91f-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3f91f-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3f91f-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3f91f-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3f91f-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="3f91f-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3f91f-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3f91f-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3f91f-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="3f91f-157">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3f91f-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3f91f-158">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3f91f-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3f91f-159">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3f91f-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="3f91f-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3f91f-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3f91f-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3f91f-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3f91f-162">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3f91f-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
