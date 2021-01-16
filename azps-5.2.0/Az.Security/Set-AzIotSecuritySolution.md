---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 30b6979be7f3aae23bec5d1ca45d48d4dd2290f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335506"
---
# <span data-ttu-id="493de-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="493de-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="493de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="493de-102">SYNOPSIS</span></span>
<span data-ttu-id="493de-103">Tworzenie lub aktualizowanie rozwiązania dotyczącego zabezpieczeń IoT</span><span class="sxs-lookup"><span data-stu-id="493de-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="493de-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="493de-104">SYNTAX</span></span>

### <span data-ttu-id="493de-105">ResourceGroupLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="493de-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="493de-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="493de-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="493de-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="493de-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="493de-108">Opis</span><span class="sxs-lookup"><span data-stu-id="493de-108">DESCRIPTION</span></span>
<span data-ttu-id="493de-109">Polecenie cmdlet Set-AzIotSecuritySolution służy do tworzenia lub aktualizowania określonego rozwiązania dotyczącego zabezpieczeń IoT.</span><span class="sxs-lookup"><span data-stu-id="493de-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="493de-110">Rozwiązanie zabezpieczeń IoT gromadzi dane i zdarzenia zabezpieczeń z urządzeń IoT oraz centrum IoT, aby ułatwić zapobieganie i wykrywanie zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="493de-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="493de-111">Nazwa rozwiązania zabezpieczającego IoT powinna być taka sama jak nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="493de-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="493de-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="493de-112">EXAMPLES</span></span>

### <span data-ttu-id="493de-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="493de-113">Example 1</span></span>
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

<span data-ttu-id="493de-114">Utwórz nowe rozwiązanie zabezpieczeń IoT "z przykładem" dla Centrum IoT o identyfikatorze zasobu "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (Nazwa rozwiązania powinna być taka sama jak nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="493de-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="493de-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="493de-115">PARAMETERS</span></span>

### <span data-ttu-id="493de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="493de-116">-DefaultProfile</span></span>
<span data-ttu-id="493de-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="493de-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="493de-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="493de-118">-DisabledDataSource</span></span>
<span data-ttu-id="493de-119">Wyłączone źródła danych.</span><span class="sxs-lookup"><span data-stu-id="493de-119">Disabled data sources.</span></span>

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

### <span data-ttu-id="493de-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="493de-120">-DisplayName</span></span>
<span data-ttu-id="493de-121">Nazwa wyświetlana.</span><span class="sxs-lookup"><span data-stu-id="493de-121">Display name.</span></span>

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

### <span data-ttu-id="493de-122">-Enabled</span><span class="sxs-lookup"><span data-stu-id="493de-122">-Enabled</span></span>
<span data-ttu-id="493de-123">Stan.</span><span class="sxs-lookup"><span data-stu-id="493de-123">Status .</span></span>

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

### <span data-ttu-id="493de-124">— Eksportuj</span><span class="sxs-lookup"><span data-stu-id="493de-124">-Export</span></span>
<span data-ttu-id="493de-125">Eksportowanie danych.</span><span class="sxs-lookup"><span data-stu-id="493de-125">Export data.</span></span>

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

### <span data-ttu-id="493de-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="493de-126">-InputObject</span></span>
<span data-ttu-id="493de-127">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="493de-127">Input Object.</span></span>

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

### <span data-ttu-id="493de-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="493de-128">-IotHub</span></span>
<span data-ttu-id="493de-129">Koncentratory IoT.</span><span class="sxs-lookup"><span data-stu-id="493de-129">Iot hubs.</span></span>

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

### <span data-ttu-id="493de-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="493de-130">-Location</span></span>
<span data-ttu-id="493de-131">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="493de-131">Location.</span></span>

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

### <span data-ttu-id="493de-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="493de-132">-Name</span></span>
<span data-ttu-id="493de-133">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="493de-133">Resource name.</span></span>

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

### <span data-ttu-id="493de-134">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="493de-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="493de-135">Konfiguracja rekomendacji.</span><span class="sxs-lookup"><span data-stu-id="493de-135">Recommendations configuration.</span></span>

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

### <span data-ttu-id="493de-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="493de-136">-ResourceGroupName</span></span>
<span data-ttu-id="493de-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="493de-137">Resource group name.</span></span>

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

### <span data-ttu-id="493de-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="493de-138">-ResourceId</span></span>
<span data-ttu-id="493de-139">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="493de-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="493de-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="493de-140">-Tag</span></span>
<span data-ttu-id="493de-141">Kolczyk.</span><span class="sxs-lookup"><span data-stu-id="493de-141">Tags.</span></span>

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

### <span data-ttu-id="493de-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="493de-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="493de-143">Niemaskowany stan rejestrowania adresów IP.</span><span class="sxs-lookup"><span data-stu-id="493de-143">Unmasked ip logging status.</span></span>

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

### <span data-ttu-id="493de-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="493de-144">-UserDefinedResource</span></span>
<span data-ttu-id="493de-145">Zasoby zdefiniowane przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="493de-145">User defined resources.</span></span>

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

### <span data-ttu-id="493de-146">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="493de-146">-Workspace</span></span>
<span data-ttu-id="493de-147">Identyfikator obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="493de-147">Workspace ID.</span></span>

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

### <span data-ttu-id="493de-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="493de-148">-Confirm</span></span>
<span data-ttu-id="493de-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="493de-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="493de-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="493de-150">-WhatIf</span></span>
<span data-ttu-id="493de-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="493de-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="493de-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="493de-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="493de-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="493de-153">CommonParameters</span></span>
<span data-ttu-id="493de-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="493de-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="493de-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="493de-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="493de-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="493de-156">INPUTS</span></span>

### <span data-ttu-id="493de-157">Microsoft. Azure. Commands. Security. models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="493de-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="493de-158">System. String</span><span class="sxs-lookup"><span data-stu-id="493de-158">System.String</span></span>

### <span data-ttu-id="493de-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="493de-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="493de-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="493de-160">System.String[]</span></span>

### <span data-ttu-id="493de-161">Microsoft. Azure. Commands. Security. models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="493de-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="493de-162">Microsoft. Azure. Commands. Security. models. IotSecuritySolutions. PSRecommendationConfiguration []</span><span class="sxs-lookup"><span data-stu-id="493de-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="493de-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="493de-163">OUTPUTS</span></span>

### <span data-ttu-id="493de-164">Microsoft. Azure. Commands. Security. models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="493de-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="493de-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="493de-165">NOTES</span></span>

## <span data-ttu-id="493de-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="493de-166">RELATED LINKS</span></span>
