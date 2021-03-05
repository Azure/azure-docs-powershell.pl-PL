---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: 0c6fa8b973af2f2ab4a9c8547dddffda18eb15c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990900"
---
# <span data-ttu-id="ef7dc-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ef7dc-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="ef7dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef7dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7dc-103">Aktualizuje filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="ef7dc-103">Updates a route filter.</span></span>

## <span data-ttu-id="ef7dc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ef7dc-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef7dc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ef7dc-105">DESCRIPTION</span></span>
<span data-ttu-id="ef7dc-106">Polecenie **cmdlet Set-AzApplicationGateway** aktualizuje filtr trasy</span><span class="sxs-lookup"><span data-stu-id="ef7dc-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="ef7dc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ef7dc-107">EXAMPLES</span></span>

### <span data-ttu-id="ef7dc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ef7dc-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="ef7dc-109">To polecenie aktualizuje filtr trasy za pomocą ustawień $rf zmienną.</span><span class="sxs-lookup"><span data-stu-id="ef7dc-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="ef7dc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef7dc-110">PARAMETERS</span></span>

### <span data-ttu-id="ef7dc-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ef7dc-111">-AsJob</span></span>
<span data-ttu-id="ef7dc-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ef7dc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef7dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef7dc-113">-DefaultProfile</span></span>
<span data-ttu-id="ef7dc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef7dc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef7dc-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ef7dc-115">-Force</span></span>
<span data-ttu-id="ef7dc-116">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="ef7dc-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ef7dc-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ef7dc-117">-RouteFilter</span></span>
<span data-ttu-id="ef7dc-118">Filtr trasy</span><span class="sxs-lookup"><span data-stu-id="ef7dc-118">The RouteFilter</span></span>

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

### <span data-ttu-id="ef7dc-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef7dc-119">-Confirm</span></span>
<span data-ttu-id="ef7dc-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ef7dc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef7dc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef7dc-121">-WhatIf</span></span>
<span data-ttu-id="ef7dc-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef7dc-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef7dc-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ef7dc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef7dc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef7dc-124">CommonParameters</span></span>
<span data-ttu-id="ef7dc-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef7dc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef7dc-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef7dc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef7dc-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef7dc-127">INPUTS</span></span>

### <span data-ttu-id="ef7dc-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ef7dc-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ef7dc-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef7dc-129">OUTPUTS</span></span>

### <span data-ttu-id="ef7dc-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ef7dc-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ef7dc-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ef7dc-131">NOTES</span></span>

## <span data-ttu-id="ef7dc-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef7dc-132">RELATED LINKS</span></span>

[<span data-ttu-id="ef7dc-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ef7dc-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="ef7dc-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ef7dc-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="ef7dc-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ef7dc-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="ef7dc-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef7dc-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ef7dc-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef7dc-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ef7dc-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef7dc-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ef7dc-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef7dc-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ef7dc-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef7dc-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
