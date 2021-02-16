---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 93e97906fc7e985d522f5af9d678392741a9022b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187386"
---
# <span data-ttu-id="11164-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="11164-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="11164-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11164-102">SYNOPSIS</span></span>
<span data-ttu-id="11164-103">Aktualizacja dla prywatnego zakresu łączy</span><span class="sxs-lookup"><span data-stu-id="11164-103">Update for private link scope</span></span>

## <span data-ttu-id="11164-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11164-104">SYNTAX</span></span>

### <span data-ttu-id="11164-105">ByResourceNameParameterSet (Domyślny)</span><span class="sxs-lookup"><span data-stu-id="11164-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11164-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11164-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11164-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11164-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11164-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="11164-108">DESCRIPTION</span></span>
<span data-ttu-id="11164-109">Aktualizacja dla prywatnego zakresu łączy</span><span class="sxs-lookup"><span data-stu-id="11164-109">Update for private link scope</span></span>

## <span data-ttu-id="11164-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11164-110">EXAMPLES</span></span>

### <span data-ttu-id="11164-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="11164-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="11164-112">zaktualizuj zakres łącza prywatnego o nazwie "scope_name" w grupie zasobów "rg_name", aby użyć tagu "klucz:wartość"</span><span class="sxs-lookup"><span data-stu-id="11164-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="11164-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="11164-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="11164-114">Aktualizowanie zakresu łącza prywatnego przy użyciu identyfikatora zasobu w celu użycia tagu "klucz:wartość"</span><span class="sxs-lookup"><span data-stu-id="11164-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="11164-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="11164-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="11164-116">Aktualizowanie zakresu łącza prywatnego z wejściowym obiektem zakresu prywatnego linku w celu użycia tagu "klucz:wartość"</span><span class="sxs-lookup"><span data-stu-id="11164-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="11164-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11164-117">PARAMETERS</span></span>

### <span data-ttu-id="11164-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11164-118">-DefaultProfile</span></span>
<span data-ttu-id="11164-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11164-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11164-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11164-120">-InputObject</span></span>
<span data-ttu-id="11164-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="11164-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="11164-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="11164-122">-Name</span></span>
<span data-ttu-id="11164-123">Nazwa zakresu łącza prywatnego</span><span class="sxs-lookup"><span data-stu-id="11164-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="11164-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11164-124">-ResourceGroupName</span></span>
<span data-ttu-id="11164-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="11164-125">Resource Group Name</span></span>

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

### <span data-ttu-id="11164-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11164-126">-ResourceId</span></span>
<span data-ttu-id="11164-127">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="11164-127">Resource Id</span></span>

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

### <span data-ttu-id="11164-128">— Tagi</span><span class="sxs-lookup"><span data-stu-id="11164-128">-Tags</span></span>
<span data-ttu-id="11164-129">Tagi</span><span class="sxs-lookup"><span data-stu-id="11164-129">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11164-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11164-130">-Confirm</span></span>
<span data-ttu-id="11164-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="11164-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11164-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11164-132">-WhatIf</span></span>
<span data-ttu-id="11164-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11164-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11164-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="11164-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11164-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11164-135">CommonParameters</span></span>
<span data-ttu-id="11164-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11164-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11164-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11164-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11164-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11164-138">INPUTS</span></span>

### <span data-ttu-id="11164-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="11164-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="11164-140">System.String</span><span class="sxs-lookup"><span data-stu-id="11164-140">System.String</span></span>

## <span data-ttu-id="11164-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11164-141">OUTPUTS</span></span>

### <span data-ttu-id="11164-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="11164-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="11164-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11164-143">NOTES</span></span>

## <span data-ttu-id="11164-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11164-144">RELATED LINKS</span></span>
