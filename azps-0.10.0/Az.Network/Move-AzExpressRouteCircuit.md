---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: ffa10dca752adaeebbdd6fbf92a6a16b094a3085
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890598"
---
# <span data-ttu-id="bcd36-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bcd36-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="bcd36-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bcd36-102">SYNOPSIS</span></span>
<span data-ttu-id="bcd36-103">Umożliwia przeniesienie obwodu ExpressRoute z modelu klasycznego wdrożenia do modelu wdrażania Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="bcd36-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="bcd36-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bcd36-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcd36-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bcd36-105">DESCRIPTION</span></span>
<span data-ttu-id="bcd36-106">Polecenie cmdlet **Move-AzExpressRouteCircuit** powoduje przeniesienie obwodu ExpressRoute z klasycznego modelu wdrożenia do modelu wdrożenia Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="bcd36-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="bcd36-107">Po przeniesieniu obwód ExpressRoute zachowuje się i działa tak, jak w przypadku wszystkich innych obwodów ExpressRoute utworzonych w modelu wdrażania Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="bcd36-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="bcd36-108">Łącza obwodów, sieci wirtualnych i bramy sieci VPN nie są przenoszone przez tę operację.</span><span class="sxs-lookup"><span data-stu-id="bcd36-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="bcd36-109">Te zasoby muszą być konfigurowane ponownie po przeniesieniu.</span><span class="sxs-lookup"><span data-stu-id="bcd36-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="bcd36-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bcd36-110">EXAMPLES</span></span>

### <span data-ttu-id="bcd36-111">Przykład 1: przenoszenie obwodu ExpressRoute do modelu wdrożenia Menedżera zasobów</span><span class="sxs-lookup"><span data-stu-id="bcd36-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="bcd36-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bcd36-112">PARAMETERS</span></span>

### <span data-ttu-id="bcd36-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcd36-113">-AsJob</span></span>
<span data-ttu-id="bcd36-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bcd36-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bcd36-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcd36-115">-DefaultProfile</span></span>
<span data-ttu-id="bcd36-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bcd36-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcd36-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bcd36-117">-Force</span></span>
<span data-ttu-id="bcd36-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bcd36-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bcd36-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bcd36-119">-Location</span></span>
<span data-ttu-id="bcd36-120">Nazwa lokalizacji platformy Azure, w której znajduje się obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bcd36-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="bcd36-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bcd36-121">-Name</span></span>
<span data-ttu-id="bcd36-122">Nazwa obwodu ExpressRoute, który ma zostać przesunięty.</span><span class="sxs-lookup"><span data-stu-id="bcd36-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="bcd36-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcd36-123">-ResourceGroupName</span></span>
<span data-ttu-id="bcd36-124">Nazwa grupy zasobów, która będzie zawierać przenoszony obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bcd36-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="bcd36-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="bcd36-125">-ServiceKey</span></span>
<span data-ttu-id="bcd36-126">Klucz usługi wykorzystywany przez obwód ExpressRoute w klasycznym modelu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="bcd36-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="bcd36-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="bcd36-127">-Tag</span></span>
<span data-ttu-id="bcd36-128">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="bcd36-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bcd36-129">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="bcd36-129">For example:</span></span>

<span data-ttu-id="bcd36-130">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="bcd36-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bcd36-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bcd36-131">-Confirm</span></span>
<span data-ttu-id="bcd36-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcd36-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcd36-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcd36-133">-WhatIf</span></span>
<span data-ttu-id="bcd36-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcd36-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcd36-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bcd36-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcd36-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcd36-136">CommonParameters</span></span>
<span data-ttu-id="bcd36-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcd36-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcd36-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcd36-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcd36-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bcd36-139">INPUTS</span></span>

## <span data-ttu-id="bcd36-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bcd36-140">OUTPUTS</span></span>

### <span data-ttu-id="bcd36-141">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bcd36-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="bcd36-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bcd36-142">NOTES</span></span>

## <span data-ttu-id="bcd36-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bcd36-143">RELATED LINKS</span></span>

[<span data-ttu-id="bcd36-144">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bcd36-144">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="bcd36-145">Nowe — AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bcd36-145">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="bcd36-146">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bcd36-146">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="bcd36-147">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bcd36-147">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
