---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: 12bf5d24421f79eecb3138a68425968b9b4fbe62
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186819"
---
# <span data-ttu-id="36a60-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="36a60-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="36a60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36a60-102">SYNOPSIS</span></span>
<span data-ttu-id="36a60-103">Modyfikuje wirtualne centrum, aby dodać do niego wirtualną tabelę tras HUb.</span><span class="sxs-lookup"><span data-stu-id="36a60-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="36a60-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="36a60-104">SYNTAX</span></span>

### <span data-ttu-id="36a60-105">ByVirtualHubName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="36a60-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36a60-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="36a60-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36a60-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="36a60-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36a60-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="36a60-108">DESCRIPTION</span></span>
<span data-ttu-id="36a60-109">{{ Wypełnij opis }}</span><span class="sxs-lookup"><span data-stu-id="36a60-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="36a60-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="36a60-110">EXAMPLES</span></span>

### <span data-ttu-id="36a60-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="36a60-111">Example 1</span></span>
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

<span data-ttu-id="36a60-112">Najpierw utworzymy obiekt Trasa centrum wirtualnego i użyjemy go do utworzenia zasobu tabeli tras centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="36a60-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="36a60-113">Następnie ustawiamy ten zasób tabeli trasy na wirtualne centrum za pomocą Set-AzVirtualHub tabeli.</span><span class="sxs-lookup"><span data-stu-id="36a60-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="36a60-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36a60-114">PARAMETERS</span></span>

### <span data-ttu-id="36a60-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="36a60-115">-AsJob</span></span>
<span data-ttu-id="36a60-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="36a60-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36a60-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a60-117">-DefaultProfile</span></span>
<span data-ttu-id="36a60-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="36a60-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36a60-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36a60-119">-InputObject</span></span>
<span data-ttu-id="36a60-120">Obiekt centrum wirtualnego do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="36a60-120">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="36a60-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="36a60-121">-Name</span></span>
<span data-ttu-id="36a60-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="36a60-122">The resource name.</span></span>

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

### <span data-ttu-id="36a60-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36a60-123">-ResourceGroupName</span></span>
<span data-ttu-id="36a60-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36a60-124">The resource group name.</span></span>

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

### <span data-ttu-id="36a60-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36a60-125">-ResourceId</span></span>
<span data-ttu-id="36a60-126">Identyfikator zasobu centrum wirtualnego do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="36a60-126">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="36a60-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="36a60-127">-RouteTable</span></span>
<span data-ttu-id="36a60-128">Tabele tras skojarzone z tym centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="36a60-128">The route tables associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="36a60-129">— Tag</span><span class="sxs-lookup"><span data-stu-id="36a60-129">-Tag</span></span>
<span data-ttu-id="36a60-130">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="36a60-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="36a60-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36a60-131">-Confirm</span></span>
<span data-ttu-id="36a60-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="36a60-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36a60-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36a60-133">-WhatIf</span></span>
<span data-ttu-id="36a60-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36a60-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36a60-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="36a60-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36a60-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a60-136">CommonParameters</span></span>
<span data-ttu-id="36a60-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36a60-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a60-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36a60-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a60-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36a60-139">INPUTS</span></span>

### <span data-ttu-id="36a60-140">System.String</span><span class="sxs-lookup"><span data-stu-id="36a60-140">System.String</span></span>

### <span data-ttu-id="36a60-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="36a60-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="36a60-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36a60-142">OUTPUTS</span></span>

### <span data-ttu-id="36a60-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="36a60-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="36a60-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="36a60-144">NOTES</span></span>

## <span data-ttu-id="36a60-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36a60-145">RELATED LINKS</span></span>
