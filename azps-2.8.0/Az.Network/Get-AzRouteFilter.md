---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 26fb3e9a7b4b097e79fdb328d79a82fc423ac675
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870627"
---
# <span data-ttu-id="82472-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="82472-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="82472-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82472-102">SYNOPSIS</span></span>
<span data-ttu-id="82472-103">Pobiera Filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="82472-103">Gets a route filter.</span></span>

## <span data-ttu-id="82472-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82472-104">SYNTAX</span></span>

### <span data-ttu-id="82472-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="82472-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82472-106">Większa</span><span class="sxs-lookup"><span data-stu-id="82472-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82472-107">Opis</span><span class="sxs-lookup"><span data-stu-id="82472-107">DESCRIPTION</span></span>
<span data-ttu-id="82472-108">Polecenie cmdlet **Get-AzRouteFilter** Pobiera Filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="82472-108">The **Get-AzRouteFilter** cmdlet gets a route filter.</span></span>

## <span data-ttu-id="82472-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82472-109">EXAMPLES</span></span>

### <span data-ttu-id="82472-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="82472-110">Example 1</span></span>
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

<span data-ttu-id="82472-111">To polecenie pobiera filtr trasy o nazwie RouteFilter01 należący do grupy zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="82472-111">This command gets the route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="82472-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="82472-112">Example 2</span></span>
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

<span data-ttu-id="82472-113">To polecenie pobiera wszystkie filtry tras rozpoczynające się od "RouteFilter".</span><span class="sxs-lookup"><span data-stu-id="82472-113">This command gets all route filters that start with "RouteFilter".</span></span>

## <span data-ttu-id="82472-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82472-114">PARAMETERS</span></span>

### <span data-ttu-id="82472-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82472-115">-DefaultProfile</span></span>
<span data-ttu-id="82472-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="82472-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82472-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="82472-117">-ExpandResource</span></span>
<span data-ttu-id="82472-118">Odwołanie do zasobu, które ma zostać rozwinięte.</span><span class="sxs-lookup"><span data-stu-id="82472-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="82472-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="82472-119">-Name</span></span>
<span data-ttu-id="82472-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="82472-120">The resource name.</span></span>

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

### <span data-ttu-id="82472-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82472-121">-ResourceGroupName</span></span>
<span data-ttu-id="82472-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="82472-122">The resource group name.</span></span>

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

### <span data-ttu-id="82472-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82472-123">CommonParameters</span></span>
<span data-ttu-id="82472-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82472-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82472-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82472-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82472-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82472-126">INPUTS</span></span>

### <span data-ttu-id="82472-127">System. String</span><span class="sxs-lookup"><span data-stu-id="82472-127">System.String</span></span>

## <span data-ttu-id="82472-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82472-128">OUTPUTS</span></span>

### <span data-ttu-id="82472-129">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="82472-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="82472-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82472-130">NOTES</span></span>

## <span data-ttu-id="82472-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82472-131">RELATED LINKS</span></span>

[<span data-ttu-id="82472-132">Nowe — AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="82472-132">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="82472-133">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="82472-133">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="82472-134">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="82472-134">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="82472-135">Dodaj-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="82472-135">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="82472-136">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="82472-136">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="82472-137">Nowe — AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="82472-137">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="82472-138">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="82472-138">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="82472-139">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="82472-139">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
