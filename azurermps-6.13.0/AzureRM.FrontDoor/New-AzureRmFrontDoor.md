---
<span data-ttu-id="0f9a2-101">plik pomocy zewnętrznej: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml Nazwa modułu: AzureRM. FrontDoor wersja online: odpowiedni adres URL powinien być następujący: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor schemat: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span><span class="sxs-lookup"><span data-stu-id="0f9a2-101">external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml Module Name: AzureRM.FrontDoor online version: The corresponding URL should be the following: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span></span>
---

# <a name="new-azurermfrontdoor"></a><span data-ttu-id="0f9a2-102">New-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="0f9a2-102">New-AzureRmFrontDoor</span></span>

## <a name="synopsis"></a><span data-ttu-id="0f9a2-103">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f9a2-103">SYNOPSIS</span></span>
<span data-ttu-id="0f9a2-104">Tworzenie nowego modułu równoważenia obciążenia przed drzwiami platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0f9a2-104">Create a new Azure Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <a name="syntax"></a><span data-ttu-id="0f9a2-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f9a2-105">SYNTAX</span></span>

```
New-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <a name="description"></a><span data-ttu-id="0f9a2-106">Opis</span><span class="sxs-lookup"><span data-stu-id="0f9a2-106">DESCRIPTION</span></span>
<span data-ttu-id="0f9a2-107">Polecenie cmdlet **New-AzureRmFrontDoor** tworzy nowy moduł równoważenia obciążenia z przodu platformy Azure w określonej grupie zasobów w obszarze bieżący abonament</span><span class="sxs-lookup"><span data-stu-id="0f9a2-107">The **New-AzureRmFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <a name="examples"></a><span data-ttu-id="0f9a2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f9a2-108">EXAMPLES</span></span>

### <a name="example-1-create-a-front-door-based-on-given-parameters"></a><span data-ttu-id="0f9a2-109">Przykład 1. Tworzenie drzwi przednich na podstawie podanych parametrów.</span><span class="sxs-lookup"><span data-stu-id="0f9a2-109">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="0f9a2-110">Utwórz drzwi przednie na podstawie podanych parametrów.</span><span class="sxs-lookup"><span data-stu-id="0f9a2-110">Create a Front Door based on given parameters.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f9a2-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f9a2-111">PARAMETERS</span></span>

### <a name="-backendpool"></a><span data-ttu-id="0f9a2-112">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="0f9a2-112">-BackendPool</span></span>
<span data-ttu-id="0f9a2-113">Backendpools dostępne dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="0f9a2-113">Backendpools available to routing rule.</span></span>

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

### <a name="-defaultprofile"></a><span data-ttu-id="0f9a2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f9a2-114">-DefaultProfile</span></span>
<span data-ttu-id="0f9a2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f9a2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <a name="-enabledstate"></a><span data-ttu-id="0f9a2-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="0f9a2-116">-EnabledState</span></span>
<span data-ttu-id="0f9a2-117">EnabledStatea na przednim obszarze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0f9a2-117">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="0f9a2-118">Wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="0f9a2-118">Default value is Enabled</span></span>

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

### <a name="-frontendendpoint"></a><span data-ttu-id="0f9a2-119">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f9a2-119">-FrontendEndpoint</span></span>
<span data-ttu-id="0f9a2-120">Punkty końcowe frontonu są dostępne dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="0f9a2-120">Frontend endpoints available to routing rule.</span></span>

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

### <a name="-healthprobesetting"></a><span data-ttu-id="0f9a2-121">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="0f9a2-121">-HealthProbeSetting</span></span>
<span data-ttu-id="0f9a2-122">Ustawienia badania kondycji skojarzone z tym wystąpieniem przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="0f9a2-122">Health probe settings associated with this Front Door instance.</span></span>

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

### <a name="-loadbalancingsetting"></a><span data-ttu-id="0f9a2-123">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="0f9a2-123">-LoadBalancingSetting</span></span>
<span data-ttu-id="0f9a2-124">Ustawienia równoważenia obciążenia skojarzone z tym wystąpieniem przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="0f9a2-124">Load balancing settings associated with this Front Door instance.</span></span>

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

### <a name="-name"></a><span data-ttu-id="0f9a2-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0f9a2-125">-Name</span></span>
<span data-ttu-id="0f9a2-126">Imię i nazwisko drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="0f9a2-126">Front Door name.</span></span>

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

### <a name="-resourcegroupname"></a><span data-ttu-id="0f9a2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f9a2-127">-ResourceGroupName</span></span>
<span data-ttu-id="0f9a2-128">Nazwa grupy zasobów, w której zostaną utworzone drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="0f9a2-128">The resource group name that the Front Door will be created in.</span></span>

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

### <a name="-routingrule"></a><span data-ttu-id="0f9a2-129">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="0f9a2-129">-RoutingRule</span></span>
<span data-ttu-id="0f9a2-130">Reguły routingu skojarzone z tym FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0f9a2-130">Routing rules associated with this FrontDoor</span></span>

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

### <a name="-tag"></a><span data-ttu-id="0f9a2-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="0f9a2-131">-Tag</span></span>
<span data-ttu-id="0f9a2-132">Tagi są kojarzone z FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="0f9a2-132">The tags associate with the FrontDoor.</span></span>

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

### <a name="-confirm"></a><span data-ttu-id="0f9a2-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f9a2-133">-Confirm</span></span>
<span data-ttu-id="0f9a2-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f9a2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <a name="-whatif"></a><span data-ttu-id="0f9a2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f9a2-135">-WhatIf</span></span>
<span data-ttu-id="0f9a2-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f9a2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f9a2-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0f9a2-137">The cmdlet is not run.</span></span>

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

### <a name="commonparameters"></a><span data-ttu-id="0f9a2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f9a2-138">CommonParameters</span></span>
<span data-ttu-id="0f9a2-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f9a2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f9a2-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f9a2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <a name="inputs"></a><span data-ttu-id="0f9a2-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f9a2-141">INPUTS</span></span>

### <a name="systemstring"></a><span data-ttu-id="0f9a2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0f9a2-142">System.String</span></span>

## <a name="outputs"></a><span data-ttu-id="0f9a2-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f9a2-143">OUTPUTS</span></span>

### <a name="microsoftazurecommandsfrontdoormodelspsfrontdoor"></a><span data-ttu-id="0f9a2-144">Microsoft. Azure. Commands. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="0f9a2-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <a name="notes"></a><span data-ttu-id="0f9a2-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f9a2-145">NOTES</span></span>

## <a name="related-links"></a><span data-ttu-id="0f9a2-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f9a2-146">RELATED LINKS</span></span>

<span data-ttu-id="0f9a2-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
 [Nowe — AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [Nowe — AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [Nowe — AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [Nowe — AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [Nowe — AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="0f9a2-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
