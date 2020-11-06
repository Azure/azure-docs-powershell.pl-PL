---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualHub.md
ms.openlocfilehash: 188d449e47155739b4bc532c12b0e9193781c7c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547412"
---
# <span data-ttu-id="e2666-101">Update-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e2666-101">Update-AzureRmVirtualHub</span></span>

## <span data-ttu-id="e2666-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2666-102">SYNOPSIS</span></span>
<span data-ttu-id="e2666-103">Umożliwia zaktualizowanie koncentratora wirtualnego do zamierzonego stanu celu.</span><span class="sxs-lookup"><span data-stu-id="e2666-103">Updates a Virtual Hub to an intended goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2666-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2666-104">SYNTAX</span></span>

### <span data-ttu-id="e2666-105">ByVirtualHubName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e2666-105">ByVirtualHubName (Default)</span></span>
```
Update-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2666-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="e2666-106">ByVirtualHubResourceId</span></span>
```
Update-AzureRmVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2666-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="e2666-107">ByVirtualHubObject</span></span>
```
Update-AzureRmVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2666-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e2666-108">DESCRIPTION</span></span>
<span data-ttu-id="e2666-109">Umożliwia zaktualizowanie koncentratora wirtualnego do zamierzonego stanu celu.</span><span class="sxs-lookup"><span data-stu-id="e2666-109">Updates a Virtual Hub to an intended goal state.</span></span>

## <span data-ttu-id="e2666-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2666-110">EXAMPLES</span></span>

### <span data-ttu-id="e2666-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e2666-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Update-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.2.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.2.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="e2666-112">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e2666-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e2666-113">Koncentrator wirtualny będzie miał przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="e2666-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="e2666-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e2666-114">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> $route1 = New-AzureRmVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzureRmVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzureRmVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> Update-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 192.168.2.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="e2666-115">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e2666-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e2666-116">Koncentrator wirtualny będzie miał przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="e2666-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="e2666-117">Ten przykład jest podobny do przykładu 1, ale umożliwia także dołączenie tabeli routingu do koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="e2666-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="e2666-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2666-118">PARAMETERS</span></span>

### <span data-ttu-id="e2666-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e2666-119">-AddressPrefix</span></span>
<span data-ttu-id="e2666-120">Ciąg przestrzeni adresowej dla tego koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="e2666-120">The address space string for this virtual hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2666-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2666-121">-AsJob</span></span>
<span data-ttu-id="e2666-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e2666-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2666-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2666-123">-DefaultProfile</span></span>
<span data-ttu-id="e2666-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2666-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2666-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e2666-125">-HubVnetConnection</span></span>
<span data-ttu-id="e2666-126">Centralne połączenia z siecią wirtualną, skojarzone z tym wirtualnym koncentratorem.</span><span class="sxs-lookup"><span data-stu-id="e2666-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="e2666-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e2666-127">-InputObject</span></span>
<span data-ttu-id="e2666-128">Wirtualny obiekt koncentratorowy do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="e2666-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2666-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2666-129">-Name</span></span>
<span data-ttu-id="e2666-130">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e2666-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2666-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2666-131">-ResourceGroupName</span></span>
<span data-ttu-id="e2666-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2666-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2666-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2666-133">-ResourceId</span></span>
<span data-ttu-id="e2666-134">Identyfikator zasobu wirtualnego koncentratora, który ma zostać zmodyfikowany.</span><span class="sxs-lookup"><span data-stu-id="e2666-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2666-135">-Routeing</span><span class="sxs-lookup"><span data-stu-id="e2666-135">-RouteTable</span></span>
<span data-ttu-id="e2666-136">Tabela tras skojarzona z tym wirtualnym koncentratorem.</span><span class="sxs-lookup"><span data-stu-id="e2666-136">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="e2666-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="e2666-137">-Tag</span></span>
<span data-ttu-id="e2666-138">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2666-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e2666-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e2666-139">-Confirm</span></span>
<span data-ttu-id="e2666-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2666-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2666-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2666-141">-WhatIf</span></span>
<span data-ttu-id="e2666-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2666-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2666-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e2666-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2666-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2666-144">CommonParameters</span></span>
<span data-ttu-id="e2666-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2666-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2666-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2666-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2666-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2666-147">INPUTS</span></span>

### <span data-ttu-id="e2666-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e2666-148">System.String</span></span>

### <span data-ttu-id="e2666-149">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e2666-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="e2666-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2666-150">OUTPUTS</span></span>

### <span data-ttu-id="e2666-151">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e2666-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="e2666-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2666-152">NOTES</span></span>

## <span data-ttu-id="e2666-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2666-153">RELATED LINKS</span></span>
