---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 0cf13aa5aa1fb558e72a4896bc810859409b5ae1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897554"
---
# <span data-ttu-id="1b41f-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b41f-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="1b41f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b41f-102">SYNOPSIS</span></span>
<span data-ttu-id="1b41f-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="1b41f-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b41f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b41f-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b41f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1b41f-105">DESCRIPTION</span></span>
<span data-ttu-id="1b41f-106">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="1b41f-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="1b41f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b41f-107">EXAMPLES</span></span>

### <span data-ttu-id="1b41f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1b41f-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1b41f-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="1b41f-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="1b41f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b41f-110">PARAMETERS</span></span>

### <span data-ttu-id="1b41f-111">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="1b41f-111">-Access</span></span>
<span data-ttu-id="1b41f-112">Typ dostępu do reguły.</span><span class="sxs-lookup"><span data-stu-id="1b41f-112">The access type of the rule.</span></span>
<span data-ttu-id="1b41f-113">Możliwe wartości: "Zezwalaj", "Odmów"</span><span class="sxs-lookup"><span data-stu-id="1b41f-113">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="1b41f-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="1b41f-114">-CommunityList</span></span>
<span data-ttu-id="1b41f-115">Lista wartości społeczności, według której filtr trasy będzie filtrować.</span><span class="sxs-lookup"><span data-stu-id="1b41f-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="1b41f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b41f-116">-DefaultProfile</span></span>
<span data-ttu-id="1b41f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b41f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b41f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1b41f-118">-Force</span></span>
<span data-ttu-id="1b41f-119">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="1b41f-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="1b41f-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b41f-120">-Name</span></span>
<span data-ttu-id="1b41f-121">Nazwa reguły filtrowania tras</span><span class="sxs-lookup"><span data-stu-id="1b41f-121">The name of the route filter rule</span></span>

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

### <span data-ttu-id="1b41f-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1b41f-122">-RouteFilter</span></span>
<span data-ttu-id="1b41f-123">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1b41f-123">The RouteFilter</span></span>

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

### <span data-ttu-id="1b41f-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="1b41f-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="1b41f-125">Typ reguły filtrowania tras.</span><span class="sxs-lookup"><span data-stu-id="1b41f-125">The route filter rule type of the rule.</span></span>
<span data-ttu-id="1b41f-126">Możliwe wartości: "społeczność"</span><span class="sxs-lookup"><span data-stu-id="1b41f-126">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="1b41f-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b41f-127">-Confirm</span></span>
<span data-ttu-id="1b41f-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b41f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b41f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b41f-129">-WhatIf</span></span>
<span data-ttu-id="1b41f-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b41f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b41f-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1b41f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b41f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b41f-132">CommonParameters</span></span>
<span data-ttu-id="1b41f-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b41f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b41f-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b41f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b41f-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b41f-135">INPUTS</span></span>

### <span data-ttu-id="1b41f-136">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1b41f-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1b41f-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b41f-137">OUTPUTS</span></span>

### <span data-ttu-id="1b41f-138">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1b41f-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1b41f-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b41f-139">NOTES</span></span>

## <span data-ttu-id="1b41f-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b41f-140">RELATED LINKS</span></span>

