---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: ff4e75e2301ef9ae2ccd6f2e5064e06aedc2dbd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980042"
---
# <span data-ttu-id="d5df9-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="d5df9-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="d5df9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5df9-102">SYNOPSIS</span></span>
<span data-ttu-id="d5df9-103">Uzyskiwanie prywatnego zasobu z zakresem linków</span><span class="sxs-lookup"><span data-stu-id="d5df9-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="d5df9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d5df9-104">SYNTAX</span></span>

### <span data-ttu-id="d5df9-105">ByScopeParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d5df9-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5df9-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5df9-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5df9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5df9-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5df9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d5df9-108">DESCRIPTION</span></span>
<span data-ttu-id="d5df9-109">Uzyskiwanie lub lista dla prywatnego zasobu z zakresem linków, zasób o ograniczonych zakresach może być obszarem roboczym analizy dziennika lub składnikiem Szczegółowych informacji o aplikacji</span><span class="sxs-lookup"><span data-stu-id="d5df9-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="d5df9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d5df9-110">EXAMPLES</span></span>

### <span data-ttu-id="d5df9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d5df9-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="d5df9-112">Zasób o zakresie listy w zakresie linków prywatnych "scope_name"</span><span class="sxs-lookup"><span data-stu-id="d5df9-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="d5df9-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d5df9-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="d5df9-114">Uzyskiwanie zasobu objętego zakresem w ramach prywatnego zakresu łączy "scope_name" o nazwie "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="d5df9-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="d5df9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5df9-115">PARAMETERS</span></span>

### <span data-ttu-id="d5df9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5df9-116">-DefaultProfile</span></span>
<span data-ttu-id="d5df9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5df9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5df9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5df9-118">-InputObject</span></span>
<span data-ttu-id="d5df9-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d5df9-119">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="d5df9-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d5df9-120">-Name</span></span>
<span data-ttu-id="d5df9-121">Nazwa zasobu o zakresie</span><span class="sxs-lookup"><span data-stu-id="d5df9-121">Scoped resource Name</span></span>

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

### <span data-ttu-id="d5df9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5df9-122">-ResourceGroupName</span></span>
<span data-ttu-id="d5df9-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d5df9-123">Resource Group Name</span></span>

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

### <span data-ttu-id="d5df9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5df9-124">-ResourceId</span></span>
<span data-ttu-id="d5df9-125">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="d5df9-125">Resource Id</span></span>

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

### <span data-ttu-id="d5df9-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="d5df9-126">-ScopeName</span></span>
<span data-ttu-id="d5df9-127">Nazwa zakresu łącza prywatnego</span><span class="sxs-lookup"><span data-stu-id="d5df9-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="d5df9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5df9-128">CommonParameters</span></span>
<span data-ttu-id="d5df9-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5df9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5df9-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5df9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5df9-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5df9-131">INPUTS</span></span>

### <span data-ttu-id="d5df9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d5df9-132">System.String</span></span>

## <span data-ttu-id="d5df9-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5df9-133">OUTPUTS</span></span>

### <span data-ttu-id="d5df9-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="d5df9-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="d5df9-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d5df9-135">NOTES</span></span>

## <span data-ttu-id="d5df9-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5df9-136">RELATED LINKS</span></span>
