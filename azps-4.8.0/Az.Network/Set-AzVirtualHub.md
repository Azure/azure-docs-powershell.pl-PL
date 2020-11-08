---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: 12bf5d24421f79eecb3138a68425968b9b4fbe62
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223027"
---
# <span data-ttu-id="3498b-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3498b-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="3498b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3498b-102">SYNOPSIS</span></span>
<span data-ttu-id="3498b-103">Modyfikuje koncentrator wirtualny, aby dodać do niego tabelę tras koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="3498b-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="3498b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3498b-104">SYNTAX</span></span>

### <span data-ttu-id="3498b-105">ByVirtualHubName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3498b-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3498b-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="3498b-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3498b-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="3498b-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3498b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3498b-108">DESCRIPTION</span></span>
<span data-ttu-id="3498b-109">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="3498b-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="3498b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3498b-110">EXAMPLES</span></span>

### <span data-ttu-id="3498b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3498b-111">Example 1</span></span>
```powershell
PS C:\> $existingHub�=�Get-AzVirtualHub�-ResourceGroupName�"testRg"�-Name�"westushub"
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> $routeTable1�=�Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"
PS C:\> Set-AzVirtualHub�-VirtualHub�$existingHub�-RouteTable�@($routeTable1)

VirtualWan                            : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/testWan
ResourceGroupName                     : testRg
Name                                  : westushub
Id                                    : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubswestushub
AddressPrefix                         : 10.40.0.0/16
RouteTable                            : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkExpressRouteConnections :
RouteTables                           : {routeTable1}
Location                              : westus
Sku                                   : Standard
Type                                  : Microsoft.Network/virtualHubs
ProvisioningState                     : Succeeded
```

<span data-ttu-id="3498b-112">Najpierw tworzymy obiekt wirtualnej tablicy węzłowej i użyj go do utworzenia zasobu tabeli routingu koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="3498b-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="3498b-113">Następnie ustawimy ten zasób tabeli tras z koncentratorem wirtualnym za pomocą polecenia Set-AzVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="3498b-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="3498b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3498b-114">PARAMETERS</span></span>

### <span data-ttu-id="3498b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3498b-115">-AsJob</span></span>
<span data-ttu-id="3498b-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3498b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3498b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3498b-117">-DefaultProfile</span></span>
<span data-ttu-id="3498b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3498b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3498b-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3498b-119">-InputObject</span></span>
<span data-ttu-id="3498b-120">Wirtualny obiekt koncentratorowy do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="3498b-120">The Virtual hub object to be modified.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3498b-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3498b-121">-Name</span></span>
<span data-ttu-id="3498b-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="3498b-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3498b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3498b-123">-ResourceGroupName</span></span>
<span data-ttu-id="3498b-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3498b-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3498b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3498b-125">-ResourceId</span></span>
<span data-ttu-id="3498b-126">Identyfikator zasobu wirtualnego koncentratora, który ma zostać zmodyfikowany.</span><span class="sxs-lookup"><span data-stu-id="3498b-126">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3498b-127">-Routeing</span><span class="sxs-lookup"><span data-stu-id="3498b-127">-RouteTable</span></span>
<span data-ttu-id="3498b-128">Tabele tras skojarzone z tym wirtualnym koncentratorem.</span><span class="sxs-lookup"><span data-stu-id="3498b-128">The route tables associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3498b-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="3498b-129">-Tag</span></span>
<span data-ttu-id="3498b-130">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="3498b-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3498b-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3498b-131">-Confirm</span></span>
<span data-ttu-id="3498b-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3498b-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3498b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3498b-133">-WhatIf</span></span>
<span data-ttu-id="3498b-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3498b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3498b-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3498b-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3498b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3498b-136">CommonParameters</span></span>
<span data-ttu-id="3498b-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3498b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3498b-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3498b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3498b-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3498b-139">INPUTS</span></span>

### <span data-ttu-id="3498b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3498b-140">System.String</span></span>

### <span data-ttu-id="3498b-141">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3498b-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="3498b-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3498b-142">OUTPUTS</span></span>

### <span data-ttu-id="3498b-143">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3498b-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="3498b-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3498b-144">NOTES</span></span>

## <span data-ttu-id="3498b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3498b-145">RELATED LINKS</span></span>
