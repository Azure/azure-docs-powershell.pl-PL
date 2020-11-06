---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
ms.openlocfilehash: ad6d2baaccdc17ec6ca414ae4b0cee84db20c94b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543264"
---
# <span data-ttu-id="6fa45-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6fa45-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="6fa45-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6fa45-102">SYNOPSIS</span></span>
<span data-ttu-id="6fa45-103">Tworzy nowy obiekt filtru przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="6fa45-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fa45-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6fa45-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fa45-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6fa45-105">DESCRIPTION</span></span>
<span data-ttu-id="6fa45-106">Polecenie cmdlet New-AzureRmPacketCaptureFilterConfig tworzy nowy obiekt filtru przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="6fa45-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="6fa45-107">Ten obiekt służy do ograniczania typu pakietów, które są przechwytywane podczas sesji przechwytywania pakietów przy użyciu określonych kryteriów.</span><span class="sxs-lookup"><span data-stu-id="6fa45-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="6fa45-108">Polecenie cmdlet New-AzureRmNetworkWatcherPacketCapture może akceptować wiele obiektów filtrowania, aby umożliwić tworzenie sesji przechwytywania.</span><span class="sxs-lookup"><span data-stu-id="6fa45-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="6fa45-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6fa45-109">EXAMPLES</span></span>

### <span data-ttu-id="6fa45-110">---Przykład 1: Tworzenie przechwytywania pakietów z wieloma filtrami---</span><span class="sxs-lookup"><span data-stu-id="6fa45-110">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="6fa45-111">W tym przykładzie tworzymy przechwycony pakiet o nazwie "PacketCaptureTest" z wieloma filtrami i limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="6fa45-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="6fa45-112">Po zakończeniu sesji zostanie ona zapisana na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="6fa45-112">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="6fa45-113">Uwaga: aby można było tworzyć przechwycenia pakietów, rozszerzenie obserwatora sieci Azure musi być zainstalowane na docelowej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6fa45-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="6fa45-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6fa45-114">PARAMETERS</span></span>

### <span data-ttu-id="6fa45-115">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="6fa45-115">-LocalIPAddress</span></span>
<span data-ttu-id="6fa45-116">Określa lokalny adres IP, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="6fa45-116">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="6fa45-117">Przykładowe dane wejściowe: "127.0.0.1" dla pojedynczego wpisu adresu.</span><span class="sxs-lookup"><span data-stu-id="6fa45-117">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="6fa45-118">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="6fa45-118">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="6fa45-119">"127.0.0.1; 127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="6fa45-119">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa45-120">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="6fa45-120">-LocalPort</span></span>
<span data-ttu-id="6fa45-121">Określa lokalny adres IP, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="6fa45-121">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="6fa45-122">Przykładowe dane wejściowe: "127.0.0.1" dla pojedynczego wpisu adresu.</span><span class="sxs-lookup"><span data-stu-id="6fa45-122">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="6fa45-123">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="6fa45-123">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="6fa45-124">"127.0.0.1; 127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="6fa45-124">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa45-125">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="6fa45-125">-Protocol</span></span>
<span data-ttu-id="6fa45-126">Określa procotol, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="6fa45-126">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="6fa45-127">Dopuszczalne wartości "TCP", "UDP", "any"</span><span class="sxs-lookup"><span data-stu-id="6fa45-127">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa45-128">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="6fa45-128">-RemoteIPAddress</span></span>
<span data-ttu-id="6fa45-129">Określa zdalny adres IP, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="6fa45-129">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="6fa45-130">Przykładowe dane wejściowe: "127.0.0.1" dla pojedynczego wpisu adresu.</span><span class="sxs-lookup"><span data-stu-id="6fa45-130">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="6fa45-131">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="6fa45-131">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="6fa45-132">"127.0.0.1; 127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="6fa45-132">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa45-133">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="6fa45-133">-RemotePort</span></span>
<span data-ttu-id="6fa45-134">Określa port zdalny, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="6fa45-134">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="6fa45-135">Przykładowe dane wejściowe portu zdalnego: "80" dla wpisu Single Port.</span><span class="sxs-lookup"><span data-stu-id="6fa45-135">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="6fa45-136">"80-85" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="6fa45-136">"80-85" for range.</span></span>
<span data-ttu-id="6fa45-137">"80; 443;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="6fa45-137">"80;443;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa45-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fa45-138">-DefaultProfile</span></span>
<span data-ttu-id="6fa45-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fa45-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fa45-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fa45-140">CommonParameters</span></span>
<span data-ttu-id="6fa45-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fa45-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fa45-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fa45-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fa45-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fa45-143">INPUTS</span></span>

### <span data-ttu-id="6fa45-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6fa45-144">System.String</span></span>

## <span data-ttu-id="6fa45-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6fa45-145">OUTPUTS</span></span>

### <span data-ttu-id="6fa45-146">Microsoft. Azure. Commands. Network. models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="6fa45-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="6fa45-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6fa45-147">NOTES</span></span>
<span data-ttu-id="6fa45-148">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor, pakiet, przechwytywanie, ruch, filtr</span><span class="sxs-lookup"><span data-stu-id="6fa45-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="6fa45-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fa45-149">RELATED LINKS</span></span>

[<span data-ttu-id="6fa45-150">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6fa45-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6fa45-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6fa45-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6fa45-152">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6fa45-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6fa45-153">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6fa45-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6fa45-154">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6fa45-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6fa45-155">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6fa45-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6fa45-156">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6fa45-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6fa45-157">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6fa45-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="6fa45-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6fa45-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="6fa45-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6fa45-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6fa45-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6fa45-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="6fa45-161">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6fa45-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
