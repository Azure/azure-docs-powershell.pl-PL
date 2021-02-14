---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
ms.openlocfilehash: 315a44b986317157a0ada22955c04ea01726327a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201731"
---
# <span data-ttu-id="8a2ac-101">New-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="8a2ac-101">New-AzSentinelDataConnector</span></span>

## <span data-ttu-id="8a2ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="8a2ac-103">Tworzenie łącznika danych.</span><span class="sxs-lookup"><span data-stu-id="8a2ac-103">Create a Data Connector.</span></span>

## <span data-ttu-id="8a2ac-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8a2ac-104">SYNTAX</span></span>

### <span data-ttu-id="8a2ac-105">AzureActiveDirectory (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8a2ac-105">AzureActiveDirectory (Default)</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureActiveDirectory] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a2ac-106">AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="8a2ac-106">AzureAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a2ac-107">AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="8a2ac-107">AzureSecurityCenter</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureSecurityCenter] -Alerts <String> -SubscriptionId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a2ac-108">AmazonWebServicesCloudTservices</span><span class="sxs-lookup"><span data-stu-id="8a2ac-108">AmazonWebServicesCloudTrail</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AmazonWebServicesCloudTrail] -AwsRoleArn <String> -Logs <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a2ac-109">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="8a2ac-109">MicrosoftCloudAppSecurity</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftCloudAppSecurity] -Alerts <String> -DiscoveryLogs <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a2ac-110">MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="8a2ac-110">MicrosoftDefenderAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftDefenderAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a2ac-111">Office 365</span><span class="sxs-lookup"><span data-stu-id="8a2ac-111">Office365</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-Office365] -Exchange <String> -SharePoint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a2ac-112">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="8a2ac-112">ThreatIntelligence</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-ThreatIntelligence] -Indicators <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a2ac-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="8a2ac-113">DESCRIPTION</span></span>
<span data-ttu-id="8a2ac-114">Polecenie **cmdlet New-AzSentinelAlertRule** tworzy regułę analityczna (reguła alertu) w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="8a2ac-114">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="8a2ac-115">Aby określić rodzaj reguły alertu do utworzenia, należy określić jeden z parametrów, na przykład —AzureActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="8a2ac-115">You must specify one of the parameters, for example -AzureActiveDirectory, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="8a2ac-116">Każdy rodzaj ma inne wymagane paramaty.</span><span class="sxs-lookup"><span data-stu-id="8a2ac-116">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="8a2ac-117">Za pomocą *parametru Confirm* i $ConfirmPreference programu Windows PowerShell możesz kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8a2ac-117">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="8a2ac-118">Uwaga: nie wszystkie łączniki danych dostępne w portalu są dostępne za pośrednictwem interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8a2ac-118">Note:  Not all data connectors available in the portal are avaialble via API.</span></span>

## <span data-ttu-id="8a2ac-119">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8a2ac-119">EXAMPLES</span></span>

### <span data-ttu-id="8a2ac-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8a2ac-120">Example 1</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AzureSecurityCenter -Alerts Enabled -SubscriptionId ((Get-AzContext).Subscription.Id)
```

<span data-ttu-id="8a2ac-121">W tym przykładzie **program DataConnector** dla usługi Azure Security Center tworzy go w określonym obszarze roboczym, a następnie zapisuje go w $DataConnector danych.</span><span class="sxs-lookup"><span data-stu-id="8a2ac-121">This example creates a **DataConnector** for Azure Security Center in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

### <span data-ttu-id="8a2ac-122">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8a2ac-122">Example 2</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftCloudAppSecurity -Alerts Enabled -DiscoveryLogs Disabled
```

<span data-ttu-id="8a2ac-123">W tym przykładzie **program DataConnector** dla zabezpieczeń aplikacji w chmurze firmy Microsoft tworzy go w określonym obszarze roboczym, a następnie zapisuje go w $DataConnector danych.</span><span class="sxs-lookup"><span data-stu-id="8a2ac-123">This example creates a **DataConnector** for Microsoft Cloud App Security in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="8a2ac-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a2ac-124">PARAMETERS</span></span>

### <span data-ttu-id="8a2ac-125">— Alerty</span><span class="sxs-lookup"><span data-stu-id="8a2ac-125">-Alerts</span></span>
<span data-ttu-id="8a2ac-126">Alerty łącznika danych</span><span class="sxs-lookup"><span data-stu-id="8a2ac-126">Data Connector Alerts</span></span>

```yaml
Type: System.String
Parameter Sets: AzureActiveDirectory, AzureAdvancedThreatProtection, AzureSecurityCenter, MicrosoftCloudAppSecurity, MicrosoftDefenderAdvancedThreatProtection
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2ac-127">-AmazonWebServicesCloudTservices</span><span class="sxs-lookup"><span data-stu-id="8a2ac-127">-AmazonWebServicesCloudTrail</span></span>
<span data-ttu-id="8a2ac-128">Data Connector Amazon Web Services Cloud Trail</span><span class="sxs-lookup"><span data-stu-id="8a2ac-128">Data Connector Amazon Web Services Cloud Trail</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2ac-129">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="8a2ac-129">-AwsRoleArn</span></span>
<span data-ttu-id="8a2ac-130">Rola AWS łącznika danych</span><span class="sxs-lookup"><span data-stu-id="8a2ac-130">Data Connector AWS Role Arn</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2ac-131">—AzureActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="8a2ac-131">-AzureActiveDirectory</span></span>
<span data-ttu-id="8a2ac-132">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8a2ac-132">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureActiveDirectory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2ac-133">-AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="8a2ac-133">-AzureAdvancedThreatProtection</span></span>
<span data-ttu-id="8a2ac-134">Zaawansowana ochrona przed zagrożeniami w dosłudze Data Connector platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8a2ac-134">Data Connector Azure Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2ac-135">— AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="8a2ac-135">-AzureSecurityCenter</span></span>
<span data-ttu-id="8a2ac-136">Data Connector Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="8a2ac-136">Data Connector Azure Security Center</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2ac-137">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="8a2ac-137">-DataConnectorId</span></span>
<span data-ttu-id="8a2ac-138">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8a2ac-138">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="8a2ac-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a2ac-139">-DefaultProfile</span></span>
<span data-ttu-id="8a2ac-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a2ac-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a2ac-141">- DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="8a2ac-141">-DiscoveryLogs</span></span>
<span data-ttu-id="8a2ac-142">Dzienniki odnajdowania łącznika danych</span><span class="sxs-lookup"><span data-stu-id="8a2ac-142">Data Connector Discovery Logs</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2ac-143">— Exchange</span><span class="sxs-lookup"><span data-stu-id="8a2ac-143">-Exchange</span></span>
<span data-ttu-id="8a2ac-144">Wymiana łączników danych</span><span class="sxs-lookup"><span data-stu-id="8a2ac-144">Data Connector Exchange</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2ac-145">— Wskaźniki</span><span class="sxs-lookup"><span data-stu-id="8a2ac-145">-Indicators</span></span>
<span data-ttu-id="8a2ac-146">Wskaźniki łącznika danych</span><span class="sxs-lookup"><span data-stu-id="8a2ac-146">Data Connector Indicators</span></span>

```yaml
Type: System.String
Parameter Sets: ThreatIntelligence
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2ac-147">— Dzienniki</span><span class="sxs-lookup"><span data-stu-id="8a2ac-147">-Logs</span></span>
<span data-ttu-id="8a2ac-148">Dzienniki łączników danych</span><span class="sxs-lookup"><span data-stu-id="8a2ac-148">Data Connector Logs</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2ac-149">-MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="8a2ac-149">-MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="8a2ac-150">Data Connector Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="8a2ac-150">Data Connector Microsoft Cloud App Security</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2ac-151">-MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="8a2ac-151">-MicrosoftDefenderAdvancedThreatProtection</span></span>
<span data-ttu-id="8a2ac-152">Data Connector Microsoft Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="8a2ac-152">Data Connector Microsoft Defender Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftDefenderAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2ac-153">— Office365</span><span class="sxs-lookup"><span data-stu-id="8a2ac-153">-Office365</span></span>
<span data-ttu-id="8a2ac-154">Łącznik danych w usłudze Office 365</span><span class="sxs-lookup"><span data-stu-id="8a2ac-154">Data Connector Office 365</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Office365
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2ac-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a2ac-155">-ResourceGroupName</span></span>
<span data-ttu-id="8a2ac-156">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8a2ac-156">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="8a2ac-157">— SharePoint</span><span class="sxs-lookup"><span data-stu-id="8a2ac-157">-SharePoint</span></span>
<span data-ttu-id="8a2ac-158">Łącznik danych w programie SharePoint</span><span class="sxs-lookup"><span data-stu-id="8a2ac-158">Data Connector SharePoint</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2ac-159">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a2ac-159">-SubscriptionId</span></span>
<span data-ttu-id="8a2ac-160">Identyfikator subskrypcji łącznika danych</span><span class="sxs-lookup"><span data-stu-id="8a2ac-160">Data connector Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2ac-161">-ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="8a2ac-161">-ThreatIntelligence</span></span>
<span data-ttu-id="8a2ac-162">Data Connector Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="8a2ac-162">Data Connector Threat Intelligence</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ThreatIntelligence
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a2ac-163">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8a2ac-163">-WorkspaceName</span></span>
<span data-ttu-id="8a2ac-164">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8a2ac-164">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="8a2ac-165">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8a2ac-165">-Confirm</span></span>
<span data-ttu-id="8a2ac-166">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8a2ac-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a2ac-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a2ac-167">-WhatIf</span></span>
<span data-ttu-id="8a2ac-168">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a2ac-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a2ac-169">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8a2ac-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a2ac-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a2ac-170">CommonParameters</span></span>
<span data-ttu-id="8a2ac-171">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a2ac-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a2ac-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a2ac-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a2ac-173">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a2ac-173">INPUTS</span></span>

### <span data-ttu-id="8a2ac-174">Brak</span><span class="sxs-lookup"><span data-stu-id="8a2ac-174">None</span></span>
## <span data-ttu-id="8a2ac-175">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a2ac-175">OUTPUTS</span></span>

### <span data-ttu-id="8a2ac-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="8a2ac-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="8a2ac-177">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8a2ac-177">NOTES</span></span>

## <span data-ttu-id="8a2ac-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a2ac-178">RELATED LINKS</span></span>
