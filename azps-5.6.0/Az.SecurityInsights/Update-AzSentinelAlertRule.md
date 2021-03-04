---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
ms.openlocfilehash: 86b6067e13a7b4d1d90e8fcb3d308af797dab354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969882"
---
# <span data-ttu-id="10a8a-101">Update-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="10a8a-101">Update-AzSentinelAlertRule</span></span>

## <span data-ttu-id="10a8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="10a8a-103">Tworzenie reguły analitycznej (reguły alertu).</span><span class="sxs-lookup"><span data-stu-id="10a8a-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="10a8a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10a8a-104">SYNTAX</span></span>

### <span data-ttu-id="10a8a-105">AlertRuleId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="10a8a-105">AlertRuleId (Default)</span></span>
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

### <span data-ttu-id="10a8a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="10a8a-106">InputObject</span></span>
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

### <span data-ttu-id="10a8a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="10a8a-107">ResourceId</span></span>
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

## <span data-ttu-id="10a8a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="10a8a-108">DESCRIPTION</span></span>
<span data-ttu-id="10a8a-109">Polecenie **cmdlet Update-AzSentinelAlertRule** aktualizuje regułę analityczna (reguła alertu) w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="10a8a-109">The **Update-AzSentinelAlertRule** cmdlet updates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="10a8a-110">Można użyć wartości -InputObject, -ResourceId lub -AlertId.</span><span class="sxs-lookup"><span data-stu-id="10a8a-110">You can use an -InputObject or -ResourceId or -AlertId.</span></span>  <span data-ttu-id="10a8a-111">Możesz zaktualizować 1 lub więcej parmaterów proprtery.</span><span class="sxs-lookup"><span data-stu-id="10a8a-111">You can update 1 or more proprtery parmaters.</span></span>
<span data-ttu-id="10a8a-112">Możesz użyć *parametru Confirm* i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="10a8a-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>


## <span data-ttu-id="10a8a-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10a8a-113">EXAMPLES</span></span>

### <span data-ttu-id="10a8a-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="10a8a-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -Disabled -DisplayName "Disabled-AlertRuleDisplayName"
```

<span data-ttu-id="10a8a-115">W tym przykładzie zmieniono ustawienie wartości **AlertRule** na *Disabled* (Wyłączone) i zmieniono nazwę na *Disabled-AlertRuleDisplayName*(Wyłączone).</span><span class="sxs-lookup"><span data-stu-id="10a8a-115">This example updates an **AlertRule** setting it to *Disabled* and renames to *Disabled-AlertRuleDisplayName*.</span></span>  <span data-ttu-id="10a8a-116">Wszystkie pozostałe właściwości pozostaną takie same.</span><span class="sxs-lookup"><span data-stu-id="10a8a-116">All other properties will remain the same.</span></span>

### <span data-ttu-id="10a8a-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="10a8a-117">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
PS C:\> Update-AzSentinelAlertRule -InputObject $AlertRule -Disabled
```

<span data-ttu-id="10a8a-118">W tym przykładzie **aktualizacja alertu AlertRule** została wyłączona przy użyciu ustawienia InputObject.</span><span class="sxs-lookup"><span data-stu-id="10a8a-118">This example updates an **AlertRule** using an InputObject setting it to *Disabled*.</span></span>  <span data-ttu-id="10a8a-119">Wszystkie pozostałe właściwości pozostaną takie same.</span><span class="sxs-lookup"><span data-stu-id="10a8a-119">All other properties will remain the same.</span></span>


## <span data-ttu-id="10a8a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10a8a-120">PARAMETERS</span></span>

### <span data-ttu-id="10a8a-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="10a8a-121">-AlertRuleId</span></span>
<span data-ttu-id="10a8a-122">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="10a8a-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="10a8a-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="10a8a-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="10a8a-124">Szablon reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="10a8a-124">Alert Rule Template.</span></span>

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

### <span data-ttu-id="10a8a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a8a-125">-DefaultProfile</span></span>
<span data-ttu-id="10a8a-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="10a8a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10a8a-127">— Opis</span><span class="sxs-lookup"><span data-stu-id="10a8a-127">-Description</span></span>
<span data-ttu-id="10a8a-128">Opis.</span><span class="sxs-lookup"><span data-stu-id="10a8a-128">Description.</span></span>

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

### <span data-ttu-id="10a8a-129">— Wyłączone</span><span class="sxs-lookup"><span data-stu-id="10a8a-129">-Disabled</span></span>
<span data-ttu-id="10a8a-130">Reguła alertu wyłączona.</span><span class="sxs-lookup"><span data-stu-id="10a8a-130">Alert Rule Disabled.</span></span>

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

### <span data-ttu-id="10a8a-131">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="10a8a-131">-DisplayName</span></span>
<span data-ttu-id="10a8a-132">Nazwa wyświetlana reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="10a8a-132">Alert Rule Display Name.</span></span>

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

### <span data-ttu-id="10a8a-133">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="10a8a-133">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="10a8a-134">Reguła alertu wyświetla nazwy wyklucz filtru.</span><span class="sxs-lookup"><span data-stu-id="10a8a-134">Alert Rule Display Names Exclude Filter.</span></span>

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

### <span data-ttu-id="10a8a-135">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="10a8a-135">-DisplayNamesFilter</span></span>
<span data-ttu-id="10a8a-136">Filtr nazw wyświetlanych w regułach alertów.</span><span class="sxs-lookup"><span data-stu-id="10a8a-136">Alert Rule Display Names Filter.</span></span>

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

### <span data-ttu-id="10a8a-137">— włączone</span><span class="sxs-lookup"><span data-stu-id="10a8a-137">-Enabled</span></span>
<span data-ttu-id="10a8a-138">Reguła alertu włączona.</span><span class="sxs-lookup"><span data-stu-id="10a8a-138">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="10a8a-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10a8a-139">-InputObject</span></span>
<span data-ttu-id="10a8a-140">InputObject.</span><span class="sxs-lookup"><span data-stu-id="10a8a-140">InputObject.</span></span>

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

### <span data-ttu-id="10a8a-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="10a8a-141">-ProductFilter</span></span>
<span data-ttu-id="10a8a-142">Alert Rule Product Filter (Filtr produktu reguły alertu).</span><span class="sxs-lookup"><span data-stu-id="10a8a-142">Alert Rule Product Filter.</span></span>

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

### <span data-ttu-id="10a8a-143">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="10a8a-143">-Query</span></span>
<span data-ttu-id="10a8a-144">Kwerenda reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="10a8a-144">Alert Rule Query.</span></span>

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

### <span data-ttu-id="10a8a-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="10a8a-145">-QueryFrequency</span></span>
<span data-ttu-id="10a8a-146">Częstotliwość kwerend reguł alertu.</span><span class="sxs-lookup"><span data-stu-id="10a8a-146">Alert Rule Query Frequency.</span></span>

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

### <span data-ttu-id="10a8a-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="10a8a-147">-QueryPeriod</span></span>
<span data-ttu-id="10a8a-148">Okres kwerendy reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="10a8a-148">Alert Rule Query Period.</span></span>

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

### <span data-ttu-id="10a8a-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10a8a-149">-ResourceGroupName</span></span>
<span data-ttu-id="10a8a-150">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10a8a-150">Resource group name.</span></span>

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

### <span data-ttu-id="10a8a-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10a8a-151">-ResourceId</span></span>
<span data-ttu-id="10a8a-152">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="10a8a-152">Resource Id.</span></span>

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

### <span data-ttu-id="10a8a-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="10a8a-153">-SeveritiesFilter</span></span>
<span data-ttu-id="10a8a-154">Filtr ważności reguł alertu.</span><span class="sxs-lookup"><span data-stu-id="10a8a-154">Alert Rule Severities Filter.</span></span>

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

### <span data-ttu-id="10a8a-155">— Ważność</span><span class="sxs-lookup"><span data-stu-id="10a8a-155">-Severity</span></span>
<span data-ttu-id="10a8a-156">Ważność zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="10a8a-156">Incident Severity.</span></span>

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

### <span data-ttu-id="10a8a-157">-NajbłędszaWyświetlona</span><span class="sxs-lookup"><span data-stu-id="10a8a-157">-SuppressionDisabled</span></span>
<span data-ttu-id="10a8a-158">Reguła alertu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="10a8a-158">Alert Rule Suppression Disabled.</span></span>

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

### <span data-ttu-id="10a8a-159">-NatłokNaDmiernie</span><span class="sxs-lookup"><span data-stu-id="10a8a-159">-SuppressionDuration</span></span>
<span data-ttu-id="10a8a-160">Czas trwania reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="10a8a-160">Alert Rule Suppression Duration.</span></span>

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

### <span data-ttu-id="10a8a-161">-NaiwneEnabled</span><span class="sxs-lookup"><span data-stu-id="10a8a-161">-SuppressionEnabled</span></span>
<span data-ttu-id="10a8a-162">Włączone regułę alertu.</span><span class="sxs-lookup"><span data-stu-id="10a8a-162">Alert Rule Suppression Enabled.</span></span>

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

### <span data-ttu-id="10a8a-163">- Taktyka</span><span class="sxs-lookup"><span data-stu-id="10a8a-163">-Tactics</span></span>
<span data-ttu-id="10a8a-164">Taktyka reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="10a8a-164">Alert Rule Tactics.</span></span>

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

### <span data-ttu-id="10a8a-165">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="10a8a-165">-TriggerOperator</span></span>
<span data-ttu-id="10a8a-166">Operator wyzwalacza reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="10a8a-166">Alert Rule Trigger Operator.</span></span>

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

### <span data-ttu-id="10a8a-167">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="10a8a-167">-TriggerThreshold</span></span>
<span data-ttu-id="10a8a-168">Próg wyzwalacza reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="10a8a-168">Alert Rule Trigger Threshold.</span></span>

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

### <span data-ttu-id="10a8a-169">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="10a8a-169">-WorkspaceName</span></span>
<span data-ttu-id="10a8a-170">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="10a8a-170">Workspace Name.</span></span>

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

### <span data-ttu-id="10a8a-171">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10a8a-171">-Confirm</span></span>
<span data-ttu-id="10a8a-172">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="10a8a-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10a8a-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10a8a-173">-WhatIf</span></span>
<span data-ttu-id="10a8a-174">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10a8a-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10a8a-175">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="10a8a-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10a8a-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a8a-176">CommonParameters</span></span>
<span data-ttu-id="10a8a-177">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10a8a-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a8a-178">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10a8a-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a8a-179">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10a8a-179">INPUTS</span></span>

### <span data-ttu-id="10a8a-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="10a8a-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="10a8a-181">System.String</span><span class="sxs-lookup"><span data-stu-id="10a8a-181">System.String</span></span>

## <span data-ttu-id="10a8a-182">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10a8a-182">OUTPUTS</span></span>

### <span data-ttu-id="10a8a-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="10a8a-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

## <span data-ttu-id="10a8a-184">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10a8a-184">NOTES</span></span>

## <span data-ttu-id="10a8a-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10a8a-185">RELATED LINKS</span></span>
