---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 698f4c19b7747ae39495c1893e7a715ca5750be1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983441"
---
# <span data-ttu-id="b4398-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="b4398-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="b4398-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4398-102">SYNOPSIS</span></span>
<span data-ttu-id="b4398-103">Tworzenie budżetu w subskrypcji lub grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4398-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="b4398-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b4398-104">SYNTAX</span></span>

### <span data-ttu-id="b4398-105">Subskrypcja (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b4398-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4398-106">Powiadomienie</span><span class="sxs-lookup"><span data-stu-id="b4398-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4398-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b4398-107">DESCRIPTION</span></span>
<span data-ttu-id="b4398-108">Polecenie New-AzConsumptionBudget cmdlet tworzy budżet w subskrypcji lub grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4398-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="b4398-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b4398-109">EXAMPLES</span></span>

### <span data-ttu-id="b4398-110">Przykład 1. Tworzenie budżetu kosztowego z nazwą budżetu na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b4398-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -Amount 60 -Name PSBudget -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="b4398-111">Przykład 2. Tworzenie budżetu kosztowego z nazwą budżetu na poziomie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b4398-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -ResourceGroupName RGBudgets -Amount 60 -Name PSBudgetRG -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="b4398-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4398-112">PARAMETERS</span></span>

### <span data-ttu-id="b4398-113">— Kwota</span><span class="sxs-lookup"><span data-stu-id="b4398-113">-Amount</span></span>
<span data-ttu-id="b4398-114">Kwota budżetu.</span><span class="sxs-lookup"><span data-stu-id="b4398-114">Amount of a budget.</span></span>

```yaml
Type: System.Decimal
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4398-115">— Kategoria</span><span class="sxs-lookup"><span data-stu-id="b4398-115">-Category</span></span>
<span data-ttu-id="b4398-116">Kategorią budżetu może być koszt lub użycie.</span><span class="sxs-lookup"><span data-stu-id="b4398-116">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4398-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="b4398-117">-ContactEmail</span></span>
<span data-ttu-id="b4398-118">Adresy e-mail do wysłania powiadomienia o budżecie po przekroczeniu progu.</span><span class="sxs-lookup"><span data-stu-id="b4398-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4398-119">- ContactGroup</span><span class="sxs-lookup"><span data-stu-id="b4398-119">-ContactGroup</span></span>
<span data-ttu-id="b4398-120">Grupy akcji, do których będą wysyłać powiadomienia o budżecie po przekroczeniu progu.</span><span class="sxs-lookup"><span data-stu-id="b4398-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4398-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="b4398-121">-ContactRole</span></span>
<span data-ttu-id="b4398-122">Role kontaktów w celu wysłania powiadomienia o budżecie po przekroczeniu progu.</span><span class="sxs-lookup"><span data-stu-id="b4398-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4398-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4398-123">-DefaultProfile</span></span>
<span data-ttu-id="b4398-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4398-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4398-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b4398-125">-EndDate</span></span>
<span data-ttu-id="b4398-126">Data zakończenia okresu budżetu (YYYY-MM-DD w czasie UTC).</span><span class="sxs-lookup"><span data-stu-id="b4398-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4398-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="b4398-127">-MeterFilter</span></span>
<span data-ttu-id="b4398-128">Rozdzielana przecinkami lista metrów, według których mają być filtrowane dane.</span><span class="sxs-lookup"><span data-stu-id="b4398-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="b4398-129">Wymagane, jeśli kategoria jest kategorią użycia.</span><span class="sxs-lookup"><span data-stu-id="b4398-129">Required if category is usage.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4398-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b4398-130">-Name</span></span>
<span data-ttu-id="b4398-131">Nazwa budżetu.</span><span class="sxs-lookup"><span data-stu-id="b4398-131">Name of a budget.</span></span>

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

### <span data-ttu-id="b4398-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="b4398-132">-NotificationEnabled</span></span>
<span data-ttu-id="b4398-133">Powiadomienie jest włączone lub nie.</span><span class="sxs-lookup"><span data-stu-id="b4398-133">The notification is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4398-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="b4398-134">-NotificationKey</span></span>
<span data-ttu-id="b4398-135">Klucz powiadomienia skojarzonego z budżetem, wymagany do utworzenia powiadomienia z włączonym przełącznikiem powiadomień, progiem powiadomień, kontaktowymi wiadomościami e-mail, grupami kontaktów lub rolami kontaktów.</span><span class="sxs-lookup"><span data-stu-id="b4398-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4398-136">- NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="b4398-136">-NotificationThreshold</span></span>
<span data-ttu-id="b4398-137">Wartość progowa skojarzona z powiadomieniem.</span><span class="sxs-lookup"><span data-stu-id="b4398-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="b4398-138">Powiadomienie jest wysyłane, gdy koszt lub użycie przekracza próg.</span><span class="sxs-lookup"><span data-stu-id="b4398-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="b4398-139">Zawsze jest to procent i musi być między 0 a 1000.</span><span class="sxs-lookup"><span data-stu-id="b4398-139">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4398-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="b4398-140">-ResourceFilter</span></span>
<span data-ttu-id="b4398-141">Rozdzielona przecinkami lista wystąpień zasobów, według których mają być filtrowane.</span><span class="sxs-lookup"><span data-stu-id="b4398-141">Comma-separated list of resource instances to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4398-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="b4398-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="b4398-143">Rozdzielona przecinkami lista grup zasobów, według których mają być filtrowane dane.</span><span class="sxs-lookup"><span data-stu-id="b4398-143">Comma-separated list of resource groups to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4398-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4398-144">-ResourceGroupName</span></span>
<span data-ttu-id="b4398-145">Grupa zasobów budżetu.</span><span class="sxs-lookup"><span data-stu-id="b4398-145">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4398-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="b4398-146">-StartDate</span></span>
<span data-ttu-id="b4398-147">Data rozpoczęcia (YYYY-MM-DD w czasie UTC) okresu budżetu.</span><span class="sxs-lookup"><span data-stu-id="b4398-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="b4398-148">Nie przed bieżącym miesiącem dla miesięcznego okresu.</span><span class="sxs-lookup"><span data-stu-id="b4398-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="b4398-149">Nie wcześniej niż trzy miesiące w przypadku kwartalnych okresów.</span><span class="sxs-lookup"><span data-stu-id="b4398-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="b4398-150">Nie wcześniej niż dwanaście miesięcy w przypadku okresowych okresów.</span><span class="sxs-lookup"><span data-stu-id="b4398-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="b4398-151">Przyszła data rozpoczęcia nie większa niż trzy miesiące.</span><span class="sxs-lookup"><span data-stu-id="b4398-151">Future start date not more than three months.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4398-152">- TimeGrain</span><span class="sxs-lookup"><span data-stu-id="b4398-152">-TimeGrain</span></span>
<span data-ttu-id="b4398-153">Część czasu w budżecie może być miesięczna, kwartalna lub rocznie.</span><span class="sxs-lookup"><span data-stu-id="b4398-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4398-154">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b4398-154">-Confirm</span></span>
<span data-ttu-id="b4398-155">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b4398-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4398-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4398-156">-WhatIf</span></span>
<span data-ttu-id="b4398-157">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4398-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4398-158">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b4398-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4398-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4398-159">CommonParameters</span></span>
<span data-ttu-id="b4398-160">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4398-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4398-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4398-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4398-162">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4398-162">INPUTS</span></span>

### <span data-ttu-id="b4398-163">Brak</span><span class="sxs-lookup"><span data-stu-id="b4398-163">None</span></span>

## <span data-ttu-id="b4398-164">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4398-164">OUTPUTS</span></span>

### <span data-ttu-id="b4398-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="b4398-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="b4398-166">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b4398-166">NOTES</span></span>

## <span data-ttu-id="b4398-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4398-167">RELATED LINKS</span></span>
