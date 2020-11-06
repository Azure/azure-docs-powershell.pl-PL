---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: e8ce107453a447ef2da4cb8528b2f3e1f24a3ebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543211"
---
# <span data-ttu-id="fe1ae-101">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="fe1ae-101">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="fe1ae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="fe1ae-103">Konfiguruje rejestrowanie przepływu dla zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-103">Configures flow logging for a target resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe1ae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe1ae-104">SYNTAX</span></span>

### <span data-ttu-id="fe1ae-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fe1ae-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe1ae-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="fe1ae-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe1ae-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fe1ae-107">DESCRIPTION</span></span>
<span data-ttu-id="fe1ae-108">Set-AzureRmNetworkWatcherConfigFlowLog konfiguruje rejestrowanie przepływu dla zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-108">The Set-AzureRmNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="fe1ae-109">Właściwości do skonfigurowania: czy rejestrowanie przepływu jest włączone dla dostarczanego zasobu, skonfigurowane konto magazynu, w którym mają być wysyłane dzienniki, oraz zasady przechowywania dzienników.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="fe1ae-110">W przypadku rejestrowania przepływów są obsługiwane obecnie grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="fe1ae-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe1ae-111">EXAMPLES</span></span>

### <span data-ttu-id="fe1ae-112">---Przykład 1: Konfigurowanie rejestrowania przepływu dla określonego NSG---</span><span class="sxs-lookup"><span data-stu-id="fe1ae-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="fe1ae-113">W tym przykładzie skonfigurowano stan rejestrowania przepływu dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="fe1ae-114">W odpowiedzi widać, że określony NSG ma włączone rejestrowanie przepływu i nie ustawiono zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="fe1ae-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe1ae-115">PARAMETERS</span></span>

### <span data-ttu-id="fe1ae-116">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="fe1ae-116">-EnableFlowLog</span></span>
<span data-ttu-id="fe1ae-117">Flaga włączenia/wyłączenia rejestrowania przepływu.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-117">Flag to enable/disable flow logging.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe1ae-118">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="fe1ae-118">-EnableRetention</span></span>
<span data-ttu-id="fe1ae-119">Flaga włączenia/wyłączenia przechowywania.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-119">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe1ae-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fe1ae-120">-NetworkWatcher</span></span>
<span data-ttu-id="fe1ae-121">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="fe1ae-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="fe1ae-122">-NetworkWatcherName</span></span>
<span data-ttu-id="fe1ae-123">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="fe1ae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe1ae-124">-ResourceGroupName</span></span>
<span data-ttu-id="fe1ae-125">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="fe1ae-126">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="fe1ae-126">-RetentionInDays</span></span>
<span data-ttu-id="fe1ae-127">Liczba dni przechowywania rekordów dziennika przepływu.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-127">Number of days to retain flow log records.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe1ae-128">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="fe1ae-128">-StorageAccountId</span></span>
<span data-ttu-id="fe1ae-129">Identyfikator konta magazynu, które służy do przechowywania dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-129">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="fe1ae-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="fe1ae-130">-TargetResourceId</span></span>
<span data-ttu-id="fe1ae-131">Identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-131">The target resource ID.</span></span>

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

### <span data-ttu-id="fe1ae-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fe1ae-132">-Confirm</span></span>
<span data-ttu-id="fe1ae-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1ae-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe1ae-134">-WhatIf</span></span>
<span data-ttu-id="fe1ae-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe1ae-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1ae-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe1ae-137">-DefaultProfile</span></span>
<span data-ttu-id="fe1ae-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe1ae-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe1ae-139">CommonParameters</span></span>
<span data-ttu-id="fe1ae-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe1ae-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe1ae-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe1ae-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe1ae-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe1ae-142">INPUTS</span></span>

### <span data-ttu-id="fe1ae-143">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fe1ae-143">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="fe1ae-144">System. String system. Boolean system. Int32</span><span class="sxs-lookup"><span data-stu-id="fe1ae-144">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="fe1ae-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe1ae-145">OUTPUTS</span></span>

### <span data-ttu-id="fe1ae-146">Microsoft. Azure. Commands. Network. models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="fe1ae-146">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="fe1ae-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe1ae-147">NOTES</span></span>
<span data-ttu-id="fe1ae-148">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor, przepływ, dzienniki, flowlog, rejestrowanie</span><span class="sxs-lookup"><span data-stu-id="fe1ae-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="fe1ae-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe1ae-149">RELATED LINKS</span></span>

[<span data-ttu-id="fe1ae-150">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="fe1ae-150">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="fe1ae-151">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fe1ae-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="fe1ae-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fe1ae-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="fe1ae-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fe1ae-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="fe1ae-154">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fe1ae-154">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fe1ae-155">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="fe1ae-155">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="fe1ae-156">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fe1ae-156">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fe1ae-157">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fe1ae-157">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fe1ae-158">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fe1ae-158">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fe1ae-159">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="fe1ae-159">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="fe1ae-160">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="fe1ae-160">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="fe1ae-161">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="fe1ae-161">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="fe1ae-162">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="fe1ae-162">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="fe1ae-163">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="fe1ae-163">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="fe1ae-164">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="fe1ae-164">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
