---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherflowlogstatus
schema: 2.0.0
ms.openlocfilehash: 96d3bea781b0c595b54387a9b07b085f173d7b0a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897934"
---
# <span data-ttu-id="f74b4-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f74b4-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="f74b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f74b4-102">SYNOPSIS</span></span>
<span data-ttu-id="f74b4-103">Pobiera stan rejestrowania przepływu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="f74b4-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f74b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f74b4-104">SYNTAX</span></span>

### <span data-ttu-id="f74b4-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f74b4-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f74b4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f74b4-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f74b4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f74b4-107">DESCRIPTION</span></span>
<span data-ttu-id="f74b4-108">Polecenie cmdlet Get-AzureRmNetworkWatcherFlowLogStatus Pobiera stan rejestrowania przepływu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="f74b4-108">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="f74b4-109">Stan uwzględnia, czy w przypadku danego zasobu jest włączone rejestrowanie przepływu, skonfigurowane konto magazynu do wysyłania dzienników oraz zasady przechowywania dzienników.</span><span class="sxs-lookup"><span data-stu-id="f74b4-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="f74b4-110">W przypadku rejestrowania przepływów są obsługiwane obecnie grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="f74b4-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="f74b4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f74b4-111">EXAMPLES</span></span>

### <span data-ttu-id="f74b4-112">---Przykład 1: uzyskiwanie stanu rejestrowania przepływu dla określonego NSG---</span><span class="sxs-lookup"><span data-stu-id="f74b4-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

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

<span data-ttu-id="f74b4-113">W tym przykładzie jest wyświetlany stan rejestrowania przepływu dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="f74b4-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="f74b4-114">Określony NSG ma włączone rejestrowanie przepływów i nie ustawiono zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="f74b4-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="f74b4-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f74b4-115">PARAMETERS</span></span>

### <span data-ttu-id="f74b4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f74b4-116">-AsJob</span></span>
<span data-ttu-id="f74b4-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f74b4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f74b4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f74b4-118">-DefaultProfile</span></span>
<span data-ttu-id="f74b4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f74b4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f74b4-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f74b4-120">-NetworkWatcher</span></span>
<span data-ttu-id="f74b4-121">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="f74b4-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="f74b4-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f74b4-122">-NetworkWatcherName</span></span>
<span data-ttu-id="f74b4-123">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="f74b4-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="f74b4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f74b4-124">-ResourceGroupName</span></span>
<span data-ttu-id="f74b4-125">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="f74b4-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f74b4-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f74b4-126">-TargetResourceId</span></span>
<span data-ttu-id="f74b4-127">Identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="f74b4-127">The target resource ID.</span></span>

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

### <span data-ttu-id="f74b4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f74b4-128">CommonParameters</span></span>
<span data-ttu-id="f74b4-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f74b4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f74b4-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f74b4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f74b4-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f74b4-131">INPUTS</span></span>

### <span data-ttu-id="f74b4-132">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f74b4-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f74b4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f74b4-133">System.String</span></span>

## <span data-ttu-id="f74b4-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f74b4-134">OUTPUTS</span></span>

### <span data-ttu-id="f74b4-135">Microsoft. Azure. Commands. Network. models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="f74b4-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="f74b4-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f74b4-136">NOTES</span></span>
<span data-ttu-id="f74b4-137">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor, przepływ, dzienniki, flowlog, rejestrowanie</span><span class="sxs-lookup"><span data-stu-id="f74b4-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="f74b4-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f74b4-138">RELATED LINKS</span></span>

[<span data-ttu-id="f74b4-139">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f74b4-139">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f74b4-140">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f74b4-140">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f74b4-141">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f74b4-141">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f74b4-142">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f74b4-142">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f74b4-143">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f74b4-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f74b4-144">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f74b4-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="f74b4-145">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f74b4-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f74b4-146">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f74b4-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f74b4-147">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f74b4-147">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f74b4-148">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f74b4-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="f74b4-149">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f74b4-149">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="f74b4-150">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f74b4-150">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f74b4-151">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f74b4-151">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="f74b4-152">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f74b4-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f74b4-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f74b4-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
