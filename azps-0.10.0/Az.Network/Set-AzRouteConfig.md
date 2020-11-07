---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: 58adfcb04fef8822624669f8a723de5a524ae3aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892738"
---
# <span data-ttu-id="1776a-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1776a-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="1776a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1776a-102">SYNOPSIS</span></span>
<span data-ttu-id="1776a-103">Ustawia stan celu dla trasy.</span><span class="sxs-lookup"><span data-stu-id="1776a-103">Sets the goal state for a route.</span></span>

## <span data-ttu-id="1776a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1776a-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1776a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1776a-105">DESCRIPTION</span></span>
<span data-ttu-id="1776a-106">Polecenie cmdlet **Set-AzRouteConfig** ustawia stan celu trasy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1776a-106">The **Set-AzRouteConfig** cmdlet sets the goal state for an Azure route.</span></span>

## <span data-ttu-id="1776a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1776a-107">EXAMPLES</span></span>

### <span data-ttu-id="1776a-108">Przykład 1. Modyfikowanie trasy</span><span class="sxs-lookup"><span data-stu-id="1776a-108">Example 1: Modify a route</span></span>
```
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

<span data-ttu-id="1776a-109">To polecenie pobiera tabelę tras o nazwie RouteTable01 przy użyciu polecenia cmdlet Get-AzRouteTable.</span><span class="sxs-lookup"><span data-stu-id="1776a-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="1776a-110">Polecenie przekazuje tę tabelę do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="1776a-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1776a-111">Bieżące polecenie cmdlet powoduje modyfikację trasy o nazwie Route02, a następnie przekazanie wyniku do polecenia cmdlet **Set-AzRouteTable** , które powoduje zaktualizowanie tabeli w celu odzwierciedlenia wprowadzonych zmian.</span><span class="sxs-lookup"><span data-stu-id="1776a-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="1776a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1776a-112">PARAMETERS</span></span>

### <span data-ttu-id="1776a-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1776a-113">-AddressPrefix</span></span>
<span data-ttu-id="1776a-114">Określa miejsce docelowe w formacie CIDR (Classless międzydomain Routing), do którego jest stosowana trasa.</span><span class="sxs-lookup"><span data-stu-id="1776a-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1776a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1776a-115">-DefaultProfile</span></span>
<span data-ttu-id="1776a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1776a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1776a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1776a-117">-Name</span></span>
<span data-ttu-id="1776a-118">Określa nazwę trasy modyfikowanej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1776a-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1776a-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="1776a-119">-NextHopIpAddress</span></span>
<span data-ttu-id="1776a-120">Określa adres IP urządzenia wirtualnego, które zostało dodane do sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1776a-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="1776a-121">Ta trasa przekazuje pakiety na ten adres.</span><span class="sxs-lookup"><span data-stu-id="1776a-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="1776a-122">Ten parametr należy określić tylko wtedy, gdy dla parametru *NextHopType* określono wartość VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="1776a-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1776a-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="1776a-123">-NextHopType</span></span>
<span data-ttu-id="1776a-124">Określa, jak ta trasa przekazuje pakiety dalej.</span><span class="sxs-lookup"><span data-stu-id="1776a-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="1776a-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1776a-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1776a-126">Internetowe.</span><span class="sxs-lookup"><span data-stu-id="1776a-126">Internet.</span></span>
<span data-ttu-id="1776a-127">Domyślna Brama internetowa oferowana przez usługę Azure.</span><span class="sxs-lookup"><span data-stu-id="1776a-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="1776a-128">Znaleziono.</span><span class="sxs-lookup"><span data-stu-id="1776a-128">None.</span></span>
<span data-ttu-id="1776a-129">Jeśli określisz tę wartość, trasa nie przesyła dalej pakietów.</span><span class="sxs-lookup"><span data-stu-id="1776a-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="1776a-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="1776a-130">VirtualAppliance.</span></span>
<span data-ttu-id="1776a-131">Urządzenie wirtualne dodane do sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1776a-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="1776a-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="1776a-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="1776a-133">Brama wirtualnej sieci prywatnej Azureserver-to-Server.</span><span class="sxs-lookup"><span data-stu-id="1776a-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="1776a-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="1776a-134">VnetLocal.</span></span>
<span data-ttu-id="1776a-135">Lokalna sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="1776a-135">The local virtual network.</span></span>
<span data-ttu-id="1776a-136">Jeśli masz dwie podsieci, 10.1.0.0/16 i 10.2.0.0/16 w tej samej sieci wirtualnej, wybierz wartość VnetLocal dla każdej podsieci, aby przekazać ją do innej podsieci.</span><span class="sxs-lookup"><span data-stu-id="1776a-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1776a-137">-Routeing</span><span class="sxs-lookup"><span data-stu-id="1776a-137">-RouteTable</span></span>
<span data-ttu-id="1776a-138">Określa tabelę tras, z którą jest skojarzona ta trasa.</span><span class="sxs-lookup"><span data-stu-id="1776a-138">Specifies the route table with which this route is associated.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1776a-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1776a-139">-Confirm</span></span>
<span data-ttu-id="1776a-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1776a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1776a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1776a-141">-WhatIf</span></span>
<span data-ttu-id="1776a-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1776a-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1776a-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1776a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1776a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1776a-144">CommonParameters</span></span>
<span data-ttu-id="1776a-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1776a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1776a-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1776a-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1776a-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1776a-147">INPUTS</span></span>

### <span data-ttu-id="1776a-148">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="1776a-148">PSRouteTable</span></span>
<span data-ttu-id="1776a-149">Parametr "routed" przyjmuje wartość typu "PSRouteTable" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="1776a-149">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="1776a-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1776a-150">OUTPUTS</span></span>

### <span data-ttu-id="1776a-151">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="1776a-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="1776a-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1776a-152">NOTES</span></span>

## <span data-ttu-id="1776a-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1776a-153">RELATED LINKS</span></span>

[<span data-ttu-id="1776a-154">Dodaj-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1776a-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="1776a-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1776a-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="1776a-156">Nowe — AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1776a-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="1776a-157">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1776a-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)


