---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: f97b9ac971a4eec1945ae4418332e7d6ff74c71c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202435"
---
# <span data-ttu-id="90559-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="90559-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="90559-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90559-102">SYNOPSIS</span></span>
<span data-ttu-id="90559-103">Umożliwia aktualizację filtru trasy.</span><span class="sxs-lookup"><span data-stu-id="90559-103">Updates a route filter.</span></span>

## <span data-ttu-id="90559-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="90559-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90559-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="90559-105">DESCRIPTION</span></span>
<span data-ttu-id="90559-106">Polecenie **cmdlet Set-AzApplicationGateway** aktualizuje filtr trasy</span><span class="sxs-lookup"><span data-stu-id="90559-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="90559-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="90559-107">EXAMPLES</span></span>

### <span data-ttu-id="90559-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="90559-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="90559-109">To polecenie aktualizuje filtr trasy za pomocą ustawień $rf zmienną.</span><span class="sxs-lookup"><span data-stu-id="90559-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="90559-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90559-110">PARAMETERS</span></span>

### <span data-ttu-id="90559-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="90559-111">-AsJob</span></span>
<span data-ttu-id="90559-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="90559-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90559-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90559-113">-DefaultProfile</span></span>
<span data-ttu-id="90559-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="90559-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90559-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="90559-115">-Force</span></span>
<span data-ttu-id="90559-116">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="90559-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="90559-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="90559-117">-RouteFilter</span></span>
<span data-ttu-id="90559-118">Filtr trasy</span><span class="sxs-lookup"><span data-stu-id="90559-118">The RouteFilter</span></span>

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

### <span data-ttu-id="90559-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90559-119">-Confirm</span></span>
<span data-ttu-id="90559-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="90559-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90559-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90559-121">-WhatIf</span></span>
<span data-ttu-id="90559-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90559-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90559-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="90559-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90559-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90559-124">CommonParameters</span></span>
<span data-ttu-id="90559-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90559-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90559-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90559-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90559-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90559-127">INPUTS</span></span>

### <span data-ttu-id="90559-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="90559-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="90559-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90559-129">OUTPUTS</span></span>

### <span data-ttu-id="90559-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="90559-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="90559-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="90559-131">NOTES</span></span>

## <span data-ttu-id="90559-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90559-132">RELATED LINKS</span></span>

[<span data-ttu-id="90559-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="90559-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="90559-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="90559-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="90559-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="90559-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="90559-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90559-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="90559-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90559-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="90559-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90559-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="90559-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90559-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="90559-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90559-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
