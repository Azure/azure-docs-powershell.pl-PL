---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 007fb7a309b9dd305f58d2f947d3d2dfc55078e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707368"
---
# <span data-ttu-id="7a206-101">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a206-101">New-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="7a206-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a206-102">SYNOPSIS</span></span>
<span data-ttu-id="7a206-103">Tworzy punkt końcowy w profilu w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="7a206-103">Creates an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="7a206-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a206-104">SYNTAX</span></span>

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a206-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7a206-105">DESCRIPTION</span></span>
<span data-ttu-id="7a206-106">Polecenie cmdlet **New-AzTrafficManagerEndpoint** tworzy punkt końcowy w profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="7a206-106">The **New-AzTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="7a206-107">To polecenie cmdlet umożliwia przekazanie każdego nowego punktu końcowego do usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="7a206-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="7a206-108">Aby dodać wiele punktów końcowych do obiektu profilu lokalnego Menedżera ruchu i przekazać zmiany w ramach jednej operacji, użyj polecenia cmdlet Add-AzTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="7a206-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="7a206-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a206-109">EXAMPLES</span></span>

### <span data-ttu-id="7a206-110">Przykład 1. Tworzenie zewnętrznego punktu końcowego dla profilu</span><span class="sxs-lookup"><span data-stu-id="7a206-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="7a206-111">To polecenie powoduje utworzenie zewnętrznego punktu końcowego o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7a206-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="7a206-112">Przykład 2: Tworzenie punktu końcowego Azure dla profilu</span><span class="sxs-lookup"><span data-stu-id="7a206-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="7a206-113">To polecenie tworzy punkt końcowy Azure o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasób ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7a206-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="7a206-114">Punkt końcowy platformy Azure wskazuje aplikację Azure Web App, której identyfikator Menedżera zasobów Azure jest określony przez ścieżkę URI w *TargetResourceId*.</span><span class="sxs-lookup"><span data-stu-id="7a206-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="7a206-115">Polecenie nie określa parametru *EndpointLocation* , ponieważ zasób aplikacji sieci Web udostępnia lokalizację.</span><span class="sxs-lookup"><span data-stu-id="7a206-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="7a206-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a206-116">PARAMETERS</span></span>

### <span data-ttu-id="7a206-117">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="7a206-117">-CustomHeader</span></span>
<span data-ttu-id="7a206-118">Lista niestandardowych par nazw nagłówków i wartości dla żądań sondujące.</span><span class="sxs-lookup"><span data-stu-id="7a206-118">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a206-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a206-119">-DefaultProfile</span></span>
<span data-ttu-id="7a206-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a206-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a206-121">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="7a206-121">-EndpointLocation</span></span>
<span data-ttu-id="7a206-122">Określa lokalizację punktu końcowego, który ma być używany w metodzie routingu ruch wydajności.</span><span class="sxs-lookup"><span data-stu-id="7a206-122">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="7a206-123">Ten parametr dotyczy tylko punktów końcowych typu ExternalEndpoints lub NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="7a206-123">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="7a206-124">Ten parametr należy określić, gdy używana jest metoda routingu ruchowego wydajności.</span><span class="sxs-lookup"><span data-stu-id="7a206-124">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="7a206-125">Określ nazwę regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7a206-125">Specify an Azure region name.</span></span>
<span data-ttu-id="7a206-126">Aby uzyskać pełną listę regionów platformy Azure, zobacz regiony platformy Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="7a206-126">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a206-127">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="7a206-127">-EndpointStatus</span></span>
<span data-ttu-id="7a206-128">Określa stan punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="7a206-128">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="7a206-129">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="7a206-129">Valid values are:</span></span> 

- <span data-ttu-id="7a206-130">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="7a206-130">Enabled</span></span> 
- <span data-ttu-id="7a206-131">Łącza</span><span class="sxs-lookup"><span data-stu-id="7a206-131">Disabled</span></span> 

<span data-ttu-id="7a206-132">Jeśli stan jest włączony, punkt końcowy jest sondowany pod kątem kondycji punktu końcowego i jest włączony do metody routingu ruchu.</span><span class="sxs-lookup"><span data-stu-id="7a206-132">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a206-133">-Geomapowanie</span><span class="sxs-lookup"><span data-stu-id="7a206-133">-GeoMapping</span></span>
<span data-ttu-id="7a206-134">Lista regionów zamapowanych do tego punktu końcowego, gdy używana jest metoda routingu ruchu "geograficzny".</span><span class="sxs-lookup"><span data-stu-id="7a206-134">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="7a206-135">Aby uzyskać pełną listę zaakceptowanych wartości, zapoznaj się z dokumentacją w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="7a206-135">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a206-136">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="7a206-136">-MinChildEndpoints</span></span>
<span data-ttu-id="7a206-137">Określ nazwę regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7a206-137">Specify an Azure region name.</span></span>
<span data-ttu-id="7a206-138">Aby uzyskać pełną listę regionów platformy Azure, zobacz regiony platformy Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="7a206-138">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a206-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7a206-139">-Name</span></span>
<span data-ttu-id="7a206-140">Określa nazwę punktu końcowego usługi Traffic Managera, który jest tworzony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a206-140">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7a206-141">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="7a206-141">-Priority</span></span>
<span data-ttu-id="7a206-142">Określa priorytet, który Menedżer ruchu przypisuje do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="7a206-142">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="7a206-143">Ten parametr jest wykorzystywany tylko w przypadku, gdy profil usługi Traffic Manager jest skonfigurowany za pomocą metody routingu ruchu w celu uzyskania priorytetu.</span><span class="sxs-lookup"><span data-stu-id="7a206-143">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="7a206-144">Prawidłowe wartości to liczby całkowite z zakresu od 1 do 1000.</span><span class="sxs-lookup"><span data-stu-id="7a206-144">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="7a206-145">Niższe wartości reprezentują wyższy priorytet.</span><span class="sxs-lookup"><span data-stu-id="7a206-145">Lower values represent higher priority.</span></span>

<span data-ttu-id="7a206-146">Jeśli określisz priorytet, musisz określić priorytety dla wszystkich punktów końcowych w profilu, a żadne dwa punkty końcowe nie mogą mieć tej samej wartości priorytetu.</span><span class="sxs-lookup"><span data-stu-id="7a206-146">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="7a206-147">Jeśli nie określono priorytetów, Menedżer ruchu przypisuje domyślne wartości priorytetu do punktów końcowych, rozpoczynając od jednej (1), w kolejności, w jakiej profil wyświetla punkty końcowe.</span><span class="sxs-lookup"><span data-stu-id="7a206-147">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a206-148">-Refilename</span><span class="sxs-lookup"><span data-stu-id="7a206-148">-ProfileName</span></span>
<span data-ttu-id="7a206-149">Określa nazwę profilu usługi Traffic Manager, do którego to polecenie cmdlet dodaje punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="7a206-149">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="7a206-150">Aby uzyskać profil, Użyj poleceń cmdlet New-AzTrafficManagerProfile lub Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="7a206-150">To obtain a profile, use the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="7a206-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a206-151">-ResourceGroupName</span></span>
<span data-ttu-id="7a206-152">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a206-152">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7a206-153">To polecenie cmdlet powoduje utworzenie punktu końcowego zarządzania ruchem w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="7a206-153">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7a206-154">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="7a206-154">-SubnetMapping</span></span>
<span data-ttu-id="7a206-155">Lista zakresów adresów lub podsieci zamapowanych do tego punktu końcowego w przypadku korzystania z metody routingu ruchu sieciowego â € ̃Subnetâ €™.</span><span class="sxs-lookup"><span data-stu-id="7a206-155">The list of address ranges or subnets mapped to this endpoint when using the â€˜Subnetâ€™ traffic routing method.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a206-156">-Target</span><span class="sxs-lookup"><span data-stu-id="7a206-156">-Target</span></span>
<span data-ttu-id="7a206-157">Określa w pełni kwalifikowaną nazwę DNS punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="7a206-157">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="7a206-158">Usługa Traffic Manager zwraca tę wartość w odpowiedziach DNS, gdy kieruje ruch do tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="7a206-158">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="7a206-159">Ten parametr można określić tylko dla typu punktu końcowego ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="7a206-159">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="7a206-160">W przypadku innych typów punktów końcowych zamiast tego określ parametr *TargetResourceId* .</span><span class="sxs-lookup"><span data-stu-id="7a206-160">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a206-161">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7a206-161">-TargetResourceId</span></span>
<span data-ttu-id="7a206-162">Określa identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="7a206-162">Specifies resource ID of the target.</span></span>
<span data-ttu-id="7a206-163">Ten parametr można określić tylko dla typów punktów końcowych AzureEndpoints i NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="7a206-163">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="7a206-164">W polu Typ punktu końcowego ExternalEndpoints określ parametr *Target* .</span><span class="sxs-lookup"><span data-stu-id="7a206-164">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a206-165">-Type</span><span class="sxs-lookup"><span data-stu-id="7a206-165">-Type</span></span>
<span data-ttu-id="7a206-166">Określa typ punktu końcowego, który jest dodawany przez to polecenie cmdlet do profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="7a206-166">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="7a206-167">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="7a206-167">Valid values are:</span></span> 

- <span data-ttu-id="7a206-168">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="7a206-168">AzureEndpoints</span></span>
- <span data-ttu-id="7a206-169">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="7a206-169">ExternalEndpoints</span></span>
- <span data-ttu-id="7a206-170">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="7a206-170">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a206-171">-Waga</span><span class="sxs-lookup"><span data-stu-id="7a206-171">-Weight</span></span>
<span data-ttu-id="7a206-172">Określa wagę, jaką Menedżer ruchu przypisuje do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="7a206-172">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="7a206-173">Prawidłowe wartości to liczby całkowite z zakresu od 1 do 1000.</span><span class="sxs-lookup"><span data-stu-id="7a206-173">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="7a206-174">Wartość domyślna to jeden (1).</span><span class="sxs-lookup"><span data-stu-id="7a206-174">The default value is one (1).</span></span>
<span data-ttu-id="7a206-175">Ten parametr jest wykorzystywany tylko wtedy, gdy profil usługi Traffic Manager jest skonfigurowany przy użyciu ważonej metody routingu ruchu.</span><span class="sxs-lookup"><span data-stu-id="7a206-175">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a206-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a206-176">CommonParameters</span></span>
<span data-ttu-id="7a206-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a206-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a206-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a206-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a206-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a206-179">INPUTS</span></span>

### <span data-ttu-id="7a206-180">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7a206-180">None</span></span>

## <span data-ttu-id="7a206-181">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a206-181">OUTPUTS</span></span>

### <span data-ttu-id="7a206-182">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a206-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="7a206-183">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a206-183">NOTES</span></span>

## <span data-ttu-id="7a206-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a206-184">RELATED LINKS</span></span>

[<span data-ttu-id="7a206-185">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a206-185">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="7a206-186">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a206-186">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="7a206-187">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a206-187">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="7a206-188">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7a206-188">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="7a206-189">Nowe — AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7a206-189">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="7a206-190">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a206-190">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="7a206-191">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7a206-191">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


