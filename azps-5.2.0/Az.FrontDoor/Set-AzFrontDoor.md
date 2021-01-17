---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 344041291f0d7f52aeebb0c968e99268ac042188
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342949"
---
# <span data-ttu-id="f19f2-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="f19f2-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="f19f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f19f2-102">SYNOPSIS</span></span>
<span data-ttu-id="f19f2-103">Aktualizowanie czołowego modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="f19f2-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="f19f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f19f2-104">SYNTAX</span></span>

### <span data-ttu-id="f19f2-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f19f2-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f19f2-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="f19f2-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f19f2-107">ByFieldsWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="f19f2-107">ByFieldsWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] -BackendPoolsSetting <PSBackendPoolsSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f19f2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f19f2-108">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f19f2-109">ByObjectWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="f19f2-109">ByObjectWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f19f2-110">ByObjectWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="f19f2-110">ByObjectWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f19f2-111">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f19f2-111">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f19f2-112">ByResourceIdWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="f19f2-112">ByResourceIdWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f19f2-113">ByResourceIdWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="f19f2-113">ByResourceIdWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f19f2-114">Opis</span><span class="sxs-lookup"><span data-stu-id="f19f2-114">DESCRIPTION</span></span>
<span data-ttu-id="f19f2-115">Polecenie cmdlet **Set-AzFrontDoor** umożliwia zaktualizowanie czołowego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f19f2-115">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="f19f2-116">Jeśli parametry wejściowe nie są podane, będą używane stare parametry z obecnego frontu drzwi.</span><span class="sxs-lookup"><span data-stu-id="f19f2-116">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="f19f2-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f19f2-117">EXAMPLES</span></span>

### <span data-ttu-id="f19f2-118">Przykład 1: aktualizowanie istniejących drzwi przednich przy użyciu FrontDoorName i ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="f19f2-118">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
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

<span data-ttu-id="f19f2-119">Zaktualizuj istniejące FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="f19f2-119">update an existing FrontDoor.</span></span>

### <span data-ttu-id="f19f2-120">Przykład 2: aktualizowanie istniejących drzwi przednich za pomocą obiektu PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="f19f2-120">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
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

<span data-ttu-id="f19f2-121">Zaktualizuj istniejące FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="f19f2-121">update an existing FrontDoor.</span></span>

### <span data-ttu-id="f19f2-122">Przykład 3: aktualizowanie istniejących drzwi przednich za pomocą ResourceId</span><span class="sxs-lookup"><span data-stu-id="f19f2-122">Example 3: update an existing Front Door with ResourceId</span></span>
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

<span data-ttu-id="f19f2-123">Zaktualizuj istniejące FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="f19f2-123">update an existing FrontDoor.</span></span>

### <span data-ttu-id="f19f2-124">Przykład 4: aktualizowanie właściwości BackendPoolSetting EnforceCertificateNameCheck istniejących drzwi przednich przy użyciu parametru-DisableCertificateNameCheck Switch</span><span class="sxs-lookup"><span data-stu-id="f19f2-124">Example 4: update BackendPoolSetting property EnforceCertificateNameCheck of an existing Front Door with -DisableCertificateNameCheck switch parameter</span></span>
<span data-ttu-id="f19f2-125">Przednie są one aktualizowane przy użyciu FrontoorName, ResourceGroupName, PSFrontDoor obiektu lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f19f2-125">Front Door to be updated can be identified using FrontoorName and ResourceGroupName, PSFrontDoor object, or ResourceId.</span></span> <span data-ttu-id="f19f2-126">(Na przykład powyżej 3 przykładów) W poniższym przykładzie użyto obiektu PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="f19f2-126">(See above 3 examples for example) The below example uses PSFrontDoor object.</span></span>

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

<span data-ttu-id="f19f2-127">Zaktualizuj istniejące FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="f19f2-127">update an existing FrontDoor.</span></span>

## <span data-ttu-id="f19f2-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f19f2-128">PARAMETERS</span></span>

### <span data-ttu-id="f19f2-129">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="f19f2-129">-BackendPool</span></span>
<span data-ttu-id="f19f2-130">Backendpools dostępne dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="f19f2-130">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="f19f2-131">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="f19f2-131">-BackendPoolsSetting</span></span>
<span data-ttu-id="f19f2-132">Ustawienia wszystkich backendPools.</span><span class="sxs-lookup"><span data-stu-id="f19f2-132">Settings for all backendPools.</span></span>

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

### <span data-ttu-id="f19f2-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f19f2-133">-DefaultProfile</span></span>
<span data-ttu-id="f19f2-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f19f2-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f19f2-135">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="f19f2-135">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="f19f2-136">Czy wyłączyć sprawdzanie nazw certyfikatów dla żądań HTTPS we wszystkich pulach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f19f2-136">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="f19f2-137">Brak wpływu na żądania inne niż HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f19f2-137">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="f19f2-138">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="f19f2-138">-EnabledState</span></span>
<span data-ttu-id="f19f2-139">Stan operacyjny modułu równoważenia obciążenia przednia drzwi.</span><span class="sxs-lookup"><span data-stu-id="f19f2-139">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="f19f2-140">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="f19f2-140">-FrontendEndpoint</span></span>
<span data-ttu-id="f19f2-141">Punkty końcowe frontonu są dostępne dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="f19f2-141">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="f19f2-142">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="f19f2-142">-HealthProbeSetting</span></span>
<span data-ttu-id="f19f2-143">Ustawienia badania kondycji skojarzone z tym wystąpieniem przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="f19f2-143">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="f19f2-144">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f19f2-144">-InputObject</span></span>
<span data-ttu-id="f19f2-145">Obiekt z przednią drzwi do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="f19f2-145">The Front Door object to update.</span></span>

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

### <span data-ttu-id="f19f2-146">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="f19f2-146">-LoadBalancingSetting</span></span>
<span data-ttu-id="f19f2-147">Ustawienia równoważenia obciążenia skojarzone z tym wystąpieniem przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="f19f2-147">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="f19f2-148">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f19f2-148">-Name</span></span>
<span data-ttu-id="f19f2-149">Nazwa przednich drzwi, które mają zostać zaktualizowane.</span><span class="sxs-lookup"><span data-stu-id="f19f2-149">The name of the Front Door to update.</span></span>

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

### <span data-ttu-id="f19f2-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f19f2-150">-ResourceGroupName</span></span>
<span data-ttu-id="f19f2-151">Grupa zasobów, do której należą przednia drzwi.</span><span class="sxs-lookup"><span data-stu-id="f19f2-151">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="f19f2-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f19f2-152">-ResourceId</span></span>
<span data-ttu-id="f19f2-153">Identyfikator zasobu przednich drzwi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="f19f2-153">Resource Id of the Front Door to update</span></span>

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

### <span data-ttu-id="f19f2-154">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="f19f2-154">-RoutingRule</span></span>
<span data-ttu-id="f19f2-155">Reguły routingu skojarzone z tym FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f19f2-155">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="f19f2-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="f19f2-156">-Tag</span></span>
<span data-ttu-id="f19f2-157">Tagi są kojarzone z FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="f19f2-157">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="f19f2-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f19f2-158">-Confirm</span></span>
<span data-ttu-id="f19f2-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f19f2-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f19f2-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f19f2-160">-WhatIf</span></span>
<span data-ttu-id="f19f2-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f19f2-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f19f2-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f19f2-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f19f2-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f19f2-163">CommonParameters</span></span>
<span data-ttu-id="f19f2-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f19f2-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f19f2-165">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f19f2-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f19f2-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f19f2-166">INPUTS</span></span>

### <span data-ttu-id="f19f2-167">Microsoft. Azure. Commands. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="f19f2-167">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
### <span data-ttu-id="f19f2-168">System. String</span><span class="sxs-lookup"><span data-stu-id="f19f2-168">System.String</span></span>
## <span data-ttu-id="f19f2-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f19f2-169">OUTPUTS</span></span>

### <span data-ttu-id="f19f2-170">Microsoft. Azure. Commands. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="f19f2-170">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="f19f2-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f19f2-171">NOTES</span></span>

## <span data-ttu-id="f19f2-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f19f2-172">RELATED LINKS</span></span>

<span data-ttu-id="f19f2-173">[Nowe — AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [Nowe — AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [Nowe — AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [Nowe — AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [Nowe — AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [Nowe — AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="f19f2-173">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
