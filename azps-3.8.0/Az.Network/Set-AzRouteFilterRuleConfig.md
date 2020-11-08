---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: eb8de50aac1b68928d5cebe8118665b9a24e8fbf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052051"
---
# <span data-ttu-id="d6991-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d6991-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="d6991-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6991-102">SYNOPSIS</span></span>
<span data-ttu-id="d6991-103">Modyfikuje regułę filtru tras filtru tras.</span><span class="sxs-lookup"><span data-stu-id="d6991-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="d6991-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6991-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6991-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d6991-105">DESCRIPTION</span></span>
<span data-ttu-id="d6991-106">Polecenie cmdlet **Set-AzRouteFilterRuleConfig** modyfikuje regułę filtru tras filtru tras.</span><span class="sxs-lookup"><span data-stu-id="d6991-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="d6991-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6991-107">EXAMPLES</span></span>

### <span data-ttu-id="d6991-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d6991-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="d6991-109">Pierwsze polecenie uzyskuje filtr trasy o nazwie RouteFilter01 i zapisuje go w zmiennej $rf.</span><span class="sxs-lookup"><span data-stu-id="d6991-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="d6991-110">Drugie polecenie modyfikuje regułę filtrowania tras o nazwie Rule01 i przechowuje zaktualizowaną filtr tras w zmiennej $rf.</span><span class="sxs-lookup"><span data-stu-id="d6991-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="d6991-111">Trzecie polecenie zapisuje zaktualizowany filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="d6991-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="d6991-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6991-112">PARAMETERS</span></span>

### <span data-ttu-id="d6991-113">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="d6991-113">-Access</span></span>
<span data-ttu-id="d6991-114">Typ dostępu do reguły.</span><span class="sxs-lookup"><span data-stu-id="d6991-114">The access type of the rule.</span></span>
<span data-ttu-id="d6991-115">Możliwe wartości: "Zezwalaj", "Odmów"</span><span class="sxs-lookup"><span data-stu-id="d6991-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="d6991-116">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="d6991-116">-CommunityList</span></span>
<span data-ttu-id="d6991-117">Lista wartości społeczności, według której filtr trasy będzie filtrować.</span><span class="sxs-lookup"><span data-stu-id="d6991-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="d6991-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6991-118">-DefaultProfile</span></span>
<span data-ttu-id="d6991-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6991-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6991-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d6991-120">-Force</span></span>
<span data-ttu-id="d6991-121">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="d6991-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d6991-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d6991-122">-Name</span></span>
<span data-ttu-id="d6991-123">Nazwa reguły filtrowania tras</span><span class="sxs-lookup"><span data-stu-id="d6991-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="d6991-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d6991-124">-RouteFilter</span></span>
<span data-ttu-id="d6991-125">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d6991-125">The RouteFilter</span></span>

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

### <span data-ttu-id="d6991-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="d6991-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="d6991-127">Typ reguły filtrowania tras.</span><span class="sxs-lookup"><span data-stu-id="d6991-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="d6991-128">Możliwe wartości: "społeczność"</span><span class="sxs-lookup"><span data-stu-id="d6991-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="d6991-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6991-129">-Confirm</span></span>
<span data-ttu-id="d6991-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6991-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6991-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6991-131">-WhatIf</span></span>
<span data-ttu-id="d6991-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6991-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6991-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d6991-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6991-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6991-134">CommonParameters</span></span>
<span data-ttu-id="d6991-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6991-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6991-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6991-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6991-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6991-137">INPUTS</span></span>

### <span data-ttu-id="d6991-138">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d6991-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="d6991-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6991-139">OUTPUTS</span></span>

### <span data-ttu-id="d6991-140">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d6991-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="d6991-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6991-141">NOTES</span></span>

## <span data-ttu-id="d6991-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6991-142">RELATED LINKS</span></span>

[<span data-ttu-id="d6991-143">Dodaj-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d6991-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="d6991-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d6991-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="d6991-145">Nowe — AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d6991-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="d6991-146">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d6991-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="d6991-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d6991-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="d6991-148">Nowe — AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d6991-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="d6991-149">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d6991-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="d6991-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d6991-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
