---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: dc6af2cb623e2d2d67b337e3a6e3ff27b5aebd69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220504"
---
# <span data-ttu-id="b7d3d-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b7d3d-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="b7d3d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="b7d3d-103">Usuwa filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="b7d3d-103">Removes a route filter.</span></span>

## <span data-ttu-id="b7d3d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7d3d-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7d3d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b7d3d-105">DESCRIPTION</span></span>
<span data-ttu-id="b7d3d-106">Polecenie cmdlet **Remove-AzRouteFilter** usuwa filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="b7d3d-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="b7d3d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7d3d-107">EXAMPLES</span></span>

### <span data-ttu-id="b7d3d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b7d3d-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b7d3d-109">Polecenie usuwa filtr trasy o nazwie RouteFilter01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="b7d3d-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="b7d3d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7d3d-110">PARAMETERS</span></span>

### <span data-ttu-id="b7d3d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7d3d-111">-DefaultProfile</span></span>
<span data-ttu-id="b7d3d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7d3d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7d3d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b7d3d-113">-Force</span></span>
<span data-ttu-id="b7d3d-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b7d3d-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b7d3d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b7d3d-115">-Name</span></span>
<span data-ttu-id="b7d3d-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b7d3d-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d3d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7d3d-117">-PassThru</span></span>
<span data-ttu-id="b7d3d-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b7d3d-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="b7d3d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7d3d-119">-ResourceGroupName</span></span>
<span data-ttu-id="b7d3d-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7d3d-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d3d-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b7d3d-121">-Confirm</span></span>
<span data-ttu-id="b7d3d-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7d3d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7d3d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7d3d-123">-WhatIf</span></span>
<span data-ttu-id="b7d3d-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7d3d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7d3d-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b7d3d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7d3d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7d3d-126">CommonParameters</span></span>
<span data-ttu-id="b7d3d-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7d3d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7d3d-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7d3d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7d3d-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7d3d-129">INPUTS</span></span>

### <span data-ttu-id="b7d3d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b7d3d-130">System.String</span></span>

## <span data-ttu-id="b7d3d-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7d3d-131">OUTPUTS</span></span>

### <span data-ttu-id="b7d3d-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7d3d-132">System.Boolean</span></span>

## <span data-ttu-id="b7d3d-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7d3d-133">NOTES</span></span>

## <span data-ttu-id="b7d3d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7d3d-134">RELATED LINKS</span></span>

[<span data-ttu-id="b7d3d-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b7d3d-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="b7d3d-136">Nowe — AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b7d3d-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="b7d3d-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b7d3d-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="b7d3d-138">Dodaj-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7d3d-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b7d3d-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7d3d-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b7d3d-140">Nowe — AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7d3d-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b7d3d-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7d3d-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b7d3d-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7d3d-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
