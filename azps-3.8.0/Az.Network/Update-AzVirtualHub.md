---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
ms.openlocfilehash: a07df2c6330757bf9e5b4f211429f6e2918fea39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894362"
---
# <span data-ttu-id="9e388-101">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9e388-101">Update-AzVirtualHub</span></span>

## <span data-ttu-id="9e388-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e388-102">SYNOPSIS</span></span>
<span data-ttu-id="9e388-103">Umożliwia zaktualizowanie koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="9e388-103">Updates a virtual hub.</span></span>

## <span data-ttu-id="9e388-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e388-104">SYNTAX</span></span>

### <span data-ttu-id="9e388-105">ByVirtualHubName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9e388-105">ByVirtualHubName (Default)</span></span>
```
Update-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e388-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="9e388-106">ByVirtualHubResourceId</span></span>
```
Update-AzVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e388-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="9e388-107">ByVirtualHubObject</span></span>
```
Update-AzVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e388-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9e388-108">DESCRIPTION</span></span>
<span data-ttu-id="9e388-109">Polecenie cmdlet **Update-AzVirtualHub** umożliwia zaktualizowanie koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="9e388-109">The **Update-AzVirtualHub** cmdlet updates a virtual hub.</span></span>

## <span data-ttu-id="9e388-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e388-110">EXAMPLES</span></span>

### <span data-ttu-id="9e388-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9e388-111">Example 1</span></span>

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

<span data-ttu-id="9e388-112">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="9e388-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="9e388-113">Koncentrator wirtualny będzie miał przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="9e388-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="9e388-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9e388-114">Example 2</span></span>

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

<span data-ttu-id="9e388-115">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="9e388-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="9e388-116">Koncentrator wirtualny będzie miał przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="9e388-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="9e388-117">Ten przykład jest podobny do przykładu 1, ale umożliwia także dołączenie tabeli routingu do koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="9e388-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="9e388-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e388-118">PARAMETERS</span></span>

### <span data-ttu-id="9e388-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9e388-119">-AddressPrefix</span></span>
<span data-ttu-id="9e388-120">Ciąg przestrzeni adresowej dla tego koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="9e388-120">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="9e388-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e388-121">-AsJob</span></span>
<span data-ttu-id="9e388-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9e388-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e388-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e388-123">-DefaultProfile</span></span>
<span data-ttu-id="9e388-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e388-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e388-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="9e388-125">-HubVnetConnection</span></span>
<span data-ttu-id="9e388-126">Centralne połączenia z siecią wirtualną, skojarzone z tym wirtualnym koncentratorem.</span><span class="sxs-lookup"><span data-stu-id="9e388-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="9e388-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9e388-127">-InputObject</span></span>
<span data-ttu-id="9e388-128">Wirtualny obiekt koncentratorowy do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="9e388-128">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="9e388-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9e388-129">-Name</span></span>
<span data-ttu-id="9e388-130">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="9e388-130">The resource name.</span></span>

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

### <span data-ttu-id="9e388-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e388-131">-ResourceGroupName</span></span>
<span data-ttu-id="9e388-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e388-132">The resource group name.</span></span>

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

### <span data-ttu-id="9e388-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e388-133">-ResourceId</span></span>
<span data-ttu-id="9e388-134">Identyfikator zasobu wirtualnego koncentratora, który ma zostać zmodyfikowany.</span><span class="sxs-lookup"><span data-stu-id="9e388-134">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="9e388-135">-Routeing</span><span class="sxs-lookup"><span data-stu-id="9e388-135">-RouteTable</span></span>
<span data-ttu-id="9e388-136">Tabela tras skojarzona z tym wirtualnym koncentratorem.</span><span class="sxs-lookup"><span data-stu-id="9e388-136">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="9e388-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="9e388-137">-Sku</span></span>
<span data-ttu-id="9e388-138">Wersja SKU koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="9e388-138">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="9e388-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e388-139">-Tag</span></span>
<span data-ttu-id="9e388-140">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e388-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9e388-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9e388-141">-Confirm</span></span>
<span data-ttu-id="9e388-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e388-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e388-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e388-143">-WhatIf</span></span>
<span data-ttu-id="9e388-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e388-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e388-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9e388-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e388-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e388-146">CommonParameters</span></span>
<span data-ttu-id="9e388-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e388-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e388-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e388-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e388-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e388-149">INPUTS</span></span>

### <span data-ttu-id="9e388-150">System. String</span><span class="sxs-lookup"><span data-stu-id="9e388-150">System.String</span></span>

### <span data-ttu-id="9e388-151">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9e388-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="9e388-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e388-152">OUTPUTS</span></span>

### <span data-ttu-id="9e388-153">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9e388-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="9e388-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e388-154">NOTES</span></span>

## <span data-ttu-id="9e388-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e388-155">RELATED LINKS</span></span>

[<span data-ttu-id="9e388-156">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9e388-156">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="9e388-157">Nowe — AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9e388-157">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="9e388-158">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9e388-158">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)
