---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 204ecf05f0781649f441399c7a9b6acfbfbd8cdd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223374"
---
# <span data-ttu-id="c0c7b-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c0c7b-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="c0c7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0c7b-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c7b-103">Dodaje regułę filtru tras do filtru tras.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="c0c7b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0c7b-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0c7b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c0c7b-105">DESCRIPTION</span></span>
<span data-ttu-id="c0c7b-106">Polecenie cmdlet Add-AzRouteFilterRuleConfig umożliwia dodanie reguły filtru tras do filtru tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="c0c7b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0c7b-107">EXAMPLES</span></span>

### <span data-ttu-id="c0c7b-108">Przykład 1: Dodawanie reguły filtru tras do filtru tras</span><span class="sxs-lookup"><span data-stu-id="c0c7b-108">Example 1: Add a route filter rule to a route filter</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="c0c7b-109">Pierwsze polecenie pobiera filtr trasy o nazwie routefilter01 przy użyciu polecenia cmdlet Get-AzRouteFilter.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="c0c7b-110">Polecenie zapisuje filtr w zmiennej $RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="c0c7b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0c7b-111">PARAMETERS</span></span>

### <span data-ttu-id="c0c7b-112">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="c0c7b-112">-Access</span></span>
<span data-ttu-id="c0c7b-113">Określa dostęp do reguły filtrowania tras, prawidłowe wartości to odmowę lub zezwolenie.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c7b-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="c0c7b-114">-CommunityList</span></span>
<span data-ttu-id="c0c7b-115">Lista wartości społeczności, według której filtr trasy będzie filtrować.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c7b-116">-DefaultProfile</span></span>
<span data-ttu-id="c0c7b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0c7b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c0c7b-118">-Force</span></span>
<span data-ttu-id="c0c7b-119">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="c0c7b-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c0c7b-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c0c7b-120">-Name</span></span>
<span data-ttu-id="c0c7b-121">Określa nazwę reguły filtru tras, którą należy dodać do filtru tras.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="c0c7b-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c0c7b-122">-RouteFilter</span></span>
<span data-ttu-id="c0c7b-123">Określa filtr trasy, do którego jest dodawana reguła filtru tras.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="c0c7b-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="c0c7b-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="c0c7b-125">Określa typ reguły filtrowania tras.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="c0c7b-126">Prawidłowe wartości: społeczność</span><span class="sxs-lookup"><span data-stu-id="c0c7b-126">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c7b-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0c7b-127">-Confirm</span></span>
<span data-ttu-id="c0c7b-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0c7b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0c7b-129">-WhatIf</span></span>
<span data-ttu-id="c0c7b-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0c7b-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0c7b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c7b-132">CommonParameters</span></span>
<span data-ttu-id="c0c7b-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c7b-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0c7b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c7b-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0c7b-135">INPUTS</span></span>

### <span data-ttu-id="c0c7b-136">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c0c7b-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="c0c7b-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0c7b-137">OUTPUTS</span></span>

### <span data-ttu-id="c0c7b-138">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c0c7b-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="c0c7b-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0c7b-139">NOTES</span></span>
<span data-ttu-id="c0c7b-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="c0c7b-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c0c7b-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0c7b-141">RELATED LINKS</span></span>

[<span data-ttu-id="c0c7b-142">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c0c7b-142">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c0c7b-143">Nowe — AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c0c7b-143">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c0c7b-144">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c0c7b-144">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c0c7b-145">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c0c7b-145">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c0c7b-146">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c0c7b-146">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="c0c7b-147">Nowe — AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c0c7b-147">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="c0c7b-148">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c0c7b-148">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="c0c7b-149">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c0c7b-149">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
