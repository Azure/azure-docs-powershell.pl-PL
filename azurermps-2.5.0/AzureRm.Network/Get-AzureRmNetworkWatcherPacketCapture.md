---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: aeadada7c6e2e2d7cb94a484e7ca3223e03b4426
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897613"
---
# <span data-ttu-id="f5a0d-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f5a0d-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="f5a0d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a0d-103">Pobiera informacje i właściwości oraz stan zasobu przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="f5a0d-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5a0d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5a0d-104">SYNTAX</span></span>

### <span data-ttu-id="f5a0d-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f5a0d-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5a0d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f5a0d-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5a0d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f5a0d-107">DESCRIPTION</span></span>
<span data-ttu-id="f5a0d-108">Get-AzureRmNetworkWatcherPacketCapture pobiera właściwości i stan zasobu przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="f5a0d-108">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="f5a0d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5a0d-109">EXAMPLES</span></span>

### <span data-ttu-id="f5a0d-110">---Przykład 1: Tworzenie przechwyconych pakietów za pomocą wielu filtrów i pobieranie ich stanu---</span><span class="sxs-lookup"><span data-stu-id="f5a0d-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="f5a0d-111">W tym przykładzie tworzymy przechwycony pakiet o nazwie "PacketCaptureTest" z wieloma filtrami i limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="f5a0d-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="f5a0d-112">Po zakończeniu sesji zostanie ona zapisana na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="f5a0d-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="f5a0d-113">Następnie dzwonimy Get-AzureRmNetworkWatcherPacketCapture, aby pobrać stan sesji przechwytywania.</span><span class="sxs-lookup"><span data-stu-id="f5a0d-113">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="f5a0d-114">Uwaga: aby można było tworzyć przechwycenia pakietów, rozszerzenie obserwatora sieci Azure musi być zainstalowane na docelowej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f5a0d-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="f5a0d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5a0d-115">PARAMETERS</span></span>

### <span data-ttu-id="f5a0d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5a0d-116">-AsJob</span></span>
<span data-ttu-id="f5a0d-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f5a0d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5a0d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5a0d-118">-DefaultProfile</span></span>
<span data-ttu-id="f5a0d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5a0d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5a0d-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f5a0d-120">-NetworkWatcher</span></span>
<span data-ttu-id="f5a0d-121">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="f5a0d-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="f5a0d-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f5a0d-122">-NetworkWatcherName</span></span>
<span data-ttu-id="f5a0d-123">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="f5a0d-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="f5a0d-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="f5a0d-124">-PacketCaptureName</span></span>
<span data-ttu-id="f5a0d-125">Nazwa przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="f5a0d-125">The packet capture name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5a0d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5a0d-126">-ResourceGroupName</span></span>
<span data-ttu-id="f5a0d-127">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="f5a0d-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f5a0d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a0d-128">CommonParameters</span></span>
<span data-ttu-id="f5a0d-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5a0d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a0d-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5a0d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a0d-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5a0d-131">INPUTS</span></span>

### <span data-ttu-id="f5a0d-132">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f5a0d-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f5a0d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f5a0d-133">System.String</span></span>

## <span data-ttu-id="f5a0d-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5a0d-134">OUTPUTS</span></span>

### <span data-ttu-id="f5a0d-135">Microsoft. Azure. Commands. Network. models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="f5a0d-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="f5a0d-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5a0d-136">NOTES</span></span>
<span data-ttu-id="f5a0d-137">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, pakiet, przechwytywanie, ruch</span><span class="sxs-lookup"><span data-stu-id="f5a0d-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="f5a0d-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5a0d-138">RELATED LINKS</span></span>

[<span data-ttu-id="f5a0d-139">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f5a0d-139">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f5a0d-140">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f5a0d-140">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="f5a0d-141">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f5a0d-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f5a0d-142">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f5a0d-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f5a0d-143">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f5a0d-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f5a0d-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f5a0d-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f5a0d-145">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f5a0d-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f5a0d-146">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f5a0d-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="f5a0d-147">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f5a0d-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="f5a0d-148">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f5a0d-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f5a0d-149">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f5a0d-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="f5a0d-150">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f5a0d-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

