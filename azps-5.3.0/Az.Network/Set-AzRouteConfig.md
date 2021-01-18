---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: ca7335abfd8fe2dc9591dcb7d96fb6ca71dda4fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503151"
---
# <span data-ttu-id="11854-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="11854-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="11854-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11854-102">SYNOPSIS</span></span>
<span data-ttu-id="11854-103">Umożliwia zaktualizowanie konfiguracji trasy dla tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="11854-103">Updates a route configuration for a route table.</span></span>

## <span data-ttu-id="11854-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11854-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11854-105">Opis</span><span class="sxs-lookup"><span data-stu-id="11854-105">DESCRIPTION</span></span>
<span data-ttu-id="11854-106">Polecenie cmdlet **Set-AzRouteConfig** umożliwia zaktualizowanie konfiguracji trasy dla tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="11854-106">The **Set-AzRouteConfig** cmdlet updates a route configuration for a route table.</span></span>

## <span data-ttu-id="11854-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11854-107">EXAMPLES</span></span>

### <span data-ttu-id="11854-108">Przykład 1. Modyfikowanie trasy</span><span class="sxs-lookup"><span data-stu-id="11854-108">Example 1: Modify a route</span></span>
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

<span data-ttu-id="11854-109">To polecenie pobiera tabelę tras o nazwie RouteTable01 przy użyciu polecenia cmdlet Get-AzRouteTable.</span><span class="sxs-lookup"><span data-stu-id="11854-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="11854-110">Polecenie przekazuje tę tabelę do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="11854-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="11854-111">Bieżące polecenie cmdlet powoduje modyfikację trasy o nazwie Route02, a następnie przekazanie wyniku do polecenia cmdlet **Set-AzRouteTable** , które powoduje zaktualizowanie tabeli w celu odzwierciedlenia wprowadzonych zmian.</span><span class="sxs-lookup"><span data-stu-id="11854-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="11854-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11854-112">PARAMETERS</span></span>

### <span data-ttu-id="11854-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="11854-113">-AddressPrefix</span></span>
<span data-ttu-id="11854-114">Określa miejsce docelowe w formacie CIDR (Classless międzydomain Routing), do którego jest stosowana trasa.</span><span class="sxs-lookup"><span data-stu-id="11854-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="11854-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11854-115">-DefaultProfile</span></span>
<span data-ttu-id="11854-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11854-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11854-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11854-117">-Name</span></span>
<span data-ttu-id="11854-118">Określa nazwę trasy modyfikowanej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11854-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="11854-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="11854-119">-NextHopIpAddress</span></span>
<span data-ttu-id="11854-120">Określa adres IP urządzenia wirtualnego, które zostało dodane do sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11854-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="11854-121">Ta trasa przekazuje pakiety na ten adres.</span><span class="sxs-lookup"><span data-stu-id="11854-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="11854-122">Ten parametr należy określić tylko wtedy, gdy dla parametru *NextHopType* określono wartość VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="11854-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="11854-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="11854-123">-NextHopType</span></span>
<span data-ttu-id="11854-124">Określa, jak ta trasa przekazuje pakiety dalej.</span><span class="sxs-lookup"><span data-stu-id="11854-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="11854-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="11854-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="11854-126">Internetowe.</span><span class="sxs-lookup"><span data-stu-id="11854-126">Internet.</span></span>
<span data-ttu-id="11854-127">Domyślna Brama internetowa oferowana przez usługę Azure.</span><span class="sxs-lookup"><span data-stu-id="11854-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="11854-128">Znaleziono.</span><span class="sxs-lookup"><span data-stu-id="11854-128">None.</span></span>
<span data-ttu-id="11854-129">Jeśli określisz tę wartość, trasa nie przesyła dalej pakietów.</span><span class="sxs-lookup"><span data-stu-id="11854-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="11854-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="11854-130">VirtualAppliance.</span></span>
<span data-ttu-id="11854-131">Urządzenie wirtualne dodane do sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11854-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="11854-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="11854-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="11854-133">Brama wirtualnej sieci prywatnej Azureserver-to-Server.</span><span class="sxs-lookup"><span data-stu-id="11854-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="11854-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="11854-134">VnetLocal.</span></span>
<span data-ttu-id="11854-135">Lokalna sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="11854-135">The local virtual network.</span></span>
<span data-ttu-id="11854-136">Jeśli masz dwie podsieci, 10.1.0.0/16 i 10.2.0.0/16 w tej samej sieci wirtualnej, wybierz wartość VnetLocal dla każdej podsieci, aby przekazać ją do innej podsieci.</span><span class="sxs-lookup"><span data-stu-id="11854-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="11854-137">-Routeing</span><span class="sxs-lookup"><span data-stu-id="11854-137">-RouteTable</span></span>
<span data-ttu-id="11854-138">Określa tabelę tras, z którą jest skojarzona ta trasa.</span><span class="sxs-lookup"><span data-stu-id="11854-138">Specifies the route table with which this route is associated.</span></span>

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

### <span data-ttu-id="11854-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11854-139">-Confirm</span></span>
<span data-ttu-id="11854-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11854-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11854-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11854-141">-WhatIf</span></span>
<span data-ttu-id="11854-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11854-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11854-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="11854-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11854-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11854-144">CommonParameters</span></span>
<span data-ttu-id="11854-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11854-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11854-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11854-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11854-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11854-147">INPUTS</span></span>

### <span data-ttu-id="11854-148">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="11854-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="11854-149">System. String</span><span class="sxs-lookup"><span data-stu-id="11854-149">System.String</span></span>

## <span data-ttu-id="11854-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11854-150">OUTPUTS</span></span>

### <span data-ttu-id="11854-151">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="11854-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="11854-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11854-152">NOTES</span></span>

## <span data-ttu-id="11854-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11854-153">RELATED LINKS</span></span>

[<span data-ttu-id="11854-154">Dodaj-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="11854-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="11854-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="11854-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="11854-156">Nowe — AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="11854-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="11854-157">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="11854-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)


