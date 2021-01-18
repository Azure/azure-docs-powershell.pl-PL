---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: f97b9ac971a4eec1945ae4418332e7d6ff74c71c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504377"
---
# <span data-ttu-id="6e8b4-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6e8b4-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="6e8b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="6e8b4-103">Aktualizuje filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="6e8b4-103">Updates a route filter.</span></span>

## <span data-ttu-id="6e8b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e8b4-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e8b4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6e8b4-105">DESCRIPTION</span></span>
<span data-ttu-id="6e8b4-106">Polecenie cmdlet **Set-AzApplicationGateway** aktualizuje filtr trasy</span><span class="sxs-lookup"><span data-stu-id="6e8b4-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="6e8b4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e8b4-107">EXAMPLES</span></span>

### <span data-ttu-id="6e8b4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6e8b4-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="6e8b4-109">To polecenie aktualizuje filtr trasy za pomocą ustawień w zmiennej $rf.</span><span class="sxs-lookup"><span data-stu-id="6e8b4-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="6e8b4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e8b4-110">PARAMETERS</span></span>

### <span data-ttu-id="6e8b4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e8b4-111">-AsJob</span></span>
<span data-ttu-id="6e8b4-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6e8b4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e8b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e8b4-113">-DefaultProfile</span></span>
<span data-ttu-id="6e8b4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e8b4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e8b4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6e8b4-115">-Force</span></span>
<span data-ttu-id="6e8b4-116">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="6e8b4-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6e8b4-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="6e8b4-117">-RouteFilter</span></span>
<span data-ttu-id="6e8b4-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="6e8b4-118">The RouteFilter</span></span>

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

### <span data-ttu-id="6e8b4-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6e8b4-119">-Confirm</span></span>
<span data-ttu-id="6e8b4-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e8b4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e8b4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e8b4-121">-WhatIf</span></span>
<span data-ttu-id="6e8b4-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e8b4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e8b4-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6e8b4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e8b4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e8b4-124">CommonParameters</span></span>
<span data-ttu-id="6e8b4-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e8b4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e8b4-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e8b4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e8b4-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e8b4-127">INPUTS</span></span>

### <span data-ttu-id="6e8b4-128">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6e8b4-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="6e8b4-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e8b4-129">OUTPUTS</span></span>

### <span data-ttu-id="6e8b4-130">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6e8b4-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="6e8b4-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e8b4-131">NOTES</span></span>

## <span data-ttu-id="6e8b4-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e8b4-132">RELATED LINKS</span></span>

[<span data-ttu-id="6e8b4-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6e8b4-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="6e8b4-134">Nowe — AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6e8b4-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="6e8b4-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6e8b4-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="6e8b4-136">Dodaj-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e8b4-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6e8b4-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e8b4-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6e8b4-138">Nowe — AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e8b4-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6e8b4-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e8b4-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6e8b4-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e8b4-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
