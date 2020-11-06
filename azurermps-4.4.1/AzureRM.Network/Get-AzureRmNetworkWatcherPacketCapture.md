---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 4cf1cb9149c0f821ad0e6164cd7c817b12ccc147
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543267"
---
# <span data-ttu-id="4d4d1-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d4d1-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="4d4d1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d4d1-102">SYNOPSIS</span></span>
<span data-ttu-id="4d4d1-103">Pobiera informacje i właściwości oraz stan zasobu przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="4d4d1-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d4d1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d4d1-104">SYNTAX</span></span>

### <span data-ttu-id="4d4d1-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4d4d1-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d4d1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4d4d1-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d4d1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4d4d1-107">DESCRIPTION</span></span>
<span data-ttu-id="4d4d1-108">Get-AzureRmNetworkWatcherPacketCapture pobiera właściwości i stan zasobu przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="4d4d1-108">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="4d4d1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d4d1-109">EXAMPLES</span></span>

### <span data-ttu-id="4d4d1-110">---Przykład 1: Tworzenie przechwyconych pakietów za pomocą wielu filtrów i pobieranie ich stanu---</span><span class="sxs-lookup"><span data-stu-id="4d4d1-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="4d4d1-111">W tym przykładzie tworzymy przechwycony pakiet o nazwie "PacketCaptureTest" z wieloma filtrami i limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="4d4d1-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="4d4d1-112">Po zakończeniu sesji zostanie ona zapisana na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="4d4d1-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="4d4d1-113">Następnie dzwonimy Get-AzureRmNetworkWatcherPacketCapture, aby pobrać stan sesji przechwytywania.</span><span class="sxs-lookup"><span data-stu-id="4d4d1-113">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="4d4d1-114">Uwaga: aby można było tworzyć przechwycenia pakietów, rozszerzenie obserwatora sieci Azure musi być zainstalowane na docelowej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4d4d1-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="4d4d1-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d4d1-115">PARAMETERS</span></span>

### <span data-ttu-id="4d4d1-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d4d1-116">-NetworkWatcher</span></span>
<span data-ttu-id="4d4d1-117">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="4d4d1-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="4d4d1-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4d4d1-118">-NetworkWatcherName</span></span>
<span data-ttu-id="4d4d1-119">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="4d4d1-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="4d4d1-120">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="4d4d1-120">-PacketCaptureName</span></span>
<span data-ttu-id="4d4d1-121">Nazwa przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="4d4d1-121">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d4d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="4d4d1-123">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="4d4d1-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4d4d1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d4d1-124">-DefaultProfile</span></span>
<span data-ttu-id="4d4d1-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d4d1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d4d1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d4d1-126">CommonParameters</span></span>
<span data-ttu-id="4d4d1-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d4d1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d4d1-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d4d1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d4d1-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d4d1-129">INPUTS</span></span>

### <span data-ttu-id="4d4d1-130">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d4d1-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4d4d1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4d4d1-131">System.String</span></span>

## <span data-ttu-id="4d4d1-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d4d1-132">OUTPUTS</span></span>

### <span data-ttu-id="4d4d1-133">Microsoft. Azure. Commands. Network. models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="4d4d1-133">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="4d4d1-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d4d1-134">NOTES</span></span>
<span data-ttu-id="4d4d1-135">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, pakiet, przechwytywanie, ruch</span><span class="sxs-lookup"><span data-stu-id="4d4d1-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="4d4d1-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d4d1-136">RELATED LINKS</span></span>

[<span data-ttu-id="4d4d1-137">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d4d1-137">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d4d1-138">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4d4d1-138">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="4d4d1-139">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d4d1-139">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d4d1-140">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d4d1-140">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d4d1-141">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d4d1-141">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4d4d1-142">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d4d1-142">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4d4d1-143">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d4d1-143">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4d4d1-144">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4d4d1-144">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="4d4d1-145">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4d4d1-145">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="4d4d1-146">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4d4d1-146">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4d4d1-147">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4d4d1-147">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="4d4d1-148">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4d4d1-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

