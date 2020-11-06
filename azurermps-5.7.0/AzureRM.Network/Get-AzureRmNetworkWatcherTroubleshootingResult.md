---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: ef730b8ee6e6c35408b9d57d9dc23b0ab51a63d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528082"
---
# <span data-ttu-id="842a2-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="842a2-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="842a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="842a2-102">SYNOPSIS</span></span>
<span data-ttu-id="842a2-103">Pobiera wyniki rozwiązywania problemów z poprzednio uruchomionej lub obecnie uruchomionej operacji rozwiązywania problemów.</span><span class="sxs-lookup"><span data-stu-id="842a2-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="842a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="842a2-104">SYNTAX</span></span>

### <span data-ttu-id="842a2-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="842a2-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="842a2-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="842a2-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="842a2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="842a2-107">DESCRIPTION</span></span>
<span data-ttu-id="842a2-108">Polecenie cmdlet Get-AzureRmNetworkWatcherTroubleshootingResult pobiera wyniki rozwiązywania problemów z poprzednio uruchomionego lub obecnie uruchomionego Start-AzureRmNetworkWatcherResourceTroubleshooting operacji.</span><span class="sxs-lookup"><span data-stu-id="842a2-108">The Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzureRmNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="842a2-109">Jeśli obecnie trwa operacja rozwiązywania problemów, wykonanie tej operacji może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="842a2-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="842a2-110">Obecnie obsługiwane są bramy sieci wirtualnej i połączenia.</span><span class="sxs-lookup"><span data-stu-id="842a2-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="842a2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="842a2-111">EXAMPLES</span></span>

### <span data-ttu-id="842a2-112">---Przykład 1: Rozpoczynanie rozwiązywania problemów z bramą sieci wirtualnej i pobieranie---wyników</span><span class="sxs-lookup"><span data-stu-id="842a2-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="842a2-113">Powyższy przykład rozpoczyna Rozwiązywanie problemów z bramą sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="842a2-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="842a2-114">Ukończenie operacji może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="842a2-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="842a2-115">Po rozpoczęciu rozwiązywania problemów z zasobem zostanie nawiązane połączenie Get-AzureRmNetworkWatcherTroubleshootingResult, aby pobrać wynik tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="842a2-115">After troubleshooting has started, a Get-AzureRmNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="842a2-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="842a2-116">PARAMETERS</span></span>

### <span data-ttu-id="842a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="842a2-117">-DefaultProfile</span></span>
<span data-ttu-id="842a2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="842a2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="842a2-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="842a2-119">-NetworkWatcher</span></span>
<span data-ttu-id="842a2-120">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="842a2-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="842a2-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="842a2-121">-NetworkWatcherName</span></span>
<span data-ttu-id="842a2-122">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="842a2-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="842a2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="842a2-123">-ResourceGroupName</span></span>
<span data-ttu-id="842a2-124">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="842a2-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="842a2-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="842a2-125">-TargetResourceId</span></span>
<span data-ttu-id="842a2-126">Identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="842a2-126">The target resource ID.</span></span>

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

### <span data-ttu-id="842a2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="842a2-127">CommonParameters</span></span>
<span data-ttu-id="842a2-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="842a2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="842a2-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="842a2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="842a2-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="842a2-130">INPUTS</span></span>

### <span data-ttu-id="842a2-131">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="842a2-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="842a2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="842a2-132">System.String</span></span>

## <span data-ttu-id="842a2-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="842a2-133">OUTPUTS</span></span>

### <span data-ttu-id="842a2-134">Microsoft. Azure. Commands. Network. models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="842a2-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="842a2-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="842a2-135">NOTES</span></span>
<span data-ttu-id="842a2-136">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, rozwiązywanie problemów, VPN, połączenie</span><span class="sxs-lookup"><span data-stu-id="842a2-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="842a2-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="842a2-137">RELATED LINKS</span></span>

[<span data-ttu-id="842a2-138">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="842a2-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="842a2-139">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="842a2-139">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="842a2-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="842a2-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="842a2-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="842a2-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="842a2-142">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="842a2-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="842a2-143">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="842a2-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="842a2-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="842a2-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="842a2-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="842a2-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="842a2-146">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="842a2-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="842a2-147">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="842a2-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="842a2-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="842a2-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="842a2-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="842a2-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="842a2-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="842a2-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
