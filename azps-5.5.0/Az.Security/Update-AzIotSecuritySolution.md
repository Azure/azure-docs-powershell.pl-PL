---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Update-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
ms.openlocfilehash: ba84bccc92b58b7f8a21812e2f1599bbc9679d38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201771"
---
# <span data-ttu-id="9cb60-101">Update-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="9cb60-101">Update-AzIotSecuritySolution</span></span>

## <span data-ttu-id="9cb60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cb60-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb60-103">Aktualizowanie co najmniej jednej z następujących właściwości w rozwiązaniu zabezpieczeń IoT: tagi, konfiguracja zalecenia, zasoby zdefiniowane przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="9cb60-103">Update one or more of the following properties in IoT security solution: tags, recommendation configuration, user defined resources</span></span>

## <span data-ttu-id="9cb60-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9cb60-104">SYNTAX</span></span>

### <span data-ttu-id="9cb60-105">ResourceGroupLevelResource (Default)</span><span class="sxs-lookup"><span data-stu-id="9cb60-105">ResourceGroupLevelResource (Default)</span></span>
```
Update-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cb60-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cb60-106">ResourceId</span></span>
```
Update-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cb60-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9cb60-107">InputObject</span></span>
```
Update-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cb60-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9cb60-108">DESCRIPTION</span></span>
<span data-ttu-id="9cb60-109">Polecenie Update-AzIotSecuritySolution updayes co najmniej jedną z następujących właściwości w konkretnym rozwiązaniu zabezpieczeń IoT: tagi, konfiguracja zalecenia, zasoby zdefiniowane przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9cb60-109">The Update-AzIotSecuritySolution cmdlet updayes one or more of the following properties in a specific IoT security solution: tags, recommendation configuration, user defined resources.</span></span>
<span data-ttu-id="9cb60-110">W rozwiązaniu zabezpieczeń systemu iot zostaną zaktualizowane tylko określone właściwości.</span><span class="sxs-lookup"><span data-stu-id="9cb60-110">Only the specified properties will be updated inside the iot security solution.</span></span>
<span data-ttu-id="9cb60-111">Rozwiązanie zabezpieczeń IoT zbiera dane zabezpieczeń i zdarzenia z urządzeń iot i centrum iot, aby chronić zagrożenia i je wykrywać.</span><span class="sxs-lookup"><span data-stu-id="9cb60-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="9cb60-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9cb60-112">EXAMPLES</span></span>

### <span data-ttu-id="9cb60-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9cb60-113">Example 1</span></span>
```powershell
PS C:\> $RecConfig = New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_OpenPorts" -Enabled $false
PS C:\> $UserDefinedResource = New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")   
PS C:\> Update-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -RecommendationsConfiguration @($RecConfig) -UserDefinedResource $UserDefinedResource

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "westus"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
    QuerySubscriptions: ["XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"]
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_OpenPorts"
    Name: "Device has open port"
    Status: "Disabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
}]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
```

<span data-ttu-id="9cb60-114">Aktualizowanie rozwiązania zabezpieczeń "MySample" z grupy zasobów "MyResourceGroup" przy użyciu konfiguracji zalecenia i zasobów zdefiniowanych przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="9cb60-114">Update iot security solution "MySample" from resource group "MyResourceGroup" with recommendation configuration and user defined resources</span></span>

## <span data-ttu-id="9cb60-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cb60-115">PARAMETERS</span></span>

### <span data-ttu-id="9cb60-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb60-116">-DefaultProfile</span></span>
<span data-ttu-id="9cb60-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9cb60-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cb60-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cb60-118">-InputObject</span></span>
<span data-ttu-id="9cb60-119">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="9cb60-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb60-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9cb60-120">-Name</span></span>
<span data-ttu-id="9cb60-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="9cb60-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb60-122">— RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="9cb60-122">-RecommendationsConfiguration</span></span>
<span data-ttu-id="9cb60-123">Konfiguracja zalecenia.</span><span class="sxs-lookup"><span data-stu-id="9cb60-123">Recommendations configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb60-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb60-124">-ResourceGroupName</span></span>
<span data-ttu-id="9cb60-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9cb60-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb60-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cb60-126">-ResourceId</span></span>
<span data-ttu-id="9cb60-127">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="9cb60-127">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb60-128">— Tag</span><span class="sxs-lookup"><span data-stu-id="9cb60-128">-Tag</span></span>
<span data-ttu-id="9cb60-129">Tagi.</span><span class="sxs-lookup"><span data-stu-id="9cb60-129">Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb60-130">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="9cb60-130">-UserDefinedResource</span></span>
<span data-ttu-id="9cb60-131">Zasoby zdefiniowane przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9cb60-131">User defined resources.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb60-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9cb60-132">-Confirm</span></span>
<span data-ttu-id="9cb60-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9cb60-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cb60-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cb60-134">-WhatIf</span></span>
<span data-ttu-id="9cb60-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cb60-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cb60-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9cb60-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cb60-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb60-137">CommonParameters</span></span>
<span data-ttu-id="9cb60-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cb60-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb60-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cb60-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb60-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cb60-140">INPUTS</span></span>

### <span data-ttu-id="9cb60-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9cb60-141">System.String</span></span>

### <span data-ttu-id="9cb60-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="9cb60-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="9cb60-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9cb60-143">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9cb60-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="9cb60-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="9cb60-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="9cb60-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="9cb60-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9cb60-146">OUTPUTS</span></span>

### <span data-ttu-id="9cb60-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="9cb60-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="9cb60-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9cb60-148">NOTES</span></span>

## <span data-ttu-id="9cb60-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cb60-149">RELATED LINKS</span></span>
