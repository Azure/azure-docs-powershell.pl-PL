---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 93e97906fc7e985d522f5af9d678392741a9022b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062650"
---
# <span data-ttu-id="6fc6b-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="6fc6b-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="6fc6b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6fc6b-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc6b-103">Aktualizacja zakresu linków prywatnych</span><span class="sxs-lookup"><span data-stu-id="6fc6b-103">Update for private link scope</span></span>

## <span data-ttu-id="6fc6b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6fc6b-104">SYNTAX</span></span>

### <span data-ttu-id="6fc6b-105">ByResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6fc6b-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fc6b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fc6b-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fc6b-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fc6b-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fc6b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6fc6b-108">DESCRIPTION</span></span>
<span data-ttu-id="6fc6b-109">Aktualizacja zakresu linków prywatnych</span><span class="sxs-lookup"><span data-stu-id="6fc6b-109">Update for private link scope</span></span>

## <span data-ttu-id="6fc6b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6fc6b-110">EXAMPLES</span></span>

### <span data-ttu-id="6fc6b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6fc6b-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="6fc6b-112">Aktualizowanie zakresu linków prywatnych o nazwie "scope_name" w obszarze Grupa zasobów "rg_name", aby użyć tagu "Key: value"</span><span class="sxs-lookup"><span data-stu-id="6fc6b-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="6fc6b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6fc6b-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="6fc6b-114">Aktualizowanie zakresu linków prywatnych za pomocą identyfikatora zasobu w celu użycia tagu "Key: value"</span><span class="sxs-lookup"><span data-stu-id="6fc6b-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="6fc6b-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="6fc6b-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="6fc6b-116">Aktualizowanie zakresu linków prywatnych za pomocą obiektu z wejściowym linkiem prywatnym w celu użycia tagu "Key: value"</span><span class="sxs-lookup"><span data-stu-id="6fc6b-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="6fc6b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6fc6b-117">PARAMETERS</span></span>

### <span data-ttu-id="6fc6b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fc6b-118">-DefaultProfile</span></span>
<span data-ttu-id="6fc6b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fc6b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fc6b-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6fc6b-120">-InputObject</span></span>
<span data-ttu-id="6fc6b-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="6fc6b-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="6fc6b-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6fc6b-122">-Name</span></span>
<span data-ttu-id="6fc6b-123">Nazwa zakresu linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="6fc6b-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="6fc6b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fc6b-124">-ResourceGroupName</span></span>
<span data-ttu-id="6fc6b-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6fc6b-125">Resource Group Name</span></span>

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

### <span data-ttu-id="6fc6b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fc6b-126">-ResourceId</span></span>
<span data-ttu-id="6fc6b-127">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="6fc6b-127">Resource Id</span></span>

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

### <span data-ttu-id="6fc6b-128">-Tagi</span><span class="sxs-lookup"><span data-stu-id="6fc6b-128">-Tags</span></span>
<span data-ttu-id="6fc6b-129">Kolczyk</span><span class="sxs-lookup"><span data-stu-id="6fc6b-129">Tags</span></span>

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

### <span data-ttu-id="6fc6b-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6fc6b-130">-Confirm</span></span>
<span data-ttu-id="6fc6b-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fc6b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fc6b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fc6b-132">-WhatIf</span></span>
<span data-ttu-id="6fc6b-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fc6b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fc6b-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6fc6b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fc6b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc6b-135">CommonParameters</span></span>
<span data-ttu-id="6fc6b-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fc6b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc6b-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fc6b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc6b-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fc6b-138">INPUTS</span></span>

### <span data-ttu-id="6fc6b-139">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="6fc6b-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="6fc6b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6fc6b-140">System.String</span></span>

## <span data-ttu-id="6fc6b-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6fc6b-141">OUTPUTS</span></span>

### <span data-ttu-id="6fc6b-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="6fc6b-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="6fc6b-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6fc6b-143">NOTES</span></span>

## <span data-ttu-id="6fc6b-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fc6b-144">RELATED LINKS</span></span>
