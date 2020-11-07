---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 1cb180d96b99a7dc2286c45a1d3f81a03a9cb212
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899310"
---
# <span data-ttu-id="4263c-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4263c-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="4263c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4263c-102">SYNOPSIS</span></span>
<span data-ttu-id="4263c-103">Dodaje regułę filtru tras do filtru tras.</span><span class="sxs-lookup"><span data-stu-id="4263c-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4263c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4263c-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4263c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4263c-105">DESCRIPTION</span></span>
<span data-ttu-id="4263c-106">Polecenie cmdlet Add-AzureRmRouteFilterRuleConfig umożliwia dodanie reguły filtru tras do filtru tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4263c-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="4263c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4263c-107">EXAMPLES</span></span>

### <span data-ttu-id="4263c-108">--------------------------Przykład 1: Dodawanie reguły filtru tras do filtru tras--------------------------</span><span class="sxs-lookup"><span data-stu-id="4263c-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="4263c-109">Pierwsze polecenie pobiera filtr trasy o nazwie routefilter01 przy użyciu polecenia cmdlet Get-AzureRmRouteFilter.</span><span class="sxs-lookup"><span data-stu-id="4263c-109">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="4263c-110">Polecenie zapisuje filtr w zmiennej $RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="4263c-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="4263c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4263c-111">PARAMETERS</span></span>

### <span data-ttu-id="4263c-112">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="4263c-112">-Access</span></span>
<span data-ttu-id="4263c-113">Określa dostęp do reguły filtrowania tras, prawidłowe wartości to odmowę lub zezwolenie.</span><span class="sxs-lookup"><span data-stu-id="4263c-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="4263c-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="4263c-114">-CommunityList</span></span>
<span data-ttu-id="4263c-115">Lista wartości społeczności, według której filtr trasy będzie filtrować.</span><span class="sxs-lookup"><span data-stu-id="4263c-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="4263c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4263c-116">-DefaultProfile</span></span>
<span data-ttu-id="4263c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4263c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4263c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4263c-118">-Force</span></span>
<span data-ttu-id="4263c-119">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="4263c-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="4263c-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4263c-120">-Name</span></span>
<span data-ttu-id="4263c-121">Określa nazwę reguły filtru tras, którą należy dodać do filtru tras.</span><span class="sxs-lookup"><span data-stu-id="4263c-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="4263c-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4263c-122">-RouteFilter</span></span>
<span data-ttu-id="4263c-123">Określa filtr trasy, do którego jest dodawana reguła filtru tras.</span><span class="sxs-lookup"><span data-stu-id="4263c-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="4263c-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="4263c-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="4263c-125">Określa typ reguły filtrowania tras.</span><span class="sxs-lookup"><span data-stu-id="4263c-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="4263c-126">Prawidłowe wartości: społeczność</span><span class="sxs-lookup"><span data-stu-id="4263c-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="4263c-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4263c-127">-Confirm</span></span>
<span data-ttu-id="4263c-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4263c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4263c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4263c-129">-WhatIf</span></span>
<span data-ttu-id="4263c-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4263c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4263c-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4263c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4263c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4263c-132">CommonParameters</span></span>
<span data-ttu-id="4263c-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4263c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4263c-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4263c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4263c-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4263c-135">INPUTS</span></span>

### <span data-ttu-id="4263c-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4263c-136">PSRouteFilter</span></span>
<span data-ttu-id="4263c-137">Parametr "RouteFilter" akceptuje wartość typu "PSRouteFilter" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="4263c-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="4263c-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4263c-138">OUTPUTS</span></span>

### <span data-ttu-id="4263c-139">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4263c-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4263c-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4263c-140">NOTES</span></span>
<span data-ttu-id="4263c-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="4263c-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4263c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4263c-142">RELATED LINKS</span></span>

[<span data-ttu-id="4263c-143">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4263c-143">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="4263c-144">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4263c-144">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)







[<span data-ttu-id="4263c-145">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4263c-145">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

