---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 2f855175065f743bdfec5fb8dc9c917af262b05b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890722"
---
# <span data-ttu-id="2a732-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2a732-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="2a732-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a732-102">SYNOPSIS</span></span>
<span data-ttu-id="2a732-103">Pobiera stan rejestrowania przepływu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="2a732-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="2a732-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a732-104">SYNTAX</span></span>

### <span data-ttu-id="2a732-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2a732-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a732-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2a732-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a732-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2a732-107">DESCRIPTION</span></span>
<span data-ttu-id="2a732-108">Polecenie cmdlet Get-AzNetworkWatcherFlowLogStatus Pobiera stan rejestrowania przepływu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="2a732-108">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="2a732-109">Stan uwzględnia, czy w przypadku danego zasobu jest włączone rejestrowanie przepływu, skonfigurowane konto magazynu do wysyłania dzienników oraz zasady przechowywania dzienników.</span><span class="sxs-lookup"><span data-stu-id="2a732-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="2a732-110">W przypadku rejestrowania przepływów są obsługiwane obecnie grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="2a732-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="2a732-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a732-111">EXAMPLES</span></span>

### <span data-ttu-id="2a732-112">---Przykład 1: uzyskiwanie stanu rejestrowania przepływu dla określonego NSG---</span><span class="sxs-lookup"><span data-stu-id="2a732-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                   }
```

<span data-ttu-id="2a732-113">W tym przykładzie jest wyświetlany stan rejestrowania przepływu dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="2a732-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="2a732-114">Określony NSG ma włączone rejestrowanie przepływów i nie ustawiono zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="2a732-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="2a732-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a732-115">PARAMETERS</span></span>

### <span data-ttu-id="2a732-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a732-116">-AsJob</span></span>
<span data-ttu-id="2a732-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2a732-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a732-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a732-118">-DefaultProfile</span></span>
<span data-ttu-id="2a732-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a732-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a732-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2a732-120">-NetworkWatcher</span></span>
<span data-ttu-id="2a732-121">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="2a732-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="2a732-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2a732-122">-NetworkWatcherName</span></span>
<span data-ttu-id="2a732-123">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="2a732-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="2a732-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a732-124">-ResourceGroupName</span></span>
<span data-ttu-id="2a732-125">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="2a732-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2a732-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2a732-126">-TargetResourceId</span></span>
<span data-ttu-id="2a732-127">Identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="2a732-127">The target resource ID.</span></span>

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

### <span data-ttu-id="2a732-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a732-128">CommonParameters</span></span>
<span data-ttu-id="2a732-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a732-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a732-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a732-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a732-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a732-131">INPUTS</span></span>

### <span data-ttu-id="2a732-132">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2a732-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2a732-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2a732-133">System.String</span></span>

## <span data-ttu-id="2a732-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a732-134">OUTPUTS</span></span>

### <span data-ttu-id="2a732-135">Microsoft. Azure. Commands. Network. models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="2a732-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="2a732-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a732-136">NOTES</span></span>
<span data-ttu-id="2a732-137">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor, przepływ, dzienniki, flowlog, rejestrowanie</span><span class="sxs-lookup"><span data-stu-id="2a732-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="2a732-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a732-138">RELATED LINKS</span></span>

[<span data-ttu-id="2a732-139">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2a732-139">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2a732-140">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2a732-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2a732-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2a732-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2a732-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2a732-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2a732-143">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2a732-143">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2a732-144">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2a732-144">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2a732-145">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2a732-145">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2a732-146">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2a732-146">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2a732-147">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2a732-147">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2a732-148">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2a732-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2a732-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2a732-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2a732-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2a732-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2a732-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2a732-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2a732-152">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2a732-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2a732-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2a732-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
