---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
ms.openlocfilehash: bb51d5bfb1ccc81aa10c7aecc4d7a255fc0f60d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543271"
---
# <span data-ttu-id="0c30f-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0c30f-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="0c30f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c30f-102">SYNOPSIS</span></span>
<span data-ttu-id="0c30f-103">Tworzy trasę dla tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="0c30f-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c30f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c30f-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig -Name <String> [-AddressPrefix <String>] -NextHopType <String>
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c30f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0c30f-105">DESCRIPTION</span></span>
<span data-ttu-id="0c30f-106">Polecenie cmdlet **New-AzureRmRouteConfig** tworzy trasę dla tabeli routingu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0c30f-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="0c30f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c30f-107">EXAMPLES</span></span>

### <span data-ttu-id="0c30f-108">Przykład 1. Tworzenie trasy</span><span class="sxs-lookup"><span data-stu-id="0c30f-108">Example 1: Create a route</span></span>
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

<span data-ttu-id="0c30f-109">Pierwsze polecenie tworzy trasę o nazwie Route07, a następnie zapisuje ją w zmiennej $Route.</span><span class="sxs-lookup"><span data-stu-id="0c30f-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="0c30f-110">Ta trasa przekazuje pakiety do lokalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0c30f-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="0c30f-111">Drugie polecenie wyświetla właściwości trasy.</span><span class="sxs-lookup"><span data-stu-id="0c30f-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="0c30f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c30f-112">PARAMETERS</span></span>

### <span data-ttu-id="0c30f-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0c30f-113">-AddressPrefix</span></span>
<span data-ttu-id="0c30f-114">Określa miejsce docelowe w formacie CIDR (Classless międzydomain Routing), do którego jest stosowana trasa.</span><span class="sxs-lookup"><span data-stu-id="0c30f-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="0c30f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0c30f-115">-Name</span></span>
<span data-ttu-id="0c30f-116">Określa nazwę trasy.</span><span class="sxs-lookup"><span data-stu-id="0c30f-116">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="0c30f-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="0c30f-117">-NextHopIpAddress</span></span>
<span data-ttu-id="0c30f-118">Określa adres IP urządzenia wirtualnego, które zostało dodane do sieci Azurevirtual.</span><span class="sxs-lookup"><span data-stu-id="0c30f-118">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="0c30f-119">Ta trasa przekazuje pakiety na ten adres.</span><span class="sxs-lookup"><span data-stu-id="0c30f-119">This route forwards packets to that address.</span></span>
<span data-ttu-id="0c30f-120">Ten parametr należy określić tylko wtedy, gdy dla parametru *NextHopType* określono wartość VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="0c30f-120">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="0c30f-121">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="0c30f-121">-NextHopType</span></span>
<span data-ttu-id="0c30f-122">Określa, jak ta trasa przekazuje pakiety dalej.</span><span class="sxs-lookup"><span data-stu-id="0c30f-122">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="0c30f-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0c30f-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0c30f-124">Internetowe.</span><span class="sxs-lookup"><span data-stu-id="0c30f-124">Internet.</span></span>
<span data-ttu-id="0c30f-125">Domyślna Brama internetowa oferowana przez usługę Azure.</span><span class="sxs-lookup"><span data-stu-id="0c30f-125">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="0c30f-126">Znaleziono.</span><span class="sxs-lookup"><span data-stu-id="0c30f-126">None.</span></span>
<span data-ttu-id="0c30f-127">Jeśli określisz tę wartość, trasa nie przesyła dalej pakietów.</span><span class="sxs-lookup"><span data-stu-id="0c30f-127">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="0c30f-128">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="0c30f-128">VirtualAppliance.</span></span>
<span data-ttu-id="0c30f-129">Urządzenie wirtualne dodane do sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0c30f-129">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="0c30f-130">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="0c30f-130">VirtualNetworkGateway.</span></span>
<span data-ttu-id="0c30f-131">Brama wirtualnej sieci prywatnej w usłudze Azure Server-to-Server.</span><span class="sxs-lookup"><span data-stu-id="0c30f-131">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="0c30f-132">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="0c30f-132">VnetLocal.</span></span>
<span data-ttu-id="0c30f-133">Lokalna sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="0c30f-133">The local virtual network.</span></span>
<span data-ttu-id="0c30f-134">Jeśli masz dwie podsieci, 10.1.0.0/16 i 10.2.0.0/16 w tej samej sieci wirtualnej, wybierz wartość VnetLocal dla każdej podsieci, aby przekazać ją do innej podsieci.</span><span class="sxs-lookup"><span data-stu-id="0c30f-134">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="0c30f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c30f-135">-DefaultProfile</span></span>
<span data-ttu-id="0c30f-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c30f-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c30f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c30f-137">CommonParameters</span></span>
<span data-ttu-id="0c30f-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c30f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c30f-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c30f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c30f-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c30f-140">INPUTS</span></span>

## <span data-ttu-id="0c30f-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c30f-141">OUTPUTS</span></span>

### <span data-ttu-id="0c30f-142">Microsoft. Azure. Commands. Network. models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="0c30f-142">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="0c30f-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c30f-143">NOTES</span></span>

## <span data-ttu-id="0c30f-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c30f-144">RELATED LINKS</span></span>

[<span data-ttu-id="0c30f-145">Dodaj-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0c30f-145">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="0c30f-146">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0c30f-146">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="0c30f-147">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0c30f-147">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="0c30f-148">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0c30f-148">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


