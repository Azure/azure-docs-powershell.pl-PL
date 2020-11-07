---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 910b432382eb24f6c5eaf77d3e0c7fe3dc547413
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890949"
---
# <span data-ttu-id="82919-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="82919-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="82919-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82919-102">SYNOPSIS</span></span>
<span data-ttu-id="82919-103">Dodaje regułę filtru tras do filtru tras.</span><span class="sxs-lookup"><span data-stu-id="82919-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="82919-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82919-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82919-105">Opis</span><span class="sxs-lookup"><span data-stu-id="82919-105">DESCRIPTION</span></span>
<span data-ttu-id="82919-106">Polecenie cmdlet Add-AzRouteFilterRuleConfig umożliwia dodanie reguły filtru tras do filtru tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="82919-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="82919-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82919-107">EXAMPLES</span></span>

### <span data-ttu-id="82919-108">--------------------------Przykład 1: Dodawanie reguły filtru tras do filtru tras--------------------------</span><span class="sxs-lookup"><span data-stu-id="82919-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="82919-109">Pierwsze polecenie pobiera filtr trasy o nazwie routefilter01 przy użyciu polecenia cmdlet Get-AzRouteFilter.</span><span class="sxs-lookup"><span data-stu-id="82919-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="82919-110">Polecenie zapisuje filtr w zmiennej $RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="82919-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="82919-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82919-111">PARAMETERS</span></span>

### <span data-ttu-id="82919-112">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="82919-112">-Access</span></span>
<span data-ttu-id="82919-113">Określa dostęp do reguły filtrowania tras, prawidłowe wartości to odmowę lub zezwolenie.</span><span class="sxs-lookup"><span data-stu-id="82919-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="82919-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="82919-114">-CommunityList</span></span>
<span data-ttu-id="82919-115">Lista wartości społeczności, według której filtr trasy będzie filtrować.</span><span class="sxs-lookup"><span data-stu-id="82919-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="82919-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82919-116">-DefaultProfile</span></span>
<span data-ttu-id="82919-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="82919-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82919-118">-Force</span><span class="sxs-lookup"><span data-stu-id="82919-118">-Force</span></span>
<span data-ttu-id="82919-119">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="82919-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="82919-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="82919-120">-Name</span></span>
<span data-ttu-id="82919-121">Określa nazwę reguły filtru tras, którą należy dodać do filtru tras.</span><span class="sxs-lookup"><span data-stu-id="82919-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="82919-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="82919-122">-RouteFilter</span></span>
<span data-ttu-id="82919-123">Określa filtr trasy, do którego jest dodawana reguła filtru tras.</span><span class="sxs-lookup"><span data-stu-id="82919-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="82919-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="82919-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="82919-125">Określa typ reguły filtrowania tras.</span><span class="sxs-lookup"><span data-stu-id="82919-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="82919-126">Prawidłowe wartości: społeczność</span><span class="sxs-lookup"><span data-stu-id="82919-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="82919-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="82919-127">-Confirm</span></span>
<span data-ttu-id="82919-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82919-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82919-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82919-129">-WhatIf</span></span>
<span data-ttu-id="82919-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82919-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82919-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="82919-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82919-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82919-132">CommonParameters</span></span>
<span data-ttu-id="82919-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82919-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82919-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82919-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82919-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82919-135">INPUTS</span></span>

### <span data-ttu-id="82919-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="82919-136">PSRouteFilter</span></span>
<span data-ttu-id="82919-137">Parametr "RouteFilter" akceptuje wartość typu "PSRouteFilter" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="82919-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="82919-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82919-138">OUTPUTS</span></span>

### <span data-ttu-id="82919-139">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="82919-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="82919-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82919-140">NOTES</span></span>
<span data-ttu-id="82919-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="82919-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="82919-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82919-142">RELATED LINKS</span></span>

[<span data-ttu-id="82919-143">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="82919-143">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="82919-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="82919-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="82919-145">Nowe — AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="82919-145">New-AzRouteFilterRuleConfigConfig</span></span>](./New-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="82919-146">Remove-AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="82919-146">Remove-AzRouteFilterRuleConfigConfig</span></span>](./Remove-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="82919-147">Set-AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="82919-147">Set-AzRouteFilterRuleConfigConfig</span></span>](./Set-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="82919-148">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="82919-148">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

