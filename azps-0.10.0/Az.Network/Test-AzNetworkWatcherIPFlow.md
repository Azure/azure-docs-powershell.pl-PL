---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 307bb2c954526b744f31763f0d3a09d0163c8057
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892662"
---
# <span data-ttu-id="6f7da-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6f7da-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="6f7da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6f7da-102">SYNOPSIS</span></span>
<span data-ttu-id="6f7da-103">Zwraca możliwość, że pakiet jest dozwolony lub odmówiony lub pochodzi z określonego miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="6f7da-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="6f7da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6f7da-104">SYNTAX</span></span>

### <span data-ttu-id="6f7da-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6f7da-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f7da-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6f7da-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f7da-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6f7da-107">DESCRIPTION</span></span>
<span data-ttu-id="6f7da-108">Polecenie cmdlet Test-AzNetworkWatcherIPFlow dla określonego zasobu maszyny wirtualnej i pakiet o określonym kierunku przy użyciu lokalnych i zdalnych adresów IP oraz portów zwraca wartość, czy pakiet jest dozwolony, czy zabroniony.</span><span class="sxs-lookup"><span data-stu-id="6f7da-108">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="6f7da-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6f7da-109">EXAMPLES</span></span>

### <span data-ttu-id="6f7da-110">---Przykład 1: Uruchom Test-AzNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="6f7da-110">--- Example 1: Run Test-AzNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="6f7da-111">W przypadku tej subskrypcji jest wyświetlany Monitor sieci na zachodnich centralach w USA, a następnie jest pobierana ta maszyna wirtualna i skojarzone z nią interfejsy sieciowe.</span><span class="sxs-lookup"><span data-stu-id="6f7da-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="6f7da-112">Następnie w pierwszym interfejsie sieciowym zostanie uruchomiona Test-AzNetworkWatcherIPFlow przy użyciu pierwszego adresu IP od pierwszego interfejsu sieciowego w celu połączenia wychodzącego z adresem IP w Internecie.</span><span class="sxs-lookup"><span data-stu-id="6f7da-112">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="6f7da-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6f7da-113">PARAMETERS</span></span>

### <span data-ttu-id="6f7da-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f7da-114">-AsJob</span></span>
<span data-ttu-id="6f7da-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6f7da-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f7da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f7da-116">-DefaultProfile</span></span>
<span data-ttu-id="6f7da-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6f7da-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f7da-118">-Direction</span><span class="sxs-lookup"><span data-stu-id="6f7da-118">-Direction</span></span>
<span data-ttu-id="6f7da-119">Obszar.</span><span class="sxs-lookup"><span data-stu-id="6f7da-119">Direction.</span></span>

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

### <span data-ttu-id="6f7da-120">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="6f7da-120">-LocalIPAddress</span></span>
<span data-ttu-id="6f7da-121">Lokalny adres IP.</span><span class="sxs-lookup"><span data-stu-id="6f7da-121">Local IP Address.</span></span>

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

### <span data-ttu-id="6f7da-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="6f7da-122">-LocalPort</span></span>
<span data-ttu-id="6f7da-123">Port lokalny.</span><span class="sxs-lookup"><span data-stu-id="6f7da-123">Local Port.</span></span>

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

### <span data-ttu-id="6f7da-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6f7da-124">-NetworkWatcher</span></span>
<span data-ttu-id="6f7da-125">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="6f7da-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="6f7da-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6f7da-126">-NetworkWatcherName</span></span>
<span data-ttu-id="6f7da-127">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="6f7da-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="6f7da-128">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="6f7da-128">-Protocol</span></span>
<span data-ttu-id="6f7da-129">Sterownika.</span><span class="sxs-lookup"><span data-stu-id="6f7da-129">Protocol.</span></span>

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

### <span data-ttu-id="6f7da-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="6f7da-130">-RemoteIPAddress</span></span>
<span data-ttu-id="6f7da-131">Zdalny adres IP.</span><span class="sxs-lookup"><span data-stu-id="6f7da-131">Remote IP Address.</span></span>

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

### <span data-ttu-id="6f7da-132">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="6f7da-132">-RemotePort</span></span>
<span data-ttu-id="6f7da-133">Port zdalny.</span><span class="sxs-lookup"><span data-stu-id="6f7da-133">Remote port.</span></span>

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

### <span data-ttu-id="6f7da-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f7da-134">-ResourceGroupName</span></span>
<span data-ttu-id="6f7da-135">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="6f7da-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6f7da-136">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="6f7da-136">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="6f7da-137">Identyfikator interfejsu sieci docelowej.</span><span class="sxs-lookup"><span data-stu-id="6f7da-137">Target network interface Id.</span></span>

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

### <span data-ttu-id="6f7da-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="6f7da-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="6f7da-139">Docelowy Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6f7da-139">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="6f7da-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f7da-140">CommonParameters</span></span>
<span data-ttu-id="6f7da-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f7da-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f7da-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f7da-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f7da-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f7da-143">INPUTS</span></span>

### <span data-ttu-id="6f7da-144">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6f7da-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6f7da-145">System. String</span><span class="sxs-lookup"><span data-stu-id="6f7da-145">System.String</span></span>

## <span data-ttu-id="6f7da-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6f7da-146">OUTPUTS</span></span>

### <span data-ttu-id="6f7da-147">Microsoft. Azure. Commands. Network. models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="6f7da-147">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="6f7da-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6f7da-148">NOTES</span></span>
<span data-ttu-id="6f7da-149">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor sieciowy, przepływ, IP</span><span class="sxs-lookup"><span data-stu-id="6f7da-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="6f7da-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f7da-150">RELATED LINKS</span></span>

[<span data-ttu-id="6f7da-151">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6f7da-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="6f7da-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6f7da-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="6f7da-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6f7da-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="6f7da-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6f7da-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="6f7da-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6f7da-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6f7da-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6f7da-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="6f7da-157">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6f7da-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6f7da-158">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6f7da-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6f7da-159">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6f7da-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="6f7da-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6f7da-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6f7da-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6f7da-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6f7da-162">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6f7da-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
