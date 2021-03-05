---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 465c4b366990bb69d437fbdbe51fe2c5f4316758
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969025"
---
# <span data-ttu-id="2f73b-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="2f73b-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="2f73b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f73b-102">SYNOPSIS</span></span>
<span data-ttu-id="2f73b-103">Tworzy plan usługi aplikacji funkcyjnej.</span><span class="sxs-lookup"><span data-stu-id="2f73b-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="2f73b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2f73b-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2f73b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2f73b-105">DESCRIPTION</span></span>
<span data-ttu-id="2f73b-106">Tworzy plan usługi aplikacji funkcyjnej.</span><span class="sxs-lookup"><span data-stu-id="2f73b-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="2f73b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2f73b-107">EXAMPLES</span></span>

### <span data-ttu-id="2f73b-108">Przykład 1. Tworzenie planu aplikacji premium dla systemu Windows w Europie Zachodniej z możliwością tworzenia nawet 10 wystąpień.</span><span class="sxs-lookup"><span data-stu-id="2f73b-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="2f73b-109">To polecenie tworzy plan aplikacji premium systemu Windows w Europie Zachodniej z możliwością tylko 10 wystąpień.</span><span class="sxs-lookup"><span data-stu-id="2f73b-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="2f73b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f73b-110">PARAMETERS</span></span>

### <span data-ttu-id="2f73b-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2f73b-111">-AsJob</span></span>
<span data-ttu-id="2f73b-112">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="2f73b-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="2f73b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f73b-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="2f73b-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2f73b-114">-Location</span></span>
<span data-ttu-id="2f73b-115">Lokalizacja planu zużycia.</span><span class="sxs-lookup"><span data-stu-id="2f73b-115">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="2f73b-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="2f73b-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="2f73b-117">Maksymalna liczba pracowników w planie usług aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2f73b-117">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="2f73b-118">-MinimumLiczbowePracownika</span><span class="sxs-lookup"><span data-stu-id="2f73b-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="2f73b-119">Minimalna liczba pracowników w planie usług aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2f73b-119">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="2f73b-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2f73b-120">-Name</span></span>
<span data-ttu-id="2f73b-121">Nazwa planu usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2f73b-121">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="2f73b-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2f73b-122">-NoWait</span></span>
<span data-ttu-id="2f73b-123">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="2f73b-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="2f73b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f73b-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f73b-125">Nazwa grupy zasobów, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="2f73b-125">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="2f73b-126">- SKU</span><span class="sxs-lookup"><span data-stu-id="2f73b-126">-Sku</span></span>
<span data-ttu-id="2f73b-127">SKU planu.</span><span class="sxs-lookup"><span data-stu-id="2f73b-127">The plan sku.</span></span>
<span data-ttu-id="2f73b-128">Prawidłowe dane wejściowe: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="2f73b-128">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="2f73b-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f73b-129">-SubscriptionId</span></span>
<span data-ttu-id="2f73b-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2f73b-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="2f73b-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="2f73b-131">-Tag</span></span>
<span data-ttu-id="2f73b-132">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="2f73b-132">Resource tags.</span></span>

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

### <span data-ttu-id="2f73b-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="2f73b-133">-WorkerType</span></span>
<span data-ttu-id="2f73b-134">Typ pracownika planu.</span><span class="sxs-lookup"><span data-stu-id="2f73b-134">The worker type for the plan.</span></span>
<span data-ttu-id="2f73b-135">Prawidłowe dane wejściowe to: Windows lub Linux.</span><span class="sxs-lookup"><span data-stu-id="2f73b-135">Valid inputs are: Windows or Linux.</span></span>

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

### <span data-ttu-id="2f73b-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f73b-136">-Confirm</span></span>
<span data-ttu-id="2f73b-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2f73b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f73b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f73b-138">-WhatIf</span></span>
<span data-ttu-id="2f73b-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f73b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f73b-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2f73b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f73b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f73b-141">CommonParameters</span></span>
<span data-ttu-id="2f73b-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f73b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f73b-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f73b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f73b-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f73b-144">INPUTS</span></span>

## <span data-ttu-id="2f73b-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f73b-145">OUTPUTS</span></span>

### <span data-ttu-id="2f73b-146">Microsoft.Azure.PowerShell.Cmdlet.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2f73b-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="2f73b-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2f73b-147">NOTES</span></span>

<span data-ttu-id="2f73b-148">ALIASY</span><span class="sxs-lookup"><span data-stu-id="2f73b-148">ALIASES</span></span>

## <span data-ttu-id="2f73b-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f73b-149">RELATED LINKS</span></span>

