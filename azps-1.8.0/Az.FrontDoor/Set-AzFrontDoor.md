---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 57f1bf57495e75167a1936799c24aff5e6387722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868339"
---
# <span data-ttu-id="cd714-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd714-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="cd714-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd714-102">SYNOPSIS</span></span>
<span data-ttu-id="cd714-103">Aktualizowanie czołowego modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="cd714-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="cd714-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd714-104">SYNTAX</span></span>

### <span data-ttu-id="cd714-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd714-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd714-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd714-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd714-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd714-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd714-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cd714-108">DESCRIPTION</span></span>
<span data-ttu-id="cd714-109">Polecenie cmdlet **Set-AzFrontDoor** umożliwia zaktualizowanie czołowego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="cd714-109">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="cd714-110">Jeśli parametry wejściowe nie są podane, będą używane stare parametry z obecnego frontu drzwi.</span><span class="sxs-lookup"><span data-stu-id="cd714-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="cd714-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd714-111">EXAMPLES</span></span>

### <span data-ttu-id="cd714-112">Przykład 1: aktualizowanie istniejących drzwi przednich przy użyciu FrontDoorName i ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="cd714-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
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

<span data-ttu-id="cd714-113">Zaktualizuj istniejące FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="cd714-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="cd714-114">Przykład 2: aktualizowanie istniejących drzwi przednich za pomocą obiektu PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="cd714-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
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

<span data-ttu-id="cd714-115">Zaktualizuj istniejące FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="cd714-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="cd714-116">Przykład 3: aktualizowanie istniejących drzwi przednich za pomocą ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd714-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
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

<span data-ttu-id="cd714-117">Zaktualizuj istniejące FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="cd714-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="cd714-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd714-118">PARAMETERS</span></span>

### <span data-ttu-id="cd714-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="cd714-119">-BackendPool</span></span>
<span data-ttu-id="cd714-120">Backendpools dostępne dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="cd714-120">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="cd714-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd714-121">-DefaultProfile</span></span>
<span data-ttu-id="cd714-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd714-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd714-123">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="cd714-123">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="cd714-124">Czy wyłączyć sprawdzanie nazw certyfikatów dla żądań HTTPS we wszystkich pulach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="cd714-124">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="cd714-125">Brak wpływu na żądania inne niż HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cd714-125">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="cd714-126">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="cd714-126">-EnabledState</span></span>
<span data-ttu-id="cd714-127">Stan operacyjny modułu równoważenia obciążenia przednia drzwi.</span><span class="sxs-lookup"><span data-stu-id="cd714-127">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="cd714-128">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd714-128">-FrontendEndpoint</span></span>
<span data-ttu-id="cd714-129">Punkty końcowe frontonu są dostępne dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="cd714-129">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="cd714-130">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="cd714-130">-HealthProbeSetting</span></span>
<span data-ttu-id="cd714-131">Ustawienia badania kondycji skojarzone z tym wystąpieniem przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="cd714-131">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="cd714-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cd714-132">-InputObject</span></span>
<span data-ttu-id="cd714-133">Obiekt z przednią drzwi do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="cd714-133">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd714-134">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="cd714-134">-LoadBalancingSetting</span></span>
<span data-ttu-id="cd714-135">Ustawienia równoważenia obciążenia skojarzone z tym wystąpieniem przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="cd714-135">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="cd714-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd714-136">-Name</span></span>
<span data-ttu-id="cd714-137">Nazwa przednich drzwi, które mają zostać zaktualizowane.</span><span class="sxs-lookup"><span data-stu-id="cd714-137">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd714-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd714-138">-ResourceGroupName</span></span>
<span data-ttu-id="cd714-139">Grupa zasobów, do której należą przednia drzwi.</span><span class="sxs-lookup"><span data-stu-id="cd714-139">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd714-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd714-140">-ResourceId</span></span>
<span data-ttu-id="cd714-141">Identyfikator zasobu przednich drzwi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="cd714-141">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd714-142">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="cd714-142">-RoutingRule</span></span>
<span data-ttu-id="cd714-143">Reguły routingu skojarzone z tym FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd714-143">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="cd714-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="cd714-144">-Tag</span></span>
<span data-ttu-id="cd714-145">Tagi są kojarzone z FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="cd714-145">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="cd714-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd714-146">-Confirm</span></span>
<span data-ttu-id="cd714-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd714-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd714-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd714-148">-WhatIf</span></span>
<span data-ttu-id="cd714-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd714-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd714-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cd714-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd714-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd714-151">CommonParameters</span></span>
<span data-ttu-id="cd714-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd714-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd714-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd714-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd714-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd714-154">INPUTS</span></span>

### <span data-ttu-id="cd714-155">Microsoft. Azure. Commands. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd714-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="cd714-156">System. String</span><span class="sxs-lookup"><span data-stu-id="cd714-156">System.String</span></span>

## <span data-ttu-id="cd714-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd714-157">OUTPUTS</span></span>

### <span data-ttu-id="cd714-158">Microsoft. Azure. Commands. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd714-158">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="cd714-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd714-159">NOTES</span></span>

## <span data-ttu-id="cd714-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd714-160">RELATED LINKS</span></span>

<span data-ttu-id="cd714-161">[Nowe — AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [Nowe — AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [Nowe — AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [Nowe — AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [Nowe — AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [Nowe — AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="cd714-161">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
