---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: f220f029b25963fa07d582b6ddd70b572791924a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552380"
---
# <span data-ttu-id="1bd17-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1bd17-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="1bd17-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1bd17-102">SYNOPSIS</span></span>
<span data-ttu-id="1bd17-103">Rozpoczynanie rozwiązywania problemów z zasobem sieciowym na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="1bd17-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bd17-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1bd17-104">SYNTAX</span></span>

### <span data-ttu-id="1bd17-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1bd17-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bd17-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1bd17-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bd17-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1bd17-107">DESCRIPTION</span></span>
<span data-ttu-id="1bd17-108">Polecenie cmdlet Start-AzureRmNetworkWatcherResourceTroubleshooting uruchamia Rozwiązywanie problemów z zasobem sieciowym na platformie Azure i zwraca informacje o potencjalnych problemach i ograniczeniach.</span><span class="sxs-lookup"><span data-stu-id="1bd17-108">The Start-AzureRmNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="1bd17-109">Obecnie obsługiwane są bramy sieci wirtualnej i połączenia.</span><span class="sxs-lookup"><span data-stu-id="1bd17-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="1bd17-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1bd17-110">EXAMPLES</span></span>

### <span data-ttu-id="1bd17-111">---Przykład 1: Rozpoczynanie rozwiązywania problemów z bramą sieci wirtualnej---</span><span class="sxs-lookup"><span data-stu-id="1bd17-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="1bd17-112">Powyższy przykład rozpoczyna Rozwiązywanie problemów z bramą sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1bd17-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="1bd17-113">Ukończenie operacji może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="1bd17-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="1bd17-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1bd17-114">PARAMETERS</span></span>

### <span data-ttu-id="1bd17-115">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1bd17-115">-NetworkWatcher</span></span>
<span data-ttu-id="1bd17-116">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="1bd17-116">The network watcher resource.</span></span>

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

### <span data-ttu-id="1bd17-117">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1bd17-117">-NetworkWatcherName</span></span>
<span data-ttu-id="1bd17-118">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="1bd17-118">The name of network watcher.</span></span>

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

### <span data-ttu-id="1bd17-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bd17-119">-ResourceGroupName</span></span>
<span data-ttu-id="1bd17-120">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="1bd17-120">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1bd17-121">-StorageId</span><span class="sxs-lookup"><span data-stu-id="1bd17-121">-StorageId</span></span>
<span data-ttu-id="1bd17-122">Identyfikator magazynu.</span><span class="sxs-lookup"><span data-stu-id="1bd17-122">The storage ID.</span></span>

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

### <span data-ttu-id="1bd17-123">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="1bd17-123">-StoragePath</span></span>
<span data-ttu-id="1bd17-124">Ścieżka do magazynu.</span><span class="sxs-lookup"><span data-stu-id="1bd17-124">The storage path.</span></span>

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

### <span data-ttu-id="1bd17-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="1bd17-125">-TargetResourceId</span></span>
<span data-ttu-id="1bd17-126">Określa identyfikator zasobu, którego dotyczy problem.</span><span class="sxs-lookup"><span data-stu-id="1bd17-126">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="1bd17-127">Przykładowy format: "/subscriptions/$ {Identyfikator subskrypcji}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {ConnectionName}"</span><span class="sxs-lookup"><span data-stu-id="1bd17-127">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="1bd17-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bd17-128">-DefaultProfile</span></span>
<span data-ttu-id="1bd17-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1bd17-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bd17-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bd17-130">CommonParameters</span></span>
<span data-ttu-id="1bd17-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bd17-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bd17-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bd17-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bd17-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1bd17-133">INPUTS</span></span>

### <span data-ttu-id="1bd17-134">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1bd17-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="1bd17-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1bd17-135">System.String</span></span>

## <span data-ttu-id="1bd17-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1bd17-136">OUTPUTS</span></span>

### <span data-ttu-id="1bd17-137">Microsoft. Azure. Commands. Network. models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="1bd17-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="1bd17-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1bd17-138">NOTES</span></span>
<span data-ttu-id="1bd17-139">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, rozwiązywanie problemów, VPN, połączenie</span><span class="sxs-lookup"><span data-stu-id="1bd17-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="1bd17-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1bd17-140">RELATED LINKS</span></span>

[<span data-ttu-id="1bd17-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1bd17-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1bd17-142">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1bd17-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1bd17-143">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1bd17-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1bd17-144">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1bd17-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1bd17-145">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1bd17-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1bd17-146">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1bd17-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="1bd17-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1bd17-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1bd17-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1bd17-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1bd17-149">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1bd17-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1bd17-150">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1bd17-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="1bd17-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1bd17-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="1bd17-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1bd17-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1bd17-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1bd17-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
