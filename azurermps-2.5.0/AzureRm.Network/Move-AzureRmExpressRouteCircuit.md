---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/move-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: bd4d51c03d26a1fb99b04c8b5245850512c2c940
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898318"
---
# <span data-ttu-id="15bfb-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="15bfb-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="15bfb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="15bfb-103">Umożliwia przeniesienie obwodu ExpressRoute z modelu klasycznego wdrożenia do modelu wdrażania Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="15bfb-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15bfb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15bfb-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15bfb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="15bfb-105">DESCRIPTION</span></span>
<span data-ttu-id="15bfb-106">Polecenie cmdlet **Move-AzureRmExpressRouteCircuit** powoduje przeniesienie obwodu ExpressRoute z klasycznego modelu wdrożenia do modelu wdrożenia Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="15bfb-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="15bfb-107">Po przeniesieniu obwód ExpressRoute zachowuje się i działa tak, jak w przypadku wszystkich innych obwodów ExpressRoute utworzonych w modelu wdrażania Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="15bfb-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="15bfb-108">Łącza obwodów, sieci wirtualnych i bramy sieci VPN nie są przenoszone przez tę operację.</span><span class="sxs-lookup"><span data-stu-id="15bfb-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="15bfb-109">Te zasoby muszą być konfigurowane ponownie po przeniesieniu.</span><span class="sxs-lookup"><span data-stu-id="15bfb-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="15bfb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15bfb-110">EXAMPLES</span></span>

### <span data-ttu-id="15bfb-111">Przykład 1: przenoszenie obwodu ExpressRoute do modelu wdrożenia Menedżera zasobów</span><span class="sxs-lookup"><span data-stu-id="15bfb-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="15bfb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15bfb-112">PARAMETERS</span></span>

### <span data-ttu-id="15bfb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15bfb-113">-AsJob</span></span>
<span data-ttu-id="15bfb-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="15bfb-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bfb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15bfb-115">-DefaultProfile</span></span>
<span data-ttu-id="15bfb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="15bfb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15bfb-117">-Force</span><span class="sxs-lookup"><span data-stu-id="15bfb-117">-Force</span></span>
<span data-ttu-id="15bfb-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="15bfb-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bfb-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="15bfb-119">-Location</span></span>
<span data-ttu-id="15bfb-120">Nazwa lokalizacji platformy Azure, w której znajduje się obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="15bfb-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bfb-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="15bfb-121">-Name</span></span>
<span data-ttu-id="15bfb-122">Nazwa obwodu ExpressRoute, który ma zostać przesunięty.</span><span class="sxs-lookup"><span data-stu-id="15bfb-122">The name of the ExpressRoute circuit to be moved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bfb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15bfb-123">-ResourceGroupName</span></span>
<span data-ttu-id="15bfb-124">Nazwa grupy zasobów, która będzie zawierać przenoszony obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="15bfb-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bfb-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="15bfb-125">-ServiceKey</span></span>
<span data-ttu-id="15bfb-126">Klucz usługi wykorzystywany przez obwód ExpressRoute w klasycznym modelu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="15bfb-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bfb-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="15bfb-127">-Tag</span></span>
<span data-ttu-id="15bfb-128">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="15bfb-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="15bfb-129">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="15bfb-129">For example:</span></span>

<span data-ttu-id="15bfb-130">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="15bfb-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bfb-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="15bfb-131">-Confirm</span></span>
<span data-ttu-id="15bfb-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15bfb-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bfb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15bfb-133">-WhatIf</span></span>
<span data-ttu-id="15bfb-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15bfb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15bfb-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="15bfb-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bfb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15bfb-136">CommonParameters</span></span>
<span data-ttu-id="15bfb-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15bfb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15bfb-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15bfb-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15bfb-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15bfb-139">INPUTS</span></span>

## <span data-ttu-id="15bfb-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15bfb-140">OUTPUTS</span></span>

### <span data-ttu-id="15bfb-141">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="15bfb-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="15bfb-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15bfb-142">NOTES</span></span>

## <span data-ttu-id="15bfb-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15bfb-143">RELATED LINKS</span></span>

[<span data-ttu-id="15bfb-144">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="15bfb-144">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="15bfb-145">Nowe — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="15bfb-145">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="15bfb-146">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="15bfb-146">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="15bfb-147">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="15bfb-147">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
