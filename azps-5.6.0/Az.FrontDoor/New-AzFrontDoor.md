---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: f3a5b61561b0886af32aa13103f3234098c76357
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977121"
---
# <span data-ttu-id="1e4c7-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="1e4c7-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="1e4c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e4c7-102">SYNOPSIS</span></span>
<span data-ttu-id="1e4c7-103">Tworzenie nowego narzędzia do równoważenia obciążenia Azure Front Door</span><span class="sxs-lookup"><span data-stu-id="1e4c7-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="1e4c7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1e4c7-104">SYNTAX</span></span>

### <span data-ttu-id="1e4c7-105">ByFieldsWithBackendPoolsSettingParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1e4c7-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e4c7-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e4c7-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e4c7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1e4c7-107">DESCRIPTION</span></span>
<span data-ttu-id="1e4c7-108">Polecenie **cmdlet New-AzFrontDoor** tworzy nowy narzędzie do równoważenia obciążenia Front Door platformy Azure w określonej grupie zasobów w ramach bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1e4c7-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="1e4c7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1e4c7-109">EXAMPLES</span></span>

### <span data-ttu-id="1e4c7-110">Przykład 1. Tworzenie drzwi przednich na podstawie podanych parametrów.</span><span class="sxs-lookup"><span data-stu-id="1e4c7-110">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="1e4c7-111">Utwórz drzwi przednie na podstawie podanych parametrów.</span><span class="sxs-lookup"><span data-stu-id="1e4c7-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="1e4c7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e4c7-112">PARAMETERS</span></span>

### <span data-ttu-id="1e4c7-113">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="1e4c7-113">-BackendPool</span></span>
<span data-ttu-id="1e4c7-114">Bufory zaplecza dostępne dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="1e4c7-114">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4c7-115">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="1e4c7-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="1e4c7-116">Ustawienia dla wszystkich buforów zaplecza</span><span class="sxs-lookup"><span data-stu-id="1e4c7-116">Settings for all backendPools</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e4c7-117">-DefaultProfile</span></span>
<span data-ttu-id="1e4c7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e4c7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e4c7-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="1e4c7-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="1e4c7-120">Czy wyłączyć sprawdzanie nazwy certyfikatu dla żądań HTTPS dla wszystkich pul zaplecza.</span><span class="sxs-lookup"><span data-stu-id="1e4c7-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="1e4c7-121">Brak wpływu na żądania inne niż HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1e4c7-121">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4c7-122">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="1e4c7-122">-EnabledState</span></span>
<span data-ttu-id="1e4c7-123">EnabledState (Stan Front Door) równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="1e4c7-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="1e4c7-124">Wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="1e4c7-124">Default value is Enabled</span></span>

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

### <span data-ttu-id="1e4c7-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e4c7-125">-FrontendEndpoint</span></span>
<span data-ttu-id="1e4c7-126">Punkty końcowe frontendu dostępne dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="1e4c7-126">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4c7-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="1e4c7-127">-HealthProbeSetting</span></span>
<span data-ttu-id="1e4c7-128">Ustawienia kondycji skojarzone z tym wystąpieniem drzwi frontowych.</span><span class="sxs-lookup"><span data-stu-id="1e4c7-128">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4c7-129">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="1e4c7-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="1e4c7-130">Ustawienia równoważenia obciążenia skojarzone z tym wystąpieniem drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="1e4c7-130">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4c7-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1e4c7-131">-Name</span></span>
<span data-ttu-id="1e4c7-132">Nazwa drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="1e4c7-132">Front Door name.</span></span>

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

### <span data-ttu-id="1e4c7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e4c7-133">-ResourceGroupName</span></span>
<span data-ttu-id="1e4c7-134">Nazwa grupy zasobów, w przypadku których zostanie utworzona brama frontowa.</span><span class="sxs-lookup"><span data-stu-id="1e4c7-134">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="1e4c7-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="1e4c7-135">-RoutingRule</span></span>
<span data-ttu-id="1e4c7-136">Reguły routingu skojarzone z tym frontdoorem</span><span class="sxs-lookup"><span data-stu-id="1e4c7-136">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4c7-137">— Tag</span><span class="sxs-lookup"><span data-stu-id="1e4c7-137">-Tag</span></span>
<span data-ttu-id="1e4c7-138">Tagi są kojarzą się z frontdoorem.</span><span class="sxs-lookup"><span data-stu-id="1e4c7-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="1e4c7-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1e4c7-139">-Confirm</span></span>
<span data-ttu-id="1e4c7-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1e4c7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e4c7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e4c7-141">-WhatIf</span></span>
<span data-ttu-id="1e4c7-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e4c7-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e4c7-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1e4c7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e4c7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e4c7-144">CommonParameters</span></span>
<span data-ttu-id="1e4c7-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e4c7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e4c7-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e4c7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e4c7-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e4c7-147">INPUTS</span></span>

### <span data-ttu-id="1e4c7-148">Brak</span><span class="sxs-lookup"><span data-stu-id="1e4c7-148">None</span></span>
## <span data-ttu-id="1e4c7-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e4c7-149">OUTPUTS</span></span>

### <span data-ttu-id="1e4c7-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="1e4c7-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="1e4c7-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1e4c7-151">NOTES</span></span>

## <span data-ttu-id="1e4c7-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e4c7-152">RELATED LINKS</span></span>

<span data-ttu-id="1e4c7-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="1e4c7-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>