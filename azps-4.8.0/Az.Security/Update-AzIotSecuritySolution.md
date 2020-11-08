---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Update-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
ms.openlocfilehash: ba84bccc92b58b7f8a21812e2f1599bbc9679d38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063213"
---
# <span data-ttu-id="bf417-101">Update-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="bf417-101">Update-AzIotSecuritySolution</span></span>

## <span data-ttu-id="bf417-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf417-102">SYNOPSIS</span></span>
<span data-ttu-id="bf417-103">Zaktualizuj co najmniej jedno z następujących właściwości w rozwiązaniu z zabezpieczeniami usługi IoT: Tagi, konfiguracja rekomendacji, zasoby zdefiniowane przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="bf417-103">Update one or more of the following properties in IoT security solution: tags, recommendation configuration, user defined resources</span></span>

## <span data-ttu-id="bf417-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf417-104">SYNTAX</span></span>

### <span data-ttu-id="bf417-105">ResourceGroupLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bf417-105">ResourceGroupLevelResource (Default)</span></span>
```
Update-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf417-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="bf417-106">ResourceId</span></span>
```
Update-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf417-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="bf417-107">InputObject</span></span>
```
Update-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf417-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bf417-108">DESCRIPTION</span></span>
<span data-ttu-id="bf417-109">Polecenie cmdlet Update-AzIotSecuritySolution updayes co najmniej jedno z następujących właściwości w określonym rozwiązaniu z zabezpieczeniami usługi IoT: Tagi, konfiguracja rekomendacji, zasoby zdefiniowane przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bf417-109">The Update-AzIotSecuritySolution cmdlet updayes one or more of the following properties in a specific IoT security solution: tags, recommendation configuration, user defined resources.</span></span>
<span data-ttu-id="bf417-110">W ramach rozwiązania zabezpieczeń IoT zostaną zaktualizowane tylko określone właściwości.</span><span class="sxs-lookup"><span data-stu-id="bf417-110">Only the specified properties will be updated inside the iot security solution.</span></span>
<span data-ttu-id="bf417-111">Rozwiązanie zabezpieczeń IoT gromadzi dane i zdarzenia zabezpieczeń z urządzeń IoT oraz centrum IoT, aby ułatwić zapobieganie i wykrywanie zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="bf417-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="bf417-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf417-112">EXAMPLES</span></span>

### <span data-ttu-id="bf417-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bf417-113">Example 1</span></span>
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

<span data-ttu-id="bf417-114">Aktualizacja rozwiązania zabezpieczającego IoT "z przykładu" z grupy zasobów "moja grupa zasobów" przy użyciu konfiguracji rekomendacji i zasobów definiowanych przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="bf417-114">Update iot security solution "MySample" from resource group "MyResourceGroup" with recommendation configuration and user defined resources</span></span>

## <span data-ttu-id="bf417-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf417-115">PARAMETERS</span></span>

### <span data-ttu-id="bf417-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf417-116">-DefaultProfile</span></span>
<span data-ttu-id="bf417-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf417-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf417-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bf417-118">-InputObject</span></span>
<span data-ttu-id="bf417-119">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="bf417-119">Input Object.</span></span>

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

### <span data-ttu-id="bf417-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf417-120">-Name</span></span>
<span data-ttu-id="bf417-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="bf417-121">Resource name.</span></span>

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

### <span data-ttu-id="bf417-122">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf417-122">-RecommendationsConfiguration</span></span>
<span data-ttu-id="bf417-123">Konfiguracja rekomendacji.</span><span class="sxs-lookup"><span data-stu-id="bf417-123">Recommendations configuration.</span></span>

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

### <span data-ttu-id="bf417-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf417-124">-ResourceGroupName</span></span>
<span data-ttu-id="bf417-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bf417-125">Resource group name.</span></span>

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

### <span data-ttu-id="bf417-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf417-126">-ResourceId</span></span>
<span data-ttu-id="bf417-127">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="bf417-127">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="bf417-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="bf417-128">-Tag</span></span>
<span data-ttu-id="bf417-129">Kolczyk.</span><span class="sxs-lookup"><span data-stu-id="bf417-129">Tags.</span></span>

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

### <span data-ttu-id="bf417-130">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="bf417-130">-UserDefinedResource</span></span>
<span data-ttu-id="bf417-131">Zasoby zdefiniowane przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bf417-131">User defined resources.</span></span>

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

### <span data-ttu-id="bf417-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bf417-132">-Confirm</span></span>
<span data-ttu-id="bf417-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf417-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf417-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf417-134">-WhatIf</span></span>
<span data-ttu-id="bf417-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf417-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf417-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bf417-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf417-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf417-137">CommonParameters</span></span>
<span data-ttu-id="bf417-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf417-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf417-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf417-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf417-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf417-140">INPUTS</span></span>

### <span data-ttu-id="bf417-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bf417-141">System.String</span></span>

### <span data-ttu-id="bf417-142">Microsoft. Azure. Commands. Security. models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="bf417-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="bf417-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bf417-143">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bf417-144">Microsoft. Azure. Commands. Security. models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="bf417-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="bf417-145">Microsoft. Azure. Commands. Security. models. IotSecuritySolutions. PSRecommendationConfiguration []</span><span class="sxs-lookup"><span data-stu-id="bf417-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="bf417-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf417-146">OUTPUTS</span></span>

### <span data-ttu-id="bf417-147">Microsoft. Azure. Commands. Security. models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="bf417-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="bf417-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf417-148">NOTES</span></span>

## <span data-ttu-id="bf417-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf417-149">RELATED LINKS</span></span>
