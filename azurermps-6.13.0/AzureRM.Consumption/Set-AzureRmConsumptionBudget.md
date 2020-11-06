---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/set-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Set-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Set-AzureRmConsumptionBudget.md
ms.openlocfilehash: f416a6cef4888e51dfabbc9f34b4afad9dbd7370
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552167"
---
# <span data-ttu-id="d71ad-101">Set-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="d71ad-101">Set-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="d71ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d71ad-102">SYNOPSIS</span></span>
<span data-ttu-id="d71ad-103">Zaktualizuj budżet w ramach subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d71ad-103">Update a budget in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d71ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d71ad-104">SYNTAX</span></span>

### <span data-ttu-id="d71ad-105">Abonament (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d71ad-105">Subscription (Default)</span></span>
```
Set-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d71ad-106">Ogłoszenia</span><span class="sxs-lookup"><span data-stu-id="d71ad-106">Notification</span></span>
```
Set-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d71ad-107">Instalacja</span><span class="sxs-lookup"><span data-stu-id="d71ad-107">Piping</span></span>
```
Set-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget>
 [-Amount <Decimal>] [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d71ad-108">Rurociągi i powiadomienia</span><span class="sxs-lookup"><span data-stu-id="d71ad-108">Piping and Notification</span></span>
```
Set-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget>
 [-Amount <Decimal>] [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d71ad-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d71ad-109">DESCRIPTION</span></span>
<span data-ttu-id="d71ad-110">Polecenie cmdlet Set-AzureRmConsumptionBudget umożliwia zaktualizowanie budżetu w ramach subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d71ad-110">The Set-AzureRmConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="d71ad-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d71ad-111">EXAMPLES</span></span>

### <span data-ttu-id="d71ad-112">Przykład 1: aktualizowanie budżetu za pomocą nowej kwoty z nazwą budżetu na poziomie abonamentu</span><span class="sxs-lookup"><span data-stu-id="d71ad-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
```powershell
PS C:\> Set-AzureRmConsumptionBudget -Name PSBudget -Amount 75
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

### <span data-ttu-id="d71ad-113">Przykład 2: aktualizowanie budżetu za pomocą powiadomienia, gdy koszt lub użycie osiągnie próg 90 procent kwoty na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d71ad-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
```powershell
PS C:\> Set-AzureRmConsumptionBudget -Name PSBudget -NotificationKey notificationKey-ps1234 -NotificationEnabled -NotificationThreshold 90 -ContactEmail johndoe@contoso.com,janesmith@contoso.com -ContactRole Owner,Reader,Contributor
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

### <span data-ttu-id="d71ad-114">Przykład 3: aktualizowanie budżetu według nowej kwoty z nazwą budżetu na poziomie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d71ad-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
```powershell
PS C:\> Set-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -Amount 75
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

## <span data-ttu-id="d71ad-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d71ad-115">PARAMETERS</span></span>

### <span data-ttu-id="d71ad-116">— Kwota</span><span class="sxs-lookup"><span data-stu-id="d71ad-116">-Amount</span></span>
<span data-ttu-id="d71ad-117">Kwota budżetu.</span><span class="sxs-lookup"><span data-stu-id="d71ad-117">Amount of a budget.</span></span>

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

### <span data-ttu-id="d71ad-118">-Category</span><span class="sxs-lookup"><span data-stu-id="d71ad-118">-Category</span></span>
<span data-ttu-id="d71ad-119">Kategoria budżetu może być kosztem lub zużyciem.</span><span class="sxs-lookup"><span data-stu-id="d71ad-119">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="d71ad-120">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="d71ad-120">-ContactEmail</span></span>
<span data-ttu-id="d71ad-121">Adresy e-mail wysyłające powiadomienie o budżecie po przekroczeniu progu.</span><span class="sxs-lookup"><span data-stu-id="d71ad-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="d71ad-122">-Contact</span><span class="sxs-lookup"><span data-stu-id="d71ad-122">-ContactGroup</span></span>
<span data-ttu-id="d71ad-123">Grupy akcji umożliwiające wysłanie powiadomienia o budżecie po przekroczeniu progu.</span><span class="sxs-lookup"><span data-stu-id="d71ad-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="d71ad-124">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="d71ad-124">-ContactRole</span></span>
<span data-ttu-id="d71ad-125">Role kontaktów, aby wysłać powiadomienie o budżecie po przekroczeniu progu.</span><span class="sxs-lookup"><span data-stu-id="d71ad-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="d71ad-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d71ad-126">-DefaultProfile</span></span>
<span data-ttu-id="d71ad-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d71ad-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d71ad-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="d71ad-128">-EndDate</span></span>
<span data-ttu-id="d71ad-129">Data końcowa (RRRR-MM-DD in UTC) okresu budżetu.</span><span class="sxs-lookup"><span data-stu-id="d71ad-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="d71ad-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d71ad-130">-InputObject</span></span>
<span data-ttu-id="d71ad-131">Obiekt budżetu.</span><span class="sxs-lookup"><span data-stu-id="d71ad-131">Budget object.</span></span>

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

### <span data-ttu-id="d71ad-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="d71ad-132">-MeterFilter</span></span>
<span data-ttu-id="d71ad-133">Rozdzielana przecinkami lista liczników, według których ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="d71ad-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="d71ad-134">Wymagane, jeśli kategoria jest taka jak użycie.</span><span class="sxs-lookup"><span data-stu-id="d71ad-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="d71ad-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d71ad-135">-Name</span></span>
<span data-ttu-id="d71ad-136">Nazwa budżetu.</span><span class="sxs-lookup"><span data-stu-id="d71ad-136">Name of a budget.</span></span>

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

### <span data-ttu-id="d71ad-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="d71ad-137">-NotificationEnabled</span></span>
<span data-ttu-id="d71ad-138">Powiadomienie jest włączone.</span><span class="sxs-lookup"><span data-stu-id="d71ad-138">The notification is enabled.</span></span>
<span data-ttu-id="d71ad-139">Jeśli ta opcja nie jest określona, powiadomienie jest domyślnie wyłączone.</span><span class="sxs-lookup"><span data-stu-id="d71ad-139">If not specified, the notification is disabled by default.</span></span>

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

### <span data-ttu-id="d71ad-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="d71ad-140">-NotificationKey</span></span>
<span data-ttu-id="d71ad-141">Klucz powiadomienia skojarzony z budżetem wymagany do utworzenia powiadomienia z przełącznikiem z włączonym powiadomieniem, progiem powiadomienia, wiadomości e-mail, grup kontaktów lub ról kontaktów.</span><span class="sxs-lookup"><span data-stu-id="d71ad-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="d71ad-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="d71ad-142">-NotificationThreshold</span></span>
<span data-ttu-id="d71ad-143">Wartość progowa skojarzona z powiadomieniem.</span><span class="sxs-lookup"><span data-stu-id="d71ad-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="d71ad-144">Powiadomienie jest wysyłane po przekroczeniu progu kosztu lub użycia.</span><span class="sxs-lookup"><span data-stu-id="d71ad-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="d71ad-145">Jest ona zawsze wartością procentową i musi być z zakresu od 0 do 1000.</span><span class="sxs-lookup"><span data-stu-id="d71ad-145">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="d71ad-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="d71ad-146">-ResourceFilter</span></span>
<span data-ttu-id="d71ad-147">Lista rozdzielanych przecinkami wystąpień zasobów, według których ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="d71ad-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="d71ad-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="d71ad-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="d71ad-149">Lista rozdzielanych przecinkami grup zasobów, według których ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="d71ad-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="d71ad-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d71ad-150">-ResourceGroupName</span></span>
<span data-ttu-id="d71ad-151">Grupa zasobów budżetu.</span><span class="sxs-lookup"><span data-stu-id="d71ad-151">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="d71ad-152">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="d71ad-152">-StartDate</span></span>
<span data-ttu-id="d71ad-153">Data początkowa (RRRR-MM-DD in UTC) okresu budżetu.</span><span class="sxs-lookup"><span data-stu-id="d71ad-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="d71ad-154">Nie przed bieżącym miesiącem dla miesięcznego ziarna czasu.</span><span class="sxs-lookup"><span data-stu-id="d71ad-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="d71ad-155">Nie wcześniej niż trzy miesiące na ziarno czasu kwartalnego.</span><span class="sxs-lookup"><span data-stu-id="d71ad-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="d71ad-156">Nie wcześniej niż dwanaście miesięcy dla ziarna rocznego.</span><span class="sxs-lookup"><span data-stu-id="d71ad-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="d71ad-157">Przyszła Data rozpoczęcia nie przekracza trzech miesięcy.</span><span class="sxs-lookup"><span data-stu-id="d71ad-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="d71ad-158">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="d71ad-158">-TimeGrain</span></span>
<span data-ttu-id="d71ad-159">Ziarno czasu w budżecie może być co miesiąc, kwartalne lub roczne.</span><span class="sxs-lookup"><span data-stu-id="d71ad-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="d71ad-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d71ad-160">-Confirm</span></span>
<span data-ttu-id="d71ad-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d71ad-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d71ad-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d71ad-162">-WhatIf</span></span>
<span data-ttu-id="d71ad-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d71ad-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d71ad-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d71ad-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d71ad-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d71ad-165">CommonParameters</span></span>
<span data-ttu-id="d71ad-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d71ad-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d71ad-167">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d71ad-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d71ad-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d71ad-168">INPUTS</span></span>

### <span data-ttu-id="d71ad-169">Microsoft. Azure. Commands.. models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="d71ad-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>
<span data-ttu-id="d71ad-170">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d71ad-170">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d71ad-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d71ad-171">OUTPUTS</span></span>

### <span data-ttu-id="d71ad-172">Microsoft. Azure. Commands.. models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="d71ad-172">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="d71ad-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d71ad-173">NOTES</span></span>

## <span data-ttu-id="d71ad-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d71ad-174">RELATED LINKS</span></span>
