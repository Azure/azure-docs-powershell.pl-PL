---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
ms.openlocfilehash: 56f1878507424c1396130aa91a5fc7b086f101c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191202"
---
# <span data-ttu-id="c82ab-101">Update-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="c82ab-101">Update-AzSentinelAlertRule</span></span>

## <span data-ttu-id="c82ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c82ab-102">SYNOPSIS</span></span>
<span data-ttu-id="c82ab-103">Tworzenie reguły analitycznej (reguły alertu).</span><span class="sxs-lookup"><span data-stu-id="c82ab-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="c82ab-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c82ab-104">SYNTAX</span></span>

### <span data-ttu-id="c82ab-105">AlertRuleId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c82ab-105">AlertRuleId (Default)</span></span>
```
Update-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled] [-DisplayName <String>]
 [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c82ab-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c82ab-106">InputObject</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -InputObject <PSSentinelAlertRule>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c82ab-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c82ab-107">ResourceId</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c82ab-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c82ab-108">DESCRIPTION</span></span>
<span data-ttu-id="c82ab-109">Polecenie **cmdlet Update-AzSentinelAlertRule** aktualizuje regułę analityczna (reguła alertu) w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="c82ab-109">The **Update-AzSentinelAlertRule** cmdlet updates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="c82ab-110">Można użyć wartości -InputObject, -ResourceId lub -AlertId.</span><span class="sxs-lookup"><span data-stu-id="c82ab-110">You can use an -InputObject or -ResourceId or -AlertId.</span></span>  <span data-ttu-id="c82ab-111">Możesz zaktualizować 1 lub więcej parmaterów proprtery.</span><span class="sxs-lookup"><span data-stu-id="c82ab-111">You can update 1 or more proprtery parmaters.</span></span>
<span data-ttu-id="c82ab-112">Za pomocą *parametru Confirm* i $ConfirmPreference programu Windows PowerShell możesz kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c82ab-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>


## <span data-ttu-id="c82ab-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c82ab-113">EXAMPLES</span></span>

### <span data-ttu-id="c82ab-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c82ab-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -Disabled -DisplayName "Disabled-AlertRuleDisplayName"
```

<span data-ttu-id="c82ab-115">W tym przykładzie zmieniono ustawienie wartości **AlertRule** na *Disabled* (Wyłączone) i zmieniono nazwę na *Disabled-AlertRuleDisplayName (Wyłączono AlertRuleDisplayName).*</span><span class="sxs-lookup"><span data-stu-id="c82ab-115">This example updates an **AlertRule** setting it to *Disabled* and renames to *Disabled-AlertRuleDisplayName*.</span></span>  <span data-ttu-id="c82ab-116">Wszystkie pozostałe właściwości pozostaną takie same.</span><span class="sxs-lookup"><span data-stu-id="c82ab-116">All other properties will remain the same.</span></span>

### <span data-ttu-id="c82ab-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c82ab-117">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
PS C:\> Update-AzSentinelAlertRule -InputObject $AlertRule -Disabled
```

<span data-ttu-id="c82ab-118">W tym przykładzie **aktualizacja alertu AlertRule** została wyłączona przy użyciu ustawienia InputObject.</span><span class="sxs-lookup"><span data-stu-id="c82ab-118">This example updates an **AlertRule** using an InputObject setting it to *Disabled*.</span></span>  <span data-ttu-id="c82ab-119">Wszystkie pozostałe właściwości pozostaną takie same.</span><span class="sxs-lookup"><span data-stu-id="c82ab-119">All other properties will remain the same.</span></span>


## <span data-ttu-id="c82ab-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c82ab-120">PARAMETERS</span></span>

### <span data-ttu-id="c82ab-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="c82ab-121">-AlertRuleId</span></span>
<span data-ttu-id="c82ab-122">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="c82ab-122">Alert Rule Id.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="c82ab-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="c82ab-124">Szablon reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="c82ab-124">Alert Rule Template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c82ab-125">-DefaultProfile</span></span>
<span data-ttu-id="c82ab-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c82ab-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-127">— Opis</span><span class="sxs-lookup"><span data-stu-id="c82ab-127">-Description</span></span>
<span data-ttu-id="c82ab-128">Opis.</span><span class="sxs-lookup"><span data-stu-id="c82ab-128">Description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-129">— Wyłączone</span><span class="sxs-lookup"><span data-stu-id="c82ab-129">-Disabled</span></span>
<span data-ttu-id="c82ab-130">Reguła alertu wyłączona.</span><span class="sxs-lookup"><span data-stu-id="c82ab-130">Alert Rule Disabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-131">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="c82ab-131">-DisplayName</span></span>
<span data-ttu-id="c82ab-132">Nazwa wyświetlana reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="c82ab-132">Alert Rule Display Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-133">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="c82ab-133">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="c82ab-134">Filtr wyklucza w regułach alertów.</span><span class="sxs-lookup"><span data-stu-id="c82ab-134">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-135">- DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="c82ab-135">-DisplayNamesFilter</span></span>
<span data-ttu-id="c82ab-136">Filtr nazw wyświetlanych w regułach alertów.</span><span class="sxs-lookup"><span data-stu-id="c82ab-136">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-137">— włączone</span><span class="sxs-lookup"><span data-stu-id="c82ab-137">-Enabled</span></span>
<span data-ttu-id="c82ab-138">Włączono regułę alertu.</span><span class="sxs-lookup"><span data-stu-id="c82ab-138">Alert Rule Enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c82ab-139">-InputObject</span></span>
<span data-ttu-id="c82ab-140">InputObject.</span><span class="sxs-lookup"><span data-stu-id="c82ab-140">InputObject.</span></span>

```yaml
Type: PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="c82ab-141">-ProductFilter</span></span>
<span data-ttu-id="c82ab-142">Alert Rule Product Filter (Filtr produktu reguły alertu).</span><span class="sxs-lookup"><span data-stu-id="c82ab-142">Alert Rule Product Filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-143">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="c82ab-143">-Query</span></span>
<span data-ttu-id="c82ab-144">Kwerenda reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="c82ab-144">Alert Rule Query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="c82ab-145">-QueryFrequency</span></span>
<span data-ttu-id="c82ab-146">Częstotliwość kwerend reguł alertu.</span><span class="sxs-lookup"><span data-stu-id="c82ab-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="c82ab-147">-QueryPeriod</span></span>
<span data-ttu-id="c82ab-148">Okres kwerendy reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="c82ab-148">Alert Rule Query Period.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c82ab-149">-ResourceGroupName</span></span>
<span data-ttu-id="c82ab-150">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c82ab-150">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c82ab-151">-ResourceId</span></span>
<span data-ttu-id="c82ab-152">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="c82ab-152">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="c82ab-153">-SeveritiesFilter</span></span>
<span data-ttu-id="c82ab-154">Filtr ważności reguł alertu.</span><span class="sxs-lookup"><span data-stu-id="c82ab-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-155">— Ważność</span><span class="sxs-lookup"><span data-stu-id="c82ab-155">-Severity</span></span>
<span data-ttu-id="c82ab-156">Ważność zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="c82ab-156">Incident Severity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-157">-NajbłędszaWyświetlona</span><span class="sxs-lookup"><span data-stu-id="c82ab-157">-SuppressionDisabled</span></span>
<span data-ttu-id="c82ab-158">Reguła alertu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="c82ab-158">Alert Rule Suppression Disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-159">-NatłokNaDmiernie</span><span class="sxs-lookup"><span data-stu-id="c82ab-159">-SuppressionDuration</span></span>
<span data-ttu-id="c82ab-160">Czas trwania reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="c82ab-160">Alert Rule Suppression Duration.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-161">-NaiwneEnabled</span><span class="sxs-lookup"><span data-stu-id="c82ab-161">-SuppressionEnabled</span></span>
<span data-ttu-id="c82ab-162">Włączone reguły alertów.</span><span class="sxs-lookup"><span data-stu-id="c82ab-162">Alert Rule Suppression Enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-163">- Taktyka</span><span class="sxs-lookup"><span data-stu-id="c82ab-163">-Tactics</span></span>
<span data-ttu-id="c82ab-164">Taktyka reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="c82ab-164">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-165">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="c82ab-165">-TriggerOperator</span></span>
<span data-ttu-id="c82ab-166">Operator wyzwalacza reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="c82ab-166">Alert Rule Trigger Operator.</span></span>

```yaml
Type: TriggerOperator
Parameter Sets: (All)
Aliases:
Accepted values: GreaterThan, LessThan, Equal, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-167">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="c82ab-167">-TriggerThreshold</span></span>
<span data-ttu-id="c82ab-168">Próg wyzwalacza reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="c82ab-168">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-169">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c82ab-169">-WorkspaceName</span></span>
<span data-ttu-id="c82ab-170">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="c82ab-170">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-171">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c82ab-171">-Confirm</span></span>
<span data-ttu-id="c82ab-172">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c82ab-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c82ab-173">-WhatIf</span></span>
<span data-ttu-id="c82ab-174">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c82ab-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c82ab-175">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c82ab-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82ab-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c82ab-176">CommonParameters</span></span>
<span data-ttu-id="c82ab-177">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c82ab-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c82ab-178">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c82ab-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c82ab-179">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c82ab-179">INPUTS</span></span>

### <span data-ttu-id="c82ab-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="c82ab-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="c82ab-181">System.String</span><span class="sxs-lookup"><span data-stu-id="c82ab-181">System.String</span></span>

## <span data-ttu-id="c82ab-182">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c82ab-182">OUTPUTS</span></span>

### <span data-ttu-id="c82ab-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="c82ab-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

## <span data-ttu-id="c82ab-184">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c82ab-184">NOTES</span></span>

## <span data-ttu-id="c82ab-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c82ab-185">RELATED LINKS</span></span>
