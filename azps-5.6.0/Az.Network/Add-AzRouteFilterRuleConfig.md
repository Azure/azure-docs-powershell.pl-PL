---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 26e759256f5641f1e38553b8a2db4ab444c2aa53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009473"
---
# <span data-ttu-id="74bd5-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74bd5-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="74bd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="74bd5-103">Dodaje regułę filtrowania trasy do filtru trasy.</span><span class="sxs-lookup"><span data-stu-id="74bd5-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="74bd5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="74bd5-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74bd5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="74bd5-105">DESCRIPTION</span></span>
<span data-ttu-id="74bd5-106">Polecenie Add-AzRouteFilterRuleConfig cmdlet dodaje regułę filtru trasy do filtru trasy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="74bd5-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="74bd5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="74bd5-107">EXAMPLES</span></span>

### <span data-ttu-id="74bd5-108">Przykład 1. Dodawanie reguły filtrowania trasy do filtru trasy</span><span class="sxs-lookup"><span data-stu-id="74bd5-108">Example 1: Add a route filter rule to a route filter</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="74bd5-109">Pierwsze polecenie pobiera filtr trasy o nazwie Filtr trasy01 przy użyciu Get-AzRouteFilter cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74bd5-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="74bd5-110">To polecenie zapisuje filtr w $RouteFilter zmienną.</span><span class="sxs-lookup"><span data-stu-id="74bd5-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="74bd5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74bd5-111">PARAMETERS</span></span>

### <span data-ttu-id="74bd5-112">— Access</span><span class="sxs-lookup"><span data-stu-id="74bd5-112">-Access</span></span>
<span data-ttu-id="74bd5-113">Określa dostęp do reguły filtrowania trasy. Prawidłowe wartości to Deny (Odmów) lub Allow (Zezwalaj).</span><span class="sxs-lookup"><span data-stu-id="74bd5-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="74bd5-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="74bd5-114">-CommunityList</span></span>
<span data-ttu-id="74bd5-115">Lista wartości społeczności, według których będzie filtrowany filtr trasy</span><span class="sxs-lookup"><span data-stu-id="74bd5-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="74bd5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74bd5-116">-DefaultProfile</span></span>
<span data-ttu-id="74bd5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="74bd5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74bd5-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="74bd5-118">-Force</span></span>
<span data-ttu-id="74bd5-119">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="74bd5-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="74bd5-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="74bd5-120">-Name</span></span>
<span data-ttu-id="74bd5-121">Określa nazwę reguły filtrowania trasy, która ma być dodawania do filtru trasy.</span><span class="sxs-lookup"><span data-stu-id="74bd5-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="74bd5-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="74bd5-122">-RouteFilter</span></span>
<span data-ttu-id="74bd5-123">Określa filtr trasy, do którego to polecenie cmdlet dodaje regułę filtrowania trasy.</span><span class="sxs-lookup"><span data-stu-id="74bd5-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="74bd5-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="74bd5-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="74bd5-125">Określa typ reguły filtru trasy.</span><span class="sxs-lookup"><span data-stu-id="74bd5-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="74bd5-126">Prawidłowe wartości to: Community</span><span class="sxs-lookup"><span data-stu-id="74bd5-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="74bd5-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74bd5-127">-Confirm</span></span>
<span data-ttu-id="74bd5-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="74bd5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74bd5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74bd5-129">-WhatIf</span></span>
<span data-ttu-id="74bd5-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74bd5-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74bd5-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="74bd5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74bd5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74bd5-132">CommonParameters</span></span>
<span data-ttu-id="74bd5-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74bd5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74bd5-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74bd5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74bd5-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74bd5-135">INPUTS</span></span>

### <span data-ttu-id="74bd5-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="74bd5-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="74bd5-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74bd5-137">OUTPUTS</span></span>

### <span data-ttu-id="74bd5-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="74bd5-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="74bd5-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="74bd5-139">NOTES</span></span>
<span data-ttu-id="74bd5-140">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="74bd5-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="74bd5-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74bd5-141">RELATED LINKS</span></span>

[<span data-ttu-id="74bd5-142">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74bd5-142">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="74bd5-143">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74bd5-143">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="74bd5-144">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74bd5-144">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="74bd5-145">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74bd5-145">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="74bd5-146">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="74bd5-146">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="74bd5-147">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="74bd5-147">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="74bd5-148">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="74bd5-148">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="74bd5-149">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="74bd5-149">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
