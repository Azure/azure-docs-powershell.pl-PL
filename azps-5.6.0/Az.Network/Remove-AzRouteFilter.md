---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 0b75cdb63d2a8bb3c01a93a90ee01db096cf7fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976618"
---
# <span data-ttu-id="0d199-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0d199-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="0d199-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d199-102">SYNOPSIS</span></span>
<span data-ttu-id="0d199-103">Usuwa filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="0d199-103">Removes a route filter.</span></span>

## <span data-ttu-id="0d199-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0d199-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d199-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0d199-105">DESCRIPTION</span></span>
<span data-ttu-id="0d199-106">Polecenie **cmdlet Remove-AzRouteFilter** usuwa filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="0d199-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="0d199-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0d199-107">EXAMPLES</span></span>

### <span data-ttu-id="0d199-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0d199-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0d199-109">To polecenie usuwa filtr trasy o nazwie RouteFilter01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0d199-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="0d199-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d199-110">PARAMETERS</span></span>

### <span data-ttu-id="0d199-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d199-111">-DefaultProfile</span></span>
<span data-ttu-id="0d199-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d199-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d199-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0d199-113">-Force</span></span>
<span data-ttu-id="0d199-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0d199-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0d199-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0d199-115">-Name</span></span>
<span data-ttu-id="0d199-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="0d199-116">The resource name.</span></span>

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

### <span data-ttu-id="0d199-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d199-117">-PassThru</span></span>
<span data-ttu-id="0d199-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0d199-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="0d199-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d199-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d199-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0d199-120">The resource group name.</span></span>

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

### <span data-ttu-id="0d199-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0d199-121">-Confirm</span></span>
<span data-ttu-id="0d199-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0d199-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d199-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d199-123">-WhatIf</span></span>
<span data-ttu-id="0d199-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d199-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d199-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0d199-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d199-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d199-126">CommonParameters</span></span>
<span data-ttu-id="0d199-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d199-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d199-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d199-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d199-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d199-129">INPUTS</span></span>

### <span data-ttu-id="0d199-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0d199-130">System.String</span></span>

## <span data-ttu-id="0d199-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d199-131">OUTPUTS</span></span>

### <span data-ttu-id="0d199-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0d199-132">System.Boolean</span></span>

## <span data-ttu-id="0d199-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0d199-133">NOTES</span></span>

## <span data-ttu-id="0d199-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d199-134">RELATED LINKS</span></span>

[<span data-ttu-id="0d199-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0d199-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="0d199-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0d199-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="0d199-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0d199-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="0d199-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d199-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0d199-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d199-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0d199-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d199-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0d199-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d199-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0d199-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d199-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
