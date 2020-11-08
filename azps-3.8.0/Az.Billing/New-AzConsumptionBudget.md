---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 1b6e815a8ccb02fe462393df8a91af9800b425df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051369"
---
# <span data-ttu-id="8bf24-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="8bf24-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="8bf24-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8bf24-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf24-103">Utwórz budżet w ramach subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8bf24-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="8bf24-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8bf24-104">SYNTAX</span></span>

### <span data-ttu-id="8bf24-105">Abonament (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="8bf24-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bf24-106">Ogłoszenia</span><span class="sxs-lookup"><span data-stu-id="8bf24-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bf24-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8bf24-107">DESCRIPTION</span></span>
<span data-ttu-id="8bf24-108">Polecenie cmdlet New-AzConsumptionBudget powoduje utworzenie budżetu w subskrypcji lub grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="8bf24-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="8bf24-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8bf24-109">EXAMPLES</span></span>

### <span data-ttu-id="8bf24-110">Przykład 1. Tworzenie budżetu kosztów z nazwą budżetu na poziomie abonamentu</span><span class="sxs-lookup"><span data-stu-id="8bf24-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
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

### <span data-ttu-id="8bf24-111">Przykład 2: Tworzenie budżetu kosztów z nazwą budżetu na poziomie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8bf24-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
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

## <span data-ttu-id="8bf24-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8bf24-112">PARAMETERS</span></span>

### <span data-ttu-id="8bf24-113">— Kwota</span><span class="sxs-lookup"><span data-stu-id="8bf24-113">-Amount</span></span>
<span data-ttu-id="8bf24-114">Kwota budżetu.</span><span class="sxs-lookup"><span data-stu-id="8bf24-114">Amount of a budget.</span></span>

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

### <span data-ttu-id="8bf24-115">-Category</span><span class="sxs-lookup"><span data-stu-id="8bf24-115">-Category</span></span>
<span data-ttu-id="8bf24-116">Kategoria budżetu może być kosztem lub zużyciem.</span><span class="sxs-lookup"><span data-stu-id="8bf24-116">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="8bf24-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="8bf24-117">-ContactEmail</span></span>
<span data-ttu-id="8bf24-118">Adresy e-mail wysyłające powiadomienie o budżecie po przekroczeniu progu.</span><span class="sxs-lookup"><span data-stu-id="8bf24-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="8bf24-119">-Contact</span><span class="sxs-lookup"><span data-stu-id="8bf24-119">-ContactGroup</span></span>
<span data-ttu-id="8bf24-120">Grupy akcji umożliwiające wysłanie powiadomienia o budżecie po przekroczeniu progu.</span><span class="sxs-lookup"><span data-stu-id="8bf24-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="8bf24-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="8bf24-121">-ContactRole</span></span>
<span data-ttu-id="8bf24-122">Role kontaktów, aby wysłać powiadomienie o budżecie po przekroczeniu progu.</span><span class="sxs-lookup"><span data-stu-id="8bf24-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="8bf24-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf24-123">-DefaultProfile</span></span>
<span data-ttu-id="8bf24-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8bf24-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bf24-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="8bf24-125">-EndDate</span></span>
<span data-ttu-id="8bf24-126">Data końcowa (RRRR-MM-DD in UTC) okresu budżetu.</span><span class="sxs-lookup"><span data-stu-id="8bf24-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="8bf24-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="8bf24-127">-MeterFilter</span></span>
<span data-ttu-id="8bf24-128">Rozdzielana przecinkami lista liczników, według których ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="8bf24-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="8bf24-129">Wymagane, jeśli kategoria jest taka jak użycie.</span><span class="sxs-lookup"><span data-stu-id="8bf24-129">Required if category is usage.</span></span>

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

### <span data-ttu-id="8bf24-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8bf24-130">-Name</span></span>
<span data-ttu-id="8bf24-131">Nazwa budżetu.</span><span class="sxs-lookup"><span data-stu-id="8bf24-131">Name of a budget.</span></span>

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

### <span data-ttu-id="8bf24-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="8bf24-132">-NotificationEnabled</span></span>
<span data-ttu-id="8bf24-133">Powiadomienie jest włączone lub nie.</span><span class="sxs-lookup"><span data-stu-id="8bf24-133">The notification is enabled or not.</span></span>

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

### <span data-ttu-id="8bf24-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="8bf24-134">-NotificationKey</span></span>
<span data-ttu-id="8bf24-135">Klucz powiadomienia skojarzony z budżetem wymagany do utworzenia powiadomienia z przełącznikiem z włączonym powiadomieniem, progiem powiadomienia, wiadomości e-mail, grup kontaktów lub ról kontaktów.</span><span class="sxs-lookup"><span data-stu-id="8bf24-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="8bf24-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="8bf24-136">-NotificationThreshold</span></span>
<span data-ttu-id="8bf24-137">Wartość progowa skojarzona z powiadomieniem.</span><span class="sxs-lookup"><span data-stu-id="8bf24-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="8bf24-138">Powiadomienie jest wysyłane po przekroczeniu progu kosztu lub użycia.</span><span class="sxs-lookup"><span data-stu-id="8bf24-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="8bf24-139">Jest ona zawsze wartością procentową i musi być z zakresu od 0 do 1000.</span><span class="sxs-lookup"><span data-stu-id="8bf24-139">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="8bf24-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="8bf24-140">-ResourceFilter</span></span>
<span data-ttu-id="8bf24-141">Lista rozdzielanych przecinkami wystąpień zasobów, według których ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="8bf24-141">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="8bf24-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="8bf24-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="8bf24-143">Lista rozdzielanych przecinkami grup zasobów, według których ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="8bf24-143">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="8bf24-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bf24-144">-ResourceGroupName</span></span>
<span data-ttu-id="8bf24-145">Grupa zasobów budżetu.</span><span class="sxs-lookup"><span data-stu-id="8bf24-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="8bf24-146">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="8bf24-146">-StartDate</span></span>
<span data-ttu-id="8bf24-147">Data początkowa (RRRR-MM-DD in UTC) okresu budżetu.</span><span class="sxs-lookup"><span data-stu-id="8bf24-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="8bf24-148">Nie przed bieżącym miesiącem dla miesięcznego ziarna czasu.</span><span class="sxs-lookup"><span data-stu-id="8bf24-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="8bf24-149">Nie wcześniej niż trzy miesiące na ziarno czasu kwartalnego.</span><span class="sxs-lookup"><span data-stu-id="8bf24-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="8bf24-150">Nie wcześniej niż dwanaście miesięcy dla ziarna rocznego.</span><span class="sxs-lookup"><span data-stu-id="8bf24-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="8bf24-151">Przyszła Data rozpoczęcia nie przekracza trzech miesięcy.</span><span class="sxs-lookup"><span data-stu-id="8bf24-151">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="8bf24-152">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="8bf24-152">-TimeGrain</span></span>
<span data-ttu-id="8bf24-153">Ziarno czasu w budżecie może być co miesiąc, kwartalne lub roczne.</span><span class="sxs-lookup"><span data-stu-id="8bf24-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="8bf24-154">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8bf24-154">-Confirm</span></span>
<span data-ttu-id="8bf24-155">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bf24-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bf24-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bf24-156">-WhatIf</span></span>
<span data-ttu-id="8bf24-157">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bf24-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bf24-158">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8bf24-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bf24-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf24-159">CommonParameters</span></span>
<span data-ttu-id="8bf24-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bf24-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf24-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bf24-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf24-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bf24-162">INPUTS</span></span>

### <span data-ttu-id="8bf24-163">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8bf24-163">None</span></span>

## <span data-ttu-id="8bf24-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8bf24-164">OUTPUTS</span></span>

### <span data-ttu-id="8bf24-165">Microsoft. Azure. Commands.. models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="8bf24-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="8bf24-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8bf24-166">NOTES</span></span>

## <span data-ttu-id="8bf24-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8bf24-167">RELATED LINKS</span></span>
