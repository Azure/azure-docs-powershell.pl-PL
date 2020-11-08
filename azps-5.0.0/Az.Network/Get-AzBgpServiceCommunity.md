---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azbgpservicecommunity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBgpServiceCommunity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBgpServiceCommunity.md
ms.openlocfilehash: 334c10d1fdeb8dae4379d495975934572fe7e340
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234354"
---
# <span data-ttu-id="bd6a3-101">Get-AzBgpServiceCommunity</span><span class="sxs-lookup"><span data-stu-id="bd6a3-101">Get-AzBgpServiceCommunity</span></span>

## <span data-ttu-id="bd6a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="bd6a3-103">Zawiera listę wszystkich usług/regionów, społeczności BGP i skojarzonych prefiksów.</span><span class="sxs-lookup"><span data-stu-id="bd6a3-103">Provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="bd6a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd6a3-104">SYNTAX</span></span>

```
Get-AzBgpServiceCommunity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd6a3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bd6a3-105">DESCRIPTION</span></span>
<span data-ttu-id="bd6a3-106">To polecenie cmdlet zawiera listę wszystkich usług/regionów, społeczności BGP i skojarzonych prefiksów.</span><span class="sxs-lookup"><span data-stu-id="bd6a3-106">This cmdlet provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="bd6a3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd6a3-107">EXAMPLES</span></span>

### <span data-ttu-id="bd6a3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bd6a3-108">Example 1</span></span>
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

<span data-ttu-id="bd6a3-109">To polecenie cmdlet zawiera listę wszystkich usług/regionów, społeczności BGP i skojarzonych prefiksów.</span><span class="sxs-lookup"><span data-stu-id="bd6a3-109">This cmdlet provides a list of all services / regions, BGP communities, and associated prefixes.</span></span>

## <span data-ttu-id="bd6a3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd6a3-110">PARAMETERS</span></span>

### <span data-ttu-id="bd6a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd6a3-111">-DefaultProfile</span></span>
<span data-ttu-id="bd6a3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd6a3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd6a3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd6a3-113">CommonParameters</span></span>
<span data-ttu-id="bd6a3-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd6a3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd6a3-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd6a3-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd6a3-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd6a3-116">INPUTS</span></span>

### <span data-ttu-id="bd6a3-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bd6a3-117">None</span></span>

## <span data-ttu-id="bd6a3-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd6a3-118">OUTPUTS</span></span>

### <span data-ttu-id="bd6a3-119">Microsoft. Azure. Commands. Network. models. PSBgpServiceCommunity</span><span class="sxs-lookup"><span data-stu-id="bd6a3-119">Microsoft.Azure.Commands.Network.Models.PSBgpServiceCommunity</span></span>

## <span data-ttu-id="bd6a3-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd6a3-120">NOTES</span></span>

## <span data-ttu-id="bd6a3-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd6a3-121">RELATED LINKS</span></span>

[<span data-ttu-id="bd6a3-122">Przenieś — AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bd6a3-122">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="bd6a3-123">Nowe — AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bd6a3-123">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="bd6a3-124">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bd6a3-124">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="bd6a3-125">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bd6a3-125">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="bd6a3-126">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bd6a3-126">Get-AzRouteFilter</span></span>](Get-AzRouteFilter.md)

[<span data-ttu-id="bd6a3-127">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bd6a3-127">Get-AzRouteFilterRuleConfig</span></span>](Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bd6a3-128">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bd6a3-128">Remove-AzRouteFilter</span></span>](Remove-AzRouteFilter.md)

[<span data-ttu-id="bd6a3-129">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bd6a3-129">Remove-AzRouteFilterRuleConfig</span></span>](Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bd6a3-130">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bd6a3-130">Set-AzRouteFilter</span></span>](Set-AzRouteFilter.md)

[<span data-ttu-id="bd6a3-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bd6a3-131">Set-AzRouteFilterRuleConfig</span></span>](Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bd6a3-132">Nowe — AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bd6a3-132">New-AzRouteFilter</span></span>](New-AzRouteFilter.md)

[<span data-ttu-id="bd6a3-133">Nowe — AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bd6a3-133">New-AzRouteFilterRuleConfig</span></span>](New-AzRouteFilterRuleConfig.md)
