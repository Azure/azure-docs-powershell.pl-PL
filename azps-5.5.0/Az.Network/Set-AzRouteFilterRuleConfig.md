---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: eb8de50aac1b68928d5cebe8118665b9a24e8fbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191619"
---
# <span data-ttu-id="8d6c9-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d6c9-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="8d6c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d6c9-102">SYNOPSIS</span></span>
<span data-ttu-id="8d6c9-103">Modyfikuje regułę filtrowania tras filtru trasy.</span><span class="sxs-lookup"><span data-stu-id="8d6c9-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="8d6c9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8d6c9-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d6c9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8d6c9-105">DESCRIPTION</span></span>
<span data-ttu-id="8d6c9-106">Polecenie **cmdlet Set-AzRouteFilterRuleConfig** modyfikuje regułę filtrowania trasy filtru trasy.</span><span class="sxs-lookup"><span data-stu-id="8d6c9-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="8d6c9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8d6c9-107">EXAMPLES</span></span>

### <span data-ttu-id="8d6c9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8d6c9-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="8d6c9-109">Pierwsze polecenie pobiera filtr trasy o nazwie RouteFilter01 i zapisuje go w $rf zmienną.</span><span class="sxs-lookup"><span data-stu-id="8d6c9-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="8d6c9-110">Drugie polecenie modyfikuje regułę filtrowania tras o nazwie Rule01 i przechowuje zaktualizowany filtr trasy w $rf zmienną.</span><span class="sxs-lookup"><span data-stu-id="8d6c9-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="8d6c9-111">Trzecie polecenie zapisuje zaktualizowany filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="8d6c9-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="8d6c9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d6c9-112">PARAMETERS</span></span>

### <span data-ttu-id="8d6c9-113">— Access</span><span class="sxs-lookup"><span data-stu-id="8d6c9-113">-Access</span></span>
<span data-ttu-id="8d6c9-114">Typ dostępu reguły.</span><span class="sxs-lookup"><span data-stu-id="8d6c9-114">The access type of the rule.</span></span>
<span data-ttu-id="8d6c9-115">Dopuszczalne wartości to: "Zezwalaj", "Odmów"</span><span class="sxs-lookup"><span data-stu-id="8d6c9-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="8d6c9-116">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="8d6c9-116">-CommunityList</span></span>
<span data-ttu-id="8d6c9-117">Lista wartości społeczności, według których będzie filtrowany filtr trasy</span><span class="sxs-lookup"><span data-stu-id="8d6c9-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="8d6c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d6c9-118">-DefaultProfile</span></span>
<span data-ttu-id="8d6c9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d6c9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d6c9-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="8d6c9-120">-Force</span></span>
<span data-ttu-id="8d6c9-121">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="8d6c9-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8d6c9-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8d6c9-122">-Name</span></span>
<span data-ttu-id="8d6c9-123">Nazwa reguły filtrowania tras</span><span class="sxs-lookup"><span data-stu-id="8d6c9-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="8d6c9-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8d6c9-124">-RouteFilter</span></span>
<span data-ttu-id="8d6c9-125">Filtr trasy</span><span class="sxs-lookup"><span data-stu-id="8d6c9-125">The RouteFilter</span></span>

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

### <span data-ttu-id="8d6c9-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="8d6c9-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="8d6c9-127">Typ reguły filtru trasy reguły.</span><span class="sxs-lookup"><span data-stu-id="8d6c9-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="8d6c9-128">Dopuszczalne wartości: "Społeczność"</span><span class="sxs-lookup"><span data-stu-id="8d6c9-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="8d6c9-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8d6c9-129">-Confirm</span></span>
<span data-ttu-id="8d6c9-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8d6c9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d6c9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d6c9-131">-WhatIf</span></span>
<span data-ttu-id="8d6c9-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d6c9-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d6c9-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8d6c9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d6c9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d6c9-134">CommonParameters</span></span>
<span data-ttu-id="8d6c9-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d6c9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d6c9-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d6c9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d6c9-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d6c9-137">INPUTS</span></span>

### <span data-ttu-id="8d6c9-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8d6c9-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="8d6c9-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d6c9-139">OUTPUTS</span></span>

### <span data-ttu-id="8d6c9-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8d6c9-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="8d6c9-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8d6c9-141">NOTES</span></span>

## <span data-ttu-id="8d6c9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d6c9-142">RELATED LINKS</span></span>

[<span data-ttu-id="8d6c9-143">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d6c9-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8d6c9-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d6c9-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8d6c9-145">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d6c9-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8d6c9-146">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d6c9-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8d6c9-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8d6c9-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="8d6c9-148">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8d6c9-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="8d6c9-149">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8d6c9-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="8d6c9-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8d6c9-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
