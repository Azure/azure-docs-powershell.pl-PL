---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: f3d00ba82bbafce42cca49c60d443cd244f83df3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234523"
---
# <span data-ttu-id="73ee6-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="73ee6-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="73ee6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73ee6-102">SYNOPSIS</span></span>
<span data-ttu-id="73ee6-103">Pobieranie zasobu z zakresem linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="73ee6-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="73ee6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73ee6-104">SYNTAX</span></span>

### <span data-ttu-id="73ee6-105">ByScopeParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="73ee6-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73ee6-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73ee6-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73ee6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73ee6-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73ee6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="73ee6-108">DESCRIPTION</span></span>
<span data-ttu-id="73ee6-109">Uzyskiwanie lub wyświetlanie listy dla linku prywatnego z zakresem zasób z zakresem może być obszarem roboczym analizy dzienników lub składnikiem usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="73ee6-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="73ee6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73ee6-110">EXAMPLES</span></span>

### <span data-ttu-id="73ee6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="73ee6-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="73ee6-112">Zasób z zakresem listy w ramach prywatnego zakresu linków "scope_name"</span><span class="sxs-lookup"><span data-stu-id="73ee6-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="73ee6-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="73ee6-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="73ee6-114">Pobierz zasób z zakresu w zakresie linków prywatnych "scope_name" o nazwie "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="73ee6-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="73ee6-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73ee6-115">PARAMETERS</span></span>

### <span data-ttu-id="73ee6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73ee6-116">-DefaultProfile</span></span>
<span data-ttu-id="73ee6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="73ee6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73ee6-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="73ee6-118">-InputObject</span></span>
<span data-ttu-id="73ee6-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="73ee6-119">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="73ee6-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="73ee6-120">-Name</span></span>
<span data-ttu-id="73ee6-121">Nazwa zasobu z zakresem</span><span class="sxs-lookup"><span data-stu-id="73ee6-121">Scoped resource Name</span></span>

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

### <span data-ttu-id="73ee6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73ee6-122">-ResourceGroupName</span></span>
<span data-ttu-id="73ee6-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="73ee6-123">Resource Group Name</span></span>

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

### <span data-ttu-id="73ee6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73ee6-124">-ResourceId</span></span>
<span data-ttu-id="73ee6-125">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="73ee6-125">Resource Id</span></span>

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

### <span data-ttu-id="73ee6-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="73ee6-126">-ScopeName</span></span>
<span data-ttu-id="73ee6-127">Nazwa zakresu linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="73ee6-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="73ee6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73ee6-128">CommonParameters</span></span>
<span data-ttu-id="73ee6-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73ee6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73ee6-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73ee6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73ee6-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73ee6-131">INPUTS</span></span>

### <span data-ttu-id="73ee6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="73ee6-132">System.String</span></span>

## <span data-ttu-id="73ee6-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73ee6-133">OUTPUTS</span></span>

### <span data-ttu-id="73ee6-134">icrosoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="73ee6-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="73ee6-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73ee6-135">NOTES</span></span>

## <span data-ttu-id="73ee6-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73ee6-136">RELATED LINKS</span></span>
