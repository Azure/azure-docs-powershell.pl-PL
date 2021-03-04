---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: a58a6216d49539d4fc40f9c9131a335f7a31b87f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990893"
---
# <span data-ttu-id="5a7cd-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a7cd-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="5a7cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a7cd-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7cd-103">Modyfikuje regułę filtrowania trasy filtru trasy.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="5a7cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a7cd-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a7cd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a7cd-105">DESCRIPTION</span></span>
<span data-ttu-id="5a7cd-106">Polecenie **cmdlet Set-AzRouteFilterRuleConfig** modyfikuje regułę filtrowania trasy filtru trasy.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="5a7cd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a7cd-107">EXAMPLES</span></span>

### <span data-ttu-id="5a7cd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5a7cd-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="5a7cd-109">Pierwsze polecenie pobiera filtr trasy o nazwie RouteFilter01 i zapisuje go w $rf zmienną.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="5a7cd-110">Drugie polecenie modyfikuje regułę filtrowania tras o nazwie Rule01 i zapisuje zaktualizowany filtr trasy w $rf zmienną.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="5a7cd-111">Trzecie polecenie zapisuje zaktualizowany filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="5a7cd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a7cd-112">PARAMETERS</span></span>

### <span data-ttu-id="5a7cd-113">— Access</span><span class="sxs-lookup"><span data-stu-id="5a7cd-113">-Access</span></span>
<span data-ttu-id="5a7cd-114">Typ dostępu reguły.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-114">The access type of the rule.</span></span>
<span data-ttu-id="5a7cd-115">Dopuszczalne wartości to: "Zezwalaj", "Odmów"</span><span class="sxs-lookup"><span data-stu-id="5a7cd-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="5a7cd-116">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="5a7cd-116">-CommunityList</span></span>
<span data-ttu-id="5a7cd-117">Lista wartości społeczności, według których będzie filtrowany filtr trasy</span><span class="sxs-lookup"><span data-stu-id="5a7cd-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="5a7cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7cd-118">-DefaultProfile</span></span>
<span data-ttu-id="5a7cd-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a7cd-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="5a7cd-120">-Force</span></span>
<span data-ttu-id="5a7cd-121">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="5a7cd-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5a7cd-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5a7cd-122">-Name</span></span>
<span data-ttu-id="5a7cd-123">Nazwa reguły filtrowania tras</span><span class="sxs-lookup"><span data-stu-id="5a7cd-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="5a7cd-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="5a7cd-124">-RouteFilter</span></span>
<span data-ttu-id="5a7cd-125">Filtr trasy</span><span class="sxs-lookup"><span data-stu-id="5a7cd-125">The RouteFilter</span></span>

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

### <span data-ttu-id="5a7cd-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="5a7cd-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="5a7cd-127">Typ reguły filtru trasy reguły.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="5a7cd-128">Dopuszczalne wartości: "Społeczność"</span><span class="sxs-lookup"><span data-stu-id="5a7cd-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="5a7cd-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a7cd-129">-Confirm</span></span>
<span data-ttu-id="5a7cd-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a7cd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a7cd-131">-WhatIf</span></span>
<span data-ttu-id="5a7cd-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a7cd-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a7cd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7cd-134">CommonParameters</span></span>
<span data-ttu-id="5a7cd-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7cd-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a7cd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7cd-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a7cd-137">INPUTS</span></span>

### <span data-ttu-id="5a7cd-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5a7cd-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="5a7cd-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a7cd-139">OUTPUTS</span></span>

### <span data-ttu-id="5a7cd-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5a7cd-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="5a7cd-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a7cd-141">NOTES</span></span>

## <span data-ttu-id="5a7cd-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a7cd-142">RELATED LINKS</span></span>

[<span data-ttu-id="5a7cd-143">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a7cd-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5a7cd-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a7cd-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5a7cd-145">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a7cd-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5a7cd-146">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a7cd-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5a7cd-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5a7cd-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="5a7cd-148">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5a7cd-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="5a7cd-149">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5a7cd-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="5a7cd-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5a7cd-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
