---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
ms.openlocfilehash: a86e5346078bd1a8c9be924cdeac3b94fab907dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543208"
---
# <span data-ttu-id="10287-101">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="10287-101">Set-AzureRmRouteConfig</span></span>

## <span data-ttu-id="10287-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10287-102">SYNOPSIS</span></span>
<span data-ttu-id="10287-103">Ustawia stan celu dla trasy.</span><span class="sxs-lookup"><span data-stu-id="10287-103">Sets the goal state for a route.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10287-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10287-104">SYNTAX</span></span>

```
Set-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-AddressPrefix <String>]
 -NextHopType <String> [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10287-105">Opis</span><span class="sxs-lookup"><span data-stu-id="10287-105">DESCRIPTION</span></span>
<span data-ttu-id="10287-106">Polecenie cmdlet **Set-AzureRmRouteConfig** ustawia stan celu trasy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="10287-106">The **Set-AzureRmRouteConfig** cmdlet sets the goal state for an Azure route.</span></span>

## <span data-ttu-id="10287-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10287-107">EXAMPLES</span></span>

### <span data-ttu-id="10287-108">Przykład 1. Modyfikowanie trasy</span><span class="sxs-lookup"><span data-stu-id="10287-108">Example 1: Modify a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
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

<span data-ttu-id="10287-109">To polecenie pobiera tabelę tras o nazwie RouteTable01 przy użyciu polecenia cmdlet Get-AzureRmRouteTable.</span><span class="sxs-lookup"><span data-stu-id="10287-109">This command gets the route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="10287-110">Polecenie przekazuje tę tabelę do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="10287-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="10287-111">Bieżące polecenie cmdlet powoduje modyfikację trasy o nazwie Route02, a następnie przekazanie wyniku do polecenia cmdlet **Set-AzureRmRouteTable** , które powoduje zaktualizowanie tabeli w celu odzwierciedlenia wprowadzonych zmian.</span><span class="sxs-lookup"><span data-stu-id="10287-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="10287-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10287-112">PARAMETERS</span></span>

### <span data-ttu-id="10287-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="10287-113">-AddressPrefix</span></span>
<span data-ttu-id="10287-114">Określa miejsce docelowe w formacie CIDR (Classless międzydomain Routing), do którego jest stosowana trasa.</span><span class="sxs-lookup"><span data-stu-id="10287-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="10287-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="10287-115">-Name</span></span>
<span data-ttu-id="10287-116">Określa nazwę trasy modyfikowanej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10287-116">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="10287-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="10287-117">-NextHopIpAddress</span></span>
<span data-ttu-id="10287-118">Określa adres IP urządzenia wirtualnego, które zostało dodane do sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="10287-118">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="10287-119">Ta trasa przekazuje pakiety na ten adres.</span><span class="sxs-lookup"><span data-stu-id="10287-119">This route forwards packets to that address.</span></span>
<span data-ttu-id="10287-120">Ten parametr należy określić tylko wtedy, gdy dla parametru *NextHopType* określono wartość VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="10287-120">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="10287-121">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="10287-121">-NextHopType</span></span>
<span data-ttu-id="10287-122">Określa, jak ta trasa przekazuje pakiety dalej.</span><span class="sxs-lookup"><span data-stu-id="10287-122">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="10287-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="10287-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10287-124">Internetowe.</span><span class="sxs-lookup"><span data-stu-id="10287-124">Internet.</span></span>
<span data-ttu-id="10287-125">Domyślna Brama internetowa oferowana przez usługę Azure.</span><span class="sxs-lookup"><span data-stu-id="10287-125">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="10287-126">Znaleziono.</span><span class="sxs-lookup"><span data-stu-id="10287-126">None.</span></span>
<span data-ttu-id="10287-127">Jeśli określisz tę wartość, trasa nie przesyła dalej pakietów.</span><span class="sxs-lookup"><span data-stu-id="10287-127">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="10287-128">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="10287-128">VirtualAppliance.</span></span>
<span data-ttu-id="10287-129">Urządzenie wirtualne dodane do sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="10287-129">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="10287-130">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="10287-130">VirtualNetworkGateway.</span></span>
<span data-ttu-id="10287-131">Brama wirtualnej sieci prywatnej Azureserver-to-Server.</span><span class="sxs-lookup"><span data-stu-id="10287-131">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="10287-132">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="10287-132">VnetLocal.</span></span>
<span data-ttu-id="10287-133">Lokalna sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="10287-133">The local virtual network.</span></span>
<span data-ttu-id="10287-134">Jeśli masz dwie podsieci, 10.1.0.0/16 i 10.2.0.0/16 w tej samej sieci wirtualnej, wybierz wartość VnetLocal dla każdej podsieci, aby przekazać ją do innej podsieci.</span><span class="sxs-lookup"><span data-stu-id="10287-134">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Internet, None, VirtualAppliance, VirtualNetworkGateway, VnetLocal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10287-135">-Routeing</span><span class="sxs-lookup"><span data-stu-id="10287-135">-RouteTable</span></span>
<span data-ttu-id="10287-136">Określa tabelę tras, z którą jest skojarzona ta trasa.</span><span class="sxs-lookup"><span data-stu-id="10287-136">Specifies the route table with which this route is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10287-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10287-137">-DefaultProfile</span></span>
<span data-ttu-id="10287-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="10287-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10287-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10287-139">CommonParameters</span></span>
<span data-ttu-id="10287-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10287-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10287-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10287-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10287-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10287-142">INPUTS</span></span>

### <span data-ttu-id="10287-143">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="10287-143">PSRouteTable</span></span>
<span data-ttu-id="10287-144">Parametr "routed" przyjmuje wartość typu "PSRouteTable" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="10287-144">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="10287-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10287-145">OUTPUTS</span></span>

### <span data-ttu-id="10287-146">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="10287-146">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="10287-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10287-147">NOTES</span></span>

## <span data-ttu-id="10287-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10287-148">RELATED LINKS</span></span>

[<span data-ttu-id="10287-149">Dodaj-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="10287-149">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="10287-150">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="10287-150">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="10287-151">Nowe — AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="10287-151">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="10287-152">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="10287-152">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)


