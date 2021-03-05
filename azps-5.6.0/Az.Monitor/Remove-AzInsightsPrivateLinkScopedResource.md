---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: 83f4fae326920b24d272ae87341c20702a2bf8fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003745"
---
# <span data-ttu-id="fc765-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="fc765-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="fc765-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc765-102">SYNOPSIS</span></span>
<span data-ttu-id="fc765-103">Delete for private link scoped resource</span><span class="sxs-lookup"><span data-stu-id="fc765-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="fc765-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fc765-104">SYNTAX</span></span>

### <span data-ttu-id="fc765-105">ByScopeParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="fc765-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc765-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc765-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc765-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc765-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc765-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fc765-108">DESCRIPTION</span></span>
<span data-ttu-id="fc765-109">Delete for private link scoped resource</span><span class="sxs-lookup"><span data-stu-id="fc765-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="fc765-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fc765-110">EXAMPLES</span></span>

### <span data-ttu-id="fc765-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fc765-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="fc765-112">Usuwanie zasobu z zakresem łącza prywatnego</span><span class="sxs-lookup"><span data-stu-id="fc765-112">delete private link scoped resource</span></span>

## <span data-ttu-id="fc765-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc765-113">PARAMETERS</span></span>

### <span data-ttu-id="fc765-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc765-114">-DefaultProfile</span></span>
<span data-ttu-id="fc765-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc765-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc765-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc765-116">-InputObject</span></span>
<span data-ttu-id="fc765-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="fc765-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="fc765-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fc765-118">-Name</span></span>
<span data-ttu-id="fc765-119">Nazwa zasobu o zakresie</span><span class="sxs-lookup"><span data-stu-id="fc765-119">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc765-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc765-120">-ResourceGroupName</span></span>
<span data-ttu-id="fc765-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fc765-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc765-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc765-122">-ResourceId</span></span>
<span data-ttu-id="fc765-123">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="fc765-123">Resource Id</span></span>

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

### <span data-ttu-id="fc765-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="fc765-124">-ScopeName</span></span>
<span data-ttu-id="fc765-125">Nazwa zakresu łącza prywatnego</span><span class="sxs-lookup"><span data-stu-id="fc765-125">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc765-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc765-126">-Confirm</span></span>
<span data-ttu-id="fc765-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fc765-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc765-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc765-128">-WhatIf</span></span>
<span data-ttu-id="fc765-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc765-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc765-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fc765-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc765-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc765-131">CommonParameters</span></span>
<span data-ttu-id="fc765-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc765-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc765-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc765-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc765-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc765-134">INPUTS</span></span>

### <span data-ttu-id="fc765-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="fc765-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="fc765-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fc765-136">System.String</span></span>

## <span data-ttu-id="fc765-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc765-137">OUTPUTS</span></span>

### <span data-ttu-id="fc765-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fc765-138">System.Boolean</span></span>

## <span data-ttu-id="fc765-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fc765-139">NOTES</span></span>

## <span data-ttu-id="fc765-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc765-140">RELATED LINKS</span></span>
