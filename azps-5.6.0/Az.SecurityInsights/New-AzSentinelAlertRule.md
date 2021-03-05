---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
ms.openlocfilehash: 0efb30f9c740362ac6e8c432179599c7d4aef88d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976369"
---
# <span data-ttu-id="291ad-101">New-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="291ad-101">New-AzSentinelAlertRule</span></span>

## <span data-ttu-id="291ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="291ad-102">SYNOPSIS</span></span>
<span data-ttu-id="291ad-103">Tworzenie reguły analitycznej (reguły alertu).</span><span class="sxs-lookup"><span data-stu-id="291ad-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="291ad-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="291ad-104">SYNTAX</span></span>

### <span data-ttu-id="291ad-105">ScheduledAlertRule (domyślne)</span><span class="sxs-lookup"><span data-stu-id="291ad-105">ScheduledAlertRule (Default)</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Scheduled]
 [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled] -DisplayName <String>
 [-Description <String>] [-SuppressionDuration <TimeSpan>] [-SuppressionEnabled] -Query <String>
 -QueryFrequency <TimeSpan> -QueryPeriod <TimeSpan> -Severity <String>
 [-Tactics <System.Collections.Generic.IList`1[System.String]>] [-TriggerOperator <TriggerOperator>]
 -TriggerThreshold <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="291ad-106">NajwłaszszowyRule</span><span class="sxs-lookup"><span data-stu-id="291ad-106">FusionAlertRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Fusion] [-AlertRuleId <String>]
 -AlertRuleTemplateName <String> [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="291ad-107">MicrosoftSecurityIncidentCreationRule</span><span class="sxs-lookup"><span data-stu-id="291ad-107">MicrosoftSecurityIncidentCreationRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-MicrosoftSecurityIncidentCreation] [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled]
 -DisplayName <String> -ProductFilter <String> [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="291ad-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="291ad-108">DESCRIPTION</span></span>
<span data-ttu-id="291ad-109">Polecenie **cmdlet New-AzSentinelAlertRule** tworzy regułę analityczna (reguła alertu) w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="291ad-109">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="291ad-110">Aby określić rodzaj reguły alertu  do utworzenia, należy określić jeden z trzech parametrów: *Prac, Scheduled* lub *MicrosoftSecurityIncidentCreation.*</span><span class="sxs-lookup"><span data-stu-id="291ad-110">You must specify one of the three parameters, *Fusion*, *Scheduled* or *MicrosoftSecurityIncidentCreation*, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="291ad-111">Każdy rodzaj ma inne wymagane paramaty.</span><span class="sxs-lookup"><span data-stu-id="291ad-111">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="291ad-112">Możesz użyć *parametru Confirm* i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="291ad-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="291ad-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="291ad-113">EXAMPLES</span></span>

### <span data-ttu-id="291ad-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="291ad-114">Example 1</span></span>
```powershell
PS C:\>$AlertRuleTemplateName = "f71aba3d-28fb-450b-b192-4e76a83015c8"
PS C:\>$AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Fusion -Enabled -AlertRuleTemplateName $AlertRuleTemplateName
```

<span data-ttu-id="291ad-115">W tym przykładzie na podstawie szablonu zaawansowanego wykrywania ataków wielosetapowych jest tworzenie alertu typu **Rule,** a następnie jest on przechowywał w zmiennej $AlertRule danych. </span><span class="sxs-lookup"><span data-stu-id="291ad-115">This example creates a **AlertRule** of the *Fusion* kind based on the Template for *Advanced Multistage Attack Detection*, and then stores it in the $AlertRule variable.</span></span>

### <span data-ttu-id="291ad-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="291ad-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplateName = "a2e0eb51-1f11-461a-999b-cd0ebe5c7a72"
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftSecurityIncidentCreation -Enabled -AlertRuleTemplateName $AlertRuleTemplateName -DisplayName "Create incidents based on Azure Security Center for IoT" -ProductFilter "Azure Security Center for IoT"
```

<span data-ttu-id="291ad-117">W tym przykładzie jest tworzenie alertu typu *MicrosoftSecurityIncidentCreation* na podstawie szablonu Tworzenie zdarzeń na podstawie alertów usługi Azure Security Center dla alertów *IoT,* **a** następnie jest on $AlertRule wariancji.</span><span class="sxs-lookup"><span data-stu-id="291ad-117">This example creates a **AlertRule** of the *MicrosoftSecurityIncidentCreation* kind based on the template for *Create incidents based on Azure Security Center for IoT alerts*, and then stores it in the $AlertRule varaible.</span></span>

### <span data-ttu-id="291ad-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="291ad-118">Example 2</span></span>
```powershell
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Scheduled -Enabled -DisplayName "Powershell Exection Alert (Several Times per Hour)" -Severity Low -Query "SecurityEvent | where EventId == 4688" -QueryFrequency (New-TimeSpan -Hours 1) -QueryPeriod (New-TimeSpan -Hours 1) -TriggerThreshold 10
```

<span data-ttu-id="291ad-119">W tym przykładzie jest  tworzenie **połączenia danych** typu Zaplanowane, a następnie jest on $AlertRule varaible.</span><span class="sxs-lookup"><span data-stu-id="291ad-119">This example creates a **DataConnector** of the *Scheduled* kind, and then stores it in the $AlertRule varaible.</span></span>

## <span data-ttu-id="291ad-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="291ad-120">PARAMETERS</span></span>

### <span data-ttu-id="291ad-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="291ad-121">-AlertRuleId</span></span>
<span data-ttu-id="291ad-122">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="291ad-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="291ad-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="291ad-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="291ad-124">Szablon reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="291ad-124">Alert Rule Template.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="291ad-125">-DefaultProfile</span></span>
<span data-ttu-id="291ad-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="291ad-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="291ad-127">— Opis</span><span class="sxs-lookup"><span data-stu-id="291ad-127">-Description</span></span>
<span data-ttu-id="291ad-128">Opis.</span><span class="sxs-lookup"><span data-stu-id="291ad-128">Description.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-129">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="291ad-129">-DisplayName</span></span>
<span data-ttu-id="291ad-130">Nazwa wyświetlana reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="291ad-130">Alert Rule Display Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-131">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="291ad-131">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="291ad-132">Reguła alertu wyświetla nazwy wyklucz filtru.</span><span class="sxs-lookup"><span data-stu-id="291ad-132">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-133">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="291ad-133">-DisplayNamesFilter</span></span>
<span data-ttu-id="291ad-134">Filtr nazw wyświetlanych w regułach alertów.</span><span class="sxs-lookup"><span data-stu-id="291ad-134">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-135">— włączone</span><span class="sxs-lookup"><span data-stu-id="291ad-135">-Enabled</span></span>
<span data-ttu-id="291ad-136">Reguła alertu włączona.</span><span class="sxs-lookup"><span data-stu-id="291ad-136">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="291ad-137">- Dorównanie</span><span class="sxs-lookup"><span data-stu-id="291ad-137">-Fusion</span></span>
<span data-ttu-id="291ad-138">Typ reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="291ad-138">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-139">-MicrosoftSecurityIncidentCreation</span><span class="sxs-lookup"><span data-stu-id="291ad-139">-MicrosoftSecurityIncidentCreation</span></span>
<span data-ttu-id="291ad-140">Typ reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="291ad-140">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="291ad-141">-ProductFilter</span></span>
<span data-ttu-id="291ad-142">Alert Rule Product Filter (Filtr produktu reguły alertu).</span><span class="sxs-lookup"><span data-stu-id="291ad-142">Alert Rule Product Filter.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-143">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="291ad-143">-Query</span></span>
<span data-ttu-id="291ad-144">Kwerenda reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="291ad-144">Alert Rule Query.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="291ad-145">-QueryFrequency</span></span>
<span data-ttu-id="291ad-146">Częstotliwość kwerend reguł alertu.</span><span class="sxs-lookup"><span data-stu-id="291ad-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="291ad-147">-QueryPeriod</span></span>
<span data-ttu-id="291ad-148">Okres kwerendy reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="291ad-148">Alert Rule Query Period.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="291ad-149">-ResourceGroupName</span></span>
<span data-ttu-id="291ad-150">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="291ad-150">Resource group name.</span></span>

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

### <span data-ttu-id="291ad-151">— Zaplanowane</span><span class="sxs-lookup"><span data-stu-id="291ad-151">-Scheduled</span></span>
<span data-ttu-id="291ad-152">Typ reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="291ad-152">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="291ad-153">-SeveritiesFilter</span></span>
<span data-ttu-id="291ad-154">Filtr ważności reguł alertu.</span><span class="sxs-lookup"><span data-stu-id="291ad-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-155">— Ważność</span><span class="sxs-lookup"><span data-stu-id="291ad-155">-Severity</span></span>
<span data-ttu-id="291ad-156">Ważność zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="291ad-156">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-157">-NatłokNaDmiernie</span><span class="sxs-lookup"><span data-stu-id="291ad-157">-SuppressionDuration</span></span>
<span data-ttu-id="291ad-158">Czas trwania reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="291ad-158">Alert Rule Suppression Duration.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-159">-NaiwneEnabled</span><span class="sxs-lookup"><span data-stu-id="291ad-159">-SuppressionEnabled</span></span>
<span data-ttu-id="291ad-160">Włączone regułę alertu.</span><span class="sxs-lookup"><span data-stu-id="291ad-160">Alert Rule Suppression Enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-161">- Taktyka</span><span class="sxs-lookup"><span data-stu-id="291ad-161">-Tactics</span></span>
<span data-ttu-id="291ad-162">Taktyka reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="291ad-162">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-163">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="291ad-163">-TriggerOperator</span></span>
<span data-ttu-id="291ad-164">Operator wyzwalacza reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="291ad-164">Alert Rule Trigger Operator.</span></span>

```yaml
Type: Microsoft.Azure.Management.SecurityInsights.Models.TriggerOperator
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: Equal, GreaterThan, LessThan, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-165">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="291ad-165">-TriggerThreshold</span></span>
<span data-ttu-id="291ad-166">Próg wyzwalacza reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="291ad-166">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ad-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="291ad-167">-WorkspaceName</span></span>
<span data-ttu-id="291ad-168">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="291ad-168">Workspace Name.</span></span>

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

### <span data-ttu-id="291ad-169">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="291ad-169">-Confirm</span></span>
<span data-ttu-id="291ad-170">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="291ad-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="291ad-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="291ad-171">-WhatIf</span></span>
<span data-ttu-id="291ad-172">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="291ad-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="291ad-173">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="291ad-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="291ad-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="291ad-174">CommonParameters</span></span>
<span data-ttu-id="291ad-175">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="291ad-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="291ad-176">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="291ad-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="291ad-177">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="291ad-177">INPUTS</span></span>

### <span data-ttu-id="291ad-178">Brak</span><span class="sxs-lookup"><span data-stu-id="291ad-178">None</span></span>
## <span data-ttu-id="291ad-179">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="291ad-179">OUTPUTS</span></span>

### <span data-ttu-id="291ad-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="291ad-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="291ad-181">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="291ad-181">NOTES</span></span>

## <span data-ttu-id="291ad-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="291ad-182">RELATED LINKS</span></span>
