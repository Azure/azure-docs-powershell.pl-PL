---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: c3d1e7e3a76a2561c77c8d580b7365f8fd2e6fee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890709"
---
# <span data-ttu-id="0e9f4-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0e9f4-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="0e9f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e9f4-102">SYNOPSIS</span></span>
<span data-ttu-id="0e9f4-103">Pobiera wyniki rozwiązywania problemów z poprzednio uruchomionej lub obecnie uruchomionej operacji rozwiązywania problemów.</span><span class="sxs-lookup"><span data-stu-id="0e9f4-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="0e9f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e9f4-104">SYNTAX</span></span>

### <span data-ttu-id="0e9f4-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0e9f4-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e9f4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0e9f4-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e9f4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0e9f4-107">DESCRIPTION</span></span>
<span data-ttu-id="0e9f4-108">Polecenie cmdlet Get-AzNetworkWatcherTroubleshootingResult pobiera wyniki rozwiązywania problemów z poprzednio uruchomionego lub obecnie uruchomionego Start-AzNetworkWatcherResourceTroubleshooting operacji.</span><span class="sxs-lookup"><span data-stu-id="0e9f4-108">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="0e9f4-109">Jeśli obecnie trwa operacja rozwiązywania problemów, wykonanie tej operacji może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="0e9f4-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="0e9f4-110">Obecnie obsługiwane są bramy sieci wirtualnej i połączenia.</span><span class="sxs-lookup"><span data-stu-id="0e9f4-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="0e9f4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e9f4-111">EXAMPLES</span></span>

### <span data-ttu-id="0e9f4-112">---Przykład 1: Rozpoczynanie rozwiązywania problemów z bramą sieci wirtualnej i pobieranie---wyników</span><span class="sxs-lookup"><span data-stu-id="0e9f4-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="0e9f4-113">Powyższy przykład rozpoczyna Rozwiązywanie problemów z bramą sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0e9f4-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="0e9f4-114">Ukończenie operacji może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="0e9f4-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="0e9f4-115">Po rozpoczęciu rozwiązywania problemów z zasobem zostanie nawiązane połączenie Get-AzNetworkWatcherTroubleshootingResult, aby pobrać wynik tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="0e9f4-115">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="0e9f4-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e9f4-116">PARAMETERS</span></span>

### <span data-ttu-id="0e9f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e9f4-117">-DefaultProfile</span></span>
<span data-ttu-id="0e9f4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e9f4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e9f4-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e9f4-119">-NetworkWatcher</span></span>
<span data-ttu-id="0e9f4-120">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="0e9f4-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="0e9f4-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0e9f4-121">-NetworkWatcherName</span></span>
<span data-ttu-id="0e9f4-122">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="0e9f4-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="0e9f4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e9f4-123">-ResourceGroupName</span></span>
<span data-ttu-id="0e9f4-124">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="0e9f4-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0e9f4-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="0e9f4-125">-TargetResourceId</span></span>
<span data-ttu-id="0e9f4-126">Identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="0e9f4-126">The target resource ID.</span></span>

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

### <span data-ttu-id="0e9f4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e9f4-127">CommonParameters</span></span>
<span data-ttu-id="0e9f4-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e9f4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e9f4-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e9f4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e9f4-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e9f4-130">INPUTS</span></span>

### <span data-ttu-id="0e9f4-131">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e9f4-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="0e9f4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0e9f4-132">System.String</span></span>

## <span data-ttu-id="0e9f4-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e9f4-133">OUTPUTS</span></span>

### <span data-ttu-id="0e9f4-134">Microsoft. Azure. Commands. Network. models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="0e9f4-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="0e9f4-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e9f4-135">NOTES</span></span>
<span data-ttu-id="0e9f4-136">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, rozwiązywanie problemów, VPN, połączenie</span><span class="sxs-lookup"><span data-stu-id="0e9f4-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="0e9f4-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e9f4-137">RELATED LINKS</span></span>

[<span data-ttu-id="0e9f4-138">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0e9f4-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0e9f4-139">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e9f4-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0e9f4-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e9f4-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0e9f4-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e9f4-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0e9f4-142">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e9f4-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e9f4-143">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0e9f4-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0e9f4-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e9f4-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e9f4-145">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e9f4-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e9f4-146">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e9f4-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e9f4-147">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0e9f4-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0e9f4-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0e9f4-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0e9f4-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0e9f4-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0e9f4-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0e9f4-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
