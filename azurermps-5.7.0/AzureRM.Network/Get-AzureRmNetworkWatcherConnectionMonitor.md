---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: a78114bbf47113983453a0dd5c1e13db0fc73a6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528086"
---
# <span data-ttu-id="7d325-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d325-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="7d325-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d325-102">SYNOPSIS</span></span>
<span data-ttu-id="7d325-103">Zwraca monitor połączenia z określoną nazwą lub z listą monitorów połączeń.</span><span class="sxs-lookup"><span data-stu-id="7d325-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d325-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d325-104">SYNTAX</span></span>

### <span data-ttu-id="7d325-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7d325-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d325-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7d325-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d325-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7d325-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d325-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7d325-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d325-109">Opis</span><span class="sxs-lookup"><span data-stu-id="7d325-109">DESCRIPTION</span></span>
<span data-ttu-id="7d325-110">Polecenie cmdlet Get-AzureRmNetworkWatcherConnectionMonitor zwraca monitor połączenia z określoną nazwą/identyfikatorem zasobu lub listą monitorów połączeń odpowiadającą określonemu obserwatorowi/lokalizacji sieci.</span><span class="sxs-lookup"><span data-stu-id="7d325-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="7d325-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d325-111">EXAMPLES</span></span>

### <span data-ttu-id="7d325-112">Przykład 1: uzyskiwanie monitora połączeń według nazwy w określonej lokalizacji</span><span class="sxs-lookup"><span data-stu-id="7d325-112">Example 1: Get connection monitor by name in the specified location</span></span>
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

<span data-ttu-id="7d325-113">W tym przykładzie monitor połączenia jest wyświetlany według nazwy w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="7d325-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="7d325-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d325-114">PARAMETERS</span></span>

### <span data-ttu-id="7d325-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d325-115">-DefaultProfile</span></span>
<span data-ttu-id="7d325-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d325-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d325-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7d325-117">-Location</span></span>
<span data-ttu-id="7d325-118">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="7d325-118">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d325-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7d325-119">-Name</span></span>
<span data-ttu-id="7d325-120">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="7d325-120">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d325-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d325-121">-NetworkWatcher</span></span>
<span data-ttu-id="7d325-122">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="7d325-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="7d325-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7d325-123">-NetworkWatcherName</span></span>
<span data-ttu-id="7d325-124">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="7d325-124">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d325-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d325-125">-ResourceGroupName</span></span>
<span data-ttu-id="7d325-126">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="7d325-126">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d325-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d325-127">-ResourceId</span></span>
<span data-ttu-id="7d325-128">Identyfikator zasobu monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="7d325-128">Resource ID of the connection monitor.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d325-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d325-129">CommonParameters</span></span>
<span data-ttu-id="7d325-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d325-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7d325-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d325-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d325-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d325-132">INPUTS</span></span>

### <span data-ttu-id="7d325-133">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d325-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7d325-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7d325-134">System.String</span></span>

## <span data-ttu-id="7d325-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d325-135">OUTPUTS</span></span>

### <span data-ttu-id="7d325-136">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="7d325-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="7d325-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d325-137">NOTES</span></span>
<span data-ttu-id="7d325-138">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="7d325-138">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="7d325-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d325-139">RELATED LINKS</span></span>

[<span data-ttu-id="7d325-140">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d325-140">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="7d325-141">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d325-141">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="7d325-142">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d325-142">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="7d325-143">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7d325-143">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="7d325-144">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7d325-144">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="7d325-145">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7d325-145">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="7d325-146">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7d325-146">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="7d325-147">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7d325-147">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="7d325-148">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7d325-148">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="7d325-149">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7d325-149">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="7d325-150">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7d325-150">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="7d325-151">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7d325-151">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="7d325-152">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d325-152">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="7d325-153">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7d325-153">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="7d325-154">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d325-154">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="7d325-155">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d325-155">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="7d325-156">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d325-156">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="7d325-157">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d325-157">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
