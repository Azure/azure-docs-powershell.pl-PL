---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
ms.openlocfilehash: 315a44b986317157a0ada22955c04ea01726327a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502971"
---
# <span data-ttu-id="35147-101">New-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="35147-101">New-AzSentinelDataConnector</span></span>

## <span data-ttu-id="35147-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35147-102">SYNOPSIS</span></span>
<span data-ttu-id="35147-103">Tworzenie łącznika danych.</span><span class="sxs-lookup"><span data-stu-id="35147-103">Create a Data Connector.</span></span>

## <span data-ttu-id="35147-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35147-104">SYNTAX</span></span>

### <span data-ttu-id="35147-105">AzureActiveDirectory (domyślny)</span><span class="sxs-lookup"><span data-stu-id="35147-105">AzureActiveDirectory (Default)</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureActiveDirectory] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35147-106">AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="35147-106">AzureAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35147-107">AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="35147-107">AzureSecurityCenter</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureSecurityCenter] -Alerts <String> -SubscriptionId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35147-108">AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="35147-108">AmazonWebServicesCloudTrail</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AmazonWebServicesCloudTrail] -AwsRoleArn <String> -Logs <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35147-109">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="35147-109">MicrosoftCloudAppSecurity</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftCloudAppSecurity] -Alerts <String> -DiscoveryLogs <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35147-110">MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="35147-110">MicrosoftDefenderAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftDefenderAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35147-111">365</span><span class="sxs-lookup"><span data-stu-id="35147-111">Office365</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-Office365] -Exchange <String> -SharePoint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35147-112">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="35147-112">ThreatIntelligence</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-ThreatIntelligence] -Indicators <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35147-113">Opis</span><span class="sxs-lookup"><span data-stu-id="35147-113">DESCRIPTION</span></span>
<span data-ttu-id="35147-114">Polecenie cmdlet **New-AzSentinelAlertRule** umożliwia utworzenie raportu analitycznego (reguły alertu) w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="35147-114">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="35147-115">Musisz określić co najmniej jedno z parametrów, na przykład-AzureActiveDirectory, aby określić rodzaj reguły alertu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="35147-115">You must specify one of the parameters, for example -AzureActiveDirectory, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="35147-116">Każdy rodzaj ma inne wymagane paramaters.</span><span class="sxs-lookup"><span data-stu-id="35147-116">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="35147-117">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="35147-117">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="35147-118">Uwaga: nie wszystkie łączniki danych dostępne w portalu są avaialble za pośrednictwem interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="35147-118">Note:  Not all data connectors available in the portal are avaialble via API.</span></span>

## <span data-ttu-id="35147-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35147-119">EXAMPLES</span></span>

### <span data-ttu-id="35147-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="35147-120">Example 1</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AzureSecurityCenter -Alerts Enabled -SubscriptionId ((Get-AzContext).Subscription.Id)
```

<span data-ttu-id="35147-121">W tym przykładzie przedstawiono tworzenie **połączenia dataconnect** dla usługi Azure Security Center w określonym obszarze roboczym, a następnie zapisanie go w zmiennej $DataConnector.</span><span class="sxs-lookup"><span data-stu-id="35147-121">This example creates a **DataConnector** for Azure Security Center in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

### <span data-ttu-id="35147-122">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="35147-122">Example 2</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftCloudAppSecurity -Alerts Enabled -DiscoveryLogs Disabled
```

<span data-ttu-id="35147-123">W tym przykładzie jest tworzone **połączenie dataconnect** dla aplikacji Microsoft Cloud App Security w określonym obszarze roboczym, a następnie przechowywane w zmiennej $DataConnector.</span><span class="sxs-lookup"><span data-stu-id="35147-123">This example creates a **DataConnector** for Microsoft Cloud App Security in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="35147-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35147-124">PARAMETERS</span></span>

### <span data-ttu-id="35147-125">-Alerty</span><span class="sxs-lookup"><span data-stu-id="35147-125">-Alerts</span></span>
<span data-ttu-id="35147-126">Alerty łącznika danych</span><span class="sxs-lookup"><span data-stu-id="35147-126">Data Connector Alerts</span></span>

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

### <span data-ttu-id="35147-127">-AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="35147-127">-AmazonWebServicesCloudTrail</span></span>
<span data-ttu-id="35147-128">Usługa sieci Web firmy Amazon Connector danych w chmurze</span><span class="sxs-lookup"><span data-stu-id="35147-128">Data Connector Amazon Web Services Cloud Trail</span></span>

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

### <span data-ttu-id="35147-129">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="35147-129">-AwsRoleArn</span></span>
<span data-ttu-id="35147-130">Łącznik danych AWS rola ARN</span><span class="sxs-lookup"><span data-stu-id="35147-130">Data Connector AWS Role Arn</span></span>

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

### <span data-ttu-id="35147-131">-AzureActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="35147-131">-AzureActiveDirectory</span></span>
<span data-ttu-id="35147-132">Usługa Azure Active Directory łącznika danych</span><span class="sxs-lookup"><span data-stu-id="35147-132">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="35147-133">-AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="35147-133">-AzureAdvancedThreatProtection</span></span>
<span data-ttu-id="35147-134">Zaawansowana ochrona przed zagrożeniami w usłudze Azure Łącznik danych</span><span class="sxs-lookup"><span data-stu-id="35147-134">Data Connector Azure Advanced Threat Protection</span></span>

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

### <span data-ttu-id="35147-135">-AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="35147-135">-AzureSecurityCenter</span></span>
<span data-ttu-id="35147-136">Centrum zabezpieczeń platformy Azure Łącznik danych</span><span class="sxs-lookup"><span data-stu-id="35147-136">Data Connector Azure Security Center</span></span>

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

### <span data-ttu-id="35147-137">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="35147-137">-DataConnectorId</span></span>
<span data-ttu-id="35147-138">Usługa Azure Active Directory łącznika danych</span><span class="sxs-lookup"><span data-stu-id="35147-138">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="35147-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35147-139">-DefaultProfile</span></span>
<span data-ttu-id="35147-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="35147-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35147-141">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="35147-141">-DiscoveryLogs</span></span>
<span data-ttu-id="35147-142">Dzienniki odnajdowania łączników danych</span><span class="sxs-lookup"><span data-stu-id="35147-142">Data Connector Discovery Logs</span></span>

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

### <span data-ttu-id="35147-143">-Exchange</span><span class="sxs-lookup"><span data-stu-id="35147-143">-Exchange</span></span>
<span data-ttu-id="35147-144">Wymiana łącznika danych</span><span class="sxs-lookup"><span data-stu-id="35147-144">Data Connector Exchange</span></span>

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

### <span data-ttu-id="35147-145">-Wskaźniki</span><span class="sxs-lookup"><span data-stu-id="35147-145">-Indicators</span></span>
<span data-ttu-id="35147-146">Wskaźniki łącznika danych</span><span class="sxs-lookup"><span data-stu-id="35147-146">Data Connector Indicators</span></span>

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

### <span data-ttu-id="35147-147">— Dzienniki</span><span class="sxs-lookup"><span data-stu-id="35147-147">-Logs</span></span>
<span data-ttu-id="35147-148">Dzienniki łącznika danych</span><span class="sxs-lookup"><span data-stu-id="35147-148">Data Connector Logs</span></span>

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

### <span data-ttu-id="35147-149">-MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="35147-149">-MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="35147-150">Łącznik danych Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="35147-150">Data Connector Microsoft Cloud App Security</span></span>

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

### <span data-ttu-id="35147-151">-MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="35147-151">-MicrosoftDefenderAdvancedThreatProtection</span></span>
<span data-ttu-id="35147-152">Łącznik danych zaawansowanej ochrony przed zagrożeniami dla programu Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="35147-152">Data Connector Microsoft Defender Advanced Threat Protection</span></span>

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

### <span data-ttu-id="35147-153">-Office 365</span><span class="sxs-lookup"><span data-stu-id="35147-153">-Office365</span></span>
<span data-ttu-id="35147-154">Łącznik danych pakietu Office 365</span><span class="sxs-lookup"><span data-stu-id="35147-154">Data Connector Office 365</span></span>

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

### <span data-ttu-id="35147-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35147-155">-ResourceGroupName</span></span>
<span data-ttu-id="35147-156">Usługa Azure Active Directory łącznika danych</span><span class="sxs-lookup"><span data-stu-id="35147-156">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="35147-157">-Program SharePoint</span><span class="sxs-lookup"><span data-stu-id="35147-157">-SharePoint</span></span>
<span data-ttu-id="35147-158">Łącznik danych programu SharePoint</span><span class="sxs-lookup"><span data-stu-id="35147-158">Data Connector SharePoint</span></span>

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

### <span data-ttu-id="35147-159">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="35147-159">-SubscriptionId</span></span>
<span data-ttu-id="35147-160">Identyfikator subskrypcji łącznika danych</span><span class="sxs-lookup"><span data-stu-id="35147-160">Data connector Subscription Id</span></span>

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

### <span data-ttu-id="35147-161">-ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="35147-161">-ThreatIntelligence</span></span>
<span data-ttu-id="35147-162">Analiza zagrożeń łącznika danych</span><span class="sxs-lookup"><span data-stu-id="35147-162">Data Connector Threat Intelligence</span></span>

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

### <span data-ttu-id="35147-163">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="35147-163">-WorkspaceName</span></span>
<span data-ttu-id="35147-164">Usługa Azure Active Directory łącznika danych</span><span class="sxs-lookup"><span data-stu-id="35147-164">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="35147-165">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35147-165">-Confirm</span></span>
<span data-ttu-id="35147-166">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35147-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35147-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35147-167">-WhatIf</span></span>
<span data-ttu-id="35147-168">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35147-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35147-169">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="35147-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35147-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35147-170">CommonParameters</span></span>
<span data-ttu-id="35147-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35147-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35147-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35147-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35147-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35147-173">INPUTS</span></span>

### <span data-ttu-id="35147-174">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="35147-174">None</span></span>
## <span data-ttu-id="35147-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35147-175">OUTPUTS</span></span>

### <span data-ttu-id="35147-176">Microsoft. Azure. Commands. SecurityInsights. models. dataconnects. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="35147-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="35147-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35147-177">NOTES</span></span>

## <span data-ttu-id="35147-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35147-178">RELATED LINKS</span></span>
