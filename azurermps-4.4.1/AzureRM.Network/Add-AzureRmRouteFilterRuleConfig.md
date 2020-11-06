---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 3cd01d2e9bb3673e2c0e42ea43418c9601796a08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550908"
---
# <span data-ttu-id="2d21b-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d21b-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="2d21b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d21b-102">SYNOPSIS</span></span>
<span data-ttu-id="2d21b-103">Dodaje regułę filtru tras do filtru tras.</span><span class="sxs-lookup"><span data-stu-id="2d21b-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d21b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d21b-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d21b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2d21b-105">DESCRIPTION</span></span>
<span data-ttu-id="2d21b-106">Polecenie cmdlet Add-AzureRmRouteFilterRuleConfig umożliwia dodanie reguły filtru tras do filtru tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2d21b-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="2d21b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d21b-107">EXAMPLES</span></span>

### <span data-ttu-id="2d21b-108">--------------------------Przykład 1: Dodawanie reguły filtru tras do filtru tras--------------------------</span><span class="sxs-lookup"><span data-stu-id="2d21b-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
<span data-ttu-id="2d21b-109">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="2d21b-109">@{paragraph=PS C:\\\>}</span></span>















```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="2d21b-110">Pierwsze polecenie pobiera filtr trasy o nazwie routefilter01 przy użyciu polecenia cmdlet Get-AzureRmRouteFilter.</span><span class="sxs-lookup"><span data-stu-id="2d21b-110">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="2d21b-111">Polecenie zapisuje filtr w zmiennej $RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="2d21b-111">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="2d21b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d21b-112">PARAMETERS</span></span>

### <span data-ttu-id="2d21b-113">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="2d21b-113">-Access</span></span>
<span data-ttu-id="2d21b-114">Określa dostęp do reguły filtrowania tras, prawidłowe wartości to odmowę lub zezwolenie.</span><span class="sxs-lookup"><span data-stu-id="2d21b-114">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="2d21b-115">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="2d21b-115">-CommunityList</span></span>
<span data-ttu-id="2d21b-116">Lista wartości społeczności, według której filtr trasy będzie filtrować.</span><span class="sxs-lookup"><span data-stu-id="2d21b-116">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d21b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2d21b-117">-Force</span></span>
<span data-ttu-id="2d21b-118">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="2d21b-118">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="2d21b-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2d21b-119">-Name</span></span>
<span data-ttu-id="2d21b-120">Określa nazwę reguły filtru tras, którą należy dodać do filtru tras.</span><span class="sxs-lookup"><span data-stu-id="2d21b-120">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="2d21b-121">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="2d21b-121">-RouteFilter</span></span>
<span data-ttu-id="2d21b-122">Określa filtr trasy, do którego jest dodawana reguła filtru tras.</span><span class="sxs-lookup"><span data-stu-id="2d21b-122">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="2d21b-123">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="2d21b-123">-RouteFilterRuleType</span></span>
<span data-ttu-id="2d21b-124">Określa typ reguły filtrowania tras.</span><span class="sxs-lookup"><span data-stu-id="2d21b-124">Specifies the route filter rule type.</span></span>
<span data-ttu-id="2d21b-125">Prawidłowe wartości: społeczność</span><span class="sxs-lookup"><span data-stu-id="2d21b-125">Valid values are: Community</span></span>

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

### <span data-ttu-id="2d21b-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2d21b-126">-Confirm</span></span>
<span data-ttu-id="2d21b-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d21b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d21b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d21b-128">-WhatIf</span></span>
<span data-ttu-id="2d21b-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d21b-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d21b-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2d21b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d21b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d21b-131">-DefaultProfile</span></span>
<span data-ttu-id="2d21b-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d21b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d21b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d21b-133">CommonParameters</span></span>
<span data-ttu-id="2d21b-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d21b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d21b-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d21b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d21b-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d21b-136">INPUTS</span></span>

### <span data-ttu-id="2d21b-137">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2d21b-137">PSRouteFilter</span></span>
<span data-ttu-id="2d21b-138">Parametr "RouteFilter" akceptuje wartość typu "PSRouteFilter" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="2d21b-138">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="2d21b-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d21b-139">OUTPUTS</span></span>

### <span data-ttu-id="2d21b-140">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2d21b-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="2d21b-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d21b-141">NOTES</span></span>
<span data-ttu-id="2d21b-142">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="2d21b-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2d21b-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d21b-143">RELATED LINKS</span></span>

[<span data-ttu-id="2d21b-144">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d21b-144">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="2d21b-145">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2d21b-145">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="2d21b-146">Nowe — AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="2d21b-146">New-AzureRmRouteFilterRuleConfigConfig</span></span>](./New-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="2d21b-147">Remove-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="2d21b-147">Remove-AzureRmRouteFilterRuleConfigConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="2d21b-148">Set-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="2d21b-148">Set-AzureRmRouteFilterRuleConfigConfig</span></span>](./Set-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="2d21b-149">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2d21b-149">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

