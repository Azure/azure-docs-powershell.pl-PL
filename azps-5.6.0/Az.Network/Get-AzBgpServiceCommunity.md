---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azbgpservicecommunity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBgpServiceCommunity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBgpServiceCommunity.md
ms.openlocfilehash: 649fb6734caf2df11a65c43c59d123db425e90bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997774"
---
# <span data-ttu-id="9bec2-101">Get-AzBgpServiceCommunity</span><span class="sxs-lookup"><span data-stu-id="9bec2-101">Get-AzBgpServiceCommunity</span></span>

## <span data-ttu-id="9bec2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bec2-102">SYNOPSIS</span></span>
<span data-ttu-id="9bec2-103">Zawiera listę wszystkich usług/regionów, społeczności BGP i skojarzonych prefiksów.</span><span class="sxs-lookup"><span data-stu-id="9bec2-103">Provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="9bec2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9bec2-104">SYNTAX</span></span>

```
Get-AzBgpServiceCommunity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bec2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9bec2-105">DESCRIPTION</span></span>
<span data-ttu-id="9bec2-106">To polecenie cmdlet zawiera listę wszystkich usług/regionów, społeczności BGP i skojarzonych prefiksów.</span><span class="sxs-lookup"><span data-stu-id="9bec2-106">This cmdlet provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="9bec2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9bec2-107">EXAMPLES</span></span>

### <span data-ttu-id="9bec2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9bec2-108">Example 1</span></span>
```
Get-AzBgpServiceCommunity

...

Name           : AzureCentralIndia
Id             : /subscriptions//resourceGroups//providers/Microsoft.Network/bgpServiceCommunities/AzureCentralIndia
Type           : Microsoft.Network/bgpServiceCommunities
BgpCommunities : [
                   {
                     "ServiceSupportedRegion": "Global",
                     "CommunityName": "Azure Central India",
                     "CommunityValue": "12076:51017",
                     "CommunityPrefixes": [
                       "13.71.0.0/18",
                       "20.190.146.0/25",
                       "40.79.214.0/24",
                       "40.81.224.0/19",
                       "40.87.224.0/22",
                       "40.112.39.0/25",
                       "40.112.39.128/26",
                       "40.126.18.0/25",
                       "52.136.24.0/24",
                       "52.140.64.0/18",
                       "52.159.64.0/19",
                       "52.172.128.0/17",
                       "52.239.135.64/26",
                       "52.239.202.0/24",
                       "52.245.96.0/22",
                       "52.253.168.0/22",
                       "104.47.210.0/23",
                       "104.211.64.0/20",
                       "104.211.81.0/24",
                       "104.211.82.0/23",
                       "104.211.84.0/22",
                       "104.211.88.0/21",
                       "104.211.96.0/19"
                     ],
                     "IsAuthorizedToUse": true,
                     "ServiceGroup": "Azure"
                   }
                 ]
...
```

<span data-ttu-id="9bec2-109">To polecenie cmdlet zawiera listę wszystkich usług/regionów, społeczności BGP i skojarzonych prefiksów.</span><span class="sxs-lookup"><span data-stu-id="9bec2-109">This cmdlet provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="9bec2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bec2-110">PARAMETERS</span></span>

### <span data-ttu-id="9bec2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bec2-111">-DefaultProfile</span></span>
<span data-ttu-id="9bec2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9bec2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bec2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bec2-113">CommonParameters</span></span>
<span data-ttu-id="9bec2-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bec2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bec2-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bec2-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bec2-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bec2-116">INPUTS</span></span>

### <span data-ttu-id="9bec2-117">Brak</span><span class="sxs-lookup"><span data-stu-id="9bec2-117">None</span></span>

## <span data-ttu-id="9bec2-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bec2-118">OUTPUTS</span></span>

### <span data-ttu-id="9bec2-119">Microsoft.Azure.Commands.Network.Models.PSBgpServiceCommunity</span><span class="sxs-lookup"><span data-stu-id="9bec2-119">Microsoft.Azure.Commands.Network.Models.PSBgpServiceCommunity</span></span>

## <span data-ttu-id="9bec2-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9bec2-120">NOTES</span></span>

## <span data-ttu-id="9bec2-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bec2-121">RELATED LINKS</span></span>

[<span data-ttu-id="9bec2-122">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9bec2-122">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="9bec2-123">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9bec2-123">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="9bec2-124">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9bec2-124">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="9bec2-125">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9bec2-125">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="9bec2-126">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9bec2-126">Get-AzRouteFilter</span></span>](Get-AzRouteFilter.md)

[<span data-ttu-id="9bec2-127">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9bec2-127">Get-AzRouteFilterRuleConfig</span></span>](Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9bec2-128">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9bec2-128">Remove-AzRouteFilter</span></span>](Remove-AzRouteFilter.md)

[<span data-ttu-id="9bec2-129">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9bec2-129">Remove-AzRouteFilterRuleConfig</span></span>](Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9bec2-130">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9bec2-130">Set-AzRouteFilter</span></span>](Set-AzRouteFilter.md)

[<span data-ttu-id="9bec2-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9bec2-131">Set-AzRouteFilterRuleConfig</span></span>](Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9bec2-132">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9bec2-132">New-AzRouteFilter</span></span>](New-AzRouteFilter.md)

[<span data-ttu-id="9bec2-133">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9bec2-133">New-AzRouteFilterRuleConfig</span></span>](New-AzRouteFilterRuleConfig.md)
