---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: ab528e837f6f2e45db5e68430d973e0d8f019850
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899106"
---
# <span data-ttu-id="fd719-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fd719-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="fd719-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd719-102">SYNOPSIS</span></span>
<span data-ttu-id="fd719-103">Tworzy trasę dla tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="fd719-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd719-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd719-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig [-AddressPrefix <String>] [-NextHopType <String>] [-NextHopIpAddress <String>]
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd719-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fd719-105">DESCRIPTION</span></span>
<span data-ttu-id="fd719-106">Polecenie cmdlet **New-AzureRmRouteConfig** tworzy trasę dla tabeli routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fd719-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="fd719-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd719-107">EXAMPLES</span></span>

### <span data-ttu-id="fd719-108">Przykład 1. Tworzenie trasy</span><span class="sxs-lookup"><span data-stu-id="fd719-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="fd719-109">Pierwsze polecenie tworzy trasę o nazwie Route07, a następnie zapisuje ją w zmiennej $Route.</span><span class="sxs-lookup"><span data-stu-id="fd719-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="fd719-110">Ta trasa przekazuje pakiety do lokalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fd719-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="fd719-111">Drugie polecenie wyświetla właściwości trasy.</span><span class="sxs-lookup"><span data-stu-id="fd719-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="fd719-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd719-112">PARAMETERS</span></span>

### <span data-ttu-id="fd719-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fd719-113">-AddressPrefix</span></span>
<span data-ttu-id="fd719-114">Określa miejsce docelowe w formacie CIDR (Classless międzydomain Routing), do którego jest stosowana trasa.</span><span class="sxs-lookup"><span data-stu-id="fd719-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="fd719-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd719-115">-DefaultProfile</span></span>
<span data-ttu-id="fd719-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd719-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd719-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd719-117">-Name</span></span>
<span data-ttu-id="fd719-118">Określa nazwę trasy.</span><span class="sxs-lookup"><span data-stu-id="fd719-118">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="fd719-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="fd719-119">-NextHopIpAddress</span></span>
<span data-ttu-id="fd719-120">Określa adres IP urządzenia wirtualnego, które zostało dodane do sieci Azurevirtual.</span><span class="sxs-lookup"><span data-stu-id="fd719-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="fd719-121">Ta trasa przekazuje pakiety na ten adres.</span><span class="sxs-lookup"><span data-stu-id="fd719-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="fd719-122">Ten parametr należy określić tylko wtedy, gdy dla parametru *NextHopType* określono wartość VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="fd719-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="fd719-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="fd719-123">-NextHopType</span></span>
<span data-ttu-id="fd719-124">Określa, jak ta trasa przekazuje pakiety dalej.</span><span class="sxs-lookup"><span data-stu-id="fd719-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="fd719-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fd719-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fd719-126">Internetowe.</span><span class="sxs-lookup"><span data-stu-id="fd719-126">Internet.</span></span>
<span data-ttu-id="fd719-127">Domyślna Brama internetowa oferowana przez usługę Azure.</span><span class="sxs-lookup"><span data-stu-id="fd719-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="fd719-128">Znaleziono.</span><span class="sxs-lookup"><span data-stu-id="fd719-128">None.</span></span>
<span data-ttu-id="fd719-129">Jeśli określisz tę wartość, trasa nie przesyła dalej pakietów.</span><span class="sxs-lookup"><span data-stu-id="fd719-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="fd719-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="fd719-130">VirtualAppliance.</span></span>
<span data-ttu-id="fd719-131">Urządzenie wirtualne dodane do sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fd719-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="fd719-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="fd719-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="fd719-133">Brama wirtualnej sieci prywatnej w usłudze Azure Server-to-Server.</span><span class="sxs-lookup"><span data-stu-id="fd719-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="fd719-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="fd719-134">VnetLocal.</span></span>
<span data-ttu-id="fd719-135">Lokalna sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="fd719-135">The local virtual network.</span></span>
<span data-ttu-id="fd719-136">Jeśli masz dwie podsieci, 10.1.0.0/16 i 10.2.0.0/16 w tej samej sieci wirtualnej, wybierz wartość VnetLocal dla każdej podsieci, aby przekazać ją do innej podsieci.</span><span class="sxs-lookup"><span data-stu-id="fd719-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="fd719-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd719-137">-Confirm</span></span>
<span data-ttu-id="fd719-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd719-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd719-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd719-139">-WhatIf</span></span>
<span data-ttu-id="fd719-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd719-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd719-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fd719-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd719-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd719-142">CommonParameters</span></span>
<span data-ttu-id="fd719-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd719-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd719-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd719-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd719-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd719-145">INPUTS</span></span>

## <span data-ttu-id="fd719-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd719-146">OUTPUTS</span></span>

### <span data-ttu-id="fd719-147">Microsoft. Azure. Commands. Network. models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="fd719-147">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="fd719-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd719-148">NOTES</span></span>

## <span data-ttu-id="fd719-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd719-149">RELATED LINKS</span></span>

[<span data-ttu-id="fd719-150">Dodaj-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fd719-150">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="fd719-151">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fd719-151">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="fd719-152">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fd719-152">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="fd719-153">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fd719-153">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


