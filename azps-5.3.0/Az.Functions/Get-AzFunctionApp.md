---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: a81bb1515e25f9000438fbd463117e4fd69b9690
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489678"
---
# <span data-ttu-id="6d8fe-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="6d8fe-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="6d8fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d8fe-102">SYNOPSIS</span></span>
<span data-ttu-id="6d8fe-103">Pobiera aplikacje funkcji w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="6d8fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d8fe-104">SYNTAX</span></span>

### <span data-ttu-id="6d8fe-105">GetAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6d8fe-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6d8fe-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="6d8fe-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d8fe-107">ByName</span><span class="sxs-lookup"><span data-stu-id="6d8fe-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6d8fe-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d8fe-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6d8fe-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6d8fe-109">DESCRIPTION</span></span>
<span data-ttu-id="6d8fe-110">Pobiera aplikacje funkcji w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="6d8fe-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d8fe-111">EXAMPLES</span></span>

### <span data-ttu-id="6d8fe-112">Przykład 1: pobieranie wszystkich aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="6d8fe-113">Przykład 2: Uzyskaj aplikacje funkcji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="6d8fe-114">Przykład 3: pobieranie aplikacji funkcji według nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="6d8fe-115">Przykład 4: pobieranie aplikacji funkcji dla danych subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="6d8fe-116">Przykład 5: pobieranie aplikacji funkcji według lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="6d8fe-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d8fe-117">PARAMETERS</span></span>

### <span data-ttu-id="6d8fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d8fe-118">-DefaultProfile</span></span>
<span data-ttu-id="6d8fe-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d8fe-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="6d8fe-120">-IncludeSlot</span></span>
<span data-ttu-id="6d8fe-121">Umożliwia określenie, czy w wynikach mają być uwzględniane gniazda wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-121">Use to specify whether to include deployment slots in results.</span></span>

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

### <span data-ttu-id="6d8fe-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6d8fe-122">-Location</span></span>
<span data-ttu-id="6d8fe-123">Lokalizacja aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-123">The location of the function app.</span></span>

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

### <span data-ttu-id="6d8fe-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6d8fe-124">-Name</span></span>
<span data-ttu-id="6d8fe-125">Nazwa aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-125">The name of the function app.</span></span>

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

### <span data-ttu-id="6d8fe-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d8fe-126">-ResourceGroupName</span></span>
<span data-ttu-id="6d8fe-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="6d8fe-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6d8fe-128">-SubscriptionId</span></span>
<span data-ttu-id="6d8fe-129">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="6d8fe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d8fe-130">CommonParameters</span></span>
<span data-ttu-id="6d8fe-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d8fe-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d8fe-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d8fe-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d8fe-133">INPUTS</span></span>

## <span data-ttu-id="6d8fe-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d8fe-134">OUTPUTS</span></span>

### <span data-ttu-id="6d8fe-135">Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="6d8fe-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="6d8fe-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d8fe-136">NOTES</span></span>

<span data-ttu-id="6d8fe-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="6d8fe-137">ALIASES</span></span>

## <span data-ttu-id="6d8fe-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d8fe-138">RELATED LINKS</span></span>

