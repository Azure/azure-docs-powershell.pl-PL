---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: cf67e27a8f502a753cded74f0cb5bf48ceb2d4ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716836"
---
# <span data-ttu-id="cceb6-101">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cceb6-101">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="cceb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cceb6-102">SYNOPSIS</span></span>
<span data-ttu-id="cceb6-103">Uruchamianie monitora połączeń</span><span class="sxs-lookup"><span data-stu-id="cceb6-103">Start a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cceb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cceb6-104">SYNTAX</span></span>

### <span data-ttu-id="cceb6-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cceb6-105">SetByName (Default)</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cceb6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cceb6-106">SetByResource</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cceb6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="cceb6-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cceb6-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cceb6-108">SetByResourceId</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cceb6-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="cceb6-109">SetByInputObject</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cceb6-110">Opis</span><span class="sxs-lookup"><span data-stu-id="cceb6-110">DESCRIPTION</span></span>
<span data-ttu-id="cceb6-111">Polecenie cmdlet Start-AzureRmNetworkWatcherConnectionMonitor uruchamia określony monitor połączeń.</span><span class="sxs-lookup"><span data-stu-id="cceb6-111">The Start-AzureRmNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="cceb6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cceb6-112">EXAMPLES</span></span>

### <span data-ttu-id="cceb6-113">Przykład 1. Uruchomienie monitora połączeń</span><span class="sxs-lookup"><span data-stu-id="cceb6-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="cceb6-114">W tym przykładzie monitor połączeń określony przez nazwę i Monitor sieci został uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="cceb6-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="cceb6-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cceb6-115">PARAMETERS</span></span>

### <span data-ttu-id="cceb6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cceb6-116">-AsJob</span></span>
<span data-ttu-id="cceb6-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cceb6-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cceb6-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cceb6-118">-Confirm</span></span>
<span data-ttu-id="cceb6-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cceb6-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cceb6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cceb6-120">-DefaultProfile</span></span>
<span data-ttu-id="cceb6-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cceb6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cceb6-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cceb6-122">-InputObject</span></span>
<span data-ttu-id="cceb6-123">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="cceb6-123">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cceb6-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cceb6-124">-Location</span></span>
<span data-ttu-id="cceb6-125">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="cceb6-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="cceb6-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cceb6-126">-Name</span></span>
<span data-ttu-id="cceb6-127">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="cceb6-127">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cceb6-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cceb6-128">-NetworkWatcher</span></span>
<span data-ttu-id="cceb6-129">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="cceb6-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="cceb6-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cceb6-130">-NetworkWatcherName</span></span>
<span data-ttu-id="cceb6-131">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="cceb6-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="cceb6-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cceb6-132">-PassThru</span></span>
<span data-ttu-id="cceb6-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="cceb6-133">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cceb6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cceb6-134">-ResourceGroupName</span></span>
<span data-ttu-id="cceb6-135">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="cceb6-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="cceb6-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cceb6-136">-ResourceId</span></span>
<span data-ttu-id="cceb6-137">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="cceb6-137">Resource ID.</span></span>

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

### <span data-ttu-id="cceb6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cceb6-138">-WhatIf</span></span>
<span data-ttu-id="cceb6-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cceb6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cceb6-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cceb6-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cceb6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cceb6-141">CommonParameters</span></span>
<span data-ttu-id="cceb6-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cceb6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cceb6-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cceb6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cceb6-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cceb6-144">INPUTS</span></span>

### <span data-ttu-id="cceb6-145">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cceb6-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="cceb6-146">System. String Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="cceb6-146">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="cceb6-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cceb6-147">OUTPUTS</span></span>

### <span data-ttu-id="cceb6-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cceb6-148">System.Boolean</span></span>

## <span data-ttu-id="cceb6-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cceb6-149">NOTES</span></span>
<span data-ttu-id="cceb6-150">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="cceb6-150">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="cceb6-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cceb6-151">RELATED LINKS</span></span>

[<span data-ttu-id="cceb6-152">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cceb6-152">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="cceb6-153">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cceb6-153">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="cceb6-154">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cceb6-154">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="cceb6-155">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cceb6-155">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="cceb6-156">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cceb6-156">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="cceb6-157">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cceb6-157">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="cceb6-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cceb6-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="cceb6-159">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cceb6-159">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="cceb6-160">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cceb6-160">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="cceb6-161">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cceb6-161">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="cceb6-162">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cceb6-162">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="cceb6-163">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cceb6-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="cceb6-164">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cceb6-164">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="cceb6-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="cceb6-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="cceb6-166">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cceb6-166">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="cceb6-167">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cceb6-167">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="cceb6-168">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cceb6-168">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="cceb6-169">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cceb6-169">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
