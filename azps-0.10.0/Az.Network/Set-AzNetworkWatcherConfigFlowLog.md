---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: f250615837f4953f63a4c5ff5f0a0ea965691856
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892753"
---
# <span data-ttu-id="d67e0-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d67e0-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="d67e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d67e0-102">SYNOPSIS</span></span>
<span data-ttu-id="d67e0-103">Konfiguruje rejestrowanie przepływu dla zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="d67e0-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="d67e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d67e0-104">SYNTAX</span></span>

### <span data-ttu-id="d67e0-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d67e0-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d67e0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d67e0-106">SetByName</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d67e0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d67e0-107">DESCRIPTION</span></span>
<span data-ttu-id="d67e0-108">Set-AzNetworkWatcherConfigFlowLog konfiguruje rejestrowanie przepływu dla zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="d67e0-108">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="d67e0-109">Właściwości do skonfigurowania: czy rejestrowanie przepływu jest włączone dla dostarczanego zasobu, skonfigurowane konto magazynu, w którym mają być wysyłane dzienniki, oraz zasady przechowywania dzienników.</span><span class="sxs-lookup"><span data-stu-id="d67e0-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="d67e0-110">W przypadku rejestrowania przepływów są obsługiwane obecnie grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="d67e0-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="d67e0-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d67e0-111">EXAMPLES</span></span>

### <span data-ttu-id="d67e0-112">---Przykład 1: Konfigurowanie rejestrowania przepływu dla określonego NSG---</span><span class="sxs-lookup"><span data-stu-id="d67e0-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="d67e0-113">W tym przykładzie skonfigurowano stan rejestrowania przepływu dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="d67e0-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="d67e0-114">W odpowiedzi widać, że określony NSG ma włączone rejestrowanie przepływu i nie ustawiono zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="d67e0-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="d67e0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d67e0-115">PARAMETERS</span></span>

### <span data-ttu-id="d67e0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d67e0-116">-AsJob</span></span>
<span data-ttu-id="d67e0-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d67e0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d67e0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d67e0-118">-DefaultProfile</span></span>
<span data-ttu-id="d67e0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d67e0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d67e0-120">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="d67e0-120">-EnableFlowLog</span></span>
<span data-ttu-id="d67e0-121">Flaga włączenia/wyłączenia rejestrowania przepływu.</span><span class="sxs-lookup"><span data-stu-id="d67e0-121">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d67e0-122">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="d67e0-122">-EnableRetention</span></span>
<span data-ttu-id="d67e0-123">Flaga włączenia/wyłączenia przechowywania.</span><span class="sxs-lookup"><span data-stu-id="d67e0-123">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d67e0-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d67e0-124">-NetworkWatcher</span></span>
<span data-ttu-id="d67e0-125">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d67e0-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="d67e0-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d67e0-126">-NetworkWatcherName</span></span>
<span data-ttu-id="d67e0-127">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d67e0-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="d67e0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d67e0-128">-ResourceGroupName</span></span>
<span data-ttu-id="d67e0-129">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d67e0-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d67e0-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d67e0-130">-RetentionInDays</span></span>
<span data-ttu-id="d67e0-131">Liczba dni przechowywania rekordów dziennika przepływu.</span><span class="sxs-lookup"><span data-stu-id="d67e0-131">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d67e0-132">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d67e0-132">-StorageAccountId</span></span>
<span data-ttu-id="d67e0-133">Identyfikator konta magazynu, które służy do przechowywania dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="d67e0-133">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="d67e0-134">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d67e0-134">-TargetResourceId</span></span>
<span data-ttu-id="d67e0-135">Identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="d67e0-135">The target resource ID.</span></span>

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

### <span data-ttu-id="d67e0-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d67e0-136">-Confirm</span></span>
<span data-ttu-id="d67e0-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d67e0-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67e0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d67e0-138">-WhatIf</span></span>
<span data-ttu-id="d67e0-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d67e0-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d67e0-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d67e0-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67e0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d67e0-141">CommonParameters</span></span>
<span data-ttu-id="d67e0-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d67e0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d67e0-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d67e0-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d67e0-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d67e0-144">INPUTS</span></span>

### <span data-ttu-id="d67e0-145">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d67e0-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d67e0-146">System. String system. Boolean system. Int32</span><span class="sxs-lookup"><span data-stu-id="d67e0-146">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="d67e0-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d67e0-147">OUTPUTS</span></span>

### <span data-ttu-id="d67e0-148">Microsoft. Azure. Commands. Network. models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="d67e0-148">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="d67e0-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d67e0-149">NOTES</span></span>
<span data-ttu-id="d67e0-150">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor, przepływ, dzienniki, flowlog, rejestrowanie</span><span class="sxs-lookup"><span data-stu-id="d67e0-150">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="d67e0-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d67e0-151">RELATED LINKS</span></span>

[<span data-ttu-id="d67e0-152">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d67e0-152">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d67e0-153">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d67e0-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d67e0-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d67e0-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d67e0-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d67e0-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d67e0-156">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d67e0-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d67e0-157">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d67e0-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d67e0-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d67e0-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d67e0-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d67e0-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d67e0-160">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d67e0-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d67e0-161">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d67e0-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d67e0-162">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d67e0-162">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d67e0-163">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d67e0-163">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d67e0-164">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d67e0-164">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d67e0-165">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d67e0-165">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d67e0-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d67e0-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
