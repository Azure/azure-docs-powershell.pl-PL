---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: 8527b383dd5469d1a9bc34b7916a1e28b3f673f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869839"
---
# <span data-ttu-id="a0da8-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a0da8-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="a0da8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0da8-102">SYNOPSIS</span></span>
<span data-ttu-id="a0da8-103">Tworzy zasób usługi Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="a0da8-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="a0da8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0da8-104">SYNTAX</span></span>

### <span data-ttu-id="a0da8-105">ByVirtualWanObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a0da8-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0da8-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="a0da8-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0da8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a0da8-107">DESCRIPTION</span></span>
<span data-ttu-id="a0da8-108">Tworzy zasób usługi Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="a0da8-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="a0da8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0da8-109">EXAMPLES</span></span>

### <span data-ttu-id="a0da8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a0da8-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="a0da8-111">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a0da8-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="a0da8-112">Koncentrator wirtualny będzie miał przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="a0da8-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="a0da8-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a0da8-113">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="a0da8-114">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a0da8-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="a0da8-115">Koncentrator wirtualny będzie miał przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="a0da8-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="a0da8-116">Ten przykład jest podobny do przykładu 1, ale używa identyfikatora zasobu, aby odwołać się do wirtualnej sieci WAN, która jest wymagana do utworzenia koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a0da8-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="a0da8-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a0da8-117">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="a0da8-118">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a0da8-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="a0da8-119">Koncentrator wirtualny będzie miał dołączoną przestrzeń adresową "10.0.1.0/24" oraz tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="a0da8-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="a0da8-120">Ten przykład jest podobny do przykładu 2, ale umożliwia także dołączenie tabeli routingu do koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a0da8-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="a0da8-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0da8-121">PARAMETERS</span></span>

### <span data-ttu-id="a0da8-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a0da8-122">-AddressPrefix</span></span>
<span data-ttu-id="a0da8-123">Ciąg przestrzeni adresowej dla tego koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a0da8-123">The address space string for this virtual hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0da8-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0da8-124">-AsJob</span></span>
<span data-ttu-id="a0da8-125">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a0da8-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0da8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0da8-126">-DefaultProfile</span></span>
<span data-ttu-id="a0da8-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0da8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0da8-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a0da8-128">-HubVnetConnection</span></span>
<span data-ttu-id="a0da8-129">Centralne połączenia z siecią wirtualną, skojarzone z tym wirtualnym koncentratorem.</span><span class="sxs-lookup"><span data-stu-id="a0da8-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0da8-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a0da8-130">-Location</span></span>
<span data-ttu-id="a0da8-131">pozycję.</span><span class="sxs-lookup"><span data-stu-id="a0da8-131">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0da8-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a0da8-132">-Name</span></span>
<span data-ttu-id="a0da8-133">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a0da8-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0da8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0da8-134">-ResourceGroupName</span></span>
<span data-ttu-id="a0da8-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0da8-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0da8-136">-Routeing</span><span class="sxs-lookup"><span data-stu-id="a0da8-136">-RouteTable</span></span>
<span data-ttu-id="a0da8-137">Tabela tras skojarzona z tym wirtualnym koncentratorem.</span><span class="sxs-lookup"><span data-stu-id="a0da8-137">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0da8-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0da8-138">-Tag</span></span>
<span data-ttu-id="a0da8-139">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0da8-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0da8-140">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="a0da8-140">-VirtualWan</span></span>
<span data-ttu-id="a0da8-141">Wirtualny obiekt sieci WAN, z którym jest połączony ten koncentrator.</span><span class="sxs-lookup"><span data-stu-id="a0da8-141">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0da8-142">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="a0da8-142">-VirtualWanId</span></span>
<span data-ttu-id="a0da8-143">Identyfikator wirtualnego obiektu sieci WAN, z którym jest połączony ten koncentrator.</span><span class="sxs-lookup"><span data-stu-id="a0da8-143">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0da8-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0da8-144">-Confirm</span></span>
<span data-ttu-id="a0da8-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0da8-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0da8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0da8-146">-WhatIf</span></span>
<span data-ttu-id="a0da8-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0da8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0da8-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a0da8-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0da8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0da8-149">CommonParameters</span></span>
<span data-ttu-id="a0da8-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0da8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0da8-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0da8-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0da8-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0da8-152">INPUTS</span></span>

### <span data-ttu-id="a0da8-153">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a0da8-153">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="a0da8-154">System. String</span><span class="sxs-lookup"><span data-stu-id="a0da8-154">System.String</span></span>

## <span data-ttu-id="a0da8-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0da8-155">OUTPUTS</span></span>

### <span data-ttu-id="a0da8-156">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a0da8-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="a0da8-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0da8-157">NOTES</span></span>

## <span data-ttu-id="a0da8-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0da8-158">RELATED LINKS</span></span>

[<span data-ttu-id="a0da8-159">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a0da8-159">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="a0da8-160">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a0da8-160">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="a0da8-161">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a0da8-161">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
