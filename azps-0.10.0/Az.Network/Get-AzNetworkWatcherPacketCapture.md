---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 8e2e7a25b2c6e2c9eaa5e53234d7c1c9c3d0fa9f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890717"
---
# <span data-ttu-id="bb070-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bb070-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="bb070-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb070-102">SYNOPSIS</span></span>
<span data-ttu-id="bb070-103">Pobiera informacje i właściwości oraz stan zasobu przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="bb070-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="bb070-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb070-104">SYNTAX</span></span>

### <span data-ttu-id="bb070-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bb070-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb070-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="bb070-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb070-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bb070-107">DESCRIPTION</span></span>
<span data-ttu-id="bb070-108">Get-AzNetworkWatcherPacketCapture pobiera właściwości i stan zasobu przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="bb070-108">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="bb070-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb070-109">EXAMPLES</span></span>

### <span data-ttu-id="bb070-110">---Przykład 1: Tworzenie przechwyconych pakietów za pomocą wielu filtrów i pobieranie ich stanu---</span><span class="sxs-lookup"><span data-stu-id="bb070-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="bb070-111">W tym przykładzie tworzymy przechwycony pakiet o nazwie "PacketCaptureTest" z wieloma filtrami i limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="bb070-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="bb070-112">Po zakończeniu sesji zostanie ona zapisana na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="bb070-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="bb070-113">Następnie dzwonimy Get-AzNetworkWatcherPacketCapture, aby pobrać stan sesji przechwytywania.</span><span class="sxs-lookup"><span data-stu-id="bb070-113">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="bb070-114">Uwaga: aby można było tworzyć przechwycenia pakietów, rozszerzenie obserwatora sieci Azure musi być zainstalowane na docelowej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bb070-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="bb070-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb070-115">PARAMETERS</span></span>

### <span data-ttu-id="bb070-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb070-116">-AsJob</span></span>
<span data-ttu-id="bb070-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bb070-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb070-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb070-118">-DefaultProfile</span></span>
<span data-ttu-id="bb070-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb070-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb070-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb070-120">-NetworkWatcher</span></span>
<span data-ttu-id="bb070-121">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="bb070-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="bb070-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="bb070-122">-NetworkWatcherName</span></span>
<span data-ttu-id="bb070-123">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="bb070-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="bb070-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="bb070-124">-PacketCaptureName</span></span>
<span data-ttu-id="bb070-125">Nazwa przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="bb070-125">The packet capture name.</span></span>

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

### <span data-ttu-id="bb070-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb070-126">-ResourceGroupName</span></span>
<span data-ttu-id="bb070-127">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="bb070-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="bb070-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb070-128">CommonParameters</span></span>
<span data-ttu-id="bb070-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb070-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb070-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb070-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb070-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb070-131">INPUTS</span></span>

### <span data-ttu-id="bb070-132">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb070-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="bb070-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bb070-133">System.String</span></span>

## <span data-ttu-id="bb070-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb070-134">OUTPUTS</span></span>

### <span data-ttu-id="bb070-135">Microsoft. Azure. Commands. Network. models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="bb070-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="bb070-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb070-136">NOTES</span></span>
<span data-ttu-id="bb070-137">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, pakiet, przechwytywanie, ruch</span><span class="sxs-lookup"><span data-stu-id="bb070-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="bb070-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb070-138">RELATED LINKS</span></span>

[<span data-ttu-id="bb070-139">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bb070-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bb070-140">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="bb070-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="bb070-141">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bb070-141">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bb070-142">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bb070-142">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bb070-143">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb070-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="bb070-144">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb070-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="bb070-145">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb070-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="bb070-146">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="bb070-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="bb070-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="bb070-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="bb070-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="bb070-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="bb070-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="bb070-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="bb070-150">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="bb070-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

