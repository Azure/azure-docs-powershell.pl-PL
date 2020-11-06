---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: e4d167f98f837434018e04da91a31973acb45c8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549115"
---
# <span data-ttu-id="4ad13-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ad13-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="4ad13-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ad13-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad13-103">Umożliwia przeniesienie obwodu ExpressRoute z modelu klasycznego wdrożenia do modelu wdrażania Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ad13-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ad13-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ad13-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ad13-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4ad13-105">DESCRIPTION</span></span>
<span data-ttu-id="4ad13-106">Polecenie cmdlet **Move-AzureRmExpressRouteCircuit** powoduje przeniesienie obwodu ExpressRoute z klasycznego modelu wdrożenia do modelu wdrożenia Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ad13-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="4ad13-107">Po przeniesieniu obwód ExpressRoute zachowuje się i działa tak, jak w przypadku wszystkich innych obwodów ExpressRoute utworzonych w modelu wdrażania Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ad13-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="4ad13-108">Łącza obwodów, sieci wirtualnych i bramy sieci VPN nie są przenoszone przez tę operację.</span><span class="sxs-lookup"><span data-stu-id="4ad13-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="4ad13-109">Te zasoby muszą być konfigurowane ponownie po przeniesieniu.</span><span class="sxs-lookup"><span data-stu-id="4ad13-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="4ad13-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ad13-110">EXAMPLES</span></span>

### <span data-ttu-id="4ad13-111">Przykład 1: przenoszenie obwodu ExpressRoute do modelu wdrożenia Menedżera zasobów</span><span class="sxs-lookup"><span data-stu-id="4ad13-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="4ad13-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ad13-112">PARAMETERS</span></span>

### <span data-ttu-id="4ad13-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4ad13-113">-Force</span></span>
<span data-ttu-id="4ad13-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4ad13-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4ad13-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4ad13-115">-Location</span></span>
<span data-ttu-id="4ad13-116">Nazwa lokalizacji platformy Azure, w której znajduje się obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4ad13-116">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="4ad13-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4ad13-117">-Name</span></span>
<span data-ttu-id="4ad13-118">Nazwa obwodu ExpressRoute, który ma zostać przesunięty.</span><span class="sxs-lookup"><span data-stu-id="4ad13-118">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="4ad13-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ad13-119">-ResourceGroupName</span></span>
<span data-ttu-id="4ad13-120">Nazwa grupy zasobów, która będzie zawierać przenoszony obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4ad13-120">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="4ad13-121">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="4ad13-121">-ServiceKey</span></span>
<span data-ttu-id="4ad13-122">Klucz usługi wykorzystywany przez obwód ExpressRoute w klasycznym modelu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="4ad13-122">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="4ad13-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="4ad13-123">-Tag</span></span>
<span data-ttu-id="4ad13-124">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4ad13-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4ad13-125">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="4ad13-125">For example:</span></span>

<span data-ttu-id="4ad13-126">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="4ad13-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4ad13-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ad13-127">-Confirm</span></span>
<span data-ttu-id="4ad13-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ad13-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ad13-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ad13-129">-WhatIf</span></span>
<span data-ttu-id="4ad13-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ad13-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ad13-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4ad13-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ad13-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad13-132">-DefaultProfile</span></span>
<span data-ttu-id="4ad13-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ad13-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ad13-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad13-134">CommonParameters</span></span>
<span data-ttu-id="4ad13-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ad13-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad13-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ad13-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad13-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ad13-137">INPUTS</span></span>

## <span data-ttu-id="4ad13-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ad13-138">OUTPUTS</span></span>

### <span data-ttu-id="4ad13-139">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ad13-139">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4ad13-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ad13-140">NOTES</span></span>

## <span data-ttu-id="4ad13-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ad13-141">RELATED LINKS</span></span>

[<span data-ttu-id="4ad13-142">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ad13-142">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4ad13-143">Nowe — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ad13-143">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4ad13-144">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ad13-144">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4ad13-145">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ad13-145">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
