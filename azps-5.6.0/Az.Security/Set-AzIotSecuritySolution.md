---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 965aaeaba9d77b28389c4493e4a891b9e01aa2df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010266"
---
# <span data-ttu-id="a9b2e-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="a9b2e-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="a9b2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9b2e-102">SYNOPSIS</span></span>
<span data-ttu-id="a9b2e-103">Tworzenie lub aktualizowanie rozwiązania zabezpieczeń IoT</span><span class="sxs-lookup"><span data-stu-id="a9b2e-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="a9b2e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a9b2e-104">SYNTAX</span></span>

### <span data-ttu-id="a9b2e-105">ResourceGroupLevelResource (Default)</span><span class="sxs-lookup"><span data-stu-id="a9b2e-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9b2e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a9b2e-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9b2e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9b2e-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9b2e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a9b2e-108">DESCRIPTION</span></span>
<span data-ttu-id="a9b2e-109">Polecenie Set-AzIotSecuritySolution cmdlet tworzy lub aktualizuje określone rozwiązanie zabezpieczeń iot.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="a9b2e-110">Rozwiązanie zabezpieczeń IoT zbiera dane zabezpieczeń i zdarzenia z urządzeń iot i centrum iot, aby chronić zagrożenia i je wykrywać.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="a9b2e-111">Nazwa rozwiązania zabezpieczającego powinna być identyczna z nazwą centrum iot.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="a9b2e-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a9b2e-112">EXAMPLES</span></span>

### <span data-ttu-id="a9b2e-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9b2e-113">Example 1</span></span>
```powershell
PS C:\> $Workspace = "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.OperationalInsights/workspaces/IoTHubWorkspace"
PS C:\> $IotHubs = @("/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample")
PS C:\> Set-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -Location "West US" 
-Workspace $Workspace -DisplayName "MySample" -Enabled $true -IotHub $IotHubs

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
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="a9b2e-114">Utwórz nowe rozwiązanie zabezpieczeń "MySample" dla centrum IoT z identyfikatorem zasobu "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (nazwa rozwiązania powinna być identyczna z nazwą centrum IoT)</span><span class="sxs-lookup"><span data-stu-id="a9b2e-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="a9b2e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9b2e-115">PARAMETERS</span></span>

### <span data-ttu-id="a9b2e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b2e-116">-DefaultProfile</span></span>
<span data-ttu-id="a9b2e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9b2e-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="a9b2e-118">-DisabledDataSource</span></span>
<span data-ttu-id="a9b2e-119">Wyłączone źródła danych.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-119">Disabled data sources.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b2e-120">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="a9b2e-120">-DisplayName</span></span>
<span data-ttu-id="a9b2e-121">Nazwa wyświetlana.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-121">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b2e-122">— włączone</span><span class="sxs-lookup"><span data-stu-id="a9b2e-122">-Enabled</span></span>
<span data-ttu-id="a9b2e-123">Stan.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-123">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b2e-124">— Eksportowanie</span><span class="sxs-lookup"><span data-stu-id="a9b2e-124">-Export</span></span>
<span data-ttu-id="a9b2e-125">Eksportowanie danych.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-125">Export data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b2e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9b2e-126">-InputObject</span></span>
<span data-ttu-id="a9b2e-127">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-127">Input Object.</span></span>

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

### <span data-ttu-id="a9b2e-128">- IotHub</span><span class="sxs-lookup"><span data-stu-id="a9b2e-128">-IotHub</span></span>
<span data-ttu-id="a9b2e-129">Koncentratory Iot.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-129">Iot hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b2e-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a9b2e-130">-Location</span></span>
<span data-ttu-id="a9b2e-131">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-131">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b2e-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a9b2e-132">-Name</span></span>
<span data-ttu-id="a9b2e-133">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-133">Resource name.</span></span>

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

### <span data-ttu-id="a9b2e-134">— RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9b2e-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="a9b2e-135">Konfiguracja zalecenia.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-135">Recommendations configuration.</span></span>

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

### <span data-ttu-id="a9b2e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9b2e-136">-ResourceGroupName</span></span>
<span data-ttu-id="a9b2e-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-137">Resource group name.</span></span>

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

### <span data-ttu-id="a9b2e-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9b2e-138">-ResourceId</span></span>
<span data-ttu-id="a9b2e-139">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a9b2e-140">— Tag</span><span class="sxs-lookup"><span data-stu-id="a9b2e-140">-Tag</span></span>
<span data-ttu-id="a9b2e-141">Tagi.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-141">Tags.</span></span>

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

### <span data-ttu-id="a9b2e-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="a9b2e-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="a9b2e-143">Unmasked ip logging status.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-143">Unmasked ip logging status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b2e-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="a9b2e-144">-UserDefinedResource</span></span>
<span data-ttu-id="a9b2e-145">Zasoby zdefiniowane przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-145">User defined resources.</span></span>

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

### <span data-ttu-id="a9b2e-146">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="a9b2e-146">-Workspace</span></span>
<span data-ttu-id="a9b2e-147">Identyfikator obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-147">Workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b2e-148">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9b2e-148">-Confirm</span></span>
<span data-ttu-id="a9b2e-149">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9b2e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9b2e-150">-WhatIf</span></span>
<span data-ttu-id="a9b2e-151">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9b2e-152">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9b2e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b2e-153">CommonParameters</span></span>
<span data-ttu-id="a9b2e-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9b2e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b2e-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9b2e-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b2e-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9b2e-156">INPUTS</span></span>

### <span data-ttu-id="a9b2e-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="a9b2e-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="a9b2e-158">System.String</span><span class="sxs-lookup"><span data-stu-id="a9b2e-158">System.String</span></span>

### <span data-ttu-id="a9b2e-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a9b2e-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a9b2e-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a9b2e-160">System.String[]</span></span>

### <span data-ttu-id="a9b2e-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="a9b2e-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="a9b2e-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="a9b2e-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="a9b2e-163">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9b2e-163">OUTPUTS</span></span>

### <span data-ttu-id="a9b2e-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="a9b2e-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="a9b2e-165">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a9b2e-165">NOTES</span></span>

## <span data-ttu-id="a9b2e-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9b2e-166">RELATED LINKS</span></span>
