---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
ms.openlocfilehash: 786f3e406228eb7929993804a8cef84e7cae109e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969082"
---
# <span data-ttu-id="a3a30-101">Get-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="a3a30-101">Get-AzFunctionAppPlan</span></span>

## <span data-ttu-id="a3a30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3a30-102">SYNOPSIS</span></span>
<span data-ttu-id="a3a30-103">Pobierz plany aplikacji funkowych w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a3a30-103">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="a3a30-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a3a30-104">SYNTAX</span></span>

### <span data-ttu-id="a3a30-105">PobierzWszystko (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a3a30-105">GetAll (Default)</span></span>
```
Get-AzFunctionAppPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a3a30-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="a3a30-106">ByLocation</span></span>
```
Get-AzFunctionAppPlan -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3a30-107">ByName</span><span class="sxs-lookup"><span data-stu-id="a3a30-107">ByName</span></span>
```
Get-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a3a30-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3a30-108">ByResourceGroupName</span></span>
```
Get-AzFunctionAppPlan [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3a30-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="a3a30-109">DESCRIPTION</span></span>
<span data-ttu-id="a3a30-110">Pobierz plany aplikacji funkowych w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a3a30-110">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="a3a30-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a3a30-111">EXAMPLES</span></span>

### <span data-ttu-id="a3a30-112">Przykład 1. Pobierz wszystkie plany aplikacji funkcyjnych.</span><span class="sxs-lookup"><span data-stu-id="a3a30-112">Example 1: Get all function app plans.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium428118799    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium677505437    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium711892854    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium819994758    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="a3a30-113">To polecenie pobiera wszystkie plany aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="a3a30-113">This command gets all function app plans.</span></span>

### <span data-ttu-id="a3a30-114">Przykład 2. Uzyskiwanie planów aplikacji funkowych według nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3a30-114">Example 2: Get function app plans by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -ResourceGroupName "West Europe"

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="a3a30-115">To polecenie pobiera plany aplikacji funkcji według nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3a30-115">This command gets function app plans by resource group name.</span></span>

### <span data-ttu-id="a3a30-116">Przykład 3. Uzyskiwanie planów aplikacji funkowych dla danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a3a30-116">Example 3: Get function app plans for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8z

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8z
```

<span data-ttu-id="a3a30-117">To polecenie pobiera plany aplikacji funkcji dla danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a3a30-117">This command gets function app plans for the given subscriptions.</span></span>

### <span data-ttu-id="a3a30-118">Przykład 4. Uzyskiwanie planów aplikacji funkowych według lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a3a30-118">Example 4: Get function app plans by location.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Location "Central US"

Name                               WorkerType SkuTier        SkuName Location   ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------   -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     Central US Func99-West-Europe-Win-Premium   3r16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="a3a30-119">To polecenie pobiera plany aplikacji funkcji według lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a3a30-119">This command gets function app plans by location.</span></span>

## <span data-ttu-id="a3a30-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3a30-120">PARAMETERS</span></span>

### <span data-ttu-id="a3a30-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3a30-121">-DefaultProfile</span></span>
<span data-ttu-id="a3a30-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3a30-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a30-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a3a30-123">-Location</span></span>
<span data-ttu-id="a3a30-124">Lokalizacja planu aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="a3a30-124">The location of the function app plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a30-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a3a30-125">-Name</span></span>
<span data-ttu-id="a3a30-126">Nazwa planu serwisowego.</span><span class="sxs-lookup"><span data-stu-id="a3a30-126">The service plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a30-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3a30-127">-ResourceGroupName</span></span>
<span data-ttu-id="a3a30-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3a30-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a30-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3a30-129">-SubscriptionId</span></span>
<span data-ttu-id="a3a30-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a3a30-130">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a30-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3a30-131">CommonParameters</span></span>
<span data-ttu-id="a3a30-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3a30-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3a30-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3a30-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3a30-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3a30-134">INPUTS</span></span>

## <span data-ttu-id="a3a30-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3a30-135">OUTPUTS</span></span>

### <span data-ttu-id="a3a30-136">Microsoft.Azure.PowerShell.Cmdlet.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a3a30-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="a3a30-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a3a30-137">NOTES</span></span>

<span data-ttu-id="a3a30-138">ALIASY</span><span class="sxs-lookup"><span data-stu-id="a3a30-138">ALIASES</span></span>

## <span data-ttu-id="a3a30-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3a30-139">RELATED LINKS</span></span>

