---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermnetworkwatcherresourcetroubleshooting
schema: 2.0.0
ms.openlocfilehash: 411b70fb6018b71b1c1c7fbf67816d0c86e6d3b6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897845"
---
# <span data-ttu-id="5b864-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5b864-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="5b864-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b864-102">SYNOPSIS</span></span>
<span data-ttu-id="5b864-103">Rozpoczynanie rozwiązywania problemów z zasobem sieciowym na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5b864-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b864-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b864-104">SYNTAX</span></span>

### <span data-ttu-id="5b864-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5b864-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b864-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5b864-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b864-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5b864-107">DESCRIPTION</span></span>
<span data-ttu-id="5b864-108">Polecenie cmdlet Start-AzureRmNetworkWatcherResourceTroubleshooting uruchamia Rozwiązywanie problemów z zasobem sieciowym na platformie Azure i zwraca informacje o potencjalnych problemach i ograniczeniach.</span><span class="sxs-lookup"><span data-stu-id="5b864-108">The Start-AzureRmNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="5b864-109">Obecnie obsługiwane są bramy sieci wirtualnej i połączenia.</span><span class="sxs-lookup"><span data-stu-id="5b864-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="5b864-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b864-110">EXAMPLES</span></span>

### <span data-ttu-id="5b864-111">---Przykład 1: Rozpoczynanie rozwiązywania problemów z bramą sieci wirtualnej---</span><span class="sxs-lookup"><span data-stu-id="5b864-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="5b864-112">Powyższy przykład rozpoczyna Rozwiązywanie problemów z bramą sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5b864-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="5b864-113">Ukończenie operacji może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="5b864-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="5b864-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b864-114">PARAMETERS</span></span>

### <span data-ttu-id="5b864-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b864-115">-DefaultProfile</span></span>
<span data-ttu-id="5b864-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b864-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b864-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5b864-117">-NetworkWatcher</span></span>
<span data-ttu-id="5b864-118">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="5b864-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="5b864-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5b864-119">-NetworkWatcherName</span></span>
<span data-ttu-id="5b864-120">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="5b864-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="5b864-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b864-121">-ResourceGroupName</span></span>
<span data-ttu-id="5b864-122">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="5b864-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5b864-123">-StorageId</span><span class="sxs-lookup"><span data-stu-id="5b864-123">-StorageId</span></span>
<span data-ttu-id="5b864-124">Identyfikator magazynu.</span><span class="sxs-lookup"><span data-stu-id="5b864-124">The storage ID.</span></span>

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

### <span data-ttu-id="5b864-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="5b864-125">-StoragePath</span></span>
<span data-ttu-id="5b864-126">Ścieżka do magazynu.</span><span class="sxs-lookup"><span data-stu-id="5b864-126">The storage path.</span></span>

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

### <span data-ttu-id="5b864-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="5b864-127">-TargetResourceId</span></span>
<span data-ttu-id="5b864-128">Określa identyfikator zasobu, którego dotyczy problem.</span><span class="sxs-lookup"><span data-stu-id="5b864-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="5b864-129">Przykładowy format: "/subscriptions/$ {Identyfikator subskrypcji}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {ConnectionName}"</span><span class="sxs-lookup"><span data-stu-id="5b864-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="5b864-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b864-130">CommonParameters</span></span>
<span data-ttu-id="5b864-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b864-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b864-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b864-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b864-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b864-133">INPUTS</span></span>

### <span data-ttu-id="5b864-134">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5b864-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5b864-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5b864-135">System.String</span></span>

## <span data-ttu-id="5b864-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b864-136">OUTPUTS</span></span>

### <span data-ttu-id="5b864-137">Microsoft. Azure. Commands. Network. models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="5b864-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="5b864-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b864-138">NOTES</span></span>
<span data-ttu-id="5b864-139">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, rozwiązywanie problemów, VPN, połączenie</span><span class="sxs-lookup"><span data-stu-id="5b864-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="5b864-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b864-140">RELATED LINKS</span></span>

[<span data-ttu-id="5b864-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5b864-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5b864-142">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5b864-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5b864-143">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5b864-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5b864-144">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5b864-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5b864-145">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5b864-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5b864-146">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5b864-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="5b864-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5b864-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5b864-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5b864-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5b864-149">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5b864-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5b864-150">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5b864-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="5b864-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5b864-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="5b864-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5b864-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5b864-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5b864-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
