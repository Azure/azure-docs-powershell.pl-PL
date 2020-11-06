---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
ms.openlocfilehash: a9f8570f1401387df8f26a9998c422e132f395e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552883"
---
# <span data-ttu-id="beeec-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="beeec-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="beeec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="beeec-102">SYNOPSIS</span></span>
<span data-ttu-id="beeec-103">Tworzy nowy obiekt filtru przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="beeec-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="beeec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="beeec-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="beeec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="beeec-105">DESCRIPTION</span></span>
<span data-ttu-id="beeec-106">Polecenie cmdlet New-AzureRmPacketCaptureFilterConfig tworzy nowy obiekt filtru przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="beeec-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="beeec-107">Ten obiekt służy do ograniczania typu pakietów, które są przechwytywane podczas sesji przechwytywania pakietów przy użyciu określonych kryteriów.</span><span class="sxs-lookup"><span data-stu-id="beeec-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="beeec-108">Polecenie cmdlet New-AzureRmNetworkWatcherPacketCapture może akceptować wiele obiektów filtrowania, aby umożliwić tworzenie sesji przechwytywania.</span><span class="sxs-lookup"><span data-stu-id="beeec-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="beeec-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="beeec-109">EXAMPLES</span></span>

### <span data-ttu-id="beeec-110">---Przykład 1: Tworzenie przechwytywania pakietów z wieloma filtrami---</span><span class="sxs-lookup"><span data-stu-id="beeec-110">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="beeec-111">W tym przykładzie tworzymy przechwycony pakiet o nazwie "PacketCaptureTest" z wieloma filtrami i limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="beeec-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="beeec-112">Po zakończeniu sesji zostanie ona zapisana na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="beeec-112">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="beeec-113">Uwaga: aby można było tworzyć przechwycenia pakietów, rozszerzenie obserwatora sieci Azure musi być zainstalowane na docelowej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="beeec-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="beeec-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="beeec-114">PARAMETERS</span></span>

### <span data-ttu-id="beeec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beeec-115">-DefaultProfile</span></span>
<span data-ttu-id="beeec-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="beeec-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="beeec-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="beeec-117">-LocalIPAddress</span></span>
<span data-ttu-id="beeec-118">Określa lokalny adres IP, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="beeec-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="beeec-119">Przykładowe dane wejściowe: "127.0.0.1" dla pojedynczego wpisu adresu.</span><span class="sxs-lookup"><span data-stu-id="beeec-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="beeec-120">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="beeec-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="beeec-121">"127.0.0.1; 127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="beeec-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beeec-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="beeec-122">-LocalPort</span></span>
<span data-ttu-id="beeec-123">Określa lokalny adres IP, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="beeec-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="beeec-124">Przykładowe dane wejściowe: "127.0.0.1" dla pojedynczego wpisu adresu.</span><span class="sxs-lookup"><span data-stu-id="beeec-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="beeec-125">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="beeec-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="beeec-126">"127.0.0.1; 127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="beeec-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beeec-127">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="beeec-127">-Protocol</span></span>
<span data-ttu-id="beeec-128">Określa procotol, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="beeec-128">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="beeec-129">Dopuszczalne wartości "TCP", "UDP", "any"</span><span class="sxs-lookup"><span data-stu-id="beeec-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="beeec-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="beeec-130">-RemoteIPAddress</span></span>
<span data-ttu-id="beeec-131">Określa zdalny adres IP, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="beeec-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="beeec-132">Przykładowe dane wejściowe: "127.0.0.1" dla pojedynczego wpisu adresu.</span><span class="sxs-lookup"><span data-stu-id="beeec-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="beeec-133">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="beeec-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="beeec-134">"127.0.0.1; 127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="beeec-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beeec-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="beeec-135">-RemotePort</span></span>
<span data-ttu-id="beeec-136">Określa port zdalny, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="beeec-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="beeec-137">Przykładowe dane wejściowe portu zdalnego: "80" dla wpisu Single Port.</span><span class="sxs-lookup"><span data-stu-id="beeec-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="beeec-138">"80-85" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="beeec-138">"80-85" for range.</span></span>
<span data-ttu-id="beeec-139">"80; 443;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="beeec-139">"80;443;" for multiple entries.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beeec-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beeec-140">CommonParameters</span></span>
<span data-ttu-id="beeec-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beeec-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beeec-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beeec-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beeec-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="beeec-143">INPUTS</span></span>

### <span data-ttu-id="beeec-144">System. String</span><span class="sxs-lookup"><span data-stu-id="beeec-144">System.String</span></span>

## <span data-ttu-id="beeec-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="beeec-145">OUTPUTS</span></span>

### <span data-ttu-id="beeec-146">Microsoft. Azure. Commands. Network. models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="beeec-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="beeec-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="beeec-147">NOTES</span></span>
<span data-ttu-id="beeec-148">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor, pakiet, przechwytywanie, ruch, filtr</span><span class="sxs-lookup"><span data-stu-id="beeec-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="beeec-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="beeec-149">RELATED LINKS</span></span>

[<span data-ttu-id="beeec-150">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="beeec-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="beeec-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="beeec-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="beeec-152">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="beeec-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="beeec-153">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="beeec-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="beeec-154">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="beeec-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="beeec-155">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="beeec-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="beeec-156">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="beeec-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="beeec-157">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="beeec-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="beeec-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="beeec-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="beeec-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="beeec-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="beeec-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="beeec-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="beeec-161">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="beeec-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
