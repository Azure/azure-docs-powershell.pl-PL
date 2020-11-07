---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 15b847034300d01df354cc7512305ffd3cab8279
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707145"
---
# <span data-ttu-id="495c7-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="495c7-101">Set-AzActionRule</span></span>

## <span data-ttu-id="495c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="495c7-102">SYNOPSIS</span></span>
<span data-ttu-id="495c7-103">Tworzenie lub aktualizowanie reguły akcji.</span><span class="sxs-lookup"><span data-stu-id="495c7-103">Create or update an action rule.</span></span>

## <span data-ttu-id="495c7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="495c7-104">SYNTAX</span></span>

### <span data-ttu-id="495c7-105">BySimplifiedFormatDiagnosticsActionRule (domyślny)</span><span class="sxs-lookup"><span data-stu-id="495c7-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="495c7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="495c7-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="495c7-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="495c7-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="495c7-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="495c7-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="495c7-109">Opis</span><span class="sxs-lookup"><span data-stu-id="495c7-109">DESCRIPTION</span></span>
<span data-ttu-id="495c7-110">**Set-AzActionRule** tworzy lub aktualizuje regułę akcji.</span><span class="sxs-lookup"><span data-stu-id="495c7-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="495c7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="495c7-111">EXAMPLES</span></span>

### <span data-ttu-id="495c7-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="495c7-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="495c7-113">To polecenie cmdlet umożliwia utworzenie reguły akcji dla supression.</span><span class="sxs-lookup"><span data-stu-id="495c7-113">This cmdlet creates an action rule for supression.</span></span>

### <span data-ttu-id="495c7-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="495c7-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="495c7-115">To polecenie cmdlet umożliwia utworzenie reguły akcji dla grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="495c7-115">This cmdlet creates an action rule for action group.</span></span>

### <span data-ttu-id="495c7-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="495c7-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="495c7-117">To polecenie cmdlet umożliwia utworzenie reguły akcji dotyczącej ustawień diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="495c7-117">This cmdlet creates an action rule for diagnostics settings.</span></span>

## <span data-ttu-id="495c7-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="495c7-118">PARAMETERS</span></span>

### <span data-ttu-id="495c7-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="495c7-119">-ActionGroupId</span></span>
<span data-ttu-id="495c7-120">Identyfikator grupy akcji, którego dotyczy powiadomienie.</span><span class="sxs-lookup"><span data-stu-id="495c7-120">Action Group Id which is to be notified.</span></span>

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

### <span data-ttu-id="495c7-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="495c7-121">-ActionRuleType</span></span>
<span data-ttu-id="495c7-122">Format JSON reguły akcji</span><span class="sxs-lookup"><span data-stu-id="495c7-122">Action rule Json format</span></span>

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

### <span data-ttu-id="495c7-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="495c7-123">-AlertContextCondition</span></span>
<span data-ttu-id="495c7-124">Oczekiwany format — { \< operacja \> : \< Lista wartości rozdzielanych przecinkami \> } dla przykładu.</span><span class="sxs-lookup"><span data-stu-id="495c7-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="495c7-125">Zawiera: smartgroups</span><span class="sxs-lookup"><span data-stu-id="495c7-125">Contains:smartgroups</span></span>

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

### <span data-ttu-id="495c7-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="495c7-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="495c7-127">Oczekiwany format — { \< operacja \> : \< Lista wartości rozdzielanych przecinkami \> } dla przykładu.</span><span class="sxs-lookup"><span data-stu-id="495c7-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="495c7-128">Równa się:/abonamentów/ad825170-845c-47dB-8f00-11978947b089/resourceGroups/abvarma/Providers/Microsoft. Insights/metricAlerts/test-mrmc-VM-abvarma</span><span class="sxs-lookup"><span data-stu-id="495c7-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

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

### <span data-ttu-id="495c7-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="495c7-129">-DefaultProfile</span></span>
<span data-ttu-id="495c7-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="495c7-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="495c7-131">— Opis</span><span class="sxs-lookup"><span data-stu-id="495c7-131">-Description</span></span>
<span data-ttu-id="495c7-132">Opis reguły akcji</span><span class="sxs-lookup"><span data-stu-id="495c7-132">Description of Action Rule</span></span>

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

### <span data-ttu-id="495c7-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="495c7-133">-DescriptionCondition</span></span>
<span data-ttu-id="495c7-134">Oczekiwany format — { \< operacja \> : \< Lista wartości rozdzielanych przecinkami \> } dla przykładu.</span><span class="sxs-lookup"><span data-stu-id="495c7-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="495c7-135">Zawiera: test alertu</span><span class="sxs-lookup"><span data-stu-id="495c7-135">Contains:Test Alert</span></span>

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

### <span data-ttu-id="495c7-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="495c7-136">-InputObject</span></span>
<span data-ttu-id="495c7-137">Zasób reguły akcji</span><span class="sxs-lookup"><span data-stu-id="495c7-137">The action rule resource</span></span>

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

### <span data-ttu-id="495c7-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="495c7-138">-MonitorCondition</span></span>
<span data-ttu-id="495c7-139">Oczekiwany format — { \< operacja \> : \< Lista wartości rozdzielanych przecinkami \> } dla przykładu.</span><span class="sxs-lookup"><span data-stu-id="495c7-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="495c7-140">NotEquals: Rozwiązano</span><span class="sxs-lookup"><span data-stu-id="495c7-140">NotEquals:Resolved</span></span>

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

### <span data-ttu-id="495c7-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="495c7-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="495c7-142">Oczekiwany format — { \< operacja \> : \< Lista wartości rozdzielanych przecinkami \> } dla przykładu.</span><span class="sxs-lookup"><span data-stu-id="495c7-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="495c7-143">Równa się: platform, Analiza dzienników</span><span class="sxs-lookup"><span data-stu-id="495c7-143">Equals:Platform,Log Analytics</span></span>

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

### <span data-ttu-id="495c7-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="495c7-144">-Name</span></span>
<span data-ttu-id="495c7-145">Nazwa reguły akcji</span><span class="sxs-lookup"><span data-stu-id="495c7-145">Action rule Name</span></span>

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

### <span data-ttu-id="495c7-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="495c7-146">-ReccurenceType</span></span>
<span data-ttu-id="495c7-147">Określa czas trwania, w jakim ma być stosowane pomijanie.</span><span class="sxs-lookup"><span data-stu-id="495c7-147">Specifies the duration when the suppression should be applied.</span></span>

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

### <span data-ttu-id="495c7-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="495c7-148">-ReccurentValue</span></span>
<span data-ttu-id="495c7-149">Reccurent wartości (jeśli ma zastosowanie). W przypadku Weekly- \[ 1, 2 \] w przypadku comiesięcznych- \[ 1, 3, 5, 30\]</span><span class="sxs-lookup"><span data-stu-id="495c7-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

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

### <span data-ttu-id="495c7-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="495c7-150">-ResourceGroupName</span></span>
<span data-ttu-id="495c7-151">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="495c7-151">Resource Group Name</span></span>

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

### <span data-ttu-id="495c7-152">-Zakres</span><span class="sxs-lookup"><span data-stu-id="495c7-152">-Scope</span></span>
<span data-ttu-id="495c7-153">Lista wartości rozdzielanych przecinkami</span><span class="sxs-lookup"><span data-stu-id="495c7-153">Comma separated list of values</span></span>

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

### <span data-ttu-id="495c7-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="495c7-154">-SeverityCondition</span></span>
<span data-ttu-id="495c7-155">Oczekiwany format — { \< operacja \> : \< Lista wartości rozdzielanych przecinkami \> } dla przykładu.</span><span class="sxs-lookup"><span data-stu-id="495c7-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="495c7-156">Równa się: Sev0; Sev1</span><span class="sxs-lookup"><span data-stu-id="495c7-156">Equals:Sev0,Sev1</span></span>

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

### <span data-ttu-id="495c7-157">-Status</span><span class="sxs-lookup"><span data-stu-id="495c7-157">-Status</span></span>
<span data-ttu-id="495c7-158">Stan reguły akcji.</span><span class="sxs-lookup"><span data-stu-id="495c7-158">Status of Action Rule.</span></span>

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

### <span data-ttu-id="495c7-159">-SuppressionEndTime</span><span class="sxs-lookup"><span data-stu-id="495c7-159">-SuppressionEndTime</span></span>
<span data-ttu-id="495c7-160">Czas zakończenia pomijania.</span><span class="sxs-lookup"><span data-stu-id="495c7-160">Suppression End Time.</span></span>
<span data-ttu-id="495c7-161">Format 12/09/2018 06:00:00 + powinien być wymieniony w przypadku harmonogramu supression Reccurent-raz, codziennie, co tydzień lub co miesiąc.</span><span class="sxs-lookup"><span data-stu-id="495c7-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="495c7-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="495c7-162">-SuppressionStartTime</span></span>
<span data-ttu-id="495c7-163">Czas rozpoczęcia pomijania.</span><span class="sxs-lookup"><span data-stu-id="495c7-163">Suppression Start Time.</span></span>
<span data-ttu-id="495c7-164">Format 12/09/2018 06:00:00 + powinien być wymieniony w przypadku harmonogramu supression Reccurent-raz, codziennie, co tydzień lub co miesiąc.</span><span class="sxs-lookup"><span data-stu-id="495c7-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="495c7-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="495c7-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="495c7-166">Oczekiwany format — { \< operacja \> : \< Lista wartości rozdzielanych przecinkami \> } dla przykładu.</span><span class="sxs-lookup"><span data-stu-id="495c7-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="495c7-167">Zawiera: maszyny wirtualne, konto magazynu</span><span class="sxs-lookup"><span data-stu-id="495c7-167">Contains:Virtual Machines,Storage Account</span></span>

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

### <span data-ttu-id="495c7-168">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="495c7-168">-Confirm</span></span>
<span data-ttu-id="495c7-169">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="495c7-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="495c7-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="495c7-170">-WhatIf</span></span>
<span data-ttu-id="495c7-171">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="495c7-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="495c7-172">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="495c7-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="495c7-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="495c7-173">CommonParameters</span></span>
<span data-ttu-id="495c7-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="495c7-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="495c7-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="495c7-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="495c7-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="495c7-176">INPUTS</span></span>

### <span data-ttu-id="495c7-177">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="495c7-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="495c7-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="495c7-178">OUTPUTS</span></span>

### <span data-ttu-id="495c7-179">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="495c7-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="495c7-180">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="495c7-180">NOTES</span></span>

## <span data-ttu-id="495c7-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="495c7-181">RELATED LINKS</span></span>
