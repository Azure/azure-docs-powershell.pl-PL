---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: 6a3a421f1da374db1cc08635891bdeec4375855a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221738"
---
# <span data-ttu-id="933f7-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="933f7-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="933f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="933f7-102">SYNOPSIS</span></span>
<span data-ttu-id="933f7-103">Pobiera aplikacje funkcji w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="933f7-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="933f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="933f7-104">SYNTAX</span></span>

### <span data-ttu-id="933f7-105">GetAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="933f7-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-IncludeSlot] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="933f7-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="933f7-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-IncludeSlot] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="933f7-107">ByName</span><span class="sxs-lookup"><span data-stu-id="933f7-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="933f7-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="933f7-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="933f7-109">Opis</span><span class="sxs-lookup"><span data-stu-id="933f7-109">DESCRIPTION</span></span>
<span data-ttu-id="933f7-110">Pobiera aplikacje funkcji w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="933f7-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="933f7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="933f7-111">EXAMPLES</span></span>

### <span data-ttu-id="933f7-112">Przykład 1: pobieranie wszystkich aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="933f7-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="933f7-113">Przykład 2: Uzyskaj aplikacje funkcji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="933f7-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="933f7-114">Przykład 3: pobieranie aplikacji funkcji według nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="933f7-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="933f7-115">Przykład 4: pobieranie aplikacji funkcji dla danych subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="933f7-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="933f7-116">Przykład 5: pobieranie aplikacji funkcji według lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="933f7-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="933f7-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="933f7-117">PARAMETERS</span></span>

### <span data-ttu-id="933f7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="933f7-118">-DefaultProfile</span></span>
<span data-ttu-id="933f7-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="933f7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="933f7-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="933f7-120">-IncludeSlot</span></span>
<span data-ttu-id="933f7-121">Umożliwia określenie, czy w wynikach mają być uwzględniane gniazda wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="933f7-121">Use to specify whether to include deployment slots in results.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="933f7-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="933f7-122">-Location</span></span>
<span data-ttu-id="933f7-123">Lokalizacja aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="933f7-123">The location of the function app.</span></span>

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

### <span data-ttu-id="933f7-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="933f7-124">-Name</span></span>
<span data-ttu-id="933f7-125">Nazwa aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="933f7-125">The name of the function app.</span></span>

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

### <span data-ttu-id="933f7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="933f7-126">-ResourceGroupName</span></span>
<span data-ttu-id="933f7-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="933f7-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="933f7-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="933f7-128">-SubscriptionId</span></span>
<span data-ttu-id="933f7-129">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="933f7-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="933f7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="933f7-130">CommonParameters</span></span>
<span data-ttu-id="933f7-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="933f7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="933f7-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="933f7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="933f7-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="933f7-133">INPUTS</span></span>

## <span data-ttu-id="933f7-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="933f7-134">OUTPUTS</span></span>

### <span data-ttu-id="933f7-135">Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="933f7-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="933f7-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="933f7-136">NOTES</span></span>

<span data-ttu-id="933f7-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="933f7-137">ALIASES</span></span>

## <span data-ttu-id="933f7-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="933f7-138">RELATED LINKS</span></span>

