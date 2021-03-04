---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 30ab203f50df9e712792e216a1b4ecf1c5378b2e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954433"
---
# <span data-ttu-id="67d89-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="67d89-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="67d89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67d89-102">SYNOPSIS</span></span>
<span data-ttu-id="67d89-103">Zwraca monitor połączenia o określonej nazwie lub listę monitorów połączeń.</span><span class="sxs-lookup"><span data-stu-id="67d89-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="67d89-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="67d89-104">SYNTAX</span></span>

### <span data-ttu-id="67d89-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="67d89-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67d89-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="67d89-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67d89-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="67d89-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67d89-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="67d89-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67d89-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="67d89-109">DESCRIPTION</span></span>
<span data-ttu-id="67d89-110">Polecenie Get-AzNetworkWatcherConnectionMonitor zwraca monitor połączenia o określonej nazwie/adresie zasobu lub na liście monitorów połączeń odpowiadających określonej pozycji/czujce sieci.</span><span class="sxs-lookup"><span data-stu-id="67d89-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="67d89-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="67d89-111">EXAMPLES</span></span>

### <span data-ttu-id="67d89-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="67d89-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="67d89-113">Nazwa: cm Id: /subscriptions/00000000-0000-0000-0000-00000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag: W/"40961b58-e379-4204-a47b-0c47773 9b095" ProvisioningState: Pomyślnie źródłowe: { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/ilinavm", "Port": 0 } Miejsce docelowe: { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds: 60 AutoStart: True StartTime: 2018-01-12 7:19:28 PM MonitoringStatus: Stopped Location : centraluseuap Type : Microsoft.Network/networkWatchers/connectionMonitors Tags : { "key1": "value1" }</span><span class="sxs-lookup"><span data-stu-id="67d89-113">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination                 : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:19:28 PM MonitoringStatus            : Stopped Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : { "key1": "value1" }</span></span>

## <span data-ttu-id="67d89-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67d89-114">PARAMETERS</span></span>

### <span data-ttu-id="67d89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d89-115">-DefaultProfile</span></span>
<span data-ttu-id="67d89-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="67d89-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67d89-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="67d89-117">-Location</span></span>
<span data-ttu-id="67d89-118">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="67d89-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="67d89-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="67d89-119">-Name</span></span>
<span data-ttu-id="67d89-120">Nazwa monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="67d89-120">The connection monitor name.</span></span>

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

### <span data-ttu-id="67d89-121">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="67d89-121">-NetworkWatcher</span></span>
<span data-ttu-id="67d89-122">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="67d89-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="67d89-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="67d89-123">-NetworkWatcherName</span></span>
<span data-ttu-id="67d89-124">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="67d89-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="67d89-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67d89-125">-ResourceGroupName</span></span>
<span data-ttu-id="67d89-126">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="67d89-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="67d89-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67d89-127">-ResourceId</span></span>
<span data-ttu-id="67d89-128">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="67d89-128">Resource ID.</span></span>

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

### <span data-ttu-id="67d89-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d89-129">CommonParameters</span></span>
<span data-ttu-id="67d89-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67d89-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d89-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67d89-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d89-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67d89-132">INPUTS</span></span>

### <span data-ttu-id="67d89-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="67d89-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="67d89-134">System.String</span><span class="sxs-lookup"><span data-stu-id="67d89-134">System.String</span></span>

## <span data-ttu-id="67d89-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67d89-135">OUTPUTS</span></span>

### <span data-ttu-id="67d89-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="67d89-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="67d89-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="67d89-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="67d89-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="67d89-138">NOTES</span></span>

## <span data-ttu-id="67d89-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67d89-139">RELATED LINKS</span></span>
