---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: d73fbe14e4b1d4c4ea34c7405ad7da5b7954ffd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552391"
---
# <span data-ttu-id="8af39-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8af39-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="8af39-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8af39-102">SYNOPSIS</span></span>
<span data-ttu-id="8af39-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="8af39-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8af39-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8af39-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8af39-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8af39-105">DESCRIPTION</span></span>
<span data-ttu-id="8af39-106">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="8af39-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="8af39-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8af39-107">EXAMPLES</span></span>

### <span data-ttu-id="8af39-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8af39-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="8af39-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="8af39-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="8af39-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8af39-110">PARAMETERS</span></span>

### <span data-ttu-id="8af39-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8af39-111">-Force</span></span>
<span data-ttu-id="8af39-112">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="8af39-112">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="8af39-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8af39-113">-Name</span></span>
<span data-ttu-id="8af39-114">Nazwa reguły filtrowania tras</span><span class="sxs-lookup"><span data-stu-id="8af39-114">The name of the route filter rule</span></span>

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

### <span data-ttu-id="8af39-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8af39-115">-RouteFilter</span></span>
<span data-ttu-id="8af39-116">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8af39-116">The RouteFilter</span></span>

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

### <span data-ttu-id="8af39-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8af39-117">-Confirm</span></span>
<span data-ttu-id="8af39-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8af39-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8af39-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8af39-119">-WhatIf</span></span>
<span data-ttu-id="8af39-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8af39-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8af39-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8af39-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8af39-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af39-122">-DefaultProfile</span></span>
<span data-ttu-id="8af39-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8af39-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8af39-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af39-124">CommonParameters</span></span>
<span data-ttu-id="8af39-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8af39-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af39-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8af39-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af39-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8af39-127">INPUTS</span></span>

### <span data-ttu-id="8af39-128">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8af39-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="8af39-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8af39-129">OUTPUTS</span></span>

### <span data-ttu-id="8af39-130">Microsoft. Azure. Commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="8af39-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="8af39-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8af39-131">NOTES</span></span>

## <span data-ttu-id="8af39-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8af39-132">RELATED LINKS</span></span>

