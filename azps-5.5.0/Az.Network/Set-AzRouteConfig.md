---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: ca7335abfd8fe2dc9591dcb7d96fb6ca71dda4fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191635"
---
# <span data-ttu-id="a684a-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a684a-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="a684a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a684a-102">SYNOPSIS</span></span>
<span data-ttu-id="a684a-103">Aktualizuje konfigurację trasy dla tabeli trasy.</span><span class="sxs-lookup"><span data-stu-id="a684a-103">Updates a route configuration for a route table.</span></span>

## <span data-ttu-id="a684a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a684a-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a684a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a684a-105">DESCRIPTION</span></span>
<span data-ttu-id="a684a-106">Polecenie **cmdlet Set-AzRouteConfig** aktualizuje konfigurację trasy dla tabeli trasy.</span><span class="sxs-lookup"><span data-stu-id="a684a-106">The **Set-AzRouteConfig** cmdlet updates a route configuration for a route table.</span></span>

## <span data-ttu-id="a684a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a684a-107">EXAMPLES</span></span>

### <span data-ttu-id="a684a-108">Przykład 1. Modyfikowanie trasy</span><span class="sxs-lookup"><span data-stu-id="a684a-108">Example 1: Modify a route</span></span>
```powershell
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
Name              : Routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"58c2922e-9efe-4554-a457-956ef44bc718"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/Routetable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.4.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="a684a-109">To polecenie pobiera tabelę tras o nazwie RouteTable01 przy użyciu Get-AzRouteTable cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a684a-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="a684a-110">Polecenie przekazuje tabelę do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="a684a-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a684a-111">Bieżące polecenie cmdlet modyfikuje trasę o nazwie Route02, a następnie przekazuje wynik do polecenia cmdlet **Set-AzRouteTable,** które aktualizuje tabelę w celu odzwierciedlenia wprowadzonych zmian.</span><span class="sxs-lookup"><span data-stu-id="a684a-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="a684a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a684a-112">PARAMETERS</span></span>

### <span data-ttu-id="a684a-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a684a-113">-AddressPrefix</span></span>
<span data-ttu-id="a684a-114">Określa miejsce docelowe w formacie CIDR (Classless Interdomain Routing), do którego ma zastosowanie trasa.</span><span class="sxs-lookup"><span data-stu-id="a684a-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="a684a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a684a-115">-DefaultProfile</span></span>
<span data-ttu-id="a684a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a684a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a684a-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a684a-117">-Name</span></span>
<span data-ttu-id="a684a-118">Określa nazwę trasy, która zostanie zmodyfikowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a684a-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a684a-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="a684a-119">-NextHopIpAddress</span></span>
<span data-ttu-id="a684a-120">Określa adres IP wirtualnego urządzenia, które dodajesz do sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a684a-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="a684a-121">Ta trasa przekazuje pakiety na ten adres.</span><span class="sxs-lookup"><span data-stu-id="a684a-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="a684a-122">Określ ten parametr tylko wtedy, gdy określisz wartość parametru VirtualAppliance *NextHopType.*</span><span class="sxs-lookup"><span data-stu-id="a684a-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="a684a-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="a684a-123">-NextHopType</span></span>
<span data-ttu-id="a684a-124">Określa sposób przekazywania pakietów przez tę trasę.</span><span class="sxs-lookup"><span data-stu-id="a684a-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="a684a-125">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a684a-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a684a-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="a684a-126">Internet.</span></span>
<span data-ttu-id="a684a-127">Domyślna brama internetowa dostarczana przez platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="a684a-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="a684a-128">Brak.</span><span class="sxs-lookup"><span data-stu-id="a684a-128">None.</span></span>
<span data-ttu-id="a684a-129">Jeśli określisz tę wartość, trasa nie będzie przesyłać dalej pakietów.</span><span class="sxs-lookup"><span data-stu-id="a684a-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="a684a-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="a684a-130">VirtualAppliance.</span></span>
<span data-ttu-id="a684a-131">Urządzenie wirtualne, które dodajesz do swojej sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a684a-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="a684a-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="a684a-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="a684a-133">Brama wirtualnej sieci prywatnej typu serwer Azureserver-to-server.</span><span class="sxs-lookup"><span data-stu-id="a684a-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="a684a-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="a684a-134">VnetLocal.</span></span>
<span data-ttu-id="a684a-135">Lokalna sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="a684a-135">The local virtual network.</span></span>
<span data-ttu-id="a684a-136">Jeśli masz dwie podsieci: 10.1.0.0/16 i 10.2.0.0/16 w tej samej sieci wirtualnej, wybierz wartość VnetLocal dla każdej podsieci, aby przesyłać ją dalej do drugiej podsieci.</span><span class="sxs-lookup"><span data-stu-id="a684a-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="a684a-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="a684a-137">-RouteTable</span></span>
<span data-ttu-id="a684a-138">Określa tabelę trasy, z którą jest skojarzona ta trasa.</span><span class="sxs-lookup"><span data-stu-id="a684a-138">Specifies the route table with which this route is associated.</span></span>

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

### <span data-ttu-id="a684a-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a684a-139">-Confirm</span></span>
<span data-ttu-id="a684a-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a684a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a684a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a684a-141">-WhatIf</span></span>
<span data-ttu-id="a684a-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a684a-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a684a-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a684a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a684a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a684a-144">CommonParameters</span></span>
<span data-ttu-id="a684a-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a684a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a684a-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a684a-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a684a-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a684a-147">INPUTS</span></span>

### <span data-ttu-id="a684a-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="a684a-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="a684a-149">System.String</span><span class="sxs-lookup"><span data-stu-id="a684a-149">System.String</span></span>

## <span data-ttu-id="a684a-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a684a-150">OUTPUTS</span></span>

### <span data-ttu-id="a684a-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="a684a-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="a684a-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a684a-152">NOTES</span></span>

## <span data-ttu-id="a684a-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a684a-153">RELATED LINKS</span></span>

[<span data-ttu-id="a684a-154">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a684a-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="a684a-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a684a-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="a684a-156">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a684a-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="a684a-157">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a684a-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)


