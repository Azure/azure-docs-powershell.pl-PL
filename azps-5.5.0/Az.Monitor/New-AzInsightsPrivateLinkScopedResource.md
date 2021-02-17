---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: fd4dc0dd771029951da4ae375141cc526301de34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192178"
---
# <span data-ttu-id="f39df-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f39df-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="f39df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f39df-102">SYNOPSIS</span></span>
<span data-ttu-id="f39df-103">Tworzenie dla prywatnego zasobu z zakresem linków</span><span class="sxs-lookup"><span data-stu-id="f39df-103">create for private link scoped resource</span></span>

## <span data-ttu-id="f39df-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f39df-104">SYNTAX</span></span>

### <span data-ttu-id="f39df-105">ByResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f39df-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f39df-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f39df-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f39df-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f39df-107">DESCRIPTION</span></span>
<span data-ttu-id="f39df-108">Tworzenie dla zasobu prywatnego z zakresem linków, zasób o ograniczonych zakresach może być obszar roboczy analizy dziennika lub składnik Szczegółowych informacji o aplikacji</span><span class="sxs-lookup"><span data-stu-id="f39df-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="f39df-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f39df-109">EXAMPLES</span></span>

### <span data-ttu-id="f39df-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f39df-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="f39df-111">Tworzenie elementu "scoped_resource_name" z zakresem zasobów połączonego ze składnikiem "ai_name"</span><span class="sxs-lookup"><span data-stu-id="f39df-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="f39df-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f39df-112">PARAMETERS</span></span>

### <span data-ttu-id="f39df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f39df-113">-DefaultProfile</span></span>
<span data-ttu-id="f39df-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f39df-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f39df-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f39df-115">-InputObject</span></span>
<span data-ttu-id="f39df-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f39df-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="f39df-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="f39df-117">-LinkedResourceId</span></span>
<span data-ttu-id="f39df-118">Identyfikator zasobu LA/AI do połączenia</span><span class="sxs-lookup"><span data-stu-id="f39df-118">LA/AI Resource Id to Link</span></span>

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

### <span data-ttu-id="f39df-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f39df-119">-Name</span></span>
<span data-ttu-id="f39df-120">Nazwa zasobu o zakresie</span><span class="sxs-lookup"><span data-stu-id="f39df-120">Scoped resource Name</span></span>

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

### <span data-ttu-id="f39df-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f39df-121">-ResourceGroupName</span></span>
<span data-ttu-id="f39df-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f39df-122">Resource Group Name</span></span>

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

### <span data-ttu-id="f39df-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="f39df-123">-ScopeName</span></span>
<span data-ttu-id="f39df-124">Nazwa zakresu łącza prywatnego</span><span class="sxs-lookup"><span data-stu-id="f39df-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="f39df-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f39df-125">-Confirm</span></span>
<span data-ttu-id="f39df-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f39df-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f39df-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f39df-127">-WhatIf</span></span>
<span data-ttu-id="f39df-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f39df-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f39df-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f39df-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f39df-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f39df-130">CommonParameters</span></span>
<span data-ttu-id="f39df-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f39df-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f39df-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f39df-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f39df-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f39df-133">INPUTS</span></span>

### <span data-ttu-id="f39df-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f39df-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="f39df-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f39df-135">System.String</span></span>

## <span data-ttu-id="f39df-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f39df-136">OUTPUTS</span></span>

### <span data-ttu-id="f39df-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f39df-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="f39df-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f39df-138">NOTES</span></span>

## <span data-ttu-id="f39df-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f39df-139">RELATED LINKS</span></span>
