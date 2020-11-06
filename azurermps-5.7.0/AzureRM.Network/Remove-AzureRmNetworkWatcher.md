---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
ms.openlocfilehash: 4fd6da3388b4058a3aa4bee2fe918fb063c8fd6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546683"
---
# <span data-ttu-id="6b271-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6b271-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="6b271-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b271-102">SYNOPSIS</span></span>
<span data-ttu-id="6b271-103">Usuwa Monitor sieci.</span><span class="sxs-lookup"><span data-stu-id="6b271-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b271-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b271-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b271-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6b271-105">DESCRIPTION</span></span>
<span data-ttu-id="6b271-106">Polecenie cmdlet Remove-AzureRmNetworkWatcher usuwa zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="6b271-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="6b271-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b271-107">EXAMPLES</span></span>

### <span data-ttu-id="6b271-108">--------------------------Przykład 1: Tworzenie i usuwanie obserwatora sieci--------------------------</span><span class="sxs-lookup"><span data-stu-id="6b271-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="6b271-109">W tym przykładzie przedstawiono tworzenie obserwatora sieci w grupie zasobów, a następnie natychmiastowe usunięcie go.</span><span class="sxs-lookup"><span data-stu-id="6b271-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="6b271-110">Należy zauważyć, że dla każdego regionu można utworzyć tylko jeden Monitor sieci dla każdej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6b271-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="6b271-111">Aby zapobiec wyświetlaniu monitu podczas usuwania sieci wirtualnej, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="6b271-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="6b271-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b271-112">PARAMETERS</span></span>

### <span data-ttu-id="6b271-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b271-113">-AsJob</span></span>
<span data-ttu-id="6b271-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6b271-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b271-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b271-115">-DefaultProfile</span></span>
<span data-ttu-id="6b271-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b271-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b271-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6b271-117">-Name</span></span>
<span data-ttu-id="6b271-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="6b271-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b271-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b271-119">-PassThru</span></span>
<span data-ttu-id="6b271-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6b271-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6b271-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b271-121">-ResourceGroupName</span></span>
<span data-ttu-id="6b271-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6b271-122">The resource group name.</span></span>

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

### <span data-ttu-id="6b271-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6b271-123">-Confirm</span></span>
<span data-ttu-id="6b271-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b271-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b271-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b271-125">-WhatIf</span></span>
<span data-ttu-id="6b271-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b271-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b271-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6b271-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b271-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b271-128">CommonParameters</span></span>
<span data-ttu-id="6b271-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b271-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b271-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b271-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b271-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b271-131">INPUTS</span></span>

### <span data-ttu-id="6b271-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6b271-132">System.String</span></span>

## <span data-ttu-id="6b271-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b271-133">OUTPUTS</span></span>

### <span data-ttu-id="6b271-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="6b271-134">System.Object</span></span>

## <span data-ttu-id="6b271-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b271-135">NOTES</span></span>
<span data-ttu-id="6b271-136">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, obserwator sieci</span><span class="sxs-lookup"><span data-stu-id="6b271-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="6b271-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b271-137">RELATED LINKS</span></span>

[<span data-ttu-id="6b271-138">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6b271-138">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6b271-139">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6b271-139">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6b271-140">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6b271-140">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6b271-141">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6b271-141">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="6b271-142">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6b271-142">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6b271-143">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6b271-143">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6b271-144">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6b271-144">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6b271-145">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6b271-145">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="6b271-146">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6b271-146">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="6b271-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6b271-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6b271-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6b271-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="6b271-149">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6b271-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
