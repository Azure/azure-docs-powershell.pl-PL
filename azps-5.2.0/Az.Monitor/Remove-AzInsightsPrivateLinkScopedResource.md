---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323330"
---
# <span data-ttu-id="7a0ba-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="7a0ba-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="7a0ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a0ba-102">SYNOPSIS</span></span>
<span data-ttu-id="7a0ba-103">Usuń dla linku prywatnego zasób z zakresem</span><span class="sxs-lookup"><span data-stu-id="7a0ba-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="7a0ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a0ba-104">SYNTAX</span></span>

### <span data-ttu-id="7a0ba-105">ByScopeParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7a0ba-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a0ba-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0ba-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a0ba-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0ba-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a0ba-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7a0ba-108">DESCRIPTION</span></span>
<span data-ttu-id="7a0ba-109">Usuń dla linku prywatnego zasób z zakresem</span><span class="sxs-lookup"><span data-stu-id="7a0ba-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="7a0ba-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a0ba-110">EXAMPLES</span></span>

### <span data-ttu-id="7a0ba-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7a0ba-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="7a0ba-112">Usuwanie zasobu z zakresem linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="7a0ba-112">delete private link scoped resource</span></span>

## <span data-ttu-id="7a0ba-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a0ba-113">PARAMETERS</span></span>

### <span data-ttu-id="7a0ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a0ba-114">-DefaultProfile</span></span>
<span data-ttu-id="7a0ba-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a0ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a0ba-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7a0ba-116">-InputObject</span></span>
<span data-ttu-id="7a0ba-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="7a0ba-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="7a0ba-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7a0ba-118">-Name</span></span>
<span data-ttu-id="7a0ba-119">Nazwa zasobu z zakresem</span><span class="sxs-lookup"><span data-stu-id="7a0ba-119">Scoped resource Name</span></span>

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

### <span data-ttu-id="7a0ba-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a0ba-120">-ResourceGroupName</span></span>
<span data-ttu-id="7a0ba-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7a0ba-121">Resource Group Name</span></span>

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

### <span data-ttu-id="7a0ba-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a0ba-122">-ResourceId</span></span>
<span data-ttu-id="7a0ba-123">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="7a0ba-123">Resource Id</span></span>

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

### <span data-ttu-id="7a0ba-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="7a0ba-124">-ScopeName</span></span>
<span data-ttu-id="7a0ba-125">Nazwa zakresu linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="7a0ba-125">Private Link Scope Name</span></span>

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

### <span data-ttu-id="7a0ba-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a0ba-126">-Confirm</span></span>
<span data-ttu-id="7a0ba-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a0ba-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a0ba-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a0ba-128">-WhatIf</span></span>
<span data-ttu-id="7a0ba-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a0ba-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a0ba-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7a0ba-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a0ba-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a0ba-131">CommonParameters</span></span>
<span data-ttu-id="7a0ba-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a0ba-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a0ba-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a0ba-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a0ba-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a0ba-134">INPUTS</span></span>

### <span data-ttu-id="7a0ba-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="7a0ba-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="7a0ba-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7a0ba-136">System.String</span></span>

## <span data-ttu-id="7a0ba-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a0ba-137">OUTPUTS</span></span>

### <span data-ttu-id="7a0ba-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7a0ba-138">System.Boolean</span></span>

## <span data-ttu-id="7a0ba-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a0ba-139">NOTES</span></span>

## <span data-ttu-id="7a0ba-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a0ba-140">RELATED LINKS</span></span>
