---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: ee678b905eba891543399c9130a8ef034daf2a16
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969098"
---
# <span data-ttu-id="d7da8-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="d7da8-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="d7da8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7da8-102">SYNOPSIS</span></span>
<span data-ttu-id="d7da8-103">Pobiera aplikacje funkcyjne w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d7da8-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="d7da8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d7da8-104">SYNTAX</span></span>

### <span data-ttu-id="d7da8-105">PobierzWszystko (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d7da8-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d7da8-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="d7da8-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7da8-107">ByName</span><span class="sxs-lookup"><span data-stu-id="d7da8-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d7da8-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7da8-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d7da8-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="d7da8-109">DESCRIPTION</span></span>
<span data-ttu-id="d7da8-110">Pobiera aplikacje funkcyjne w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d7da8-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="d7da8-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d7da8-111">EXAMPLES</span></span>

### <span data-ttu-id="d7da8-112">Przykład 1. Pobierz wszystkie aplikacje funkcyjne.</span><span class="sxs-lookup"><span data-stu-id="d7da8-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="d7da8-113">Przykład 2. Uzyskiwanie aplikacji funkowych według nazwy.</span><span class="sxs-lookup"><span data-stu-id="d7da8-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="d7da8-114">Przykład 3. Uzyskiwanie aplikacji funkowych według nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d7da8-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="d7da8-115">Przykład 4. Pobierz aplikacje funkcyjne dla danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d7da8-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="d7da8-116">Przykład 5. Pobierz aplikacje funkcyjne według lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d7da8-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="d7da8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7da8-117">PARAMETERS</span></span>

### <span data-ttu-id="d7da8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7da8-118">-DefaultProfile</span></span>
<span data-ttu-id="d7da8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7da8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7da8-120">— IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="d7da8-120">-IncludeSlot</span></span>
<span data-ttu-id="d7da8-121">Umożliwia określenie, czy w wynikach mają być uwzględniane miejsca wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d7da8-121">Use to specify whether to include deployment slots in results.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7da8-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d7da8-122">-Location</span></span>
<span data-ttu-id="d7da8-123">Lokalizacja aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="d7da8-123">The location of the function app.</span></span>

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

### <span data-ttu-id="d7da8-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d7da8-124">-Name</span></span>
<span data-ttu-id="d7da8-125">Nazwa aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="d7da8-125">The name of the function app.</span></span>

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

### <span data-ttu-id="d7da8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7da8-126">-ResourceGroupName</span></span>
<span data-ttu-id="d7da8-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d7da8-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="d7da8-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7da8-128">-SubscriptionId</span></span>
<span data-ttu-id="d7da8-129">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d7da8-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="d7da8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7da8-130">CommonParameters</span></span>
<span data-ttu-id="d7da8-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7da8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7da8-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7da8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7da8-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7da8-133">INPUTS</span></span>

## <span data-ttu-id="d7da8-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7da8-134">OUTPUTS</span></span>

### <span data-ttu-id="d7da8-135">Microsoft.Azure.PowerShell.cmdlet.functions.models.api20190801.iSite</span><span class="sxs-lookup"><span data-stu-id="d7da8-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="d7da8-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d7da8-136">NOTES</span></span>

<span data-ttu-id="d7da8-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d7da8-137">ALIASES</span></span>

## <span data-ttu-id="d7da8-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7da8-138">RELATED LINKS</span></span>

