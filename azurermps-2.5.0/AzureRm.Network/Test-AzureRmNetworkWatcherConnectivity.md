---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcherconnectivity
schema: 2.0.0
ms.openlocfilehash: 55dc2682c4c3e62b42a6a23ac12f93991e4873fc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897818"
---
# <span data-ttu-id="f8f91-101">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f8f91-101">Test-AzureRmNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="f8f91-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8f91-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f91-103">Zwraca informacje o łączności dla określonego źródłowej maszyny wirtualnej i miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="f8f91-103">Returns connectivity information for a specified source VM and a destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8f91-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8f91-104">SYNTAX</span></span>

### <span data-ttu-id="f8f91-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f8f91-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8f91-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f8f91-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8f91-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f8f91-107">DESCRIPTION</span></span>
<span data-ttu-id="f8f91-108">Polecenie cmdlet Test-AzureRmNetworkWatcherConnectivity zwraca informacje o łączności dla określonego źródłowej maszyny wirtualnej i miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="f8f91-108">The Test-AzureRmNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="f8f91-109">Jeśli nie można ustanowić łączności między źródłem a miejscem docelowym, polecenie cmdlet zwróci szczegółowe informacje o tym problemie.</span><span class="sxs-lookup"><span data-stu-id="f8f91-109">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="f8f91-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8f91-110">EXAMPLES</span></span>

### <span data-ttu-id="f8f91-111">---------------Przykład 1: Testowanie łączności obserwatora sieci z maszyny wirtualnej w witrynie sieci Web---------------</span><span class="sxs-lookup"><span data-stu-id="f8f91-111">---------------  Example 1: Test Network Watcher Connectivity from a VM to a website  ---------------</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


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

<span data-ttu-id="f8f91-112">W tym przykładzie testujemy łączność z maszyny wirtualnej na platformie Azure z www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="f8f91-112">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="f8f91-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8f91-113">PARAMETERS</span></span>

### <span data-ttu-id="f8f91-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8f91-114">-AsJob</span></span>
<span data-ttu-id="f8f91-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f8f91-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8f91-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8f91-116">-DefaultProfile</span></span>
<span data-ttu-id="f8f91-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8f91-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8f91-118">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="f8f91-118">-DestinationAddress</span></span>
<span data-ttu-id="f8f91-119">Adres IP lub identyfikator URI zasobu, do którego będzie podejmowana próba nawiązania połączenia.</span><span class="sxs-lookup"><span data-stu-id="f8f91-119">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="f8f91-120">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="f8f91-120">-DestinationId</span></span>
<span data-ttu-id="f8f91-121">Identyfikator zasobu, z którym zostanie podjęta próba nawiązania połączenia.</span><span class="sxs-lookup"><span data-stu-id="f8f91-121">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="f8f91-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="f8f91-122">-DestinationPort</span></span>
<span data-ttu-id="f8f91-123">Port, na którym zostanie przeprowadzone połączenie kontrolne.</span><span class="sxs-lookup"><span data-stu-id="f8f91-123">Port on which check connectivity will be performed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f91-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8f91-124">-NetworkWatcher</span></span>
<span data-ttu-id="f8f91-125">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="f8f91-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="f8f91-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f8f91-126">-NetworkWatcherName</span></span>
<span data-ttu-id="f8f91-127">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="f8f91-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8f91-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8f91-128">-ResourceGroupName</span></span>
<span data-ttu-id="f8f91-129">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="f8f91-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f8f91-130">-SourceId</span><span class="sxs-lookup"><span data-stu-id="f8f91-130">-SourceId</span></span>
<span data-ttu-id="f8f91-131">Identyfikator zasobu, z którego zostanie zainicjowany test łączności.</span><span class="sxs-lookup"><span data-stu-id="f8f91-131">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="f8f91-132">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="f8f91-132">-SourcePort</span></span>
<span data-ttu-id="f8f91-133">Port źródłowy, z którego zostanie przeprowadzone sprawdzenie łączności.</span><span class="sxs-lookup"><span data-stu-id="f8f91-133">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8f91-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f91-134">CommonParameters</span></span>
<span data-ttu-id="f8f91-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8f91-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f91-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8f91-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f91-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8f91-137">INPUTS</span></span>

### <span data-ttu-id="f8f91-138">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8f91-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f8f91-139">System. String system. Int32</span><span class="sxs-lookup"><span data-stu-id="f8f91-139">System.String System.Int32</span></span>

## <span data-ttu-id="f8f91-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8f91-140">OUTPUTS</span></span>

### <span data-ttu-id="f8f91-141">Microsoft. Azure. Commands. Network. models. PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="f8f91-141">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="f8f91-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8f91-142">NOTES</span></span>
<span data-ttu-id="f8f91-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, łączność, zarządzanie, Menedżer, Sieć, Sieć, Monitor sieci</span><span class="sxs-lookup"><span data-stu-id="f8f91-143">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="f8f91-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8f91-144">RELATED LINKS</span></span>

<span data-ttu-id="f8f91-145">[Nowe — AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="f8f91-145">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="f8f91-146">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="f8f91-146">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="f8f91-147">[Nowe — AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Nowe — AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Zatrzymaj — AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="f8f91-147">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>
