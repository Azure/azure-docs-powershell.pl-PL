---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: a72f494518b3a511eac3e4b1a92330f666bbca64
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892681"
---
# <span data-ttu-id="ea715-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ea715-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="ea715-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea715-102">SYNOPSIS</span></span>
<span data-ttu-id="ea715-103">Rozpoczynanie rozwiązywania problemów z zasobem sieciowym na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ea715-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="ea715-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea715-104">SYNTAX</span></span>

### <span data-ttu-id="ea715-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ea715-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea715-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ea715-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea715-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ea715-107">DESCRIPTION</span></span>
<span data-ttu-id="ea715-108">Polecenie cmdlet Start-AzNetworkWatcherResourceTroubleshooting uruchamia Rozwiązywanie problemów z zasobem sieciowym na platformie Azure i zwraca informacje o potencjalnych problemach i ograniczeniach.</span><span class="sxs-lookup"><span data-stu-id="ea715-108">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="ea715-109">Obecnie obsługiwane są bramy sieci wirtualnej i połączenia.</span><span class="sxs-lookup"><span data-stu-id="ea715-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="ea715-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea715-110">EXAMPLES</span></span>

### <span data-ttu-id="ea715-111">---Przykład 1: Rozpoczynanie rozwiązywania problemów z bramą sieci wirtualnej---</span><span class="sxs-lookup"><span data-stu-id="ea715-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="ea715-112">Powyższy przykład rozpoczyna Rozwiązywanie problemów z bramą sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ea715-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="ea715-113">Ukończenie operacji może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="ea715-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="ea715-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea715-114">PARAMETERS</span></span>

### <span data-ttu-id="ea715-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea715-115">-DefaultProfile</span></span>
<span data-ttu-id="ea715-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea715-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea715-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ea715-117">-NetworkWatcher</span></span>
<span data-ttu-id="ea715-118">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="ea715-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="ea715-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ea715-119">-NetworkWatcherName</span></span>
<span data-ttu-id="ea715-120">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="ea715-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="ea715-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea715-121">-ResourceGroupName</span></span>
<span data-ttu-id="ea715-122">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="ea715-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ea715-123">-StorageId</span><span class="sxs-lookup"><span data-stu-id="ea715-123">-StorageId</span></span>
<span data-ttu-id="ea715-124">Identyfikator magazynu.</span><span class="sxs-lookup"><span data-stu-id="ea715-124">The storage ID.</span></span>

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

### <span data-ttu-id="ea715-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="ea715-125">-StoragePath</span></span>
<span data-ttu-id="ea715-126">Ścieżka do magazynu.</span><span class="sxs-lookup"><span data-stu-id="ea715-126">The storage path.</span></span>

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

### <span data-ttu-id="ea715-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ea715-127">-TargetResourceId</span></span>
<span data-ttu-id="ea715-128">Określa identyfikator zasobu, którego dotyczy problem.</span><span class="sxs-lookup"><span data-stu-id="ea715-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="ea715-129">Przykładowy format: "/subscriptions/$ {Identyfikator subskrypcji}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {ConnectionName}"</span><span class="sxs-lookup"><span data-stu-id="ea715-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="ea715-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea715-130">CommonParameters</span></span>
<span data-ttu-id="ea715-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea715-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea715-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea715-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea715-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea715-133">INPUTS</span></span>

### <span data-ttu-id="ea715-134">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ea715-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ea715-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ea715-135">System.String</span></span>

## <span data-ttu-id="ea715-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea715-136">OUTPUTS</span></span>

### <span data-ttu-id="ea715-137">Microsoft. Azure. Commands. Network. models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="ea715-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="ea715-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea715-138">NOTES</span></span>
<span data-ttu-id="ea715-139">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, rozwiązywanie problemów, VPN, połączenie</span><span class="sxs-lookup"><span data-stu-id="ea715-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="ea715-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea715-140">RELATED LINKS</span></span>

[<span data-ttu-id="ea715-141">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ea715-141">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ea715-142">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ea715-142">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ea715-143">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ea715-143">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ea715-144">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ea715-144">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ea715-145">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ea715-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ea715-146">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ea715-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ea715-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ea715-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ea715-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ea715-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ea715-149">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ea715-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ea715-150">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ea715-150">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ea715-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ea715-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ea715-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ea715-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ea715-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ea715-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
