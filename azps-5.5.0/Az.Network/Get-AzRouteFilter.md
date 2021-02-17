---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 88b755a8865a5ce07a5dc86c94958de0c0e72485
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184691"
---
# <span data-ttu-id="b081e-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b081e-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="b081e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b081e-102">SYNOPSIS</span></span>
<span data-ttu-id="b081e-103">Pobiera filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="b081e-103">Gets a route filter.</span></span>

## <span data-ttu-id="b081e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b081e-104">SYNTAX</span></span>

### <span data-ttu-id="b081e-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="b081e-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b081e-106">Rozwiń</span><span class="sxs-lookup"><span data-stu-id="b081e-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b081e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b081e-107">DESCRIPTION</span></span>
<span data-ttu-id="b081e-108">Polecenie **cmdlet Get-AzRouteFilter** pobiera filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="b081e-108">The **Get-AzRouteFilter** cmdlet gets a route filter.</span></span>

## <span data-ttu-id="b081e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b081e-109">EXAMPLES</span></span>

### <span data-ttu-id="b081e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b081e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="b081e-111">To polecenie pobiera filtr trasy o nazwie RouteFilter01, który należy do grupy zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="b081e-111">This command gets the route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="b081e-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b081e-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter*"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []

Name              : RouteFilter02
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter02
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="b081e-113">To polecenie pobiera wszystkie filtry tras, które zaczynają się od "Filtr trasy".</span><span class="sxs-lookup"><span data-stu-id="b081e-113">This command gets all route filters that start with "RouteFilter".</span></span>

## <span data-ttu-id="b081e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b081e-114">PARAMETERS</span></span>

### <span data-ttu-id="b081e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b081e-115">-DefaultProfile</span></span>
<span data-ttu-id="b081e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b081e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b081e-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="b081e-117">-ExpandResource</span></span>
<span data-ttu-id="b081e-118">Odwołanie do zasobu do rozwinięcia.</span><span class="sxs-lookup"><span data-stu-id="b081e-118">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b081e-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b081e-119">-Name</span></span>
<span data-ttu-id="b081e-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b081e-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b081e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b081e-121">-ResourceGroupName</span></span>
<span data-ttu-id="b081e-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b081e-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b081e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b081e-123">CommonParameters</span></span>
<span data-ttu-id="b081e-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b081e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b081e-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b081e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b081e-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b081e-126">INPUTS</span></span>

### <span data-ttu-id="b081e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="b081e-127">System.String</span></span>

## <span data-ttu-id="b081e-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b081e-128">OUTPUTS</span></span>

### <span data-ttu-id="b081e-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b081e-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b081e-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b081e-130">NOTES</span></span>

## <span data-ttu-id="b081e-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b081e-131">RELATED LINKS</span></span>

[<span data-ttu-id="b081e-132">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b081e-132">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="b081e-133">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b081e-133">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="b081e-134">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b081e-134">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="b081e-135">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b081e-135">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b081e-136">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b081e-136">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b081e-137">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b081e-137">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b081e-138">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b081e-138">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b081e-139">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b081e-139">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
