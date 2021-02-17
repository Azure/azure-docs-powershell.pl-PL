---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 75a2071e8f60ed15420b69815eba22d6f82e9f82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192594"
---
# <span data-ttu-id="cd4b5-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="cd4b5-101">Set-AzActionRule</span></span>

## <span data-ttu-id="cd4b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd4b5-102">SYNOPSIS</span></span>
<span data-ttu-id="cd4b5-103">Utwórz lub zaktualizuj regułę akcji.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-103">Create or update an action rule.</span></span>

## <span data-ttu-id="cd4b5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cd4b5-104">SYNTAX</span></span>

### <span data-ttu-id="cd4b5-105">BySimplifiedFormatDiagnosticsActionRule (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="cd4b5-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd4b5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cd4b5-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd4b5-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="cd4b5-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd4b5-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="cd4b5-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd4b5-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="cd4b5-109">DESCRIPTION</span></span>
<span data-ttu-id="cd4b5-110">**Set-AzActionRule** tworzy lub aktualizuje regułę akcji.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="cd4b5-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cd4b5-111">EXAMPLES</span></span>

### <span data-ttu-id="cd4b5-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd4b5-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="cd4b5-113">To polecenie cmdlet tworzy regułę akcji dla kompresji z zakresem subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-113">This cmdlet creates an action rule for supression, with a subscription scope.</span></span>

### <span data-ttu-id="cd4b5-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cd4b5-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="cd4b5-115">To polecenie cmdlet tworzy regułę akcji dla grupy akcji z listą zakresu grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-115">This cmdlet creates an action rule for action group, with a list of resource groups scope.</span></span>

### <span data-ttu-id="cd4b5-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="cd4b5-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab/providers/microsoft.insights/metricAlerts/Total Requests Exceeded" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="cd4b5-117">To polecenie cmdlet tworzy regułę akcji dla ustawień diagnostycznych z zakresem zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-117">This cmdlet creates an action rule for diagnostics settings, with a resource scope.</span></span>

## <span data-ttu-id="cd4b5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd4b5-118">PARAMETERS</span></span>

### <span data-ttu-id="cd4b5-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="cd4b5-119">-ActionGroupId</span></span>
<span data-ttu-id="cd4b5-120">Identyfikator grupy akcji, który ma zostać powiadomiony.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-120">Action Group Id which is to be notified.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatActionGroupActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="cd4b5-121">-ActionRuleType</span></span>
<span data-ttu-id="cd4b5-122">Format Json reguły akcji</span><span class="sxs-lookup"><span data-stu-id="cd4b5-122">Action rule Json format</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="cd4b5-123">-AlertContextCondition</span></span>
<span data-ttu-id="cd4b5-124">Oczekiwany format - { \<operation\> : } W przypadku \<comma separated list of values\> np.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="cd4b5-125">Zawiera:grupy inteligentne</span><span class="sxs-lookup"><span data-stu-id="cd4b5-125">Contains:smartgroups</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="cd4b5-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="cd4b5-127">Oczekiwany format - { \<operation\> : } W przypadku \<comma separated list of values\> np.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="cd4b5-128">Równa się:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span><span class="sxs-lookup"><span data-stu-id="cd4b5-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd4b5-129">-DefaultProfile</span></span>
<span data-ttu-id="cd4b5-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd4b5-131">— Opis</span><span class="sxs-lookup"><span data-stu-id="cd4b5-131">-Description</span></span>
<span data-ttu-id="cd4b5-132">Opis reguły akcji</span><span class="sxs-lookup"><span data-stu-id="cd4b5-132">Description of Action Rule</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="cd4b5-133">-DescriptionCondition</span></span>
<span data-ttu-id="cd4b5-134">Oczekiwany format - { \<operation\> : } W przypadku \<comma separated list of values\> np.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="cd4b5-135">Zawiera:Test alertu</span><span class="sxs-lookup"><span data-stu-id="cd4b5-135">Contains:Test Alert</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd4b5-136">-InputObject</span></span>
<span data-ttu-id="cd4b5-137">Zasób reguły akcji</span><span class="sxs-lookup"><span data-stu-id="cd4b5-137">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-138">- MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="cd4b5-138">-MonitorCondition</span></span>
<span data-ttu-id="cd4b5-139">Oczekiwany format - { \<operation\> : } W przypadku \<comma separated list of values\> np.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="cd4b5-140">Nierówne:Rozwiązane</span><span class="sxs-lookup"><span data-stu-id="cd4b5-140">NotEquals:Resolved</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="cd4b5-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="cd4b5-142">Oczekiwany format - { \<operation\> : } W przypadku \<comma separated list of values\> np.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="cd4b5-143">Równa się:Platforma,Analiza dziennika</span><span class="sxs-lookup"><span data-stu-id="cd4b5-143">Equals:Platform,Log Analytics</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-144">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cd4b5-144">-Name</span></span>
<span data-ttu-id="cd4b5-145">Nazwa reguły akcji</span><span class="sxs-lookup"><span data-stu-id="cd4b5-145">Action rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="cd4b5-146">-ReccurenceType</span></span>
<span data-ttu-id="cd4b5-147">Określa czas trwania, przez który należy chcieć je stosować.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-147">Specifies the duration when the suppression should be applied.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="cd4b5-148">-ReccurentValue</span></span>
<span data-ttu-id="cd4b5-149">Wartości cykliczne, jeśli mają zastosowanie. W przypadku tygodniowych - \[ 1,2 \] W przypadku miesięcznej - \[ 1,3,5,30\]</span><span class="sxs-lookup"><span data-stu-id="cd4b5-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd4b5-150">-ResourceGroupName</span></span>
<span data-ttu-id="cd4b5-151">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cd4b5-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-152">— Zakres</span><span class="sxs-lookup"><span data-stu-id="cd4b5-152">-Scope</span></span>
<span data-ttu-id="cd4b5-153">Rozdzielona przecinkami lista wartości</span><span class="sxs-lookup"><span data-stu-id="cd4b5-153">Comma separated list of values</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-154">- SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="cd4b5-154">-SeverityCondition</span></span>
<span data-ttu-id="cd4b5-155">Oczekiwany format - { \<operation\> : } W przypadku \<comma separated list of values\> np.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="cd4b5-156">Równa się:Sev0,Sev1</span><span class="sxs-lookup"><span data-stu-id="cd4b5-156">Equals:Sev0,Sev1</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-157">— Status</span><span class="sxs-lookup"><span data-stu-id="cd4b5-157">-Status</span></span>
<span data-ttu-id="cd4b5-158">Stan reguły akcji.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-158">Status of Action Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-159">-WymuszeńGodziny</span><span class="sxs-lookup"><span data-stu-id="cd4b5-159">-SuppressionEndTime</span></span>
<span data-ttu-id="cd4b5-160">Czas zakończenia.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-160">Suppression End Time.</span></span>
<span data-ttu-id="cd4b5-161">Format 2018-12-09 06:00:00 powinien być wzmiankowany w przypadku cyklicznego harmonogramu kompresji — raz, codziennie, co tydzień lub co miesiąc.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-162">- WymuszeniePoczątego Rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="cd4b5-162">-SuppressionStartTime</span></span>
<span data-ttu-id="cd4b5-163">Godzina rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-163">Suppression Start Time.</span></span>
<span data-ttu-id="cd4b5-164">Format 2018-12-09 06:00:00 powinien być wzmiankowany w przypadku cyklicznego harmonogramu kompresji — raz, codziennie, co tydzień lub co miesiąc.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="cd4b5-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="cd4b5-166">Oczekiwany format - { \<operation\> : } W przypadku \<comma separated list of values\> np.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="cd4b5-167">Zawiera:Maszyny wirtualne,Konto magazynu</span><span class="sxs-lookup"><span data-stu-id="cd4b5-167">Contains:Virtual Machines,Storage Account</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4b5-168">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd4b5-168">-Confirm</span></span>
<span data-ttu-id="cd4b5-169">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd4b5-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd4b5-170">-WhatIf</span></span>
<span data-ttu-id="cd4b5-171">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd4b5-172">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd4b5-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd4b5-173">CommonParameters</span></span>
<span data-ttu-id="cd4b5-174">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd4b5-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd4b5-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd4b5-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd4b5-176">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd4b5-176">INPUTS</span></span>

### <span data-ttu-id="cd4b5-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="cd4b5-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="cd4b5-178">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd4b5-178">OUTPUTS</span></span>

### <span data-ttu-id="cd4b5-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="cd4b5-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="cd4b5-180">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cd4b5-180">NOTES</span></span>

## <span data-ttu-id="cd4b5-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd4b5-181">RELATED LINKS</span></span>
