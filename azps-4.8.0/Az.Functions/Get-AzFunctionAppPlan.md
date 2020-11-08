---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
ms.openlocfilehash: d08d050253842e13967d001889e1b7d1b331ce17
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222541"
---
# <span data-ttu-id="b7a8f-101">Get-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="b7a8f-101">Get-AzFunctionAppPlan</span></span>

## <span data-ttu-id="b7a8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a8f-103">Pobierz aplikacje funkcyjne plany w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-103">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="b7a8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7a8f-104">SYNTAX</span></span>

### <span data-ttu-id="b7a8f-105">GetAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b7a8f-105">GetAll (Default)</span></span>
```
Get-AzFunctionAppPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b7a8f-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="b7a8f-106">ByLocation</span></span>
```
Get-AzFunctionAppPlan -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7a8f-107">ByName</span><span class="sxs-lookup"><span data-stu-id="b7a8f-107">ByName</span></span>
```
Get-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b7a8f-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7a8f-108">ByResourceGroupName</span></span>
```
Get-AzFunctionAppPlan [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7a8f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b7a8f-109">DESCRIPTION</span></span>
<span data-ttu-id="b7a8f-110">Pobierz aplikacje funkcyjne plany w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-110">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="b7a8f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7a8f-111">EXAMPLES</span></span>

### <span data-ttu-id="b7a8f-112">Przykład 1: Pobierz wszystkie plany aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-112">Example 1: Get all function app plans.</span></span>
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

<span data-ttu-id="b7a8f-113">To polecenie pobiera wszystkie plany aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-113">This command gets all function app plans.</span></span>

### <span data-ttu-id="b7a8f-114">Przykład 2: Pobieranie funkcji planów aplikacji według nazw grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-114">Example 2: Get function app plans by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -ResourceGroupName "West Europe"

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="b7a8f-115">To polecenie pobiera za pomocą nazwy grupy zasobów funkcji plany aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-115">This command gets function app plans by resource group name.</span></span>

### <span data-ttu-id="b7a8f-116">Przykład 3: Pobieranie funkcji planów aplikacji dla podanych subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-116">Example 3: Get function app plans for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8z

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8z
```

<span data-ttu-id="b7a8f-117">To polecenie pobiera plany aplikacji dotyczące danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-117">This command gets function app plans for the given subscriptions.</span></span>

### <span data-ttu-id="b7a8f-118">Przykład 4: Pobieranie funkcji planów aplikacji według lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-118">Example 4: Get function app plans by location.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Location "Central US"

Name                               WorkerType SkuTier        SkuName Location   ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------   -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     Central US Func99-West-Europe-Win-Premium   3r16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="b7a8f-119">To polecenie pobiera za pomocą funkcji plany aplikacji według lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-119">This command gets function app plans by location.</span></span>

## <span data-ttu-id="b7a8f-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7a8f-120">PARAMETERS</span></span>

### <span data-ttu-id="b7a8f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7a8f-121">-DefaultProfile</span></span>
<span data-ttu-id="b7a8f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7a8f-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b7a8f-123">-Location</span></span>
<span data-ttu-id="b7a8f-124">Lokalizacja planu aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-124">The location of the function app plan.</span></span>

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

### <span data-ttu-id="b7a8f-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b7a8f-125">-Name</span></span>
<span data-ttu-id="b7a8f-126">Nazwa planu usługi.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-126">The service plan name.</span></span>

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

### <span data-ttu-id="b7a8f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7a8f-127">-ResourceGroupName</span></span>
<span data-ttu-id="b7a8f-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7a8f-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b7a8f-129">-SubscriptionId</span></span>
<span data-ttu-id="b7a8f-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="b7a8f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a8f-131">CommonParameters</span></span>
<span data-ttu-id="b7a8f-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a8f-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7a8f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a8f-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7a8f-134">INPUTS</span></span>

## <span data-ttu-id="b7a8f-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7a8f-135">OUTPUTS</span></span>

### <span data-ttu-id="b7a8f-136">Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b7a8f-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="b7a8f-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7a8f-137">NOTES</span></span>

<span data-ttu-id="b7a8f-138">PISUJE</span><span class="sxs-lookup"><span data-stu-id="b7a8f-138">ALIASES</span></span>

## <span data-ttu-id="b7a8f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7a8f-139">RELATED LINKS</span></span>

