---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: fe315ac4b6c29b8ffd1c82c8045ba9b7a7aab4a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890713"
---
# <span data-ttu-id="cd499-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cd499-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="cd499-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd499-102">SYNOPSIS</span></span>
<span data-ttu-id="cd499-103">Wyświetl skonfigurowane i efektywne reguły grupowych zabezpieczeń sieci stosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cd499-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="cd499-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd499-104">SYNTAX</span></span>

### <span data-ttu-id="cd499-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd499-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd499-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="cd499-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd499-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cd499-107">DESCRIPTION</span></span>
<span data-ttu-id="cd499-108">Get-AzNetworkWatcherSecurityGroupView pozwala wyświetlić skonfigurowane i efektywne reguły grupowych zabezpieczeń sieci stosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cd499-108">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="cd499-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd499-109">EXAMPLES</span></span>

### <span data-ttu-id="cd499-110">---Przykład 1: Tworzenie grup zabezpieczeń w celu wyświetlania połączeń na---maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="cd499-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="cd499-111">W powyższym przykładzie najpierw jest wyświetlany regionalny Monitor sieci, a następnie maszyna wirtualna w regionie.</span><span class="sxs-lookup"><span data-stu-id="cd499-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="cd499-112">Następnie nawiązanie połączenia z grupą zabezpieczeń na określonej maszynie wirtualnej jest włączone.</span><span class="sxs-lookup"><span data-stu-id="cd499-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="cd499-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd499-113">PARAMETERS</span></span>

### <span data-ttu-id="cd499-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd499-114">-AsJob</span></span>
<span data-ttu-id="cd499-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cd499-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd499-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd499-116">-DefaultProfile</span></span>
<span data-ttu-id="cd499-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd499-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd499-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd499-118">-NetworkWatcher</span></span>
<span data-ttu-id="cd499-119">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="cd499-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="cd499-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cd499-120">-NetworkWatcherName</span></span>
<span data-ttu-id="cd499-121">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="cd499-121">The name of network watcher.</span></span>

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

### <span data-ttu-id="cd499-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd499-122">-ResourceGroupName</span></span>
<span data-ttu-id="cd499-123">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="cd499-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="cd499-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="cd499-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="cd499-125">Docelowy Identyfikator maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="cd499-125">The target VM Id</span></span>

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

### <span data-ttu-id="cd499-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd499-126">CommonParameters</span></span>
<span data-ttu-id="cd499-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd499-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd499-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd499-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd499-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd499-129">INPUTS</span></span>

### <span data-ttu-id="cd499-130">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd499-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="cd499-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cd499-131">System.String</span></span>

## <span data-ttu-id="cd499-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd499-132">OUTPUTS</span></span>

### <span data-ttu-id="cd499-133">Microsoft. Azure. Commands. Network. models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="cd499-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="cd499-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd499-134">NOTES</span></span>
<span data-ttu-id="cd499-135">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor sieciowy, przepływ, IP</span><span class="sxs-lookup"><span data-stu-id="cd499-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="cd499-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd499-136">RELATED LINKS</span></span>

[<span data-ttu-id="cd499-137">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd499-137">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="cd499-138">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd499-138">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="cd499-139">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd499-139">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="cd499-140">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="cd499-140">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="cd499-141">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cd499-141">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="cd499-142">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cd499-142">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="cd499-143">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cd499-143">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="cd499-144">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd499-144">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd499-145">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cd499-145">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="cd499-146">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd499-146">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd499-147">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd499-147">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd499-148">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd499-148">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

