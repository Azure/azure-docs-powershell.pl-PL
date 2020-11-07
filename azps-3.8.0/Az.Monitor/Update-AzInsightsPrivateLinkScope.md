---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 93e97906fc7e985d522f5af9d678392741a9022b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894234"
---
# <span data-ttu-id="73f0c-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="73f0c-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="73f0c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="73f0c-103">Aktualizacja zakresu linków prywatnych</span><span class="sxs-lookup"><span data-stu-id="73f0c-103">Update for private link scope</span></span>

## <span data-ttu-id="73f0c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73f0c-104">SYNTAX</span></span>

### <span data-ttu-id="73f0c-105">ByResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="73f0c-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73f0c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73f0c-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73f0c-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73f0c-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73f0c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="73f0c-108">DESCRIPTION</span></span>
<span data-ttu-id="73f0c-109">Aktualizacja zakresu linków prywatnych</span><span class="sxs-lookup"><span data-stu-id="73f0c-109">Update for private link scope</span></span>

## <span data-ttu-id="73f0c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73f0c-110">EXAMPLES</span></span>

### <span data-ttu-id="73f0c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="73f0c-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="73f0c-112">Aktualizowanie zakresu linków prywatnych o nazwie "scope_name" w obszarze Grupa zasobów "rg_name", aby użyć tagu "Key: value"</span><span class="sxs-lookup"><span data-stu-id="73f0c-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="73f0c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="73f0c-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="73f0c-114">Aktualizowanie zakresu linków prywatnych za pomocą identyfikatora zasobu w celu użycia tagu "Key: value"</span><span class="sxs-lookup"><span data-stu-id="73f0c-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="73f0c-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="73f0c-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="73f0c-116">Aktualizowanie zakresu linków prywatnych za pomocą obiektu z wejściowym linkiem prywatnym w celu użycia tagu "Key: value"</span><span class="sxs-lookup"><span data-stu-id="73f0c-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="73f0c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73f0c-117">PARAMETERS</span></span>

### <span data-ttu-id="73f0c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f0c-118">-DefaultProfile</span></span>
<span data-ttu-id="73f0c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="73f0c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73f0c-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="73f0c-120">-InputObject</span></span>
<span data-ttu-id="73f0c-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="73f0c-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="73f0c-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="73f0c-122">-Name</span></span>
<span data-ttu-id="73f0c-123">Nazwa zakresu linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="73f0c-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="73f0c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73f0c-124">-ResourceGroupName</span></span>
<span data-ttu-id="73f0c-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="73f0c-125">Resource Group Name</span></span>

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

### <span data-ttu-id="73f0c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73f0c-126">-ResourceId</span></span>
<span data-ttu-id="73f0c-127">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="73f0c-127">Resource Id</span></span>

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

### <span data-ttu-id="73f0c-128">-Tagi</span><span class="sxs-lookup"><span data-stu-id="73f0c-128">-Tags</span></span>
<span data-ttu-id="73f0c-129">Kolczyk</span><span class="sxs-lookup"><span data-stu-id="73f0c-129">Tags</span></span>

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

### <span data-ttu-id="73f0c-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="73f0c-130">-Confirm</span></span>
<span data-ttu-id="73f0c-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73f0c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73f0c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73f0c-132">-WhatIf</span></span>
<span data-ttu-id="73f0c-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73f0c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73f0c-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="73f0c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73f0c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f0c-135">CommonParameters</span></span>
<span data-ttu-id="73f0c-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73f0c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f0c-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73f0c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f0c-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73f0c-138">INPUTS</span></span>

### <span data-ttu-id="73f0c-139">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="73f0c-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="73f0c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="73f0c-140">System.String</span></span>

## <span data-ttu-id="73f0c-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73f0c-141">OUTPUTS</span></span>

### <span data-ttu-id="73f0c-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="73f0c-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="73f0c-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73f0c-143">NOTES</span></span>

## <span data-ttu-id="73f0c-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73f0c-144">RELATED LINKS</span></span>
