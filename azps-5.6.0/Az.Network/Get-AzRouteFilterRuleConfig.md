---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 0ed7233cda87c376707e0a5b5682a61a179550d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954081"
---
# <span data-ttu-id="0dfa2-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0dfa2-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="0dfa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dfa2-102">SYNOPSIS</span></span>
<span data-ttu-id="0dfa2-103">Pobiera regułę filtrowania trasy w filtrze trasy.</span><span class="sxs-lookup"><span data-stu-id="0dfa2-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="0dfa2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0dfa2-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dfa2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0dfa2-105">DESCRIPTION</span></span>
<span data-ttu-id="0dfa2-106">Polecenie **cmdlet Get-AzRouteFilterRuleConfig** pobiera regułę filtrowania trasy lub listę reguł filtrowania trasy w filtrze trasy.</span><span class="sxs-lookup"><span data-stu-id="0dfa2-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="0dfa2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0dfa2-107">EXAMPLES</span></span>

### <span data-ttu-id="0dfa2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0dfa2-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="0dfa2-109">Pierwsze polecenie pobiera filtr trasy o nazwie MyRouteFilter, a następnie zapisuje go w zmiennym $rf.</span><span class="sxs-lookup"><span data-stu-id="0dfa2-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="0dfa2-110">Drugie polecenie pobiera regułę filtrowania tras o nazwie Reguła01 skojarzoną z tym filtrem trasy.</span><span class="sxs-lookup"><span data-stu-id="0dfa2-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="0dfa2-111">Trzecie polecenie otrzymuje listę reguł filtrowania tras skojarzonych z tym filtrem trasy.</span><span class="sxs-lookup"><span data-stu-id="0dfa2-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="0dfa2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0dfa2-112">PARAMETERS</span></span>

### <span data-ttu-id="0dfa2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dfa2-113">-DefaultProfile</span></span>
<span data-ttu-id="0dfa2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0dfa2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dfa2-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0dfa2-115">-Name</span></span>
<span data-ttu-id="0dfa2-116">Nazwa reguły filtrowania tras</span><span class="sxs-lookup"><span data-stu-id="0dfa2-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="0dfa2-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="0dfa2-117">-RouteFilter</span></span>
<span data-ttu-id="0dfa2-118">Filtr trasy</span><span class="sxs-lookup"><span data-stu-id="0dfa2-118">The RouteFilter</span></span>

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

### <span data-ttu-id="0dfa2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dfa2-119">CommonParameters</span></span>
<span data-ttu-id="0dfa2-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dfa2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dfa2-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0dfa2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dfa2-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0dfa2-122">INPUTS</span></span>

### <span data-ttu-id="0dfa2-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0dfa2-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="0dfa2-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0dfa2-124">OUTPUTS</span></span>

### <span data-ttu-id="0dfa2-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="0dfa2-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="0dfa2-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0dfa2-126">NOTES</span></span>

## <span data-ttu-id="0dfa2-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0dfa2-127">RELATED LINKS</span></span>

[<span data-ttu-id="0dfa2-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0dfa2-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0dfa2-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0dfa2-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0dfa2-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0dfa2-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0dfa2-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0dfa2-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0dfa2-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0dfa2-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="0dfa2-133">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0dfa2-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="0dfa2-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0dfa2-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="0dfa2-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0dfa2-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
