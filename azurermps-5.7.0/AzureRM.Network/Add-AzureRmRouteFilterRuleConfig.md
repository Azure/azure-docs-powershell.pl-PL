---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 5daf0c5f764a095906e31167d6ddbc764ae68d19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548943"
---
# <span data-ttu-id="1ee14-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ee14-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="1ee14-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ee14-102">SYNOPSIS</span></span>
<span data-ttu-id="1ee14-103">Dodaje regułę filtru tras do filtru tras.</span><span class="sxs-lookup"><span data-stu-id="1ee14-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ee14-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ee14-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ee14-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ee14-105">DESCRIPTION</span></span>
<span data-ttu-id="1ee14-106">Polecenie cmdlet Add-AzureRmRouteFilterRuleConfig umożliwia dodanie reguły filtru tras do filtru tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1ee14-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="1ee14-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ee14-107">EXAMPLES</span></span>

### <span data-ttu-id="1ee14-108">--------------------------Przykład 1: Dodawanie reguły filtru tras do filtru tras--------------------------</span><span class="sxs-lookup"><span data-stu-id="1ee14-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="1ee14-109">Pierwsze polecenie pobiera filtr trasy o nazwie routefilter01 przy użyciu polecenia cmdlet Get-AzureRmRouteFilter.</span><span class="sxs-lookup"><span data-stu-id="1ee14-109">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="1ee14-110">Polecenie zapisuje filtr w zmiennej $RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="1ee14-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="1ee14-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ee14-111">PARAMETERS</span></span>

### <span data-ttu-id="1ee14-112">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="1ee14-112">-Access</span></span>
<span data-ttu-id="1ee14-113">Określa dostęp do reguły filtrowania tras, prawidłowe wartości to odmowę lub zezwolenie.</span><span class="sxs-lookup"><span data-stu-id="1ee14-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee14-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="1ee14-114">-CommunityList</span></span>
<span data-ttu-id="1ee14-115">Lista wartości społeczności, według której filtr trasy będzie filtrować.</span><span class="sxs-lookup"><span data-stu-id="1ee14-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="1ee14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ee14-116">-DefaultProfile</span></span>
<span data-ttu-id="1ee14-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ee14-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee14-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1ee14-118">-Force</span></span>
<span data-ttu-id="1ee14-119">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="1ee14-119">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee14-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ee14-120">-Name</span></span>
<span data-ttu-id="1ee14-121">Określa nazwę reguły filtru tras, którą należy dodać do filtru tras.</span><span class="sxs-lookup"><span data-stu-id="1ee14-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee14-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1ee14-122">-RouteFilter</span></span>
<span data-ttu-id="1ee14-123">Określa filtr trasy, do którego jest dodawana reguła filtru tras.</span><span class="sxs-lookup"><span data-stu-id="1ee14-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee14-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="1ee14-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="1ee14-125">Określa typ reguły filtrowania tras.</span><span class="sxs-lookup"><span data-stu-id="1ee14-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="1ee14-126">Prawidłowe wartości: społeczność</span><span class="sxs-lookup"><span data-stu-id="1ee14-126">Valid values are: Community</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee14-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ee14-127">-Confirm</span></span>
<span data-ttu-id="1ee14-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ee14-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee14-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ee14-129">-WhatIf</span></span>
<span data-ttu-id="1ee14-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ee14-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ee14-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1ee14-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee14-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee14-132">CommonParameters</span></span>
<span data-ttu-id="1ee14-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ee14-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee14-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ee14-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee14-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ee14-135">INPUTS</span></span>

### <span data-ttu-id="1ee14-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1ee14-136">PSRouteFilter</span></span>
<span data-ttu-id="1ee14-137">Parametr "RouteFilter" akceptuje wartość typu "PSRouteFilter" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="1ee14-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="1ee14-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ee14-138">OUTPUTS</span></span>

### <span data-ttu-id="1ee14-139">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1ee14-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1ee14-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ee14-140">NOTES</span></span>
<span data-ttu-id="1ee14-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="1ee14-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1ee14-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ee14-142">RELATED LINKS</span></span>

[<span data-ttu-id="1ee14-143">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ee14-143">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="1ee14-144">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1ee14-144">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="1ee14-145">Nowe — AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="1ee14-145">New-AzureRmRouteFilterRuleConfigConfig</span></span>](./New-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="1ee14-146">Remove-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="1ee14-146">Remove-AzureRmRouteFilterRuleConfigConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="1ee14-147">Set-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="1ee14-147">Set-AzureRmRouteFilterRuleConfigConfig</span></span>](./Set-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="1ee14-148">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1ee14-148">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

