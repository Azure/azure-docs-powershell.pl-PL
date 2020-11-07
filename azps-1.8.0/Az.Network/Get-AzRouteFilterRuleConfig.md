---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 5d83678d26804c97a0e21da4dcbff3f5af75d409
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709467"
---
# <span data-ttu-id="f252e-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f252e-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="f252e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f252e-102">SYNOPSIS</span></span>
<span data-ttu-id="f252e-103">Pobiera regułę filtru tras w filtrze trasy.</span><span class="sxs-lookup"><span data-stu-id="f252e-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="f252e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f252e-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f252e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f252e-105">DESCRIPTION</span></span>
<span data-ttu-id="f252e-106">Polecenie cmdlet **Get-AzRouteFilterRuleConfig** pobiera regułę filtru tras lub listę reguł filtrowania tras w filtrze tras.</span><span class="sxs-lookup"><span data-stu-id="f252e-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="f252e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f252e-107">EXAMPLES</span></span>

### <span data-ttu-id="f252e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f252e-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="f252e-109">Pierwsze polecenie uzyskuje filtr trasy o nazwie MyRouteFilter, a następnie zapisuje go w zmiennej $rf.</span><span class="sxs-lookup"><span data-stu-id="f252e-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="f252e-110">Drugie polecenie pobiera regułę filtru tras o nazwie Rule01 skojarzoną z tym filtrem trasy.</span><span class="sxs-lookup"><span data-stu-id="f252e-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="f252e-111">W trzecim poleceniu jest pobierana lista reguł filtru tras skojarzonych z tym filtrem trasy.</span><span class="sxs-lookup"><span data-stu-id="f252e-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="f252e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f252e-112">PARAMETERS</span></span>

### <span data-ttu-id="f252e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f252e-113">-DefaultProfile</span></span>
<span data-ttu-id="f252e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f252e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f252e-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f252e-115">-Name</span></span>
<span data-ttu-id="f252e-116">Nazwa reguły filtrowania tras</span><span class="sxs-lookup"><span data-stu-id="f252e-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="f252e-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="f252e-117">-RouteFilter</span></span>
<span data-ttu-id="f252e-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="f252e-118">The RouteFilter</span></span>

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

### <span data-ttu-id="f252e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f252e-119">CommonParameters</span></span>
<span data-ttu-id="f252e-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f252e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f252e-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f252e-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f252e-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f252e-122">INPUTS</span></span>

### <span data-ttu-id="f252e-123">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f252e-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="f252e-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f252e-124">OUTPUTS</span></span>

### <span data-ttu-id="f252e-125">Microsoft. Azure. Commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="f252e-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="f252e-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f252e-126">NOTES</span></span>

## <span data-ttu-id="f252e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f252e-127">RELATED LINKS</span></span>

[<span data-ttu-id="f252e-128">Dodaj-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f252e-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f252e-129">Nowe — AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f252e-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f252e-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f252e-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f252e-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f252e-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f252e-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f252e-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="f252e-133">Nowe — AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f252e-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="f252e-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f252e-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="f252e-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f252e-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
