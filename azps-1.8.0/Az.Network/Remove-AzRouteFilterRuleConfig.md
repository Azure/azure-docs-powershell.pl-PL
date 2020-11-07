---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 7a3f6e6927449d9bc8eb1d6fe58616333aa3163c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709089"
---
# <span data-ttu-id="428a3-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="428a3-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="428a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="428a3-102">SYNOPSIS</span></span>
<span data-ttu-id="428a3-103">Usuwa regułę filtru tras z filtru tras.</span><span class="sxs-lookup"><span data-stu-id="428a3-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="428a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="428a3-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="428a3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="428a3-105">DESCRIPTION</span></span>
<span data-ttu-id="428a3-106">Polecenie cmdlet **Remove-AzRouteFilterRuleConfig** usuwa regułę filtru tras z filtru tras.</span><span class="sxs-lookup"><span data-stu-id="428a3-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="428a3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="428a3-107">EXAMPLES</span></span>

### <span data-ttu-id="428a3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="428a3-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="428a3-109">Pierwsze polecenie pobiera filtr trasy o nazwie RouteFilter01 należący do grupy zasobów o nazwie ResourceGroup01 i zapisuje go w zmiennej $rf.</span><span class="sxs-lookup"><span data-stu-id="428a3-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="428a3-110">Drugie polecenie usuwa regułę filtru tras o nazwie Rule01 z filtru tras przechowywanego w $rf.</span><span class="sxs-lookup"><span data-stu-id="428a3-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="428a3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="428a3-111">PARAMETERS</span></span>

### <span data-ttu-id="428a3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="428a3-112">-DefaultProfile</span></span>
<span data-ttu-id="428a3-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="428a3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="428a3-114">-Force</span><span class="sxs-lookup"><span data-stu-id="428a3-114">-Force</span></span>
<span data-ttu-id="428a3-115">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="428a3-115">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="428a3-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="428a3-116">-Name</span></span>
<span data-ttu-id="428a3-117">Nazwa reguły filtrowania tras</span><span class="sxs-lookup"><span data-stu-id="428a3-117">The name of the route filter rule</span></span>

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

### <span data-ttu-id="428a3-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="428a3-118">-RouteFilter</span></span>
<span data-ttu-id="428a3-119">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="428a3-119">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="428a3-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="428a3-120">-Confirm</span></span>
<span data-ttu-id="428a3-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="428a3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="428a3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="428a3-122">-WhatIf</span></span>
<span data-ttu-id="428a3-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="428a3-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="428a3-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="428a3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="428a3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="428a3-125">CommonParameters</span></span>
<span data-ttu-id="428a3-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="428a3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="428a3-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="428a3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="428a3-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="428a3-128">INPUTS</span></span>

### <span data-ttu-id="428a3-129">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="428a3-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="428a3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="428a3-130">OUTPUTS</span></span>

### <span data-ttu-id="428a3-131">Microsoft. Azure. Commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="428a3-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="428a3-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="428a3-132">NOTES</span></span>

## <span data-ttu-id="428a3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="428a3-133">RELATED LINKS</span></span>

[<span data-ttu-id="428a3-134">Dodaj-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="428a3-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="428a3-135">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="428a3-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="428a3-136">Nowe — AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="428a3-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="428a3-137">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="428a3-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="428a3-138">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="428a3-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="428a3-139">Nowe — AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="428a3-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="428a3-140">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="428a3-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="428a3-141">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="428a3-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
