---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
ms.openlocfilehash: 97a07b515cff6cfd8521033dbe7380eb2a7bc1d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502978"
---
# <span data-ttu-id="cbe7a-101">New-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="cbe7a-101">New-AzSentinelAlertRule</span></span>

## <span data-ttu-id="cbe7a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cbe7a-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe7a-103">Tworzenie raportu analitycznego (reguły alertu).</span><span class="sxs-lookup"><span data-stu-id="cbe7a-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="cbe7a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cbe7a-104">SYNTAX</span></span>

### <span data-ttu-id="cbe7a-105">ScheduledAlertRule (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cbe7a-105">ScheduledAlertRule (Default)</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Scheduled]
 [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled] -DisplayName <String>
 [-Description <String>] [-SuppressionDuration <TimeSpan>] [-SuppressionEnabled] -Query <String>
 -QueryFrequency <TimeSpan> -QueryPeriod <TimeSpan> -Severity <String>
 [-Tactics <System.Collections.Generic.IList`1[System.String]>] [-TriggerOperator <TriggerOperator>]
 -TriggerThreshold <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbe7a-106">FusionAlertRule</span><span class="sxs-lookup"><span data-stu-id="cbe7a-106">FusionAlertRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Fusion] [-AlertRuleId <String>]
 -AlertRuleTemplateName <String> [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cbe7a-107">MicrosoftSecurityIncidentCreationRule</span><span class="sxs-lookup"><span data-stu-id="cbe7a-107">MicrosoftSecurityIncidentCreationRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-MicrosoftSecurityIncidentCreation] [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled]
 -DisplayName <String> -ProductFilter <String> [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbe7a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cbe7a-108">DESCRIPTION</span></span>
<span data-ttu-id="cbe7a-109">Polecenie cmdlet **New-AzSentinelAlertRule** umożliwia utworzenie raportu analitycznego (reguły alertu) w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-109">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="cbe7a-110">Aby określić rodzaj reguły alertu do utworzenia, należy określić jedno z trzech parametrów: *Fusion*, *zaplanowane* lub *MicrosoftSecurityIncidentCreation*.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-110">You must specify one of the three parameters, *Fusion*, *Scheduled* or *MicrosoftSecurityIncidentCreation*, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="cbe7a-111">Każdy rodzaj ma inne wymagane paramaters.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-111">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="cbe7a-112">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="cbe7a-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cbe7a-113">EXAMPLES</span></span>

### <span data-ttu-id="cbe7a-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cbe7a-114">Example 1</span></span>
```powershell
PS C:\>$AlertRuleTemplateName = "f71aba3d-28fb-450b-b192-4e76a83015c8"
PS C:\>$AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Fusion -Enabled -AlertRuleTemplateName $AlertRuleTemplateName
```

<span data-ttu-id="cbe7a-115">W tym przykładzie jest tworzony **AlertRule** rodzajów *fuzji* opartych na szablonie *zaawansowanego wykrywania ataku Multistage*, a następnie zapisanie go w zmiennej $AlertRule.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-115">This example creates a **AlertRule** of the *Fusion* kind based on the Template for *Advanced Multistage Attack Detection*, and then stores it in the $AlertRule variable.</span></span>

### <span data-ttu-id="cbe7a-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cbe7a-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplateName = "a2e0eb51-1f11-461a-999b-cd0ebe5c7a72"
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftSecurityIncidentCreation -Enabled -AlertRuleTemplateName $AlertRuleTemplateName -DisplayName "Create incidents based on Azure Security Center for IoT" -ProductFilter "Azure Security Center for IoT"
```

<span data-ttu-id="cbe7a-117">W tym przykładzie jest tworzony **AlertRule** typu *MicrosoftSecurityIncidentCreation* na podstawie szablonu *Tworzenie zdarzeń na podstawie usługi Azure Security Center dla alertów IoT*, a następnie zapisanie go w $AlertRule varaible.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-117">This example creates a **AlertRule** of the *MicrosoftSecurityIncidentCreation* kind based on the template for *Create incidents based on Azure Security Center for IoT alerts*, and then stores it in the $AlertRule varaible.</span></span>

### <span data-ttu-id="cbe7a-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cbe7a-118">Example 2</span></span>
```powershell
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Scheduled -Enabled -DisplayName "Powershell Exection Alert (Several Times per Hour)" -Severity Low -Query "SecurityEvent | where EventId == 4688" -QueryFrequency (New-TimeSpan -Hours 1) -QueryPeriod (New-TimeSpan -Hours 1) -TriggerThreshold 10
```

<span data-ttu-id="cbe7a-119">W tym przykładzie jest tworzony program **dataconnect** o *zaplanowanym* rodzaju, a następnie przechowywany w $AlertRule varaible.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-119">This example creates a **DataConnector** of the *Scheduled* kind, and then stores it in the $AlertRule varaible.</span></span>

## <span data-ttu-id="cbe7a-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cbe7a-120">PARAMETERS</span></span>

### <span data-ttu-id="cbe7a-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="cbe7a-121">-AlertRuleId</span></span>
<span data-ttu-id="cbe7a-122">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="cbe7a-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="cbe7a-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="cbe7a-124">Szablon reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-124">Alert Rule Template.</span></span>

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

### <span data-ttu-id="cbe7a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbe7a-125">-DefaultProfile</span></span>
<span data-ttu-id="cbe7a-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbe7a-127">— Opis</span><span class="sxs-lookup"><span data-stu-id="cbe7a-127">-Description</span></span>
<span data-ttu-id="cbe7a-128">Opis.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-128">Description.</span></span>

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

### <span data-ttu-id="cbe7a-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cbe7a-129">-DisplayName</span></span>
<span data-ttu-id="cbe7a-130">Nazwa wyświetlana reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-130">Alert Rule Display Name.</span></span>

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

### <span data-ttu-id="cbe7a-131">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="cbe7a-131">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="cbe7a-132">Nazwa wyświetlana reguły alertu z wykluczeniem filtru.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-132">Alert Rule Display Names Exclude Filter.</span></span>

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

### <span data-ttu-id="cbe7a-133">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="cbe7a-133">-DisplayNamesFilter</span></span>
<span data-ttu-id="cbe7a-134">Filtr nazw wyświetlanych w regułach alertów.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-134">Alert Rule Display Names Filter.</span></span>

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

### <span data-ttu-id="cbe7a-135">-Enabled</span><span class="sxs-lookup"><span data-stu-id="cbe7a-135">-Enabled</span></span>
<span data-ttu-id="cbe7a-136">Włączono regułę alertu.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-136">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="cbe7a-137">-Fusion</span><span class="sxs-lookup"><span data-stu-id="cbe7a-137">-Fusion</span></span>
<span data-ttu-id="cbe7a-138">Rodzaj reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-138">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="cbe7a-139">-MicrosoftSecurityIncidentCreation</span><span class="sxs-lookup"><span data-stu-id="cbe7a-139">-MicrosoftSecurityIncidentCreation</span></span>
<span data-ttu-id="cbe7a-140">Rodzaj reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-140">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="cbe7a-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="cbe7a-141">-ProductFilter</span></span>
<span data-ttu-id="cbe7a-142">Filtr produktu reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-142">Alert Rule Product Filter.</span></span>

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

### <span data-ttu-id="cbe7a-143">-Query</span><span class="sxs-lookup"><span data-stu-id="cbe7a-143">-Query</span></span>
<span data-ttu-id="cbe7a-144">Kwerenda reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-144">Alert Rule Query.</span></span>

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

### <span data-ttu-id="cbe7a-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="cbe7a-145">-QueryFrequency</span></span>
<span data-ttu-id="cbe7a-146">Częstotliwość kwerend reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-146">Alert Rule Query Frequency.</span></span>

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

### <span data-ttu-id="cbe7a-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="cbe7a-147">-QueryPeriod</span></span>
<span data-ttu-id="cbe7a-148">Okres zapytania reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-148">Alert Rule Query Period.</span></span>

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

### <span data-ttu-id="cbe7a-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbe7a-149">-ResourceGroupName</span></span>
<span data-ttu-id="cbe7a-150">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-150">Resource group name.</span></span>

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

### <span data-ttu-id="cbe7a-151">— Zaplanowane</span><span class="sxs-lookup"><span data-stu-id="cbe7a-151">-Scheduled</span></span>
<span data-ttu-id="cbe7a-152">Rodzaj reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-152">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="cbe7a-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="cbe7a-153">-SeveritiesFilter</span></span>
<span data-ttu-id="cbe7a-154">Filtr dotyczący wykluczeń reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-154">Alert Rule Severities Filter.</span></span>

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

### <span data-ttu-id="cbe7a-155">— Ważność</span><span class="sxs-lookup"><span data-stu-id="cbe7a-155">-Severity</span></span>
<span data-ttu-id="cbe7a-156">Ważność incydentu.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-156">Incident Severity.</span></span>

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

### <span data-ttu-id="cbe7a-157">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="cbe7a-157">-SuppressionDuration</span></span>
<span data-ttu-id="cbe7a-158">Czas trwania ukrywania reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-158">Alert Rule Suppression Duration.</span></span>

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

### <span data-ttu-id="cbe7a-159">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="cbe7a-159">-SuppressionEnabled</span></span>
<span data-ttu-id="cbe7a-160">Włączono pomijanie reguł alertów.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-160">Alert Rule Suppression Enabled.</span></span>

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

### <span data-ttu-id="cbe7a-161">-Taktykom</span><span class="sxs-lookup"><span data-stu-id="cbe7a-161">-Tactics</span></span>
<span data-ttu-id="cbe7a-162">Reguła alertu taktykom.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-162">Alert Rule Tactics.</span></span>

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

### <span data-ttu-id="cbe7a-163">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="cbe7a-163">-TriggerOperator</span></span>
<span data-ttu-id="cbe7a-164">Operator wyzwalacza reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-164">Alert Rule Trigger Operator.</span></span>

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

### <span data-ttu-id="cbe7a-165">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="cbe7a-165">-TriggerThreshold</span></span>
<span data-ttu-id="cbe7a-166">Próg wyzwalacza reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-166">Alert Rule Trigger Threshold.</span></span>

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

### <span data-ttu-id="cbe7a-167">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="cbe7a-167">-WorkspaceName</span></span>
<span data-ttu-id="cbe7a-168">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-168">Workspace Name.</span></span>

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

### <span data-ttu-id="cbe7a-169">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cbe7a-169">-Confirm</span></span>
<span data-ttu-id="cbe7a-170">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbe7a-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbe7a-171">-WhatIf</span></span>
<span data-ttu-id="cbe7a-172">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cbe7a-173">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbe7a-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe7a-174">CommonParameters</span></span>
<span data-ttu-id="cbe7a-175">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbe7a-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe7a-176">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbe7a-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe7a-177">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbe7a-177">INPUTS</span></span>

### <span data-ttu-id="cbe7a-178">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cbe7a-178">None</span></span>
## <span data-ttu-id="cbe7a-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cbe7a-179">OUTPUTS</span></span>

### <span data-ttu-id="cbe7a-180">Microsoft. Azure. Commands. SecurityInsights. models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="cbe7a-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="cbe7a-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cbe7a-181">NOTES</span></span>

## <span data-ttu-id="cbe7a-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cbe7a-182">RELATED LINKS</span></span>
