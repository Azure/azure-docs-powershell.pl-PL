---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 9fe23ea5fa9bef544feae6112879cb1be6eeae7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527849"
---
# <span data-ttu-id="98c00-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="98c00-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="98c00-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98c00-102">SYNOPSIS</span></span>
<span data-ttu-id="98c00-103">Wyświetl skonfigurowane i efektywne reguły grupowych zabezpieczeń sieci stosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="98c00-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98c00-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98c00-104">SYNTAX</span></span>

### <span data-ttu-id="98c00-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="98c00-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98c00-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="98c00-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98c00-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="98c00-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98c00-108">Opis</span><span class="sxs-lookup"><span data-stu-id="98c00-108">DESCRIPTION</span></span>
<span data-ttu-id="98c00-109">Get-AzureRmNetworkWatcherSecurityGroupView pozwala wyświetlić skonfigurowane i efektywne reguły grupowych zabezpieczeń sieci stosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="98c00-109">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="98c00-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98c00-110">EXAMPLES</span></span>

### <span data-ttu-id="98c00-111">Przykład 1. Tworzenie grup zabezpieczeń w celu wyświetlania połączeń na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="98c00-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="98c00-112">W powyższym przykładzie najpierw jest wyświetlany regionalny Monitor sieci, a następnie maszyna wirtualna w regionie.</span><span class="sxs-lookup"><span data-stu-id="98c00-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="98c00-113">Następnie nawiązanie połączenia z grupą zabezpieczeń na określonej maszynie wirtualnej jest włączone.</span><span class="sxs-lookup"><span data-stu-id="98c00-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="98c00-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98c00-114">PARAMETERS</span></span>

### <span data-ttu-id="98c00-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98c00-115">-AsJob</span></span>
<span data-ttu-id="98c00-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="98c00-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98c00-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c00-117">-DefaultProfile</span></span>
<span data-ttu-id="98c00-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98c00-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98c00-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="98c00-119">-Location</span></span>
<span data-ttu-id="98c00-120">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="98c00-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="98c00-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="98c00-121">-NetworkWatcher</span></span>
<span data-ttu-id="98c00-122">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="98c00-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="98c00-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="98c00-123">-NetworkWatcherName</span></span>
<span data-ttu-id="98c00-124">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="98c00-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="98c00-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98c00-125">-ResourceGroupName</span></span>
<span data-ttu-id="98c00-126">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="98c00-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="98c00-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="98c00-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="98c00-128">Docelowy Identyfikator maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="98c00-128">The target VM Id</span></span>

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

### <span data-ttu-id="98c00-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c00-129">CommonParameters</span></span>
<span data-ttu-id="98c00-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98c00-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c00-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98c00-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c00-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98c00-132">INPUTS</span></span>

### <span data-ttu-id="98c00-133">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="98c00-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="98c00-134">Parametry: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="98c00-134">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="98c00-135">System. String</span><span class="sxs-lookup"><span data-stu-id="98c00-135">System.String</span></span>
<span data-ttu-id="98c00-136">Parametry: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="98c00-136">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="98c00-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98c00-137">OUTPUTS</span></span>

### <span data-ttu-id="98c00-138">Microsoft. Azure. Commands. Network. models. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="98c00-138">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="98c00-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98c00-139">NOTES</span></span>
<span data-ttu-id="98c00-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor sieciowy, przepływ, IP</span><span class="sxs-lookup"><span data-stu-id="98c00-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="98c00-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98c00-141">RELATED LINKS</span></span>

[<span data-ttu-id="98c00-142">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="98c00-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="98c00-143">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="98c00-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="98c00-144">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="98c00-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="98c00-145">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="98c00-145">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="98c00-146">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="98c00-146">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="98c00-147">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="98c00-147">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="98c00-148">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="98c00-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="98c00-149">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="98c00-149">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="98c00-150">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="98c00-150">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="98c00-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="98c00-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="98c00-152">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="98c00-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="98c00-153">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="98c00-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="98c00-154">Nowe — AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="98c00-154">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="98c00-155">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="98c00-155">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="98c00-156">Test — AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="98c00-156">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="98c00-157">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98c00-157">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="98c00-158">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98c00-158">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="98c00-159">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98c00-159">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="98c00-160">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="98c00-160">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="98c00-161">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98c00-161">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="98c00-162">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98c00-162">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="98c00-163">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="98c00-163">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="98c00-164">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="98c00-164">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="98c00-165">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="98c00-165">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="98c00-166">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="98c00-166">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="98c00-167">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="98c00-167">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="98c00-168">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98c00-168">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
