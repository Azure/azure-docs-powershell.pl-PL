---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 934c8ed95a31f4b953096da40b5ac480020dbc1f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340858"
---
# <span data-ttu-id="c17ee-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="c17ee-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="c17ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c17ee-102">SYNOPSIS</span></span>
<span data-ttu-id="c17ee-103">Tworzy plan usługi App Service (funkcja).</span><span class="sxs-lookup"><span data-stu-id="c17ee-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="c17ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c17ee-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c17ee-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c17ee-105">DESCRIPTION</span></span>
<span data-ttu-id="c17ee-106">Tworzy plan usługi App Service (funkcja).</span><span class="sxs-lookup"><span data-stu-id="c17ee-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="c17ee-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c17ee-107">EXAMPLES</span></span>

### <span data-ttu-id="c17ee-108">Przykład 1: Tworzenie planu aplikacji systemu Windows Premium w zachodniej Europie z możliwością tworzenia serii do 10 wystąpień.</span><span class="sxs-lookup"><span data-stu-id="c17ee-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="c17ee-109">To polecenie tworzy plan aplikacji Windows Premium w zachodniej Europie z możliwością tworzenia serii do 10 wystąpień.</span><span class="sxs-lookup"><span data-stu-id="c17ee-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="c17ee-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c17ee-110">PARAMETERS</span></span>

### <span data-ttu-id="c17ee-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c17ee-111">-AsJob</span></span>
<span data-ttu-id="c17ee-112">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="c17ee-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="c17ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c17ee-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="c17ee-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c17ee-114">-Location</span></span>
<span data-ttu-id="c17ee-115">Lokalizacja planu zużycia.</span><span class="sxs-lookup"><span data-stu-id="c17ee-115">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="c17ee-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="c17ee-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="c17ee-117">Maksymalna liczba pracowników planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="c17ee-117">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17ee-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="c17ee-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="c17ee-119">Minimalna liczba pracowników planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="c17ee-119">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17ee-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c17ee-120">-Name</span></span>
<span data-ttu-id="c17ee-121">Nazwa planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="c17ee-121">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="c17ee-122">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c17ee-122">-NoWait</span></span>
<span data-ttu-id="c17ee-123">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="c17ee-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="c17ee-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c17ee-124">-ResourceGroupName</span></span>
<span data-ttu-id="c17ee-125">Nazwa grupy zasobów, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="c17ee-125">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="c17ee-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="c17ee-126">-Sku</span></span>
<span data-ttu-id="c17ee-127">Wersja planu.</span><span class="sxs-lookup"><span data-stu-id="c17ee-127">The plan sku.</span></span>
<span data-ttu-id="c17ee-128">Prawidłowe dane wejściowe to: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="c17ee-128">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="c17ee-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c17ee-129">-SubscriptionId</span></span>
<span data-ttu-id="c17ee-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c17ee-130">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17ee-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="c17ee-131">-Tag</span></span>
<span data-ttu-id="c17ee-132">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="c17ee-132">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17ee-133">-Workertype</span><span class="sxs-lookup"><span data-stu-id="c17ee-133">-WorkerType</span></span>
<span data-ttu-id="c17ee-134">Typ pracownika planu.</span><span class="sxs-lookup"><span data-stu-id="c17ee-134">The worker type for the plan.</span></span>
<span data-ttu-id="c17ee-135">Prawidłowe dane wejściowe to: Windows lub Linux.</span><span class="sxs-lookup"><span data-stu-id="c17ee-135">Valid inputs are: Windows or Linux.</span></span>

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

### <span data-ttu-id="c17ee-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c17ee-136">-Confirm</span></span>
<span data-ttu-id="c17ee-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c17ee-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c17ee-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c17ee-138">-WhatIf</span></span>
<span data-ttu-id="c17ee-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c17ee-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c17ee-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c17ee-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c17ee-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c17ee-141">CommonParameters</span></span>
<span data-ttu-id="c17ee-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c17ee-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c17ee-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c17ee-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c17ee-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c17ee-144">INPUTS</span></span>

## <span data-ttu-id="c17ee-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c17ee-145">OUTPUTS</span></span>

### <span data-ttu-id="c17ee-146">Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c17ee-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="c17ee-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c17ee-147">NOTES</span></span>

<span data-ttu-id="c17ee-148">PISUJE</span><span class="sxs-lookup"><span data-stu-id="c17ee-148">ALIASES</span></span>

## <span data-ttu-id="c17ee-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c17ee-149">RELATED LINKS</span></span>

