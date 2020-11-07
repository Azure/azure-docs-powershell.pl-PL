---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHub.md
ms.openlocfilehash: 4058f9a2ba0de1e5610773ad4af21c8bb788d58c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717623"
---
# <span data-ttu-id="fd298-101">New-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="fd298-101">New-AzureRmVirtualHub</span></span>

## <span data-ttu-id="fd298-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd298-102">SYNOPSIS</span></span>
<span data-ttu-id="fd298-103">Tworzy zasób usługi Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="fd298-103">Creates an Azure VirtualHub resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd298-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd298-104">SYNTAX</span></span>

### <span data-ttu-id="fd298-105">ByVirtualWanObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fd298-105">ByVirtualWanObject (Default)</span></span>
```
New-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan>
 -AddressPrefix <String> -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd298-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="fd298-106">ByVirtualWanResourceId</span></span>
```
New-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd298-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fd298-107">DESCRIPTION</span></span>
<span data-ttu-id="fd298-108">Tworzy zasób usługi Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="fd298-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="fd298-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd298-109">EXAMPLES</span></span>

### <span data-ttu-id="fd298-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd298-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

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

<span data-ttu-id="fd298-111">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="fd298-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="fd298-112">Koncentrator wirtualny będzie miał przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="fd298-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="fd298-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fd298-113">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

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

<span data-ttu-id="fd298-114">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="fd298-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="fd298-115">Koncentrator wirtualny będzie miał przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="fd298-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="fd298-116">Ten przykład jest podobny do przykładu 1, ale używa identyfikatora zasobu, aby odwołać się do wirtualnej sieci WAN, która jest wymagana do utworzenia koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="fd298-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="fd298-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="fd298-117">Example 3</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzureRmVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzureRmVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzureRmVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzureRmVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

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

<span data-ttu-id="fd298-118">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="fd298-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="fd298-119">Koncentrator wirtualny będzie miał dołączoną przestrzeń adresową "10.0.1.0/24" oraz tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="fd298-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="fd298-120">Ten przykład jest podobny do przykładu 2, ale umożliwia także dołączenie tabeli routingu do koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="fd298-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="fd298-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd298-121">PARAMETERS</span></span>

### <span data-ttu-id="fd298-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fd298-122">-AddressPrefix</span></span>
<span data-ttu-id="fd298-123">Ciąg przestrzeni adresowej dla tego koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="fd298-123">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="fd298-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd298-124">-AsJob</span></span>
<span data-ttu-id="fd298-125">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fd298-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd298-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd298-126">-DefaultProfile</span></span>
<span data-ttu-id="fd298-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd298-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd298-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="fd298-128">-HubVnetConnection</span></span>
<span data-ttu-id="fd298-129">Centralne połączenia z siecią wirtualną, skojarzone z tym wirtualnym koncentratorem.</span><span class="sxs-lookup"><span data-stu-id="fd298-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="fd298-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fd298-130">-Location</span></span>
<span data-ttu-id="fd298-131">pozycję.</span><span class="sxs-lookup"><span data-stu-id="fd298-131">location.</span></span>

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

### <span data-ttu-id="fd298-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd298-132">-Name</span></span>
<span data-ttu-id="fd298-133">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="fd298-133">The resource name.</span></span>

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

### <span data-ttu-id="fd298-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd298-134">-ResourceGroupName</span></span>
<span data-ttu-id="fd298-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd298-135">The resource group name.</span></span>

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

### <span data-ttu-id="fd298-136">-Routeing</span><span class="sxs-lookup"><span data-stu-id="fd298-136">-RouteTable</span></span>
<span data-ttu-id="fd298-137">Tabela tras skojarzona z tym wirtualnym koncentratorem.</span><span class="sxs-lookup"><span data-stu-id="fd298-137">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="fd298-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="fd298-138">-Tag</span></span>
<span data-ttu-id="fd298-139">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd298-139">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fd298-140">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="fd298-140">-VirtualWan</span></span>
<span data-ttu-id="fd298-141">Wirtualny obiekt sieci WAN, z którym jest połączony ten koncentrator.</span><span class="sxs-lookup"><span data-stu-id="fd298-141">The virtual wan object this hub is linked to.</span></span>

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

### <span data-ttu-id="fd298-142">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="fd298-142">-VirtualWanId</span></span>
<span data-ttu-id="fd298-143">Identyfikator wirtualnego obiektu sieci WAN, z którym jest połączony ten koncentrator.</span><span class="sxs-lookup"><span data-stu-id="fd298-143">The id of virtual wan object this hub is linked to.</span></span>

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

### <span data-ttu-id="fd298-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd298-144">-Confirm</span></span>
<span data-ttu-id="fd298-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd298-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd298-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd298-146">-WhatIf</span></span>
<span data-ttu-id="fd298-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd298-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd298-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fd298-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd298-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd298-149">CommonParameters</span></span>
<span data-ttu-id="fd298-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd298-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd298-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd298-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd298-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd298-152">INPUTS</span></span>

### <span data-ttu-id="fd298-153">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="fd298-153">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="fd298-154">System. String</span><span class="sxs-lookup"><span data-stu-id="fd298-154">System.String</span></span>

## <span data-ttu-id="fd298-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd298-155">OUTPUTS</span></span>

### <span data-ttu-id="fd298-156">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="fd298-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="fd298-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd298-157">NOTES</span></span>

## <span data-ttu-id="fd298-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd298-158">RELATED LINKS</span></span>
