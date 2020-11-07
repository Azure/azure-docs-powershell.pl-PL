---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
ms.openlocfilehash: 10018ad3a58de005ecf5798aafaa610c4899d4d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719411"
---
# <span data-ttu-id="68c07-101">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="68c07-101">Add-AzureRmRouteConfig</span></span>

## <span data-ttu-id="68c07-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68c07-102">SYNOPSIS</span></span>
<span data-ttu-id="68c07-103">Umożliwia dodanie trasy do tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="68c07-103">Adds a route to a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68c07-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68c07-104">SYNTAX</span></span>

```
Add-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>]
 [-NextHopType <String>] [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68c07-105">Opis</span><span class="sxs-lookup"><span data-stu-id="68c07-105">DESCRIPTION</span></span>
<span data-ttu-id="68c07-106">Polecenie cmdlet **Add-AzureRmRouteConfig** umożliwia dodanie trasy do tabeli routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="68c07-106">The **Add-AzureRmRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="68c07-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68c07-107">EXAMPLES</span></span>

### <span data-ttu-id="68c07-108">Przykład 1. Dodawanie trasy do tabeli tras</span><span class="sxs-lookup"><span data-stu-id="68c07-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzureRmRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="68c07-109">Pierwsze polecenie pobiera tabelę tras o nazwie RouteTable01 przy użyciu polecenia cmdlet Get-AzureRmRouteTable.</span><span class="sxs-lookup"><span data-stu-id="68c07-109">The first command gets a route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="68c07-110">Polecenie zapisuje tabelę w zmiennej $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="68c07-110">The command stores the table in the $RouteTable variable.</span></span>
<span data-ttu-id="68c07-111">Drugie polecenie dodaje trasę o nazwie Route13 do tabeli tras przechowywanej w $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="68c07-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="68c07-112">Ta trasa przekazuje pakiety do lokalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="68c07-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="68c07-113">Przykład 2: Dodawanie trasy do tabeli tras za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="68c07-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
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

<span data-ttu-id="68c07-114">To polecenie pobiera tabelę tras o nazwie RouteTable01 przy użyciu polecenia **Get-AzureRmRouteTable**.</span><span class="sxs-lookup"><span data-stu-id="68c07-114">This command gets the route table named RouteTable01 by using **Get-AzureRmRouteTable**.</span></span>
<span data-ttu-id="68c07-115">Polecenie przekazuje tę tabelę do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="68c07-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="68c07-116">Bieżące polecenie cmdlet umożliwia dodanie trasy o nazwie Route02, a następnie przekazanie wyniku do polecenia cmdlet **Set-AzureRmRouteTable** , które powoduje zaktualizowanie tabeli w celu odzwierciedlenia wprowadzonych zmian.</span><span class="sxs-lookup"><span data-stu-id="68c07-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="68c07-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68c07-117">PARAMETERS</span></span>

### <span data-ttu-id="68c07-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="68c07-118">-AddressPrefix</span></span>
<span data-ttu-id="68c07-119">Określa miejsce docelowe w formacie CIDR (Classless międzydomain Routing), do którego jest stosowana trasa.</span><span class="sxs-lookup"><span data-stu-id="68c07-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="68c07-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68c07-120">-DefaultProfile</span></span>
<span data-ttu-id="68c07-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="68c07-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68c07-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="68c07-122">-Name</span></span>
<span data-ttu-id="68c07-123">Określa nazwę trasy, którą należy dodać do tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="68c07-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="68c07-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="68c07-124">-NextHopIpAddress</span></span>
<span data-ttu-id="68c07-125">Określa adres IP urządzenia wirtualnego, które zostało dodane do sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="68c07-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="68c07-126">Ta trasa przekazuje pakiety na ten adres.</span><span class="sxs-lookup"><span data-stu-id="68c07-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="68c07-127">Ten parametr należy określić tylko wtedy, gdy dla parametru *NextHopType* określono wartość VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="68c07-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="68c07-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="68c07-128">-NextHopType</span></span>
<span data-ttu-id="68c07-129">Określa, jak ta trasa przekazuje pakiety dalej.</span><span class="sxs-lookup"><span data-stu-id="68c07-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="68c07-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="68c07-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68c07-131">Internetowe.</span><span class="sxs-lookup"><span data-stu-id="68c07-131">Internet.</span></span>
<span data-ttu-id="68c07-132">Domyślna Brama internetowa oferowana przez usługę Azure.</span><span class="sxs-lookup"><span data-stu-id="68c07-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="68c07-133">Znaleziono.</span><span class="sxs-lookup"><span data-stu-id="68c07-133">None.</span></span>
<span data-ttu-id="68c07-134">Jeśli określisz tę wartość, trasa nie przesyła dalej pakietów.</span><span class="sxs-lookup"><span data-stu-id="68c07-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="68c07-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="68c07-135">VirtualAppliance.</span></span>
<span data-ttu-id="68c07-136">Urządzenie wirtualne dodane do sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="68c07-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="68c07-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="68c07-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="68c07-138">Brama wirtualnej sieci prywatnej w usłudze Azure Server-to-Server.</span><span class="sxs-lookup"><span data-stu-id="68c07-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="68c07-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="68c07-139">VnetLocal.</span></span>
<span data-ttu-id="68c07-140">Lokalna sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="68c07-140">The local virtual network.</span></span>
<span data-ttu-id="68c07-141">Jeśli masz dwie podsieci, 10.1.0.0/16 i 10.2.0.0/16 w tej samej sieci wirtualnej, wybierz wartość VnetLocal dla każdej podsieci, aby przekazać ją do innej podsieci.</span><span class="sxs-lookup"><span data-stu-id="68c07-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="68c07-142">-Routeing</span><span class="sxs-lookup"><span data-stu-id="68c07-142">-RouteTable</span></span>
<span data-ttu-id="68c07-143">Określa tabelę tras, z którą to polecenie cmdlet dodaje trasę.</span><span class="sxs-lookup"><span data-stu-id="68c07-143">Specifies the route table to which this cmdlet adds a route.</span></span>

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

### <span data-ttu-id="68c07-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68c07-144">-Confirm</span></span>
<span data-ttu-id="68c07-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68c07-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68c07-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68c07-146">-WhatIf</span></span>
<span data-ttu-id="68c07-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68c07-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68c07-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="68c07-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68c07-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68c07-149">CommonParameters</span></span>
<span data-ttu-id="68c07-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68c07-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68c07-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68c07-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68c07-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68c07-152">INPUTS</span></span>

### <span data-ttu-id="68c07-153">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="68c07-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="68c07-154">System. String</span><span class="sxs-lookup"><span data-stu-id="68c07-154">System.String</span></span>

## <span data-ttu-id="68c07-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68c07-155">OUTPUTS</span></span>

### <span data-ttu-id="68c07-156">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="68c07-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="68c07-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68c07-157">NOTES</span></span>

## <span data-ttu-id="68c07-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68c07-158">RELATED LINKS</span></span>

[<span data-ttu-id="68c07-159">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="68c07-159">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="68c07-160">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="68c07-160">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="68c07-161">Nowe — AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="68c07-161">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="68c07-162">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="68c07-162">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="68c07-163">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="68c07-163">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)

[<span data-ttu-id="68c07-164">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="68c07-164">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


