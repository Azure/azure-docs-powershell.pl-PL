---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 8f48cf6fb5b3c4489a116ef0f7ee5a32649d96ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869680"
---
# <span data-ttu-id="7d8a8-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7d8a8-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="7d8a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d8a8-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8a8-103">Usuwa filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="7d8a8-103">Removes a route filter.</span></span>

## <span data-ttu-id="7d8a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d8a8-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d8a8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7d8a8-105">DESCRIPTION</span></span>
<span data-ttu-id="7d8a8-106">Polecenie cmdlet **Remove-AzRouteFilter** usuwa filtr trasy.</span><span class="sxs-lookup"><span data-stu-id="7d8a8-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="7d8a8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d8a8-107">EXAMPLES</span></span>

### <span data-ttu-id="7d8a8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7d8a8-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7d8a8-109">Polecenie usuwa filtr trasy o nazwie RouteFilter01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="7d8a8-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="7d8a8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d8a8-110">PARAMETERS</span></span>

### <span data-ttu-id="7d8a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8a8-111">-DefaultProfile</span></span>
<span data-ttu-id="7d8a8-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8a8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d8a8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7d8a8-113">-Force</span></span>
<span data-ttu-id="7d8a8-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7d8a8-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7d8a8-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7d8a8-115">-Name</span></span>
<span data-ttu-id="7d8a8-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="7d8a8-116">The resource name.</span></span>

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

### <span data-ttu-id="7d8a8-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d8a8-117">-PassThru</span></span>
<span data-ttu-id="7d8a8-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="7d8a8-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="7d8a8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d8a8-119">-ResourceGroupName</span></span>
<span data-ttu-id="7d8a8-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7d8a8-120">The resource group name.</span></span>

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

### <span data-ttu-id="7d8a8-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7d8a8-121">-Confirm</span></span>
<span data-ttu-id="7d8a8-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d8a8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d8a8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d8a8-123">-WhatIf</span></span>
<span data-ttu-id="7d8a8-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d8a8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d8a8-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7d8a8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d8a8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8a8-126">CommonParameters</span></span>
<span data-ttu-id="7d8a8-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d8a8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8a8-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d8a8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8a8-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d8a8-129">INPUTS</span></span>

### <span data-ttu-id="7d8a8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7d8a8-130">System.String</span></span>

## <span data-ttu-id="7d8a8-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d8a8-131">OUTPUTS</span></span>

### <span data-ttu-id="7d8a8-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7d8a8-132">System.Boolean</span></span>

## <span data-ttu-id="7d8a8-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d8a8-133">NOTES</span></span>

## <span data-ttu-id="7d8a8-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d8a8-134">RELATED LINKS</span></span>

[<span data-ttu-id="7d8a8-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7d8a8-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="7d8a8-136">Nowe — AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7d8a8-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="7d8a8-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7d8a8-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="7d8a8-138">Dodaj-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d8a8-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7d8a8-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d8a8-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7d8a8-140">Nowe — AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d8a8-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7d8a8-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d8a8-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7d8a8-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d8a8-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
