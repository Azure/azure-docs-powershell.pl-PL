---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
ms.openlocfilehash: 9df0d0855ca22e9ea7141a99c69c8b44f16f489d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554124"
---
# <span data-ttu-id="09ef0-101">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="09ef0-101">Get-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="09ef0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="09ef0-103">Pobiera właściwości obserwatora sieci</span><span class="sxs-lookup"><span data-stu-id="09ef0-103">Gets the properties of a Network Watcher</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09ef0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09ef0-104">SYNTAX</span></span>

### <span data-ttu-id="09ef0-105">Pobierz</span><span class="sxs-lookup"><span data-stu-id="09ef0-105">Get</span></span>
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09ef0-106">Lista</span><span class="sxs-lookup"><span data-stu-id="09ef0-106">List</span></span>
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09ef0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="09ef0-107">DESCRIPTION</span></span>
<span data-ttu-id="09ef0-108">Polecenie cmdlet Get-AzureRmNetworkWatcher powoduje wyświetlenie co najmniej jednego zasobu obserwatora sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="09ef0-108">The Get-AzureRmNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="09ef0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09ef0-109">EXAMPLES</span></span>

### <span data-ttu-id="09ef0-110">--------------------------Przykład 1: uzyskiwanie monitora sieci--------------------------</span><span class="sxs-lookup"><span data-stu-id="09ef0-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="09ef0-111">Pobiera Monitor sieci o nazwie NetworkWatcher_westcentralus w grupie zasobów NetworkWatcherRG.</span><span class="sxs-lookup"><span data-stu-id="09ef0-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="09ef0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09ef0-112">PARAMETERS</span></span>

### <span data-ttu-id="09ef0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09ef0-113">-DefaultProfile</span></span>
<span data-ttu-id="09ef0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="09ef0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09ef0-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="09ef0-115">-Name</span></span>
<span data-ttu-id="09ef0-116">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="09ef0-116">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09ef0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09ef0-117">-ResourceGroupName</span></span>
<span data-ttu-id="09ef0-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="09ef0-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09ef0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ef0-119">CommonParameters</span></span>
<span data-ttu-id="09ef0-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09ef0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ef0-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09ef0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ef0-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09ef0-122">INPUTS</span></span>

### <span data-ttu-id="09ef0-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="09ef0-123">None</span></span>

## <span data-ttu-id="09ef0-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09ef0-124">OUTPUTS</span></span>

### <span data-ttu-id="09ef0-125">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="09ef0-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="09ef0-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09ef0-126">NOTES</span></span>
<span data-ttu-id="09ef0-127">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, obserwator sieci</span><span class="sxs-lookup"><span data-stu-id="09ef0-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="09ef0-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09ef0-128">RELATED LINKS</span></span>

[<span data-ttu-id="09ef0-129">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="09ef0-129">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="09ef0-130">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="09ef0-130">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="09ef0-131">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="09ef0-131">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="09ef0-132">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="09ef0-132">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="09ef0-133">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="09ef0-133">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="09ef0-134">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="09ef0-134">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="09ef0-135">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="09ef0-135">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="09ef0-136">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="09ef0-136">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="09ef0-137">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="09ef0-137">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="09ef0-138">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="09ef0-138">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="09ef0-139">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="09ef0-139">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="09ef0-140">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="09ef0-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
