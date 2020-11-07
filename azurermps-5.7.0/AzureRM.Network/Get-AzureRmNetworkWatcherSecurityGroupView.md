---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 5b48cbabfe91b16924a1296a73354db659ec8f3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719454"
---
# <span data-ttu-id="a6501-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a6501-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="a6501-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6501-102">SYNOPSIS</span></span>
<span data-ttu-id="a6501-103">Wyświetl skonfigurowane i efektywne reguły grupowych zabezpieczeń sieci stosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a6501-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6501-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6501-104">SYNTAX</span></span>

### <span data-ttu-id="a6501-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a6501-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6501-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a6501-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6501-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a6501-107">DESCRIPTION</span></span>
<span data-ttu-id="a6501-108">Get-AzureRmNetworkWatcherSecurityGroupView pozwala wyświetlić skonfigurowane i efektywne reguły grupowych zabezpieczeń sieci stosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a6501-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="a6501-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6501-109">EXAMPLES</span></span>

### <span data-ttu-id="a6501-110">---Przykład 1: Tworzenie grup zabezpieczeń w celu wyświetlania połączeń na---maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a6501-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="a6501-111">W powyższym przykładzie najpierw jest wyświetlany regionalny Monitor sieci, a następnie maszyna wirtualna w regionie.</span><span class="sxs-lookup"><span data-stu-id="a6501-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="a6501-112">Następnie nawiązanie połączenia z grupą zabezpieczeń na określonej maszynie wirtualnej jest włączone.</span><span class="sxs-lookup"><span data-stu-id="a6501-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="a6501-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6501-113">PARAMETERS</span></span>

### <span data-ttu-id="a6501-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6501-114">-AsJob</span></span>
<span data-ttu-id="a6501-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a6501-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6501-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6501-116">-DefaultProfile</span></span>
<span data-ttu-id="a6501-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6501-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6501-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6501-118">-NetworkWatcher</span></span>
<span data-ttu-id="a6501-119">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="a6501-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="a6501-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a6501-120">-NetworkWatcherName</span></span>
<span data-ttu-id="a6501-121">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="a6501-121">The name of network watcher.</span></span>

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

### <span data-ttu-id="a6501-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6501-122">-ResourceGroupName</span></span>
<span data-ttu-id="a6501-123">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="a6501-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a6501-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="a6501-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="a6501-125">Docelowy Identyfikator maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a6501-125">The target VM Id</span></span>

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

### <span data-ttu-id="a6501-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6501-126">CommonParameters</span></span>
<span data-ttu-id="a6501-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6501-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6501-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6501-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6501-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6501-129">INPUTS</span></span>

### <span data-ttu-id="a6501-130">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6501-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a6501-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a6501-131">System.String</span></span>

## <span data-ttu-id="a6501-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6501-132">OUTPUTS</span></span>

### <span data-ttu-id="a6501-133">Microsoft. Azure. Commands. Network. models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="a6501-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="a6501-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6501-134">NOTES</span></span>
<span data-ttu-id="a6501-135">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor sieciowy, przepływ, IP</span><span class="sxs-lookup"><span data-stu-id="a6501-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="a6501-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6501-136">RELATED LINKS</span></span>

[<span data-ttu-id="a6501-137">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6501-137">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a6501-138">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6501-138">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a6501-139">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6501-139">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a6501-140">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a6501-140">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="a6501-141">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a6501-141">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="a6501-142">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a6501-142">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="a6501-143">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a6501-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a6501-144">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6501-144">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a6501-145">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a6501-145">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="a6501-146">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6501-146">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a6501-147">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6501-147">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a6501-148">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6501-148">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

