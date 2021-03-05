---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 2212ffb43f646e49a4552713b6408091dd985aae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996108"
---
# <span data-ttu-id="86f09-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86f09-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="86f09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86f09-102">SYNOPSIS</span></span>
<span data-ttu-id="86f09-103">Usuwa regułę filtrowania trasy z filtru trasy.</span><span class="sxs-lookup"><span data-stu-id="86f09-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="86f09-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="86f09-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86f09-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="86f09-105">DESCRIPTION</span></span>
<span data-ttu-id="86f09-106">Polecenie **cmdlet Remove-AzRouteFilterRuleConfig** usuwa regułę filtrowania trasy z filtru trasy.</span><span class="sxs-lookup"><span data-stu-id="86f09-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="86f09-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="86f09-107">EXAMPLES</span></span>

### <span data-ttu-id="86f09-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="86f09-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="86f09-109">Pierwsze polecenie pobiera filtr trasy o nazwie RouteFilter01, który należy do grupy zasobów o nazwie ResourceGroup01 i przechowuje go w $rf danych.</span><span class="sxs-lookup"><span data-stu-id="86f09-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="86f09-110">Drugie polecenie usuwa regułę filtrowania tras o nazwie Rule01 z filtru trasy przechowywanego w $rf.</span><span class="sxs-lookup"><span data-stu-id="86f09-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="86f09-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86f09-111">PARAMETERS</span></span>

### <span data-ttu-id="86f09-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86f09-112">-DefaultProfile</span></span>
<span data-ttu-id="86f09-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="86f09-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86f09-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="86f09-114">-Force</span></span>
<span data-ttu-id="86f09-115">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="86f09-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="86f09-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="86f09-116">-Name</span></span>
<span data-ttu-id="86f09-117">Nazwa reguły filtrowania tras</span><span class="sxs-lookup"><span data-stu-id="86f09-117">The name of the route filter rule</span></span>

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

### <span data-ttu-id="86f09-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="86f09-118">-RouteFilter</span></span>
<span data-ttu-id="86f09-119">Filtr trasy</span><span class="sxs-lookup"><span data-stu-id="86f09-119">The RouteFilter</span></span>

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

### <span data-ttu-id="86f09-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="86f09-120">-Confirm</span></span>
<span data-ttu-id="86f09-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="86f09-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86f09-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86f09-122">-WhatIf</span></span>
<span data-ttu-id="86f09-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86f09-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86f09-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="86f09-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86f09-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f09-125">CommonParameters</span></span>
<span data-ttu-id="86f09-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86f09-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f09-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86f09-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f09-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86f09-128">INPUTS</span></span>

### <span data-ttu-id="86f09-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="86f09-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="86f09-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86f09-130">OUTPUTS</span></span>

### <span data-ttu-id="86f09-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="86f09-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="86f09-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="86f09-132">NOTES</span></span>

## <span data-ttu-id="86f09-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86f09-133">RELATED LINKS</span></span>

[<span data-ttu-id="86f09-134">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86f09-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="86f09-135">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86f09-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="86f09-136">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86f09-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="86f09-137">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86f09-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="86f09-138">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="86f09-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="86f09-139">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="86f09-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="86f09-140">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="86f09-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="86f09-141">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="86f09-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
