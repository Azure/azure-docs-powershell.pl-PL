---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: 3f08ada3dd485a1e18bb6f0a91037ba1df0b5f25
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351142"
---
# <span data-ttu-id="d244a-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d244a-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="d244a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d244a-102">SYNOPSIS</span></span>
<span data-ttu-id="d244a-103">Tworzenie nowego modułu równoważenia obciążenia przed drzwiami platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d244a-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="d244a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d244a-104">SYNTAX</span></span>

### <span data-ttu-id="d244a-105">ByFieldsWithBackendPoolsSettingParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d244a-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d244a-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="d244a-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d244a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d244a-107">DESCRIPTION</span></span>
<span data-ttu-id="d244a-108">Polecenie cmdlet **New-AzFrontDoor** tworzy nowy moduł równoważenia obciążenia z przodu platformy Azure w określonej grupie zasobów w obszarze bieżący abonament</span><span class="sxs-lookup"><span data-stu-id="d244a-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="d244a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d244a-109">EXAMPLES</span></span>

### <span data-ttu-id="d244a-110">Przykład 1. Tworzenie drzwi przednich na podstawie podanych parametrów.</span><span class="sxs-lookup"><span data-stu-id="d244a-110">Example 1: Create a Front Door based on given parameters.</span></span>
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

<span data-ttu-id="d244a-111">Utwórz drzwi przednie na podstawie podanych parametrów.</span><span class="sxs-lookup"><span data-stu-id="d244a-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="d244a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d244a-112">PARAMETERS</span></span>

### <span data-ttu-id="d244a-113">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="d244a-113">-BackendPool</span></span>
<span data-ttu-id="d244a-114">Backendpools dostępne dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="d244a-114">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="d244a-115">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="d244a-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="d244a-116">Ustawienia wszystkich backendPools</span><span class="sxs-lookup"><span data-stu-id="d244a-116">Settings for all backendPools</span></span>

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

### <span data-ttu-id="d244a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d244a-117">-DefaultProfile</span></span>
<span data-ttu-id="d244a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d244a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d244a-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="d244a-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="d244a-120">Czy wyłączyć sprawdzanie nazw certyfikatów dla żądań HTTPS we wszystkich pulach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d244a-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="d244a-121">Brak wpływu na żądania inne niż HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d244a-121">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="d244a-122">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="d244a-122">-EnabledState</span></span>
<span data-ttu-id="d244a-123">EnabledStatea na przednim obszarze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="d244a-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="d244a-124">Wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="d244a-124">Default value is Enabled</span></span>

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

### <span data-ttu-id="d244a-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="d244a-125">-FrontendEndpoint</span></span>
<span data-ttu-id="d244a-126">Punkty końcowe frontonu są dostępne dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="d244a-126">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="d244a-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="d244a-127">-HealthProbeSetting</span></span>
<span data-ttu-id="d244a-128">Ustawienia badania kondycji skojarzone z tym wystąpieniem przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="d244a-128">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="d244a-129">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="d244a-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="d244a-130">Ustawienia równoważenia obciążenia skojarzone z tym wystąpieniem przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="d244a-130">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="d244a-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d244a-131">-Name</span></span>
<span data-ttu-id="d244a-132">Imię i nazwisko drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="d244a-132">Front Door name.</span></span>

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

### <span data-ttu-id="d244a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d244a-133">-ResourceGroupName</span></span>
<span data-ttu-id="d244a-134">Nazwa grupy zasobów, w której zostaną utworzone drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="d244a-134">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="d244a-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="d244a-135">-RoutingRule</span></span>
<span data-ttu-id="d244a-136">Reguły routingu skojarzone z tym FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d244a-136">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="d244a-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="d244a-137">-Tag</span></span>
<span data-ttu-id="d244a-138">Tagi są kojarzone z FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="d244a-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="d244a-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d244a-139">-Confirm</span></span>
<span data-ttu-id="d244a-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d244a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d244a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d244a-141">-WhatIf</span></span>
<span data-ttu-id="d244a-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d244a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d244a-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d244a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d244a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d244a-144">CommonParameters</span></span>
<span data-ttu-id="d244a-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d244a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d244a-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d244a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d244a-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d244a-147">INPUTS</span></span>

### <span data-ttu-id="d244a-148">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d244a-148">None</span></span>
## <span data-ttu-id="d244a-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d244a-149">OUTPUTS</span></span>

### <span data-ttu-id="d244a-150">Microsoft. Azure. Commands. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d244a-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="d244a-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d244a-151">NOTES</span></span>

## <span data-ttu-id="d244a-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d244a-152">RELATED LINKS</span></span>

<span data-ttu-id="d244a-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [Nowe — AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [Nowe — AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [Nowe — AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [Nowe — AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [Nowe — AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="d244a-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>