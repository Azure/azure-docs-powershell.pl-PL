---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: c2da2b9173b3977a606699fd8e1def3dae2a68d9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335626"
---
# <span data-ttu-id="820f5-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="820f5-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="820f5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="820f5-102">SYNOPSIS</span></span>
<span data-ttu-id="820f5-103">Zwraca monitor połączenia z określoną nazwą lub z listą monitorów połączeń.</span><span class="sxs-lookup"><span data-stu-id="820f5-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="820f5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="820f5-104">SYNTAX</span></span>

### <span data-ttu-id="820f5-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="820f5-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="820f5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="820f5-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="820f5-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="820f5-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="820f5-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="820f5-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="820f5-109">Opis</span><span class="sxs-lookup"><span data-stu-id="820f5-109">DESCRIPTION</span></span>
<span data-ttu-id="820f5-110">Polecenie cmdlet Get-AzNetworkWatcherConnectionMonitor zwraca monitor połączenia z określoną nazwą/identyfikatorem zasobu lub listą monitorów połączeń odpowiadającą określonemu obserwatorowi/lokalizacji sieci.</span><span class="sxs-lookup"><span data-stu-id="820f5-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="820f5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="820f5-111">EXAMPLES</span></span>

### <span data-ttu-id="820f5-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="820f5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="820f5-113">Nazwa: Identyfikator cm:/subscriptions/00000000-0000-0000-0000-000000000000/resourceGro/NetworkWatcherRG/Providers/Microsoft. Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm ETag: W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState: Źródło powiodło się: {"ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/Providers/Microsoft. C ompute/virtualMachines/irinavm", "Port": 0} miejsce docelowe: {"adres": "google.com", "Port": 80} MonitoringIntervalInSeconds: 60 Autostart: prawda rozpoczęcia: 1/12/2018 7:19:28 PM MonitoringStatus: Lokalizacja zatrzymana: centraluseuap Type: Microsoft. Network/networkWatchers/connectionMonitors znaczniki: {"KEY1": "wartość1"}</span><span class="sxs-lookup"><span data-stu-id="820f5-113">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination                 : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:19:28 PM MonitoringStatus            : Stopped Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : { "key1": "value1" }</span></span>

## <span data-ttu-id="820f5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="820f5-114">PARAMETERS</span></span>

### <span data-ttu-id="820f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="820f5-115">-DefaultProfile</span></span>
<span data-ttu-id="820f5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="820f5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="820f5-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="820f5-117">-Location</span></span>
<span data-ttu-id="820f5-118">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="820f5-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="820f5-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="820f5-119">-Name</span></span>
<span data-ttu-id="820f5-120">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="820f5-120">The connection monitor name.</span></span>

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

### <span data-ttu-id="820f5-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="820f5-121">-NetworkWatcher</span></span>
<span data-ttu-id="820f5-122">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="820f5-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="820f5-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="820f5-123">-NetworkWatcherName</span></span>
<span data-ttu-id="820f5-124">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="820f5-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="820f5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="820f5-125">-ResourceGroupName</span></span>
<span data-ttu-id="820f5-126">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="820f5-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="820f5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="820f5-127">-ResourceId</span></span>
<span data-ttu-id="820f5-128">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="820f5-128">Resource ID.</span></span>

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

### <span data-ttu-id="820f5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="820f5-129">CommonParameters</span></span>
<span data-ttu-id="820f5-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="820f5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="820f5-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="820f5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="820f5-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="820f5-132">INPUTS</span></span>

### <span data-ttu-id="820f5-133">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="820f5-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="820f5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="820f5-134">System.String</span></span>

## <span data-ttu-id="820f5-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="820f5-135">OUTPUTS</span></span>

### <span data-ttu-id="820f5-136">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="820f5-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="820f5-137">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="820f5-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="820f5-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="820f5-138">NOTES</span></span>

## <span data-ttu-id="820f5-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="820f5-139">RELATED LINKS</span></span>
