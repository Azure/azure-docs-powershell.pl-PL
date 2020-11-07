---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: d11de748c8c86c974b45ac2f171b5eb54b97ee6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898696"
---
# <span data-ttu-id="4caf1-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4caf1-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="4caf1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4caf1-102">SYNOPSIS</span></span>
<span data-ttu-id="4caf1-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="4caf1-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4caf1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4caf1-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4caf1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4caf1-105">DESCRIPTION</span></span>
<span data-ttu-id="4caf1-106">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="4caf1-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="4caf1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4caf1-107">EXAMPLES</span></span>

### <span data-ttu-id="4caf1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4caf1-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="4caf1-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="4caf1-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="4caf1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4caf1-110">PARAMETERS</span></span>

### <span data-ttu-id="4caf1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4caf1-111">-DefaultProfile</span></span>
<span data-ttu-id="4caf1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4caf1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4caf1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4caf1-113">-Force</span></span>
<span data-ttu-id="4caf1-114">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="4caf1-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="4caf1-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4caf1-115">-Name</span></span>
<span data-ttu-id="4caf1-116">Nazwa reguły filtrowania tras</span><span class="sxs-lookup"><span data-stu-id="4caf1-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="4caf1-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4caf1-117">-RouteFilter</span></span>
<span data-ttu-id="4caf1-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4caf1-118">The RouteFilter</span></span>

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

### <span data-ttu-id="4caf1-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4caf1-119">-Confirm</span></span>
<span data-ttu-id="4caf1-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4caf1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4caf1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4caf1-121">-WhatIf</span></span>
<span data-ttu-id="4caf1-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4caf1-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4caf1-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4caf1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4caf1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4caf1-124">CommonParameters</span></span>
<span data-ttu-id="4caf1-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4caf1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4caf1-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4caf1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4caf1-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4caf1-127">INPUTS</span></span>

### <span data-ttu-id="4caf1-128">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4caf1-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4caf1-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4caf1-129">OUTPUTS</span></span>

### <span data-ttu-id="4caf1-130">Microsoft. Azure. Commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="4caf1-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="4caf1-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4caf1-131">NOTES</span></span>

## <span data-ttu-id="4caf1-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4caf1-132">RELATED LINKS</span></span>

