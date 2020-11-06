---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
ms.openlocfilehash: 250fa8a5638e1aa9d67d212fd45352c7756d2aef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524398"
---
# <span data-ttu-id="9867c-101">Set-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="9867c-101">Set-AzureRmFrontDoor</span></span>

## <span data-ttu-id="9867c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9867c-102">SYNOPSIS</span></span>
<span data-ttu-id="9867c-103">Aktualizowanie czołowego modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="9867c-103">Update a Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9867c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9867c-104">SYNTAX</span></span>

### <span data-ttu-id="9867c-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9867c-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9867c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9867c-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9867c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9867c-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9867c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9867c-108">DESCRIPTION</span></span>
<span data-ttu-id="9867c-109">Polecenie cmdlet **Set-AzureRmFrontDoor** umożliwia zaktualizowanie czołowego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9867c-109">The **Set-AzureRmFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="9867c-110">Jeśli parametry wejściowe nie są podane, będą używane stare parametry z obecnego frontu drzwi.</span><span class="sxs-lookup"><span data-stu-id="9867c-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="9867c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9867c-111">EXAMPLES</span></span>

### <span data-ttu-id="9867c-112">Przykład 1: aktualizowanie istniejących drzwi przednich przy użyciu FrontDoorName i ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="9867c-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="9867c-113">Zaktualizuj istniejące FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="9867c-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="9867c-114">Przykład 2: aktualizowanie istniejących drzwi przednich za pomocą obiektu PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="9867c-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="9867c-115">Zaktualizuj istniejące FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="9867c-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="9867c-116">Przykład 3: aktualizowanie istniejących drzwi przednich za pomocą ResourceId</span><span class="sxs-lookup"><span data-stu-id="9867c-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="9867c-117">Zaktualizuj istniejące FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="9867c-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="9867c-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9867c-118">PARAMETERS</span></span>

### <span data-ttu-id="9867c-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="9867c-119">-BackendPool</span></span>
<span data-ttu-id="9867c-120">Backendpools dostępne dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="9867c-120">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="9867c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9867c-121">-DefaultProfile</span></span>
<span data-ttu-id="9867c-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9867c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9867c-123">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="9867c-123">-EnabledState</span></span>
<span data-ttu-id="9867c-124">Stan operacyjny modułu równoważenia obciążenia przednia drzwi.</span><span class="sxs-lookup"><span data-stu-id="9867c-124">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="9867c-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="9867c-125">-FrontendEndpoint</span></span>
<span data-ttu-id="9867c-126">Punkty końcowe frontonu są dostępne dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="9867c-126">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="9867c-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="9867c-127">-HealthProbeSetting</span></span>
<span data-ttu-id="9867c-128">Ustawienia badania kondycji skojarzone z tym wystąpieniem przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="9867c-128">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="9867c-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9867c-129">-InputObject</span></span>
<span data-ttu-id="9867c-130">Obiekt z przednią drzwi do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="9867c-130">The Front Door object to update.</span></span>

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

### <span data-ttu-id="9867c-131">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="9867c-131">-LoadBalancingSetting</span></span>
<span data-ttu-id="9867c-132">Ustawienia równoważenia obciążenia skojarzone z tym wystąpieniem przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="9867c-132">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="9867c-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9867c-133">-Name</span></span>
<span data-ttu-id="9867c-134">Nazwa przednich drzwi, które mają zostać zaktualizowane.</span><span class="sxs-lookup"><span data-stu-id="9867c-134">The name of the Front Door to update.</span></span>

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

### <span data-ttu-id="9867c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9867c-135">-ResourceGroupName</span></span>
<span data-ttu-id="9867c-136">Grupa zasobów, do której należą przednia drzwi.</span><span class="sxs-lookup"><span data-stu-id="9867c-136">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="9867c-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9867c-137">-ResourceId</span></span>
<span data-ttu-id="9867c-138">Identyfikator zasobu przednich drzwi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="9867c-138">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9867c-139">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="9867c-139">-RoutingRule</span></span>
<span data-ttu-id="9867c-140">Reguły routingu skojarzone z tym FrontDoor</span><span class="sxs-lookup"><span data-stu-id="9867c-140">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="9867c-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="9867c-141">-Tag</span></span>
<span data-ttu-id="9867c-142">Tagi są kojarzone z FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="9867c-142">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="9867c-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9867c-143">-Confirm</span></span>
<span data-ttu-id="9867c-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9867c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9867c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9867c-145">-WhatIf</span></span>
<span data-ttu-id="9867c-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9867c-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9867c-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9867c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9867c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9867c-148">CommonParameters</span></span>
<span data-ttu-id="9867c-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9867c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9867c-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9867c-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9867c-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9867c-151">INPUTS</span></span>

### <span data-ttu-id="9867c-152">Microsoft. Azure. Commands. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="9867c-152">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="9867c-153">System. String</span><span class="sxs-lookup"><span data-stu-id="9867c-153">System.String</span></span>

## <span data-ttu-id="9867c-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9867c-154">OUTPUTS</span></span>

### <span data-ttu-id="9867c-155">Microsoft. Azure. Commands. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="9867c-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="9867c-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9867c-156">NOTES</span></span>

## <span data-ttu-id="9867c-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9867c-157">RELATED LINKS</span></span>

<span data-ttu-id="9867c-158">[Nowe — AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
 [Nowe — AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [Nowe — AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [Nowe — AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [Nowe — AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [Nowe — AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="9867c-158">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
