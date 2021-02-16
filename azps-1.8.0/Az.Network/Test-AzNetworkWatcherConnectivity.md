---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: 6b689a96a4f737b2f92b4146f71faff7a09d8d36
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402715"
---
# <span data-ttu-id="10352-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="10352-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="10352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10352-102">SYNOPSIS</span></span>
<span data-ttu-id="10352-103">Zwraca informacje o łączności dla określonej źródłowej maszyny wirtualnej i miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="10352-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="10352-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10352-104">SYNTAX</span></span>

### <span data-ttu-id="10352-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="10352-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10352-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="10352-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10352-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="10352-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10352-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="10352-108">DESCRIPTION</span></span>
<span data-ttu-id="10352-109">Polecenie Test-AzNetworkWatcherConnectivity zwraca informacje o łączności dla określonej źródłowej maszyny wirtualnej i miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="10352-109">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="10352-110">Jeśli nie można ustalić łączności między źródłem a miejscem docelowym, polecenie cmdlet zwraca szczegółowe informacje o problemie.</span><span class="sxs-lookup"><span data-stu-id="10352-110">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="10352-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10352-111">EXAMPLES</span></span>

### <span data-ttu-id="10352-112">Przykład 1. Testowanie łączności usługi Network Watcher z maszyny wirtualnej z witryną sieci Web</span><span class="sxs-lookup"><span data-stu-id="10352-112">Example 1: Test Network Watcher Connectivity from a VM to a website</span></span>
```
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

<span data-ttu-id="10352-113">W tym przykładzie testujemy łączność z maszyny wirtualnej na platformie Azure z www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="10352-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="10352-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10352-114">PARAMETERS</span></span>

### <span data-ttu-id="10352-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="10352-115">-AsJob</span></span>
<span data-ttu-id="10352-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="10352-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10352-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10352-117">-DefaultProfile</span></span>
<span data-ttu-id="10352-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="10352-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10352-119">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="10352-119">-DestinationAddress</span></span>
<span data-ttu-id="10352-120">Adres IP lub URI zasobu, z którym zostanie nawiązana próba połączenia.</span><span class="sxs-lookup"><span data-stu-id="10352-120">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="10352-121">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="10352-121">-DestinationId</span></span>
<span data-ttu-id="10352-122">Identyfikator zasobu, z którym zostanie nawiązaniu połączenia.</span><span class="sxs-lookup"><span data-stu-id="10352-122">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="10352-123">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="10352-123">-DestinationPort</span></span>
<span data-ttu-id="10352-124">Port, na którym zostanie wykonana łączność podczas sprawdzania.</span><span class="sxs-lookup"><span data-stu-id="10352-124">Port on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="10352-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="10352-125">-Location</span></span>
<span data-ttu-id="10352-126">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="10352-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="10352-127">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="10352-127">-NetworkWatcher</span></span>
<span data-ttu-id="10352-128">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="10352-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="10352-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="10352-129">-NetworkWatcherName</span></span>
<span data-ttu-id="10352-130">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="10352-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="10352-131">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="10352-131">-ProtocolConfiguration</span></span>
<span data-ttu-id="10352-132">Konfiguracja protokółowa, w przypadku której zostanie wykonana łączność kontrolna.</span><span class="sxs-lookup"><span data-stu-id="10352-132">Protocal configuration on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="10352-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10352-133">-ResourceGroupName</span></span>
<span data-ttu-id="10352-134">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="10352-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="10352-135">-SourceId</span><span class="sxs-lookup"><span data-stu-id="10352-135">-SourceId</span></span>
<span data-ttu-id="10352-136">Identyfikator zasobu, z którego zostanie zainicjowane sprawdzanie łączności.</span><span class="sxs-lookup"><span data-stu-id="10352-136">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="10352-137">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="10352-137">-SourcePort</span></span>
<span data-ttu-id="10352-138">Port źródłowy, z którego zostanie wykonane sprawdzanie łączności.</span><span class="sxs-lookup"><span data-stu-id="10352-138">The source port from which a connectivity check will be performed.</span></span>

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

### <span data-ttu-id="10352-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10352-139">CommonParameters</span></span>
<span data-ttu-id="10352-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10352-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10352-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10352-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10352-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10352-142">INPUTS</span></span>

### <span data-ttu-id="10352-143">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="10352-143">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="10352-144">System.String</span><span class="sxs-lookup"><span data-stu-id="10352-144">System.String</span></span>

### <span data-ttu-id="10352-145">System.Int32</span><span class="sxs-lookup"><span data-stu-id="10352-145">System.Int32</span></span>

## <span data-ttu-id="10352-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10352-146">OUTPUTS</span></span>

### <span data-ttu-id="10352-147">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="10352-147">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="10352-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10352-148">NOTES</span></span>
<span data-ttu-id="10352-149">Słowa kluczowe: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span><span class="sxs-lookup"><span data-stu-id="10352-149">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="10352-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10352-150">RELATED LINKS</span></span>

<span data-ttu-id="10352-151">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="10352-151">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="10352-152">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="10352-152">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="10352-153">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="10352-153">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>


<span data-ttu-id="10352-154">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md) 
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
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="10352-154">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)
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
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)</span></span>
