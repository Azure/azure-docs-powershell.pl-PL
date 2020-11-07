---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 014942f38abf0caae01463d07343b5ad473a24d7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897937"
---
# <span data-ttu-id="47e31-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47e31-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="47e31-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47e31-102">SYNOPSIS</span></span>
<span data-ttu-id="47e31-103">Zwraca monitor połączenia z określoną nazwą lub z listą monitorów połączeń.</span><span class="sxs-lookup"><span data-stu-id="47e31-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47e31-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47e31-104">SYNTAX</span></span>

### <span data-ttu-id="47e31-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="47e31-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="47e31-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="47e31-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="47e31-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="47e31-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="47e31-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="47e31-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="47e31-109">Opis</span><span class="sxs-lookup"><span data-stu-id="47e31-109">DESCRIPTION</span></span>
<span data-ttu-id="47e31-110">Polecenie cmdlet Get-AzureRmNetworkWatcherConnectionMonitor zwraca monitor połączenia z określoną nazwą/identyfikatorem zasobu lub listą monitorów połączeń odpowiadającą określonemu obserwatorowi/lokalizacji sieci.</span><span class="sxs-lookup"><span data-stu-id="47e31-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="47e31-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47e31-111">EXAMPLES</span></span>

### <span data-ttu-id="47e31-112">---------------Przykład 1: Uzyskaj monitor połączenia według nazwy w określonej lokalizacji---------------</span><span class="sxs-lookup"><span data-stu-id="47e31-112">---------------  Example 1: Get connection monitor by name in the specified location ---------------</span></span>
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

<span data-ttu-id="47e31-113">W tym przykładzie monitor połączenia jest wyświetlany według nazwy w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="47e31-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="47e31-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47e31-114">PARAMETERS</span></span>

### <span data-ttu-id="47e31-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47e31-115">-AsJob</span></span>
<span data-ttu-id="47e31-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="47e31-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47e31-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e31-117">-DefaultProfile</span></span>
<span data-ttu-id="47e31-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47e31-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47e31-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="47e31-119">-Location</span></span>
<span data-ttu-id="47e31-120">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="47e31-120">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47e31-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="47e31-121">-Name</span></span>
<span data-ttu-id="47e31-122">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="47e31-122">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47e31-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47e31-123">-NetworkWatcher</span></span>
<span data-ttu-id="47e31-124">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="47e31-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="47e31-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="47e31-125">-NetworkWatcherName</span></span>
<span data-ttu-id="47e31-126">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="47e31-126">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47e31-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47e31-127">-ResourceGroupName</span></span>
<span data-ttu-id="47e31-128">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="47e31-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="47e31-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47e31-129">-ResourceId</span></span>
<span data-ttu-id="47e31-130">Identyfikator zasobu monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="47e31-130">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="47e31-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e31-131">CommonParameters</span></span>
<span data-ttu-id="47e31-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47e31-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e31-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47e31-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e31-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47e31-134">INPUTS</span></span>

### <span data-ttu-id="47e31-135">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47e31-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="47e31-136">System. String</span><span class="sxs-lookup"><span data-stu-id="47e31-136">System.String</span></span>


## <span data-ttu-id="47e31-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47e31-137">OUTPUTS</span></span>

### <span data-ttu-id="47e31-138">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="47e31-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="47e31-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47e31-139">NOTES</span></span>
<span data-ttu-id="47e31-140">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="47e31-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="47e31-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47e31-141">RELATED LINKS</span></span>
<span data-ttu-id="47e31-142">[Nowe — AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="47e31-142">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="47e31-143">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="47e31-143">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="47e31-144">[Nowe — AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Nowe — AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Zatrzymaj — AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="47e31-144">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="47e31-145">[Nowe — AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="47e31-145">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span></span>
