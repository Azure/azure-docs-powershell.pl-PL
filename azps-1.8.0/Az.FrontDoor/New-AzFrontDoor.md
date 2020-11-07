---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: cea5b69b279b6f7f7a8e783d4ed328237377c18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868411"
---
# <span data-ttu-id="f9445-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9445-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="f9445-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9445-102">SYNOPSIS</span></span>
<span data-ttu-id="f9445-103">Tworzenie nowego modułu równoważenia obciążenia przed drzwiami platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f9445-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="f9445-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9445-104">SYNTAX</span></span>

```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9445-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f9445-105">DESCRIPTION</span></span>
<span data-ttu-id="f9445-106">Polecenie cmdlet **New-AzFrontDoor** tworzy nowy moduł równoważenia obciążenia z przodu platformy Azure w określonej grupie zasobów w obszarze bieżący abonament</span><span class="sxs-lookup"><span data-stu-id="f9445-106">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="f9445-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9445-107">EXAMPLES</span></span>

### <span data-ttu-id="f9445-108">Przykład 1. Tworzenie drzwi przednich na podstawie podanych parametrów.</span><span class="sxs-lookup"><span data-stu-id="f9445-108">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="f9445-109">Utwórz drzwi przednie na podstawie podanych parametrów.</span><span class="sxs-lookup"><span data-stu-id="f9445-109">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="f9445-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9445-110">PARAMETERS</span></span>

### <span data-ttu-id="f9445-111">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="f9445-111">-BackendPool</span></span>
<span data-ttu-id="f9445-112">Backendpools dostępne dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="f9445-112">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="f9445-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9445-113">-DefaultProfile</span></span>
<span data-ttu-id="f9445-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9445-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9445-115">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="f9445-115">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="f9445-116">Czy wyłączyć sprawdzanie nazw certyfikatów dla żądań HTTPS we wszystkich pulach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f9445-116">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="f9445-117">Brak wpływu na żądania inne niż HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f9445-117">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="f9445-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="f9445-118">-EnabledState</span></span>
<span data-ttu-id="f9445-119">EnabledStatea na przednim obszarze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f9445-119">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="f9445-120">Wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="f9445-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="f9445-121">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9445-121">-FrontendEndpoint</span></span>
<span data-ttu-id="f9445-122">Punkty końcowe frontonu są dostępne dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="f9445-122">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="f9445-123">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="f9445-123">-HealthProbeSetting</span></span>
<span data-ttu-id="f9445-124">Ustawienia badania kondycji skojarzone z tym wystąpieniem przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="f9445-124">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="f9445-125">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="f9445-125">-LoadBalancingSetting</span></span>
<span data-ttu-id="f9445-126">Ustawienia równoważenia obciążenia skojarzone z tym wystąpieniem przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="f9445-126">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="f9445-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f9445-127">-Name</span></span>
<span data-ttu-id="f9445-128">Imię i nazwisko drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="f9445-128">Front Door name.</span></span>

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

### <span data-ttu-id="f9445-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9445-129">-ResourceGroupName</span></span>
<span data-ttu-id="f9445-130">Nazwa grupy zasobów, w której zostaną utworzone drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="f9445-130">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="f9445-131">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="f9445-131">-RoutingRule</span></span>
<span data-ttu-id="f9445-132">Reguły routingu skojarzone z tym FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9445-132">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="f9445-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="f9445-133">-Tag</span></span>
<span data-ttu-id="f9445-134">Tagi są kojarzone z FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="f9445-134">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="f9445-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f9445-135">-Confirm</span></span>
<span data-ttu-id="f9445-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9445-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9445-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9445-137">-WhatIf</span></span>
<span data-ttu-id="f9445-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9445-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9445-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f9445-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9445-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9445-140">CommonParameters</span></span>
<span data-ttu-id="f9445-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9445-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9445-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9445-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9445-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9445-143">INPUTS</span></span>

### <span data-ttu-id="f9445-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f9445-144">None</span></span>

## <span data-ttu-id="f9445-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9445-145">OUTPUTS</span></span>

### <span data-ttu-id="f9445-146">Microsoft. Azure. Commands. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9445-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="f9445-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9445-147">NOTES</span></span>

## <span data-ttu-id="f9445-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9445-148">RELATED LINKS</span></span>

<span data-ttu-id="f9445-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [Nowe — AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [Nowe — AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [Nowe — AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [Nowe — AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [Nowe — AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="f9445-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>