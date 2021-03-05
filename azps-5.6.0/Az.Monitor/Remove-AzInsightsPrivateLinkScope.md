---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: af33bf23e6cd488f98e38c9bd2696029b5510aca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984509"
---
# <span data-ttu-id="912f4-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="912f4-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="912f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="912f4-102">SYNOPSIS</span></span>
<span data-ttu-id="912f4-103">Usuwanie zakresu prywatnego linku</span><span class="sxs-lookup"><span data-stu-id="912f4-103">delete private link scope</span></span>

## <span data-ttu-id="912f4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="912f4-104">SYNTAX</span></span>

### <span data-ttu-id="912f4-105">ByResourceNameParameterSet (Domyślny)</span><span class="sxs-lookup"><span data-stu-id="912f4-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="912f4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="912f4-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="912f4-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="912f4-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="912f4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="912f4-108">DESCRIPTION</span></span>
<span data-ttu-id="912f4-109">Usuwanie zakresu prywatnego linku</span><span class="sxs-lookup"><span data-stu-id="912f4-109">delete private link scope</span></span>

## <span data-ttu-id="912f4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="912f4-110">EXAMPLES</span></span>

### <span data-ttu-id="912f4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="912f4-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="912f4-112">Usuwanie zakresu prywatnego linku o nazwie "scope_name" w grupie zasobów "rg_name"</span><span class="sxs-lookup"><span data-stu-id="912f4-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="912f4-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="912f4-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="912f4-114">Usuwanie zakresu łącza prywatnego przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="912f4-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="912f4-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="912f4-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="912f4-116">Usuwanie prywatnego zakresu łączy z obiektem wejściowego zakresu łącza prywatnego</span><span class="sxs-lookup"><span data-stu-id="912f4-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="912f4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="912f4-117">PARAMETERS</span></span>

### <span data-ttu-id="912f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="912f4-118">-DefaultProfile</span></span>
<span data-ttu-id="912f4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="912f4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="912f4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="912f4-120">-InputObject</span></span>
<span data-ttu-id="912f4-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="912f4-121">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="912f4-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="912f4-122">-Name</span></span>
<span data-ttu-id="912f4-123">Nazwa zakresu łącza prywatnego</span><span class="sxs-lookup"><span data-stu-id="912f4-123">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="912f4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="912f4-124">-ResourceGroupName</span></span>
<span data-ttu-id="912f4-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="912f4-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="912f4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="912f4-126">-ResourceId</span></span>
<span data-ttu-id="912f4-127">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="912f4-127">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="912f4-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="912f4-128">-Confirm</span></span>
<span data-ttu-id="912f4-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="912f4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="912f4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="912f4-130">-WhatIf</span></span>
<span data-ttu-id="912f4-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="912f4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="912f4-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="912f4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="912f4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="912f4-133">CommonParameters</span></span>
<span data-ttu-id="912f4-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="912f4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="912f4-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="912f4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="912f4-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="912f4-136">INPUTS</span></span>

### <span data-ttu-id="912f4-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="912f4-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="912f4-138">System.String</span><span class="sxs-lookup"><span data-stu-id="912f4-138">System.String</span></span>

## <span data-ttu-id="912f4-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="912f4-139">OUTPUTS</span></span>

### <span data-ttu-id="912f4-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="912f4-140">System.Boolean</span></span>

## <span data-ttu-id="912f4-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="912f4-141">NOTES</span></span>

## <span data-ttu-id="912f4-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="912f4-142">RELATED LINKS</span></span>
