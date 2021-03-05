---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: 10ae3aab71cd977d3447501d13870eb10a8129ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009505"
---
# <span data-ttu-id="f3c63-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f3c63-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="f3c63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3c63-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c63-103">Tworzenie dla prywatnego zasobu z zakresem linków</span><span class="sxs-lookup"><span data-stu-id="f3c63-103">create for private link scoped resource</span></span>

## <span data-ttu-id="f3c63-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f3c63-104">SYNTAX</span></span>

### <span data-ttu-id="f3c63-105">ByResourceNameParameterSet (Domyślny)</span><span class="sxs-lookup"><span data-stu-id="f3c63-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3c63-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3c63-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3c63-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f3c63-107">DESCRIPTION</span></span>
<span data-ttu-id="f3c63-108">Tworzenie dla prywatnego zasobu z zakresem łączy zasób o ograniczonych zakresach może być obszarem roboczym analizy dziennika lub składnikiem Szczegółowych informacji o aplikacji</span><span class="sxs-lookup"><span data-stu-id="f3c63-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="f3c63-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f3c63-109">EXAMPLES</span></span>

### <span data-ttu-id="f3c63-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f3c63-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="f3c63-111">Tworzenie elementu "scoped_resource_name" z zakresem zasobów połączonego ze składnikiem "ai_name"</span><span class="sxs-lookup"><span data-stu-id="f3c63-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="f3c63-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3c63-112">PARAMETERS</span></span>

### <span data-ttu-id="f3c63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c63-113">-DefaultProfile</span></span>
<span data-ttu-id="f3c63-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3c63-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3c63-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3c63-115">-InputObject</span></span>
<span data-ttu-id="f3c63-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f3c63-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="f3c63-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="f3c63-117">-LinkedResourceId</span></span>
<span data-ttu-id="f3c63-118">Identyfikator zasobu LA/AI do połączenia</span><span class="sxs-lookup"><span data-stu-id="f3c63-118">LA/AI Resource Id to Link</span></span>

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

### <span data-ttu-id="f3c63-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f3c63-119">-Name</span></span>
<span data-ttu-id="f3c63-120">Nazwa zasobu o zakresie</span><span class="sxs-lookup"><span data-stu-id="f3c63-120">Scoped resource Name</span></span>

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

### <span data-ttu-id="f3c63-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3c63-121">-ResourceGroupName</span></span>
<span data-ttu-id="f3c63-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f3c63-122">Resource Group Name</span></span>

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

### <span data-ttu-id="f3c63-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="f3c63-123">-ScopeName</span></span>
<span data-ttu-id="f3c63-124">Nazwa zakresu łącza prywatnego</span><span class="sxs-lookup"><span data-stu-id="f3c63-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="f3c63-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3c63-125">-Confirm</span></span>
<span data-ttu-id="f3c63-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f3c63-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3c63-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3c63-127">-WhatIf</span></span>
<span data-ttu-id="f3c63-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3c63-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3c63-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f3c63-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3c63-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c63-130">CommonParameters</span></span>
<span data-ttu-id="f3c63-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3c63-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c63-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3c63-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c63-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3c63-133">INPUTS</span></span>

### <span data-ttu-id="f3c63-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f3c63-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="f3c63-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f3c63-135">System.String</span></span>

## <span data-ttu-id="f3c63-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3c63-136">OUTPUTS</span></span>

### <span data-ttu-id="f3c63-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f3c63-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="f3c63-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f3c63-138">NOTES</span></span>

## <span data-ttu-id="f3c63-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3c63-139">RELATED LINKS</span></span>
