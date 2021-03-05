---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/set-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
ms.openlocfilehash: fa0b8ae9adaca5a187136f068dfd8797ed9e4b0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960881"
---
# <span data-ttu-id="68e8a-101">Set-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="68e8a-101">Set-AzConsumptionBudget</span></span>

## <span data-ttu-id="68e8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="68e8a-103">Aktualizowanie budżetu w ramach subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="68e8a-103">Update a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="68e8a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="68e8a-104">SYNTAX</span></span>

### <span data-ttu-id="68e8a-105">Subskrypcja (domyślna)</span><span class="sxs-lookup"><span data-stu-id="68e8a-105">Subscription (Default)</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68e8a-106">Powiadomienie</span><span class="sxs-lookup"><span data-stu-id="68e8a-106">Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68e8a-107">Piping</span><span class="sxs-lookup"><span data-stu-id="68e8a-107">Piping</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68e8a-108">Piping and Notification</span><span class="sxs-lookup"><span data-stu-id="68e8a-108">Piping and Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68e8a-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="68e8a-109">DESCRIPTION</span></span>
<span data-ttu-id="68e8a-110">Polecenie Set-AzConsumptionBudget aktualizuje budżet w ramach subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="68e8a-110">The Set-AzConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="68e8a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="68e8a-111">EXAMPLES</span></span>

### <span data-ttu-id="68e8a-112">Przykład 1. Aktualizowanie budżetu o nową kwotę przy użyciu nazwy budżetu na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="68e8a-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="68e8a-113">Przykład 2. Aktualizacja budżetu z powiadomieniem, gdy koszt lub użycie osiągnie próg 90 procent kwoty na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="68e8a-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -NotificationKey notificationKey-ps1234 -NotificationEnabled -NotificationThreshold 90 -ContactEmail johndoe@contoso.com,janesmith@contoso.com -ContactRole Owner,Reader,Contributor
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
Notification:  NotificationKey:  notificationKey-ps1234
               Threshold:  90
               Enabled:  true
               ContactEmail:  johndoe@contoso.com,janesmith@contoso.com
               ContactRole:  Owner,Reader,Contributor
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="68e8a-114">Przykład 3. Aktualizowanie budżetu według nowej kwoty przy użyciu nazwy budżetu na poziomie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="68e8a-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="68e8a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68e8a-115">PARAMETERS</span></span>

### <span data-ttu-id="68e8a-116">— Kwota</span><span class="sxs-lookup"><span data-stu-id="68e8a-116">-Amount</span></span>
<span data-ttu-id="68e8a-117">Kwota budżetu.</span><span class="sxs-lookup"><span data-stu-id="68e8a-117">Amount of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e8a-118">— Kategoria</span><span class="sxs-lookup"><span data-stu-id="68e8a-118">-Category</span></span>
<span data-ttu-id="68e8a-119">Kategorią budżetu może być koszt lub użycie.</span><span class="sxs-lookup"><span data-stu-id="68e8a-119">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e8a-120">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="68e8a-120">-ContactEmail</span></span>
<span data-ttu-id="68e8a-121">Adresy e-mail do wysłania powiadomienia o budżecie po przekroczeniu progu.</span><span class="sxs-lookup"><span data-stu-id="68e8a-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e8a-122">- ContactGroup</span><span class="sxs-lookup"><span data-stu-id="68e8a-122">-ContactGroup</span></span>
<span data-ttu-id="68e8a-123">Grupy akcji, do których będą wysyłać powiadomienia o budżecie po przekroczeniu progu.</span><span class="sxs-lookup"><span data-stu-id="68e8a-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e8a-124">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="68e8a-124">-ContactRole</span></span>
<span data-ttu-id="68e8a-125">Role kontaktów w celu wysłania powiadomienia o budżecie po przekroczeniu progu.</span><span class="sxs-lookup"><span data-stu-id="68e8a-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e8a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68e8a-126">-DefaultProfile</span></span>
<span data-ttu-id="68e8a-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="68e8a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68e8a-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="68e8a-128">-EndDate</span></span>
<span data-ttu-id="68e8a-129">Data zakończenia okresu budżetu (YYYY-MM-DD w czasie UTC).</span><span class="sxs-lookup"><span data-stu-id="68e8a-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="68e8a-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68e8a-130">-InputObject</span></span>
<span data-ttu-id="68e8a-131">Obiekt Budżet.</span><span class="sxs-lookup"><span data-stu-id="68e8a-131">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68e8a-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="68e8a-132">-MeterFilter</span></span>
<span data-ttu-id="68e8a-133">Rozdzielana przecinkami lista metrów, według których mają być filtrowane dane.</span><span class="sxs-lookup"><span data-stu-id="68e8a-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="68e8a-134">Wymagane, jeśli kategoria jest kategorią użycia.</span><span class="sxs-lookup"><span data-stu-id="68e8a-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="68e8a-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="68e8a-135">-Name</span></span>
<span data-ttu-id="68e8a-136">Nazwa budżetu.</span><span class="sxs-lookup"><span data-stu-id="68e8a-136">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e8a-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="68e8a-137">-NotificationEnabled</span></span>
<span data-ttu-id="68e8a-138">Powiadomienie jest włączone.</span><span class="sxs-lookup"><span data-stu-id="68e8a-138">The notification is enabled.</span></span>
<span data-ttu-id="68e8a-139">Jeśli nie zostanie określone, powiadomienie jest domyślnie wyłączone.</span><span class="sxs-lookup"><span data-stu-id="68e8a-139">If not specified, the notification is disabled by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e8a-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="68e8a-140">-NotificationKey</span></span>
<span data-ttu-id="68e8a-141">Klucz powiadomienia skojarzonego z budżetem, wymagany do utworzenia powiadomienia z włączonym przełącznikiem powiadomień, progiem powiadomień, kontaktowymi wiadomościami e-mail, grupami kontaktów lub rolami kontaktów.</span><span class="sxs-lookup"><span data-stu-id="68e8a-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e8a-142">- NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="68e8a-142">-NotificationThreshold</span></span>
<span data-ttu-id="68e8a-143">Wartość progowa skojarzona z powiadomieniem.</span><span class="sxs-lookup"><span data-stu-id="68e8a-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="68e8a-144">Powiadomienie jest wysyłane, gdy koszt lub użycie przekracza próg.</span><span class="sxs-lookup"><span data-stu-id="68e8a-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="68e8a-145">Zawsze jest to procent i musi być między 0 a 1000.</span><span class="sxs-lookup"><span data-stu-id="68e8a-145">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e8a-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="68e8a-146">-ResourceFilter</span></span>
<span data-ttu-id="68e8a-147">Rozdzielona przecinkami lista wystąpień zasobów, według których mają być filtrowane.</span><span class="sxs-lookup"><span data-stu-id="68e8a-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="68e8a-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="68e8a-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="68e8a-149">Rozdzielona przecinkami lista grup zasobów, według których mają być filtrowane dane.</span><span class="sxs-lookup"><span data-stu-id="68e8a-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="68e8a-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68e8a-150">-ResourceGroupName</span></span>
<span data-ttu-id="68e8a-151">Grupa zasobów budżetu.</span><span class="sxs-lookup"><span data-stu-id="68e8a-151">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e8a-152">-StartDate</span><span class="sxs-lookup"><span data-stu-id="68e8a-152">-StartDate</span></span>
<span data-ttu-id="68e8a-153">Data rozpoczęcia (YYYY-MM-DD w czasie UTC) okresu budżetu.</span><span class="sxs-lookup"><span data-stu-id="68e8a-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="68e8a-154">Nie przed bieżącym miesiącem dla miesięcznego okresu.</span><span class="sxs-lookup"><span data-stu-id="68e8a-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="68e8a-155">Nie wcześniej niż trzy miesiące w przypadku kwartalnych okresów.</span><span class="sxs-lookup"><span data-stu-id="68e8a-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="68e8a-156">Nie wcześniej niż dwanaście miesięcy w przypadku okresowych okresów.</span><span class="sxs-lookup"><span data-stu-id="68e8a-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="68e8a-157">Przyszła data rozpoczęcia nie większa niż trzy miesiące.</span><span class="sxs-lookup"><span data-stu-id="68e8a-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="68e8a-158">- TimeGrain</span><span class="sxs-lookup"><span data-stu-id="68e8a-158">-TimeGrain</span></span>
<span data-ttu-id="68e8a-159">Część czasu w budżecie może być miesięczna, kwartalna lub rocznie.</span><span class="sxs-lookup"><span data-stu-id="68e8a-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e8a-160">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68e8a-160">-Confirm</span></span>
<span data-ttu-id="68e8a-161">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="68e8a-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68e8a-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68e8a-162">-WhatIf</span></span>
<span data-ttu-id="68e8a-163">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68e8a-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68e8a-164">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="68e8a-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68e8a-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e8a-165">CommonParameters</span></span>
<span data-ttu-id="68e8a-166">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68e8a-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e8a-167">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68e8a-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e8a-168">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68e8a-168">INPUTS</span></span>

### <span data-ttu-id="68e8a-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="68e8a-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="68e8a-170">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68e8a-170">OUTPUTS</span></span>

### <span data-ttu-id="68e8a-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="68e8a-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="68e8a-172">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="68e8a-172">NOTES</span></span>

## <span data-ttu-id="68e8a-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68e8a-173">RELATED LINKS</span></span>
