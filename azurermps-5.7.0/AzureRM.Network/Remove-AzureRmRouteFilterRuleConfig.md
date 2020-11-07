---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 59a8ff1467bf70cea2eafe2117850d3423236f18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718642"
---
# <span data-ttu-id="869e6-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="869e6-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="869e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="869e6-102">SYNOPSIS</span></span>
<span data-ttu-id="869e6-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="869e6-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="869e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="869e6-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="869e6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="869e6-105">DESCRIPTION</span></span>
<span data-ttu-id="869e6-106">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="869e6-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="869e6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="869e6-107">EXAMPLES</span></span>

### <span data-ttu-id="869e6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="869e6-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="869e6-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="869e6-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="869e6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="869e6-110">PARAMETERS</span></span>

### <span data-ttu-id="869e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="869e6-111">-DefaultProfile</span></span>
<span data-ttu-id="869e6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="869e6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="869e6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="869e6-113">-Force</span></span>
<span data-ttu-id="869e6-114">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="869e6-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="869e6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="869e6-115">-Name</span></span>
<span data-ttu-id="869e6-116">Nazwa reguły filtrowania tras</span><span class="sxs-lookup"><span data-stu-id="869e6-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="869e6-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="869e6-117">-RouteFilter</span></span>
<span data-ttu-id="869e6-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="869e6-118">The RouteFilter</span></span>

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

### <span data-ttu-id="869e6-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="869e6-119">-Confirm</span></span>
<span data-ttu-id="869e6-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="869e6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="869e6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="869e6-121">-WhatIf</span></span>
<span data-ttu-id="869e6-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="869e6-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="869e6-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="869e6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="869e6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="869e6-124">CommonParameters</span></span>
<span data-ttu-id="869e6-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="869e6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="869e6-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="869e6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="869e6-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="869e6-127">INPUTS</span></span>

### <span data-ttu-id="869e6-128">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="869e6-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="869e6-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="869e6-129">OUTPUTS</span></span>

### <span data-ttu-id="869e6-130">Microsoft. Azure. Commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="869e6-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="869e6-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="869e6-131">NOTES</span></span>

## <span data-ttu-id="869e6-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="869e6-132">RELATED LINKS</span></span>

