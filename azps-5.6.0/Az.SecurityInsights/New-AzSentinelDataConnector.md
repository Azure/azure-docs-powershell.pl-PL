---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
ms.openlocfilehash: 7eb4675e44a252feec913b531a30f9062f6b791b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976346"
---
# <span data-ttu-id="45b2c-101">New-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="45b2c-101">New-AzSentinelDataConnector</span></span>

## <span data-ttu-id="45b2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="45b2c-103">Tworzenie łącznika danych.</span><span class="sxs-lookup"><span data-stu-id="45b2c-103">Create a Data Connector.</span></span>

## <span data-ttu-id="45b2c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="45b2c-104">SYNTAX</span></span>

### <span data-ttu-id="45b2c-105">AzureActiveDirectory (domyślne)</span><span class="sxs-lookup"><span data-stu-id="45b2c-105">AzureActiveDirectory (Default)</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureActiveDirectory] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45b2c-106">AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="45b2c-106">AzureAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b2c-107">AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="45b2c-107">AzureSecurityCenter</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureSecurityCenter] -Alerts <String> -SubscriptionId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b2c-108">AmazonWebServicesCloudTservices</span><span class="sxs-lookup"><span data-stu-id="45b2c-108">AmazonWebServicesCloudTrail</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AmazonWebServicesCloudTrail] -AwsRoleArn <String> -Logs <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b2c-109">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="45b2c-109">MicrosoftCloudAppSecurity</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftCloudAppSecurity] -Alerts <String> -DiscoveryLogs <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b2c-110">MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="45b2c-110">MicrosoftDefenderAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftDefenderAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b2c-111">Office 365</span><span class="sxs-lookup"><span data-stu-id="45b2c-111">Office365</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-Office365] -Exchange <String> -SharePoint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b2c-112">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="45b2c-112">ThreatIntelligence</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-ThreatIntelligence] -Indicators <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45b2c-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="45b2c-113">DESCRIPTION</span></span>
<span data-ttu-id="45b2c-114">Polecenie **cmdlet New-AzSentinelAlertRule** tworzy regułę analityczna (reguła alertu) w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="45b2c-114">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="45b2c-115">Aby określić rodzaj reguły alertu do utworzenia, należy określić jeden z parametrów, na przykład —AzureActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="45b2c-115">You must specify one of the parameters, for example -AzureActiveDirectory, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="45b2c-116">Każdy rodzaj ma inne wymagane paramaty.</span><span class="sxs-lookup"><span data-stu-id="45b2c-116">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="45b2c-117">Możesz użyć *parametru Confirm* i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="45b2c-117">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="45b2c-118">Uwaga: Nie wszystkie łączniki danych dostępne w portalu są dostępne za pośrednictwem interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="45b2c-118">Note:  Not all data connectors available in the portal are avaialble via API.</span></span>

## <span data-ttu-id="45b2c-119">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="45b2c-119">EXAMPLES</span></span>

### <span data-ttu-id="45b2c-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="45b2c-120">Example 1</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AzureSecurityCenter -Alerts Enabled -SubscriptionId ((Get-AzContext).Subscription.Id)
```

<span data-ttu-id="45b2c-121">W tym przykładzie **program DataConnector** dla usługi Azure Security Center tworzy go w określonym obszarze roboczym, a następnie zapisuje go w $DataConnector danych.</span><span class="sxs-lookup"><span data-stu-id="45b2c-121">This example creates a **DataConnector** for Azure Security Center in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

### <span data-ttu-id="45b2c-122">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="45b2c-122">Example 2</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftCloudAppSecurity -Alerts Enabled -DiscoveryLogs Disabled
```

<span data-ttu-id="45b2c-123">W tym przykładzie **program DataConnector** dla zabezpieczeń aplikacji w chmurze firmy Microsoft tworzy go w określonym obszarze roboczym, a następnie zapisuje go w $DataConnector danych.</span><span class="sxs-lookup"><span data-stu-id="45b2c-123">This example creates a **DataConnector** for Microsoft Cloud App Security in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="45b2c-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45b2c-124">PARAMETERS</span></span>

### <span data-ttu-id="45b2c-125">— Alerty</span><span class="sxs-lookup"><span data-stu-id="45b2c-125">-Alerts</span></span>
<span data-ttu-id="45b2c-126">Alerty łącznika danych</span><span class="sxs-lookup"><span data-stu-id="45b2c-126">Data Connector Alerts</span></span>

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

### <span data-ttu-id="45b2c-127">-AmazonWebServicesCloudTservices</span><span class="sxs-lookup"><span data-stu-id="45b2c-127">-AmazonWebServicesCloudTrail</span></span>
<span data-ttu-id="45b2c-128">Data Connector Amazon Web Services Cloud Trail</span><span class="sxs-lookup"><span data-stu-id="45b2c-128">Data Connector Amazon Web Services Cloud Trail</span></span>

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

### <span data-ttu-id="45b2c-129">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="45b2c-129">-AwsRoleArn</span></span>
<span data-ttu-id="45b2c-130">Rola AWS łącznika danych</span><span class="sxs-lookup"><span data-stu-id="45b2c-130">Data Connector AWS Role Arn</span></span>

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

### <span data-ttu-id="45b2c-131">—AzureActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="45b2c-131">-AzureActiveDirectory</span></span>
<span data-ttu-id="45b2c-132">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="45b2c-132">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="45b2c-133">-AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="45b2c-133">-AzureAdvancedThreatProtection</span></span>
<span data-ttu-id="45b2c-134">Zaawansowana ochrona przed zagrożeniami w dosłudze Data Connector platformy Azure</span><span class="sxs-lookup"><span data-stu-id="45b2c-134">Data Connector Azure Advanced Threat Protection</span></span>

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

### <span data-ttu-id="45b2c-135">— AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="45b2c-135">-AzureSecurityCenter</span></span>
<span data-ttu-id="45b2c-136">Data Connector Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="45b2c-136">Data Connector Azure Security Center</span></span>

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

### <span data-ttu-id="45b2c-137">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="45b2c-137">-DataConnectorId</span></span>
<span data-ttu-id="45b2c-138">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="45b2c-138">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="45b2c-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b2c-139">-DefaultProfile</span></span>
<span data-ttu-id="45b2c-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="45b2c-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45b2c-141">- DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="45b2c-141">-DiscoveryLogs</span></span>
<span data-ttu-id="45b2c-142">Dzienniki odnajdowania łącznika danych</span><span class="sxs-lookup"><span data-stu-id="45b2c-142">Data Connector Discovery Logs</span></span>

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

### <span data-ttu-id="45b2c-143">— Exchange</span><span class="sxs-lookup"><span data-stu-id="45b2c-143">-Exchange</span></span>
<span data-ttu-id="45b2c-144">Wymiana łączników danych</span><span class="sxs-lookup"><span data-stu-id="45b2c-144">Data Connector Exchange</span></span>

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

### <span data-ttu-id="45b2c-145">— Wskaźniki</span><span class="sxs-lookup"><span data-stu-id="45b2c-145">-Indicators</span></span>
<span data-ttu-id="45b2c-146">Wskaźniki łącznika danych</span><span class="sxs-lookup"><span data-stu-id="45b2c-146">Data Connector Indicators</span></span>

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

### <span data-ttu-id="45b2c-147">— Dzienniki</span><span class="sxs-lookup"><span data-stu-id="45b2c-147">-Logs</span></span>
<span data-ttu-id="45b2c-148">Dzienniki łączników danych</span><span class="sxs-lookup"><span data-stu-id="45b2c-148">Data Connector Logs</span></span>

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

### <span data-ttu-id="45b2c-149">-MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="45b2c-149">-MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="45b2c-150">Data Connector Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="45b2c-150">Data Connector Microsoft Cloud App Security</span></span>

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

### <span data-ttu-id="45b2c-151">-MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="45b2c-151">-MicrosoftDefenderAdvancedThreatProtection</span></span>
<span data-ttu-id="45b2c-152">Data Connector Microsoft Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="45b2c-152">Data Connector Microsoft Defender Advanced Threat Protection</span></span>

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

### <span data-ttu-id="45b2c-153">— Office365</span><span class="sxs-lookup"><span data-stu-id="45b2c-153">-Office365</span></span>
<span data-ttu-id="45b2c-154">Łącznik danych w usłudze Office 365</span><span class="sxs-lookup"><span data-stu-id="45b2c-154">Data Connector Office 365</span></span>

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

### <span data-ttu-id="45b2c-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45b2c-155">-ResourceGroupName</span></span>
<span data-ttu-id="45b2c-156">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="45b2c-156">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="45b2c-157">— SharePoint</span><span class="sxs-lookup"><span data-stu-id="45b2c-157">-SharePoint</span></span>
<span data-ttu-id="45b2c-158">Łącznik danych w programie SharePoint</span><span class="sxs-lookup"><span data-stu-id="45b2c-158">Data Connector SharePoint</span></span>

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

### <span data-ttu-id="45b2c-159">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45b2c-159">-SubscriptionId</span></span>
<span data-ttu-id="45b2c-160">Identyfikator subskrypcji łącznika danych</span><span class="sxs-lookup"><span data-stu-id="45b2c-160">Data connector Subscription Id</span></span>

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

### <span data-ttu-id="45b2c-161">-ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="45b2c-161">-ThreatIntelligence</span></span>
<span data-ttu-id="45b2c-162">Data Connector Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="45b2c-162">Data Connector Threat Intelligence</span></span>

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

### <span data-ttu-id="45b2c-163">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="45b2c-163">-WorkspaceName</span></span>
<span data-ttu-id="45b2c-164">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="45b2c-164">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="45b2c-165">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="45b2c-165">-Confirm</span></span>
<span data-ttu-id="45b2c-166">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="45b2c-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45b2c-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45b2c-167">-WhatIf</span></span>
<span data-ttu-id="45b2c-168">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b2c-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45b2c-169">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="45b2c-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45b2c-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b2c-170">CommonParameters</span></span>
<span data-ttu-id="45b2c-171">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b2c-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b2c-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45b2c-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b2c-173">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45b2c-173">INPUTS</span></span>

### <span data-ttu-id="45b2c-174">Brak</span><span class="sxs-lookup"><span data-stu-id="45b2c-174">None</span></span>
## <span data-ttu-id="45b2c-175">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45b2c-175">OUTPUTS</span></span>

### <span data-ttu-id="45b2c-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="45b2c-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="45b2c-177">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="45b2c-177">NOTES</span></span>

## <span data-ttu-id="45b2c-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45b2c-178">RELATED LINKS</span></span>
