---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
ms.openlocfilehash: 871847c9b089a53021d90cdf5b290bf7f9241867
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951578"
---
# <span data-ttu-id="6d9ed-101">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6d9ed-101">Update-AzVirtualHub</span></span>

## <span data-ttu-id="6d9ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d9ed-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9ed-103">Aktualizuje centrum wirtualne.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-103">Updates a virtual hub.</span></span>

## <span data-ttu-id="6d9ed-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6d9ed-104">SYNTAX</span></span>

### <span data-ttu-id="6d9ed-105">ByVirtualHubName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="6d9ed-105">ByVirtualHubName (Default)</span></span>
```
Update-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d9ed-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="6d9ed-106">ByVirtualHubResourceId</span></span>
```
Update-AzVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d9ed-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="6d9ed-107">ByVirtualHubObject</span></span>
```
Update-AzVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d9ed-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6d9ed-108">DESCRIPTION</span></span>
<span data-ttu-id="6d9ed-109">Polecenie **cmdlet Update-AzVirtualHub** aktualizuje centrum wirtualne.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-109">The **Update-AzVirtualHub** cmdlet updates a virtual hub.</span></span>

## <span data-ttu-id="6d9ed-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6d9ed-110">EXAMPLES</span></span>

### <span data-ttu-id="6d9ed-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6d9ed-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Update-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.2.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.2.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="6d9ed-112">Powyższe spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i centrum wirtualnego w Zachód w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="6d9ed-113">Centrum wirtualne będzie mieć przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="6d9ed-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="6d9ed-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6d9ed-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> Update-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 192.168.2.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="6d9ed-115">Powyższe spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i centrum wirtualnego w Zachód w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="6d9ed-116">Centrum wirtualne będzie mieć przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="6d9ed-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="6d9ed-117">Ten przykład jest podobny do przykładu 1, ale także dołącza tabelę trasy do centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="6d9ed-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d9ed-118">PARAMETERS</span></span>

### <span data-ttu-id="6d9ed-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6d9ed-119">-AddressPrefix</span></span>
<span data-ttu-id="6d9ed-120">Ciąg obszaru adresu dla tego centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-120">The address space string for this virtual hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9ed-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="6d9ed-121">-AsJob</span></span>
<span data-ttu-id="6d9ed-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6d9ed-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d9ed-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9ed-123">-DefaultProfile</span></span>
<span data-ttu-id="6d9ed-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d9ed-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6d9ed-125">-HubVnetConnection</span></span>
<span data-ttu-id="6d9ed-126">Połączenia sieci wirtualnej centrum skojarzone z tym centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9ed-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d9ed-127">-InputObject</span></span>
<span data-ttu-id="6d9ed-128">Obiekt centrum wirtualnego do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-128">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="6d9ed-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6d9ed-129">-Name</span></span>
<span data-ttu-id="6d9ed-130">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9ed-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d9ed-131">-ResourceGroupName</span></span>
<span data-ttu-id="6d9ed-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-132">The resource group name.</span></span>

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

### <span data-ttu-id="6d9ed-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d9ed-133">-ResourceId</span></span>
<span data-ttu-id="6d9ed-134">Identyfikator zasobu centrum wirtualnego do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-134">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="6d9ed-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="6d9ed-135">-RouteTable</span></span>
<span data-ttu-id="6d9ed-136">Tabela trasy skojarzona z tym wirtualnym centrum.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-136">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9ed-137">- SKU</span><span class="sxs-lookup"><span data-stu-id="6d9ed-137">-Sku</span></span>
<span data-ttu-id="6d9ed-138">SKU Centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-138">The sku of the Virtual Hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9ed-139">— Tag</span><span class="sxs-lookup"><span data-stu-id="6d9ed-139">-Tag</span></span>
<span data-ttu-id="6d9ed-140">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6d9ed-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6d9ed-141">-Confirm</span></span>
<span data-ttu-id="6d9ed-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d9ed-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d9ed-143">-WhatIf</span></span>
<span data-ttu-id="6d9ed-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d9ed-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d9ed-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9ed-146">CommonParameters</span></span>
<span data-ttu-id="6d9ed-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d9ed-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d9ed-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d9ed-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9ed-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d9ed-149">INPUTS</span></span>

### <span data-ttu-id="6d9ed-150">System.String</span><span class="sxs-lookup"><span data-stu-id="6d9ed-150">System.String</span></span>

### <span data-ttu-id="6d9ed-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6d9ed-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="6d9ed-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d9ed-152">OUTPUTS</span></span>

### <span data-ttu-id="6d9ed-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6d9ed-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="6d9ed-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6d9ed-154">NOTES</span></span>

## <span data-ttu-id="6d9ed-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d9ed-155">RELATED LINKS</span></span>

[<span data-ttu-id="6d9ed-156">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6d9ed-156">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="6d9ed-157">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6d9ed-157">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="6d9ed-158">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6d9ed-158">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)
