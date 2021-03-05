---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/powershell/module/az.network/add-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
ms.openlocfilehash: 8b0e50bfd335fd8efecef44d4f40e540da8afe09
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972698"
---
# <span data-ttu-id="e0865-101">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e0865-101">Add-AzRouteConfig</span></span>

## <span data-ttu-id="e0865-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0865-102">SYNOPSIS</span></span>
<span data-ttu-id="e0865-103">Dodaje trasę do tabeli trasy.</span><span class="sxs-lookup"><span data-stu-id="e0865-103">Adds a route to a route table.</span></span>

## <span data-ttu-id="e0865-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0865-104">SYNTAX</span></span>

```
Add-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0865-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0865-105">DESCRIPTION</span></span>
<span data-ttu-id="e0865-106">Polecenie **cmdlet Add-AzRouteConfig** dodaje trasę do tabeli trasy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0865-106">The **Add-AzRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="e0865-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0865-107">EXAMPLES</span></span>

### <span data-ttu-id="e0865-108">Przykład 1. Dodawanie trasy do tabeli tras</span><span class="sxs-lookup"><span data-stu-id="e0865-108">Example 1: Add a route to a route table</span></span>
```powershell
PS C:\>$RouteTable = Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="e0865-109">Pierwsze polecenie pobiera tabelę trasy o nazwie RouteTable01 przy użyciu Get-AzRouteTable cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0865-109">The first command gets a route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="e0865-110">Polecenie przechowuje tabelę w $RouteTable zmienną.</span><span class="sxs-lookup"><span data-stu-id="e0865-110">The command stores the table in the $RouteTable variable.</span></span>
<span data-ttu-id="e0865-111">Drugie polecenie dodaje trasę o nazwie Trasa13 do tabeli trasy przechowywanej w $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="e0865-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="e0865-112">Ta trasa przesyła pakiety do lokalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e0865-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="e0865-113">Przykład 2. Dodawanie trasy do tabeli trasy przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="e0865-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```powershell
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="e0865-114">To polecenie pobiera tabelę tras o nazwie RouteTable01 przy użyciu tabeli **Get-AzRouteTable.**</span><span class="sxs-lookup"><span data-stu-id="e0865-114">This command gets the route table named RouteTable01 by using **Get-AzRouteTable**.</span></span>
<span data-ttu-id="e0865-115">Polecenie przekazuje tabelę do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="e0865-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e0865-116">Bieżące polecenie cmdlet dodaje trasę o nazwie Route02, a następnie przekazuje wynik do polecenia cmdlet **Set-AzRouteTable,** które aktualizuje tabelę w celu odzwierciedlenia wprowadzonych zmian.</span><span class="sxs-lookup"><span data-stu-id="e0865-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="e0865-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0865-117">PARAMETERS</span></span>

### <span data-ttu-id="e0865-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e0865-118">-AddressPrefix</span></span>
<span data-ttu-id="e0865-119">Określa miejsce docelowe w formacie CIDR (Classless Interdomain Routing), do którego ma zastosowanie trasa.</span><span class="sxs-lookup"><span data-stu-id="e0865-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0865-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0865-120">-DefaultProfile</span></span>
<span data-ttu-id="e0865-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0865-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0865-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e0865-122">-Name</span></span>
<span data-ttu-id="e0865-123">Określa nazwę trasy, która ma być dodawania do tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="e0865-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="e0865-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="e0865-124">-NextHopIpAddress</span></span>
<span data-ttu-id="e0865-125">Określa adres IP wirtualnego urządzenia, które dodajesz do sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0865-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="e0865-126">Ta trasa przesyła pakiety na ten adres.</span><span class="sxs-lookup"><span data-stu-id="e0865-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="e0865-127">Określ ten parametr tylko wtedy, gdy określisz wartość parametru VirtualAppliance *NextHopType.*</span><span class="sxs-lookup"><span data-stu-id="e0865-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0865-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="e0865-128">-NextHopType</span></span>
<span data-ttu-id="e0865-129">Określa sposób przekazywania pakietów przez tę trasę.</span><span class="sxs-lookup"><span data-stu-id="e0865-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="e0865-130">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e0865-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e0865-131">Internet.</span><span class="sxs-lookup"><span data-stu-id="e0865-131">Internet.</span></span>
<span data-ttu-id="e0865-132">Domyślna brama internetowa dostarczana przez platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="e0865-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="e0865-133">Brak.</span><span class="sxs-lookup"><span data-stu-id="e0865-133">None.</span></span>
<span data-ttu-id="e0865-134">Jeśli określisz tę wartość, trasa nie będzie przesyłać dalej pakietów.</span><span class="sxs-lookup"><span data-stu-id="e0865-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="e0865-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="e0865-135">VirtualAppliance.</span></span>
<span data-ttu-id="e0865-136">Urządzenie wirtualne, które dodajesz do swojej sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0865-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="e0865-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="e0865-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="e0865-138">Brama wirtualnej sieci prywatnej typu serwer-serwer platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0865-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="e0865-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="e0865-139">VnetLocal.</span></span>
<span data-ttu-id="e0865-140">Lokalna sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="e0865-140">The local virtual network.</span></span>
<span data-ttu-id="e0865-141">Jeśli masz dwie podsieci: 10.1.0.0/16 i 10.2.0.0/16 w tej samej sieci wirtualnej, wybierz wartość VnetLocal dla każdej podsieci, aby przesyłać ją dalej do drugiej podsieci.</span><span class="sxs-lookup"><span data-stu-id="e0865-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0865-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e0865-142">-RouteTable</span></span>
<span data-ttu-id="e0865-143">Określa tabelę trasy, do której to polecenie cmdlet dodaje trasę.</span><span class="sxs-lookup"><span data-stu-id="e0865-143">Specifies the route table to which this cmdlet adds a route.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0865-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0865-144">-Confirm</span></span>
<span data-ttu-id="e0865-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e0865-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0865-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0865-146">-WhatIf</span></span>
<span data-ttu-id="e0865-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0865-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0865-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e0865-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0865-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0865-149">CommonParameters</span></span>
<span data-ttu-id="e0865-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0865-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0865-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0865-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0865-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0865-152">INPUTS</span></span>

### <span data-ttu-id="e0865-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e0865-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="e0865-154">System.String</span><span class="sxs-lookup"><span data-stu-id="e0865-154">System.String</span></span>

## <span data-ttu-id="e0865-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0865-155">OUTPUTS</span></span>

### <span data-ttu-id="e0865-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e0865-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="e0865-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0865-157">NOTES</span></span>

## <span data-ttu-id="e0865-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0865-158">RELATED LINKS</span></span>

[<span data-ttu-id="e0865-159">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e0865-159">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="e0865-160">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="e0865-160">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="e0865-161">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e0865-161">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="e0865-162">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e0865-162">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="e0865-163">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e0865-163">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)

[<span data-ttu-id="e0865-164">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="e0865-164">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


