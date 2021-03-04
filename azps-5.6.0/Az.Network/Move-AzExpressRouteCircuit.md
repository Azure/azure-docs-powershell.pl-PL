---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 6964767438fac6a1afd8da4333560f49cfe1bb44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952202"
---
# <span data-ttu-id="bd7bb-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bd7bb-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="bd7bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="bd7bb-103">Przenosi obwód usługi ExpressRoute z klasycznego modelu wdrażania do modelu wdrażania Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="bd7bb-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="bd7bb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bd7bb-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd7bb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bd7bb-105">DESCRIPTION</span></span>
<span data-ttu-id="bd7bb-106">Polecenie **cmdlet Move-AzExpressRouteCircuit** przenosi obwód usługi ExpressRoute z klasycznego modelu wdrażania do modelu wdrażania menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="bd7bb-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="bd7bb-107">Po zakończeniu przenoszenia obwód usługi ExpressRoute zachowuje się i wykonuje tak samo jak każdy inny obwód usługi ExpressRoute utworzony w modelu wdrażania menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="bd7bb-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="bd7bb-108">W ramach tej operacji nie są przenoszone linki obwodów, sieci wirtualne ani bramy VPN.</span><span class="sxs-lookup"><span data-stu-id="bd7bb-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="bd7bb-109">Te zasoby należy ponownie skonfigurować po zakończeniu przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="bd7bb-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="bd7bb-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bd7bb-110">EXAMPLES</span></span>

### <span data-ttu-id="bd7bb-111">Przykład 1. Przenoszenie obwodu usługi ExpressRoute do modelu wdrażania Menedżera zasobów</span><span class="sxs-lookup"><span data-stu-id="bd7bb-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="bd7bb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd7bb-112">PARAMETERS</span></span>

### <span data-ttu-id="bd7bb-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="bd7bb-113">-AsJob</span></span>
<span data-ttu-id="bd7bb-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bd7bb-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd7bb-115">-DefaultProfile</span></span>
<span data-ttu-id="bd7bb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd7bb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd7bb-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="bd7bb-117">-Force</span></span>
<span data-ttu-id="bd7bb-118">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bd7bb-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7bb-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bd7bb-119">-Location</span></span>
<span data-ttu-id="bd7bb-120">Nazwa lokalizacji platformy Azure, w której znajduje się obwód usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bd7bb-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7bb-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bd7bb-121">-Name</span></span>
<span data-ttu-id="bd7bb-122">Nazwa obwodu expressroute, który ma zostać przeniesiony.</span><span class="sxs-lookup"><span data-stu-id="bd7bb-122">The name of the ExpressRoute circuit to be moved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7bb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd7bb-123">-ResourceGroupName</span></span>
<span data-ttu-id="bd7bb-124">Nazwa grupy zasobów, która będzie zawierać przenoszony obwód expressRoute.</span><span class="sxs-lookup"><span data-stu-id="bd7bb-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7bb-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="bd7bb-125">-ServiceKey</span></span>
<span data-ttu-id="bd7bb-126">Klucz usługi używany przez obwód usługi ExpressRoute w klasycznym modelu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="bd7bb-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7bb-127">— Tag</span><span class="sxs-lookup"><span data-stu-id="bd7bb-127">-Tag</span></span>
<span data-ttu-id="bd7bb-128">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="bd7bb-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bd7bb-129">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="bd7bb-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7bb-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd7bb-130">-Confirm</span></span>
<span data-ttu-id="bd7bb-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bd7bb-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7bb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd7bb-132">-WhatIf</span></span>
<span data-ttu-id="bd7bb-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd7bb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd7bb-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bd7bb-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7bb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd7bb-135">CommonParameters</span></span>
<span data-ttu-id="bd7bb-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd7bb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd7bb-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd7bb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd7bb-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd7bb-138">INPUTS</span></span>

### <span data-ttu-id="bd7bb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="bd7bb-139">System.String</span></span>

### <span data-ttu-id="bd7bb-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bd7bb-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bd7bb-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd7bb-141">OUTPUTS</span></span>

### <span data-ttu-id="bd7bb-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bd7bb-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="bd7bb-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bd7bb-143">NOTES</span></span>

## <span data-ttu-id="bd7bb-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd7bb-144">RELATED LINKS</span></span>

[<span data-ttu-id="bd7bb-145">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bd7bb-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="bd7bb-146">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bd7bb-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="bd7bb-147">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bd7bb-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="bd7bb-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bd7bb-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
