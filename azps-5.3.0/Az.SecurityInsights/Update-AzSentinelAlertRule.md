---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
ms.openlocfilehash: 56f1878507424c1396130aa91a5fc7b086f101c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502956"
---
# <span data-ttu-id="2c848-101">Update-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="2c848-101">Update-AzSentinelAlertRule</span></span>

## <span data-ttu-id="2c848-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c848-102">SYNOPSIS</span></span>
<span data-ttu-id="2c848-103">Tworzenie raportu analitycznego (reguły alertu).</span><span class="sxs-lookup"><span data-stu-id="2c848-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="2c848-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c848-104">SYNTAX</span></span>

### <span data-ttu-id="2c848-105">AlertRuleId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2c848-105">AlertRuleId (Default)</span></span>
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

### <span data-ttu-id="2c848-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="2c848-106">InputObject</span></span>
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

### <span data-ttu-id="2c848-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="2c848-107">ResourceId</span></span>
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

## <span data-ttu-id="2c848-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2c848-108">DESCRIPTION</span></span>
<span data-ttu-id="2c848-109">Polecenie cmdlet **Update-AzSentinelAlertRule** aktualizuje dane analityczne (regułę alertu) w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="2c848-109">The **Update-AzSentinelAlertRule** cmdlet updates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="2c848-110">Możesz użyć elementu-Inputobject lub-ResourceId lub-AlertId.</span><span class="sxs-lookup"><span data-stu-id="2c848-110">You can use an -InputObject or -ResourceId or -AlertId.</span></span>  <span data-ttu-id="2c848-111">Możesz zaktualizować co najmniej 1 proprtery parmaters.</span><span class="sxs-lookup"><span data-stu-id="2c848-111">You can update 1 or more proprtery parmaters.</span></span>
<span data-ttu-id="2c848-112">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2c848-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>


## <span data-ttu-id="2c848-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c848-113">EXAMPLES</span></span>

### <span data-ttu-id="2c848-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2c848-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -Disabled -DisplayName "Disabled-AlertRuleDisplayName"
```

<span data-ttu-id="2c848-115">W tym przykładzie Zaktualizowano **AlertRule** ustawienie wyłączone *i* ponowne nadawanie nazwy *wyłączone-AlertRuleDisplayName*.</span><span class="sxs-lookup"><span data-stu-id="2c848-115">This example updates an **AlertRule** setting it to *Disabled* and renames to *Disabled-AlertRuleDisplayName*.</span></span>  <span data-ttu-id="2c848-116">Pozostałe właściwości pozostaną bez zmian.</span><span class="sxs-lookup"><span data-stu-id="2c848-116">All other properties will remain the same.</span></span>

### <span data-ttu-id="2c848-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2c848-117">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
PS C:\> Update-AzSentinelAlertRule -InputObject $AlertRule -Disabled
```

<span data-ttu-id="2c848-118">W tym przykładzie Zaktualizowano **AlertRule** przy użyciu ustawienia inputobject, które można ustawić jako *wyłączone*.</span><span class="sxs-lookup"><span data-stu-id="2c848-118">This example updates an **AlertRule** using an InputObject setting it to *Disabled*.</span></span>  <span data-ttu-id="2c848-119">Pozostałe właściwości pozostaną bez zmian.</span><span class="sxs-lookup"><span data-stu-id="2c848-119">All other properties will remain the same.</span></span>


## <span data-ttu-id="2c848-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c848-120">PARAMETERS</span></span>

### <span data-ttu-id="2c848-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="2c848-121">-AlertRuleId</span></span>
<span data-ttu-id="2c848-122">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="2c848-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="2c848-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="2c848-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="2c848-124">Szablon reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="2c848-124">Alert Rule Template.</span></span>

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

### <span data-ttu-id="2c848-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c848-125">-DefaultProfile</span></span>
<span data-ttu-id="2c848-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c848-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c848-127">— Opis</span><span class="sxs-lookup"><span data-stu-id="2c848-127">-Description</span></span>
<span data-ttu-id="2c848-128">Opis.</span><span class="sxs-lookup"><span data-stu-id="2c848-128">Description.</span></span>

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

### <span data-ttu-id="2c848-129">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="2c848-129">-Disabled</span></span>
<span data-ttu-id="2c848-130">Reguła alertu wyłączona.</span><span class="sxs-lookup"><span data-stu-id="2c848-130">Alert Rule Disabled.</span></span>

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

### <span data-ttu-id="2c848-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2c848-131">-DisplayName</span></span>
<span data-ttu-id="2c848-132">Nazwa wyświetlana reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="2c848-132">Alert Rule Display Name.</span></span>

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

### <span data-ttu-id="2c848-133">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="2c848-133">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="2c848-134">Nazwa wyświetlana reguły alertu z wykluczeniem filtru.</span><span class="sxs-lookup"><span data-stu-id="2c848-134">Alert Rule Display Names Exclude Filter.</span></span>

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

### <span data-ttu-id="2c848-135">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="2c848-135">-DisplayNamesFilter</span></span>
<span data-ttu-id="2c848-136">Filtr nazw wyświetlanych w regułach alertów.</span><span class="sxs-lookup"><span data-stu-id="2c848-136">Alert Rule Display Names Filter.</span></span>

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

### <span data-ttu-id="2c848-137">-Enabled</span><span class="sxs-lookup"><span data-stu-id="2c848-137">-Enabled</span></span>
<span data-ttu-id="2c848-138">Włączono regułę alertu.</span><span class="sxs-lookup"><span data-stu-id="2c848-138">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="2c848-139">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2c848-139">-InputObject</span></span>
<span data-ttu-id="2c848-140">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="2c848-140">InputObject.</span></span>

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

### <span data-ttu-id="2c848-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="2c848-141">-ProductFilter</span></span>
<span data-ttu-id="2c848-142">Filtr produktu reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="2c848-142">Alert Rule Product Filter.</span></span>

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

### <span data-ttu-id="2c848-143">-Query</span><span class="sxs-lookup"><span data-stu-id="2c848-143">-Query</span></span>
<span data-ttu-id="2c848-144">Kwerenda reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="2c848-144">Alert Rule Query.</span></span>

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

### <span data-ttu-id="2c848-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="2c848-145">-QueryFrequency</span></span>
<span data-ttu-id="2c848-146">Częstotliwość kwerend reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="2c848-146">Alert Rule Query Frequency.</span></span>

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

### <span data-ttu-id="2c848-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="2c848-147">-QueryPeriod</span></span>
<span data-ttu-id="2c848-148">Okres zapytania reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="2c848-148">Alert Rule Query Period.</span></span>

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

### <span data-ttu-id="2c848-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c848-149">-ResourceGroupName</span></span>
<span data-ttu-id="2c848-150">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2c848-150">Resource group name.</span></span>

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

### <span data-ttu-id="2c848-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c848-151">-ResourceId</span></span>
<span data-ttu-id="2c848-152">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="2c848-152">Resource Id.</span></span>

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

### <span data-ttu-id="2c848-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="2c848-153">-SeveritiesFilter</span></span>
<span data-ttu-id="2c848-154">Filtr dotyczący wykluczeń reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="2c848-154">Alert Rule Severities Filter.</span></span>

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

### <span data-ttu-id="2c848-155">— Ważność</span><span class="sxs-lookup"><span data-stu-id="2c848-155">-Severity</span></span>
<span data-ttu-id="2c848-156">Ważność incydentu.</span><span class="sxs-lookup"><span data-stu-id="2c848-156">Incident Severity.</span></span>

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

### <span data-ttu-id="2c848-157">-SuppressionDisabled</span><span class="sxs-lookup"><span data-stu-id="2c848-157">-SuppressionDisabled</span></span>
<span data-ttu-id="2c848-158">Wyłączono pomijanie reguł alertów.</span><span class="sxs-lookup"><span data-stu-id="2c848-158">Alert Rule Suppression Disabled.</span></span>

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

### <span data-ttu-id="2c848-159">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="2c848-159">-SuppressionDuration</span></span>
<span data-ttu-id="2c848-160">Czas trwania ukrywania reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="2c848-160">Alert Rule Suppression Duration.</span></span>

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

### <span data-ttu-id="2c848-161">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="2c848-161">-SuppressionEnabled</span></span>
<span data-ttu-id="2c848-162">Włączono pomijanie reguł alertów.</span><span class="sxs-lookup"><span data-stu-id="2c848-162">Alert Rule Suppression Enabled.</span></span>

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

### <span data-ttu-id="2c848-163">-Taktykom</span><span class="sxs-lookup"><span data-stu-id="2c848-163">-Tactics</span></span>
<span data-ttu-id="2c848-164">Reguła alertu taktykom.</span><span class="sxs-lookup"><span data-stu-id="2c848-164">Alert Rule Tactics.</span></span>

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

### <span data-ttu-id="2c848-165">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="2c848-165">-TriggerOperator</span></span>
<span data-ttu-id="2c848-166">Operator wyzwalacza reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="2c848-166">Alert Rule Trigger Operator.</span></span>

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

### <span data-ttu-id="2c848-167">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="2c848-167">-TriggerThreshold</span></span>
<span data-ttu-id="2c848-168">Próg wyzwalacza reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="2c848-168">Alert Rule Trigger Threshold.</span></span>

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

### <span data-ttu-id="2c848-169">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="2c848-169">-WorkspaceName</span></span>
<span data-ttu-id="2c848-170">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="2c848-170">Workspace Name.</span></span>

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

### <span data-ttu-id="2c848-171">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c848-171">-Confirm</span></span>
<span data-ttu-id="2c848-172">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c848-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c848-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c848-173">-WhatIf</span></span>
<span data-ttu-id="2c848-174">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c848-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c848-175">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2c848-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c848-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c848-176">CommonParameters</span></span>
<span data-ttu-id="2c848-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c848-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c848-178">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c848-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c848-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c848-179">INPUTS</span></span>

### <span data-ttu-id="2c848-180">Microsoft. Azure. Commands. SecurityInsights. models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="2c848-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="2c848-181">System. String</span><span class="sxs-lookup"><span data-stu-id="2c848-181">System.String</span></span>

## <span data-ttu-id="2c848-182">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c848-182">OUTPUTS</span></span>

### <span data-ttu-id="2c848-183">Microsoft. Azure. Commands. SecurityInsights. models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="2c848-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

## <span data-ttu-id="2c848-184">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c848-184">NOTES</span></span>

## <span data-ttu-id="2c848-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c848-185">RELATED LINKS</span></span>
