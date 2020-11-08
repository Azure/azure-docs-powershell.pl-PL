---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: fd4dc0dd771029951da4ae375141cc526301de34
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233330"
---
# <span data-ttu-id="3fed1-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="3fed1-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="3fed1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3fed1-102">SYNOPSIS</span></span>
<span data-ttu-id="3fed1-103">Utwórz dla linku prywatnego zasób z zakresem</span><span class="sxs-lookup"><span data-stu-id="3fed1-103">create for private link scoped resource</span></span>

## <span data-ttu-id="3fed1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3fed1-104">SYNTAX</span></span>

### <span data-ttu-id="3fed1-105">ByResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3fed1-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3fed1-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fed1-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3fed1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3fed1-107">DESCRIPTION</span></span>
<span data-ttu-id="3fed1-108">Tworzenie dla linku prywatnego, zasób z zakresem może być obszarem roboczym analizy dzienników lub składnikiem usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="3fed1-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="3fed1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3fed1-109">EXAMPLES</span></span>

### <span data-ttu-id="3fed1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3fed1-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="3fed1-111">Utwórz zasób z zakresem "scoped_resource_name" połączony z składnikiem usługi Application Insights "ai_name"</span><span class="sxs-lookup"><span data-stu-id="3fed1-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="3fed1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3fed1-112">PARAMETERS</span></span>

### <span data-ttu-id="3fed1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fed1-113">-DefaultProfile</span></span>
<span data-ttu-id="3fed1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3fed1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fed1-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3fed1-115">-InputObject</span></span>
<span data-ttu-id="3fed1-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="3fed1-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="3fed1-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="3fed1-117">-LinkedResourceId</span></span>
<span data-ttu-id="3fed1-118">Identyfikator zasobu LA/AI do połączenia</span><span class="sxs-lookup"><span data-stu-id="3fed1-118">LA/AI Resource Id to Link</span></span>

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

### <span data-ttu-id="3fed1-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3fed1-119">-Name</span></span>
<span data-ttu-id="3fed1-120">Nazwa zasobu z zakresem</span><span class="sxs-lookup"><span data-stu-id="3fed1-120">Scoped resource Name</span></span>

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

### <span data-ttu-id="3fed1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fed1-121">-ResourceGroupName</span></span>
<span data-ttu-id="3fed1-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3fed1-122">Resource Group Name</span></span>

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

### <span data-ttu-id="3fed1-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="3fed1-123">-ScopeName</span></span>
<span data-ttu-id="3fed1-124">Nazwa zakresu linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="3fed1-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="3fed1-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3fed1-125">-Confirm</span></span>
<span data-ttu-id="3fed1-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fed1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fed1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fed1-127">-WhatIf</span></span>
<span data-ttu-id="3fed1-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fed1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fed1-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3fed1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fed1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fed1-130">CommonParameters</span></span>
<span data-ttu-id="3fed1-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fed1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fed1-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fed1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fed1-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fed1-133">INPUTS</span></span>

### <span data-ttu-id="3fed1-134">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="3fed1-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="3fed1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3fed1-135">System.String</span></span>

## <span data-ttu-id="3fed1-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3fed1-136">OUTPUTS</span></span>

### <span data-ttu-id="3fed1-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="3fed1-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="3fed1-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3fed1-138">NOTES</span></span>

## <span data-ttu-id="3fed1-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fed1-139">RELATED LINKS</span></span>
