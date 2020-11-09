---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: 8d3a714f2798c4866df39cd63c664228f078c37c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318517"
---
# <span data-ttu-id="d2380-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d2380-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="d2380-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2380-102">SYNOPSIS</span></span>
<span data-ttu-id="d2380-103">Zwraca informacje o łączności dla określonego źródłowej maszyny wirtualnej i miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="d2380-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="d2380-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2380-104">SYNTAX</span></span>

### <span data-ttu-id="d2380-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d2380-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2380-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d2380-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2380-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d2380-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2380-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d2380-108">DESCRIPTION</span></span>
<span data-ttu-id="d2380-109">Polecenie cmdlet Test-AzNetworkWatcherConnectivity zwraca informacje o łączności dla określonego źródłowej maszyny wirtualnej i miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="d2380-109">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="d2380-110">Jeśli nie można ustanowić łączności między źródłem a miejscem docelowym, polecenie cmdlet zwróci szczegółowe informacje o tym problemie.</span><span class="sxs-lookup"><span data-stu-id="d2380-110">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="d2380-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2380-111">EXAMPLES</span></span>

### <span data-ttu-id="d2380-112">Przykład 1: Testowanie łączności obserwatora sieci z maszyny wirtualnej w witrynie sieci Web</span><span class="sxs-lookup"><span data-stu-id="d2380-112">Example 1: Test Network Watcher Connectivity from a VM to a website</span></span>
```powershell
Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="d2380-113">W tym przykładzie testujemy łączność z maszyny wirtualnej na platformie Azure z www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="d2380-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

### <span data-ttu-id="d2380-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d2380-114">Example 2</span></span>

<span data-ttu-id="d2380-115">Zwraca informacje o łączności dla określonego źródłowej maszyny wirtualnej i miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="d2380-115">Returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="d2380-116">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="d2380-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Test-AzNetworkWatcherConnectivity -DestinationAddress 'bing.com' -DestinationPort 80 -NetworkWatcher <PSNetworkWatcher> -SourceId '/subscriptions/00000000-0000-0000-0000-00000000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0'
```

## <span data-ttu-id="d2380-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2380-117">PARAMETERS</span></span>

### <span data-ttu-id="d2380-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2380-118">-AsJob</span></span>
<span data-ttu-id="d2380-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d2380-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2380-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2380-120">-DefaultProfile</span></span>
<span data-ttu-id="d2380-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2380-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2380-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="d2380-122">-DestinationAddress</span></span>
<span data-ttu-id="d2380-123">Adres IP lub identyfikator URI zasobu, do którego będzie podejmowana próba nawiązania połączenia.</span><span class="sxs-lookup"><span data-stu-id="d2380-123">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="d2380-124">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="d2380-124">-DestinationId</span></span>
<span data-ttu-id="d2380-125">Identyfikator zasobu, z którym zostanie podjęta próba nawiązania połączenia.</span><span class="sxs-lookup"><span data-stu-id="d2380-125">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="d2380-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="d2380-126">-DestinationPort</span></span>
<span data-ttu-id="d2380-127">Port, na którym zostanie przeprowadzone połączenie kontrolne.</span><span class="sxs-lookup"><span data-stu-id="d2380-127">Port on which check connectivity will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2380-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d2380-128">-Location</span></span>
<span data-ttu-id="d2380-129">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d2380-129">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2380-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d2380-130">-NetworkWatcher</span></span>
<span data-ttu-id="d2380-131">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d2380-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="d2380-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d2380-132">-NetworkWatcherName</span></span>
<span data-ttu-id="d2380-133">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d2380-133">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2380-134">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2380-134">-ProtocolConfiguration</span></span>
<span data-ttu-id="d2380-135">Konfiguracja protokołu, na którym ma być przeprowadzana łączność za pośrednictwem sprawdzania.</span><span class="sxs-lookup"><span data-stu-id="d2380-135">Protocol configuration on which check connectivity will be performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2380-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2380-136">-ResourceGroupName</span></span>
<span data-ttu-id="d2380-137">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d2380-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d2380-138">-SourceId</span><span class="sxs-lookup"><span data-stu-id="d2380-138">-SourceId</span></span>
<span data-ttu-id="d2380-139">Identyfikator zasobu, z którego zostanie zainicjowany test łączności.</span><span class="sxs-lookup"><span data-stu-id="d2380-139">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="d2380-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="d2380-140">-SourcePort</span></span>
<span data-ttu-id="d2380-141">Port źródłowy, z którego zostanie przeprowadzone sprawdzenie łączności.</span><span class="sxs-lookup"><span data-stu-id="d2380-141">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2380-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2380-142">CommonParameters</span></span>
<span data-ttu-id="d2380-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2380-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2380-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2380-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2380-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2380-145">INPUTS</span></span>

### <span data-ttu-id="d2380-146">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d2380-146">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d2380-147">System. String</span><span class="sxs-lookup"><span data-stu-id="d2380-147">System.String</span></span>

### <span data-ttu-id="d2380-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d2380-148">System.Int32</span></span>

## <span data-ttu-id="d2380-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2380-149">OUTPUTS</span></span>

### <span data-ttu-id="d2380-150">Microsoft. Azure. Commands. Network. models. PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="d2380-150">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="d2380-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2380-151">NOTES</span></span>
<span data-ttu-id="d2380-152">Słowa kluczowe: Azure, azurerm, ARM, Resource, łączność, zarządzanie, Menedżer, Sieć, Sieć, Monitor sieci</span><span class="sxs-lookup"><span data-stu-id="d2380-152">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="d2380-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2380-153">RELATED LINKS</span></span>

<span data-ttu-id="d2380-154">[Nowe — AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="d2380-154">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="d2380-155">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="d2380-155">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="d2380-156">[Nowe — AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Nowe — AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Zatrzymaj — AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="d2380-156">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>


<span data-ttu-id="d2380-157">[Start — AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md) 
 [Nowe — AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md) 
 [Test — AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md) 
 [Test — AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md) 
 [Zatrzymaj — AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md) 
 [Start — AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Nowe — AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md) 
 [Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md) 
 [Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span><span class="sxs-lookup"><span data-stu-id="d2380-157">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)
[New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md)
[Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md)
[Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md)
[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md)
[Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md)
[Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span></span>
