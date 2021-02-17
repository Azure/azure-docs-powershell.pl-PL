---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 344041291f0d7f52aeebb0c968e99268ac042188
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243538"
---
# <span data-ttu-id="7d74b-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="7d74b-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="7d74b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d74b-102">SYNOPSIS</span></span>
<span data-ttu-id="7d74b-103">Aktualizowanie równoważenia obciążenia drzwi przednich</span><span class="sxs-lookup"><span data-stu-id="7d74b-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="7d74b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7d74b-104">SYNTAX</span></span>

### <span data-ttu-id="7d74b-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="7d74b-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d74b-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d74b-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d74b-107">ByFieldsWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d74b-107">ByFieldsWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] -BackendPoolsSetting <PSBackendPoolsSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d74b-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d74b-108">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d74b-109">ByObjectWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d74b-109">ByObjectWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d74b-110">ByObjectWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d74b-110">ByObjectWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d74b-111">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d74b-111">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d74b-112">ByResourceIdWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d74b-112">ByResourceIdWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d74b-113">ByResourceIdWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d74b-113">ByResourceIdWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d74b-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="7d74b-114">DESCRIPTION</span></span>
<span data-ttu-id="7d74b-115">Polecenie **cmdlet Set-AzFrontDoor** aktualizuje równoważenie obciążenia drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="7d74b-115">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="7d74b-116">Jeśli parametry wejściowe nie zostaną podane, zostaną użyte stare parametry z istniejących drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="7d74b-116">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="7d74b-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7d74b-117">EXAMPLES</span></span>

### <span data-ttu-id="7d74b-118">Przykład 1. Aktualizowanie istniejących drzwi frontowych za pomocą frontoronu FrontDoorName i ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="7d74b-118">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="7d74b-119">zaktualizować istniejący element FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="7d74b-119">update an existing FrontDoor.</span></span>

### <span data-ttu-id="7d74b-120">Przykład 2. Aktualizowanie istniejących drzwi frontowych za pomocą obiektu PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="7d74b-120">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="7d74b-121">zaktualizować istniejący element FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="7d74b-121">update an existing FrontDoor.</span></span>

### <span data-ttu-id="7d74b-122">Przykład 3. Aktualizowanie istniejących drzwi frontowych przy użyciu usługi ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d74b-122">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="7d74b-123">zaktualizować istniejący element FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="7d74b-123">update an existing FrontDoor.</span></span>

### <span data-ttu-id="7d74b-124">Przykład 4. Aktualizacja właściwości BackendPoolSetting EnforceCertificateNameCheck istniejącej bramy frontowej za pomocą parametru przełącznika -DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="7d74b-124">Example 4: update BackendPoolSetting property EnforceCertificateNameCheck of an existing Front Door with -DisableCertificateNameCheck switch parameter</span></span>
<span data-ttu-id="7d74b-125">Przednie drzwi do zaktualizowania można zidentyfikować za pomocą obiektów FrontoorName i ResourceGroupName, PSFrontDoor lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7d74b-125">Front Door to be updated can be identified using FrontoorName and ResourceGroupName, PSFrontDoor object, or ResourceId.</span></span> <span data-ttu-id="7d74b-126">(Zobacz na przykład 3 powyższe przykłady) W poniższym przykładzie użyto obiektu PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="7d74b-126">(See above 3 examples for example) The below example uses PSFrontDoor object.</span></span>

```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -DisableCertificateNameCheck

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {PSBackendPoolsSetting object with EnforceCertificateNameCheck is set to Disabled}
EnforceCertificateNameCheck : Disabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="7d74b-127">zaktualizować istniejący element FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="7d74b-127">update an existing FrontDoor.</span></span>

## <span data-ttu-id="7d74b-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d74b-128">PARAMETERS</span></span>

### <span data-ttu-id="7d74b-129">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="7d74b-129">-BackendPool</span></span>
<span data-ttu-id="7d74b-130">Bufory zaplecza dostępne dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="7d74b-130">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d74b-131">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="7d74b-131">-BackendPoolsSetting</span></span>
<span data-ttu-id="7d74b-132">Ustawienia dla wszystkich buforów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="7d74b-132">Settings for all backendPools.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet, ByObjectWithBackendPoolsSettingParameterSet, ByResourceIdWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d74b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d74b-133">-DefaultProfile</span></span>
<span data-ttu-id="7d74b-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d74b-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d74b-135">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="7d74b-135">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="7d74b-136">Czy wyłączyć sprawdzanie nazwy certyfikatu dla żądań HTTPS dla wszystkich pul zaplecza.</span><span class="sxs-lookup"><span data-stu-id="7d74b-136">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="7d74b-137">Brak wpływu na żądania inne niż HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7d74b-137">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet, ByObjectWithCertificateNameCheckParameterSet, ByResourceIdWithCertificateNameCheckParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d74b-138">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="7d74b-138">-EnabledState</span></span>
<span data-ttu-id="7d74b-139">Stan operacyjny urządzenia do równoważenia obciążenia drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="7d74b-139">Operational status of the Front Door load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d74b-140">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d74b-140">-FrontendEndpoint</span></span>
<span data-ttu-id="7d74b-141">Punkty końcowe frontendu dostępne dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="7d74b-141">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d74b-142">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="7d74b-142">-HealthProbeSetting</span></span>
<span data-ttu-id="7d74b-143">Ustawienia kondycji skojarzone z tym wystąpieniem drzwi frontowych.</span><span class="sxs-lookup"><span data-stu-id="7d74b-143">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d74b-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d74b-144">-InputObject</span></span>
<span data-ttu-id="7d74b-145">Obiekt Front Door do aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="7d74b-145">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet, ByObjectWithCertificateNameCheckParameterSet, ByObjectWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d74b-146">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="7d74b-146">-LoadBalancingSetting</span></span>
<span data-ttu-id="7d74b-147">Ustawienia równoważenia obciążenia skojarzone z tym wystąpieniem drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="7d74b-147">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d74b-148">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7d74b-148">-Name</span></span>
<span data-ttu-id="7d74b-149">Nazwa drzwi frontowych do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="7d74b-149">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithCertificateNameCheckParameterSet, ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d74b-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d74b-150">-ResourceGroupName</span></span>
<span data-ttu-id="7d74b-151">Grupa zasobów, do której należy drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="7d74b-151">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithCertificateNameCheckParameterSet, ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d74b-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d74b-152">-ResourceId</span></span>
<span data-ttu-id="7d74b-153">Identyfikator zasobu drzwi frontowych do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="7d74b-153">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithCertificateNameCheckParameterSet, ByResourceIdWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d74b-154">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="7d74b-154">-RoutingRule</span></span>
<span data-ttu-id="7d74b-155">Reguły routingu skojarzone z tym frontdoorem</span><span class="sxs-lookup"><span data-stu-id="7d74b-155">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d74b-156">— Tag</span><span class="sxs-lookup"><span data-stu-id="7d74b-156">-Tag</span></span>
<span data-ttu-id="7d74b-157">Tagi są kojarzą się z frontdoorem.</span><span class="sxs-lookup"><span data-stu-id="7d74b-157">The tags associate with the FrontDoor.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d74b-158">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7d74b-158">-Confirm</span></span>
<span data-ttu-id="7d74b-159">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7d74b-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d74b-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d74b-160">-WhatIf</span></span>
<span data-ttu-id="7d74b-161">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d74b-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d74b-162">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7d74b-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d74b-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d74b-163">CommonParameters</span></span>
<span data-ttu-id="7d74b-164">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d74b-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d74b-165">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d74b-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d74b-166">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d74b-166">INPUTS</span></span>

### <span data-ttu-id="7d74b-167">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="7d74b-167">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
### <span data-ttu-id="7d74b-168">System.String</span><span class="sxs-lookup"><span data-stu-id="7d74b-168">System.String</span></span>
## <span data-ttu-id="7d74b-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d74b-169">OUTPUTS</span></span>

### <span data-ttu-id="7d74b-170">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="7d74b-170">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="7d74b-171">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7d74b-171">NOTES</span></span>

## <span data-ttu-id="7d74b-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d74b-172">RELATED LINKS</span></span>

<span data-ttu-id="7d74b-173">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="7d74b-173">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
