---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpacketcapturefilterconfig
schema: 2.0.0
ms.openlocfilehash: 1d6054307ad1e499fbb36342f6c81e7e32227f37
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898285"
---
# <span data-ttu-id="c7bdc-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c7bdc-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="c7bdc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="c7bdc-103">Tworzy nowy obiekt filtru przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7bdc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7bdc-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7bdc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c7bdc-105">DESCRIPTION</span></span>
<span data-ttu-id="c7bdc-106">Polecenie cmdlet New-AzureRmPacketCaptureFilterConfig tworzy nowy obiekt filtru przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="c7bdc-107">Ten obiekt służy do ograniczania typu pakietów, które są przechwytywane podczas sesji przechwytywania pakietów przy użyciu określonych kryteriów.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="c7bdc-108">Polecenie cmdlet New-AzureRmNetworkWatcherPacketCapture może akceptować wiele obiektów filtrowania, aby umożliwić tworzenie sesji przechwytywania.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="c7bdc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7bdc-109">EXAMPLES</span></span>

### <span data-ttu-id="c7bdc-110">---Przykład 1: Tworzenie przechwytywania pakietów z wieloma filtrami---</span><span class="sxs-lookup"><span data-stu-id="c7bdc-110">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="c7bdc-111">W tym przykładzie tworzymy przechwycony pakiet o nazwie "PacketCaptureTest" z wieloma filtrami i limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="c7bdc-112">Po zakończeniu sesji zostanie ona zapisana na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-112">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="c7bdc-113">Uwaga: aby można było tworzyć przechwycenia pakietów, rozszerzenie obserwatora sieci Azure musi być zainstalowane na docelowej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="c7bdc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7bdc-114">PARAMETERS</span></span>

### <span data-ttu-id="c7bdc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7bdc-115">-DefaultProfile</span></span>
<span data-ttu-id="c7bdc-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7bdc-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="c7bdc-117">-LocalIPAddress</span></span>
<span data-ttu-id="c7bdc-118">Określa lokalny adres IP, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="c7bdc-119">Przykładowe dane wejściowe: "127.0.0.1" dla pojedynczego wpisu adresu.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="c7bdc-120">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="c7bdc-121">"127.0.0.1; 127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="c7bdc-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="c7bdc-122">-LocalPort</span></span>
<span data-ttu-id="c7bdc-123">Określa lokalny adres IP, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="c7bdc-124">Przykładowe dane wejściowe: "127.0.0.1" dla pojedynczego wpisu adresu.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="c7bdc-125">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="c7bdc-126">"127.0.0.1; 127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="c7bdc-127">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="c7bdc-127">-Protocol</span></span>
<span data-ttu-id="c7bdc-128">Określa procotol, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-128">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="c7bdc-129">Dopuszczalne wartości "TCP", "UDP", "any"</span><span class="sxs-lookup"><span data-stu-id="c7bdc-129">Acceptable values "TCP","UDP","Any"</span></span>

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

### <span data-ttu-id="c7bdc-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="c7bdc-130">-RemoteIPAddress</span></span>
<span data-ttu-id="c7bdc-131">Określa zdalny adres IP, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="c7bdc-132">Przykładowe dane wejściowe: "127.0.0.1" dla pojedynczego wpisu adresu.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="c7bdc-133">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="c7bdc-134">"127.0.0.1; 127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="c7bdc-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="c7bdc-135">-RemotePort</span></span>
<span data-ttu-id="c7bdc-136">Określa port zdalny, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="c7bdc-137">Przykładowe dane wejściowe portu zdalnego: "80" dla wpisu Single Port.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="c7bdc-138">"80-85" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-138">"80-85" for range.</span></span>
<span data-ttu-id="c7bdc-139">"80; 443;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="c7bdc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7bdc-140">CommonParameters</span></span>
<span data-ttu-id="c7bdc-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7bdc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7bdc-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7bdc-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7bdc-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7bdc-143">INPUTS</span></span>

### <span data-ttu-id="c7bdc-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c7bdc-144">System.String</span></span>

## <span data-ttu-id="c7bdc-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7bdc-145">OUTPUTS</span></span>

### <span data-ttu-id="c7bdc-146">Microsoft. Azure. Commands. Network. models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="c7bdc-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="c7bdc-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7bdc-147">NOTES</span></span>
<span data-ttu-id="c7bdc-148">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor, pakiet, przechwytywanie, ruch, filtr</span><span class="sxs-lookup"><span data-stu-id="c7bdc-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="c7bdc-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7bdc-149">RELATED LINKS</span></span>

[<span data-ttu-id="c7bdc-150">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7bdc-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7bdc-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7bdc-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7bdc-152">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7bdc-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7bdc-153">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7bdc-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7bdc-154">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7bdc-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c7bdc-155">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7bdc-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c7bdc-156">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7bdc-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c7bdc-157">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c7bdc-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="c7bdc-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c7bdc-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="c7bdc-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c7bdc-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c7bdc-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c7bdc-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="c7bdc-161">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c7bdc-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
