---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7c32c58167336fc032e543261e237430de36653c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547431"
---
# <span data-ttu-id="d7cc8-101">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7cc8-101">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="d7cc8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7cc8-102">SYNOPSIS</span></span>
<span data-ttu-id="d7cc8-103">Uruchamianie monitora połączeń</span><span class="sxs-lookup"><span data-stu-id="d7cc8-103">Start a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7cc8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7cc8-104">SYNTAX</span></span>

### <span data-ttu-id="d7cc8-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d7cc8-105">SetByName (Default)</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7cc8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d7cc8-106">SetByResource</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7cc8-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d7cc8-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7cc8-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d7cc8-108">SetByResourceId</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7cc8-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="d7cc8-109">SetByInputObject</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7cc8-110">Opis</span><span class="sxs-lookup"><span data-stu-id="d7cc8-110">DESCRIPTION</span></span>
<span data-ttu-id="d7cc8-111">Polecenie cmdlet Start-AzureRmNetworkWatcherConnectionMonitor uruchamia określony monitor połączeń.</span><span class="sxs-lookup"><span data-stu-id="d7cc8-111">The Start-AzureRmNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="d7cc8-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7cc8-112">EXAMPLES</span></span>

### <span data-ttu-id="d7cc8-113">Przykład 1. Uruchomienie monitora połączeń</span><span class="sxs-lookup"><span data-stu-id="d7cc8-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="d7cc8-114">W tym przykładzie monitor połączeń określony przez nazwę i Monitor sieci został uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="d7cc8-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="d7cc8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7cc8-115">PARAMETERS</span></span>

### <span data-ttu-id="d7cc8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7cc8-116">-AsJob</span></span>
<span data-ttu-id="d7cc8-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d7cc8-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7cc8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7cc8-118">-DefaultProfile</span></span>
<span data-ttu-id="d7cc8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7cc8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7cc8-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d7cc8-120">-InputObject</span></span>
<span data-ttu-id="d7cc8-121">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="d7cc8-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7cc8-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d7cc8-122">-Location</span></span>
<span data-ttu-id="d7cc8-123">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d7cc8-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d7cc8-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d7cc8-124">-Name</span></span>
<span data-ttu-id="d7cc8-125">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="d7cc8-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7cc8-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7cc8-126">-NetworkWatcher</span></span>
<span data-ttu-id="d7cc8-127">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d7cc8-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="d7cc8-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d7cc8-128">-NetworkWatcherName</span></span>
<span data-ttu-id="d7cc8-129">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d7cc8-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="d7cc8-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7cc8-130">-PassThru</span></span>
<span data-ttu-id="d7cc8-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d7cc8-131">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7cc8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7cc8-132">-ResourceGroupName</span></span>
<span data-ttu-id="d7cc8-133">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d7cc8-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d7cc8-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7cc8-134">-ResourceId</span></span>
<span data-ttu-id="d7cc8-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="d7cc8-135">Resource ID.</span></span>

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

### <span data-ttu-id="d7cc8-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7cc8-136">-Confirm</span></span>
<span data-ttu-id="d7cc8-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7cc8-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7cc8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7cc8-138">-WhatIf</span></span>
<span data-ttu-id="d7cc8-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7cc8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7cc8-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7cc8-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7cc8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7cc8-141">CommonParameters</span></span>
<span data-ttu-id="d7cc8-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7cc8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7cc8-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7cc8-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7cc8-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7cc8-144">INPUTS</span></span>

### <span data-ttu-id="d7cc8-145">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7cc8-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d7cc8-146">Parametry: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d7cc8-146">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="d7cc8-147">System. String</span><span class="sxs-lookup"><span data-stu-id="d7cc8-147">System.String</span></span>

### <span data-ttu-id="d7cc8-148">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="d7cc8-148">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="d7cc8-149">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d7cc8-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d7cc8-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7cc8-150">OUTPUTS</span></span>

### <span data-ttu-id="d7cc8-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7cc8-151">System.Boolean</span></span>

## <span data-ttu-id="d7cc8-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7cc8-152">NOTES</span></span>
<span data-ttu-id="d7cc8-153">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="d7cc8-153">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="d7cc8-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7cc8-154">RELATED LINKS</span></span>

[<span data-ttu-id="d7cc8-155">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7cc8-155">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="d7cc8-156">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7cc8-156">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="d7cc8-157">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7cc8-157">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="d7cc8-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d7cc8-158">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="d7cc8-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d7cc8-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="d7cc8-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d7cc8-160">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="d7cc8-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d7cc8-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="d7cc8-162">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7cc8-162">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="d7cc8-163">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d7cc8-163">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="d7cc8-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7cc8-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="d7cc8-165">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7cc8-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="d7cc8-166">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7cc8-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="d7cc8-167">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7cc8-167">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d7cc8-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d7cc8-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="d7cc8-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7cc8-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d7cc8-170">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7cc8-170">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d7cc8-171">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7cc8-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d7cc8-172">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7cc8-172">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d7cc8-173">Nowe — AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7cc8-173">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="d7cc8-174">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d7cc8-174">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="d7cc8-175">Test — AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d7cc8-175">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="d7cc8-176">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d7cc8-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="d7cc8-177">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7cc8-177">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d7cc8-178">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d7cc8-178">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="d7cc8-179">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d7cc8-179">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="d7cc8-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d7cc8-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="d7cc8-181">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d7cc8-181">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
