---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 3f380135cc6edde875c927dd9d640a10cdf14957
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718297"
---
# <span data-ttu-id="681db-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="681db-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="681db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="681db-102">SYNOPSIS</span></span>
<span data-ttu-id="681db-103">Zwraca monitor połączenia z określoną nazwą lub z listą monitorów połączeń.</span><span class="sxs-lookup"><span data-stu-id="681db-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="681db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="681db-104">SYNTAX</span></span>

### <span data-ttu-id="681db-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="681db-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="681db-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="681db-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="681db-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="681db-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="681db-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="681db-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="681db-109">Opis</span><span class="sxs-lookup"><span data-stu-id="681db-109">DESCRIPTION</span></span>
<span data-ttu-id="681db-110">Polecenie cmdlet Get-AzureRmNetworkWatcherConnectionMonitor zwraca monitor połączenia z określoną nazwą/identyfikatorem zasobu lub listą monitorów połączeń odpowiadającą określonemu obserwatorowi/lokalizacji sieci.</span><span class="sxs-lookup"><span data-stu-id="681db-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="681db-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="681db-111">EXAMPLES</span></span>

### <span data-ttu-id="681db-112">Przykład 1: uzyskiwanie monitora połączeń według nazwy w określonej lokalizacji</span><span class="sxs-lookup"><span data-stu-id="681db-112">Example 1: Get connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="681db-113">W tym przykładzie monitor połączenia jest wyświetlany według nazwy w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="681db-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="681db-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="681db-114">PARAMETERS</span></span>

### <span data-ttu-id="681db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="681db-115">-DefaultProfile</span></span>
<span data-ttu-id="681db-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="681db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="681db-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="681db-117">-Location</span></span>
<span data-ttu-id="681db-118">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="681db-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="681db-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="681db-119">-Name</span></span>
<span data-ttu-id="681db-120">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="681db-120">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="681db-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="681db-121">-NetworkWatcher</span></span>
<span data-ttu-id="681db-122">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="681db-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="681db-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="681db-123">-NetworkWatcherName</span></span>
<span data-ttu-id="681db-124">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="681db-124">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="681db-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="681db-125">-ResourceGroupName</span></span>
<span data-ttu-id="681db-126">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="681db-126">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="681db-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="681db-127">-ResourceId</span></span>
<span data-ttu-id="681db-128">Identyfikator zasobu monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="681db-128">Resource ID of the connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="681db-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="681db-129">CommonParameters</span></span>
<span data-ttu-id="681db-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="681db-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="681db-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="681db-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="681db-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="681db-132">INPUTS</span></span>

### <span data-ttu-id="681db-133">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="681db-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="681db-134">Parametry: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="681db-134">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="681db-135">System. String</span><span class="sxs-lookup"><span data-stu-id="681db-135">System.String</span></span>

## <span data-ttu-id="681db-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="681db-136">OUTPUTS</span></span>

### <span data-ttu-id="681db-137">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="681db-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="681db-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="681db-138">NOTES</span></span>
<span data-ttu-id="681db-139">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="681db-139">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="681db-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="681db-140">RELATED LINKS</span></span>

[<span data-ttu-id="681db-141">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="681db-141">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="681db-142">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="681db-142">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="681db-143">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="681db-143">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="681db-144">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="681db-144">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="681db-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="681db-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="681db-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="681db-146">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="681db-147">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="681db-147">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="681db-148">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="681db-148">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="681db-149">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="681db-149">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="681db-150">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="681db-150">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="681db-151">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="681db-151">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="681db-152">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="681db-152">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="681db-153">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="681db-153">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="681db-154">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="681db-154">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="681db-155">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="681db-155">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="681db-156">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="681db-156">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="681db-157">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="681db-157">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="681db-158">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="681db-158">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="681db-159">Nowe — AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="681db-159">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="681db-160">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="681db-160">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="681db-161">Test — AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="681db-161">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="681db-162">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="681db-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="681db-163">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="681db-163">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="681db-164">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="681db-164">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="681db-165">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="681db-165">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="681db-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="681db-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="681db-167">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="681db-167">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
