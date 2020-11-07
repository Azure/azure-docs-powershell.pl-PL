---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 01e8a41c8d8854527037c447545f3d0601d4daf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718802"
---
# <span data-ttu-id="c29dc-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c29dc-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="c29dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c29dc-102">SYNOPSIS</span></span>
<span data-ttu-id="c29dc-103">Usuwanie monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="c29dc-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c29dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c29dc-104">SYNTAX</span></span>

### <span data-ttu-id="c29dc-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c29dc-105">SetByName (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c29dc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c29dc-106">SetByResource</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c29dc-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c29dc-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c29dc-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c29dc-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c29dc-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="c29dc-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c29dc-110">Opis</span><span class="sxs-lookup"><span data-stu-id="c29dc-110">DESCRIPTION</span></span>
<span data-ttu-id="c29dc-111">Polecenie cmdlet Remove-AzureRmNetworkWatcherConnectionMonitor umożliwia usunięcie określonego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="c29dc-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="c29dc-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c29dc-112">EXAMPLES</span></span>

### <span data-ttu-id="c29dc-113">Przykład 1: usuwanie określonego monitora połączeń</span><span class="sxs-lookup"><span data-stu-id="c29dc-113">Example 1: Remove the specified connection monitor</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="c29dc-114">W tym przykładzie został usunięty monitor połączenia określony przez lokalizację i nazwę.</span><span class="sxs-lookup"><span data-stu-id="c29dc-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="c29dc-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c29dc-115">PARAMETERS</span></span>

### <span data-ttu-id="c29dc-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c29dc-116">-AsJob</span></span>
<span data-ttu-id="c29dc-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c29dc-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c29dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c29dc-118">-DefaultProfile</span></span>
<span data-ttu-id="c29dc-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c29dc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c29dc-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c29dc-120">-InputObject</span></span>
<span data-ttu-id="c29dc-121">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="c29dc-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="c29dc-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c29dc-122">-Location</span></span>
<span data-ttu-id="c29dc-123">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="c29dc-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c29dc-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c29dc-124">-Name</span></span>
<span data-ttu-id="c29dc-125">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="c29dc-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="c29dc-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c29dc-126">-NetworkWatcher</span></span>
<span data-ttu-id="c29dc-127">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="c29dc-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="c29dc-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c29dc-128">-NetworkWatcherName</span></span>
<span data-ttu-id="c29dc-129">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="c29dc-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="c29dc-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c29dc-130">-PassThru</span></span>
<span data-ttu-id="c29dc-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c29dc-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c29dc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c29dc-132">-ResourceGroupName</span></span>
<span data-ttu-id="c29dc-133">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="c29dc-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c29dc-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c29dc-134">-ResourceId</span></span>
<span data-ttu-id="c29dc-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="c29dc-135">Resource ID.</span></span>

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

### <span data-ttu-id="c29dc-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c29dc-136">-Confirm</span></span>
<span data-ttu-id="c29dc-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c29dc-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c29dc-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c29dc-138">-WhatIf</span></span>
<span data-ttu-id="c29dc-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c29dc-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c29dc-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c29dc-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c29dc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c29dc-141">CommonParameters</span></span>
<span data-ttu-id="c29dc-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c29dc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c29dc-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c29dc-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c29dc-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c29dc-144">INPUTS</span></span>

### <span data-ttu-id="c29dc-145">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c29dc-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c29dc-146">Parametry: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c29dc-146">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="c29dc-147">System. String</span><span class="sxs-lookup"><span data-stu-id="c29dc-147">System.String</span></span>

### <span data-ttu-id="c29dc-148">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="c29dc-148">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="c29dc-149">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c29dc-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c29dc-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c29dc-150">OUTPUTS</span></span>

### <span data-ttu-id="c29dc-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c29dc-151">System.Boolean</span></span>

## <span data-ttu-id="c29dc-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c29dc-152">NOTES</span></span>
<span data-ttu-id="c29dc-153">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="c29dc-153">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="c29dc-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c29dc-154">RELATED LINKS</span></span>

[<span data-ttu-id="c29dc-155">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c29dc-155">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="c29dc-156">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c29dc-156">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="c29dc-157">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c29dc-157">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="c29dc-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c29dc-158">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="c29dc-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c29dc-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="c29dc-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c29dc-160">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="c29dc-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c29dc-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="c29dc-162">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c29dc-162">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="c29dc-163">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c29dc-163">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="c29dc-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c29dc-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="c29dc-165">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c29dc-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="c29dc-166">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c29dc-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="c29dc-167">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c29dc-167">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="c29dc-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c29dc-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="c29dc-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c29dc-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="c29dc-170">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c29dc-170">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="c29dc-171">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c29dc-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="c29dc-172">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c29dc-172">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="c29dc-173">Nowe — AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c29dc-173">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="c29dc-174">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c29dc-174">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="c29dc-175">Test — AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c29dc-175">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="c29dc-176">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c29dc-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="c29dc-177">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c29dc-177">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="c29dc-178">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c29dc-178">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="c29dc-179">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c29dc-179">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="c29dc-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c29dc-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="c29dc-181">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c29dc-181">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
