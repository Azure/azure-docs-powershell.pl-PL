---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: f3d00ba82bbafce42cca49c60d443cd244f83df3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241210"
---
# <span data-ttu-id="5353a-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="5353a-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="5353a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5353a-102">SYNOPSIS</span></span>
<span data-ttu-id="5353a-103">Uzyskiwanie prywatnego zasobu z zakresem linków</span><span class="sxs-lookup"><span data-stu-id="5353a-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="5353a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5353a-104">SYNTAX</span></span>

### <span data-ttu-id="5353a-105">ByScopeParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5353a-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5353a-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5353a-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5353a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5353a-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5353a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5353a-108">DESCRIPTION</span></span>
<span data-ttu-id="5353a-109">Uzyskiwanie lub lista dla prywatnego zasobu z zakresem linków o zakresie zasobów może być obszarem roboczym analizy dziennika lub składnikiem Szczegółowych informacji o aplikacji</span><span class="sxs-lookup"><span data-stu-id="5353a-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="5353a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5353a-110">EXAMPLES</span></span>

### <span data-ttu-id="5353a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5353a-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="5353a-112">Zasób z zakresem listy w zakresie linków prywatnych "scope_name"</span><span class="sxs-lookup"><span data-stu-id="5353a-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="5353a-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5353a-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="5353a-114">Uzyskiwanie zasobu objętego zakresem w ramach prywatnego zakresu łączy "scope_name" o nazwie "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="5353a-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="5353a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5353a-115">PARAMETERS</span></span>

### <span data-ttu-id="5353a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5353a-116">-DefaultProfile</span></span>
<span data-ttu-id="5353a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5353a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5353a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5353a-118">-InputObject</span></span>
<span data-ttu-id="5353a-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="5353a-119">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5353a-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5353a-120">-Name</span></span>
<span data-ttu-id="5353a-121">Nazwa zasobu o zakresie</span><span class="sxs-lookup"><span data-stu-id="5353a-121">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5353a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5353a-122">-ResourceGroupName</span></span>
<span data-ttu-id="5353a-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5353a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="5353a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5353a-124">-ResourceId</span></span>
<span data-ttu-id="5353a-125">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="5353a-125">Resource Id</span></span>

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

### <span data-ttu-id="5353a-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="5353a-126">-ScopeName</span></span>
<span data-ttu-id="5353a-127">Nazwa zakresu łącza prywatnego</span><span class="sxs-lookup"><span data-stu-id="5353a-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="5353a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5353a-128">CommonParameters</span></span>
<span data-ttu-id="5353a-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5353a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5353a-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5353a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5353a-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5353a-131">INPUTS</span></span>

### <span data-ttu-id="5353a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5353a-132">System.String</span></span>

## <span data-ttu-id="5353a-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5353a-133">OUTPUTS</span></span>

### <span data-ttu-id="5353a-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="5353a-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="5353a-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5353a-135">NOTES</span></span>

## <span data-ttu-id="5353a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5353a-136">RELATED LINKS</span></span>
