---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195514"
---
# <span data-ttu-id="43d09-101">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="43d09-101">New-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="43d09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43d09-102">SYNOPSIS</span></span>
<span data-ttu-id="43d09-103">Tworzy punkt końcowy w profilu Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="43d09-103">Creates an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="43d09-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="43d09-104">SYNTAX</span></span>

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43d09-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="43d09-105">DESCRIPTION</span></span>
<span data-ttu-id="43d09-106">Polecenie **cmdlet New-AzTrafficManagerEndpoint** tworzy punkt końcowy w profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="43d09-106">The **New-AzTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="43d09-107">To polecenie cmdlet zatwierdza każdy nowy punkt końcowy w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="43d09-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="43d09-108">Aby dodać wiele punktów końcowych do obiektu profilu lokalnego menedżera ruchu i zatwierdzić zmiany w ramach jednej operacji, użyj Add-AzTrafficManagerEndpointConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43d09-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="43d09-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="43d09-109">EXAMPLES</span></span>

### <span data-ttu-id="43d09-110">Przykład 1. Tworzenie zewnętrznego punktu końcowego profilu</span><span class="sxs-lookup"><span data-stu-id="43d09-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="43d09-111">To polecenie tworzy zewnętrzny punkt końcowy o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasobów o nazwie Grupa Zasobów11.</span><span class="sxs-lookup"><span data-stu-id="43d09-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="43d09-112">Przykład 2. Tworzenie punktu końcowego platformy Azure dla profilu</span><span class="sxs-lookup"><span data-stu-id="43d09-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="43d09-113">To polecenie tworzy punkt końcowy platformy Azure o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="43d09-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="43d09-114">Punkt końcowy platformy Azure wskazuje aplikację Azure Web App, której identyfikator Azure Resource Manager jest podawany przez ścieżkę URI *w identyfikatorze TargetResourceId.*</span><span class="sxs-lookup"><span data-stu-id="43d09-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="43d09-115">To polecenie nie określa *parametru EndpointLocation,* ponieważ zasób aplikacji Sieci Web dostarcza lokalizację.</span><span class="sxs-lookup"><span data-stu-id="43d09-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="43d09-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43d09-116">PARAMETERS</span></span>

### <span data-ttu-id="43d09-117">- CustomHeader</span><span class="sxs-lookup"><span data-stu-id="43d09-117">-CustomHeader</span></span>
<span data-ttu-id="43d09-118">Lista niestandardowych par nazw nagłówków i wartości dla żądań zakupu.</span><span class="sxs-lookup"><span data-stu-id="43d09-118">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="43d09-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d09-119">-DefaultProfile</span></span>
<span data-ttu-id="43d09-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="43d09-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43d09-121">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="43d09-121">-EndpointLocation</span></span>
<span data-ttu-id="43d09-122">Określa lokalizację punktu końcowego do użycia w metodzie routingu ruchu wydajności.</span><span class="sxs-lookup"><span data-stu-id="43d09-122">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="43d09-123">Ten parametr ma zastosowanie tylko do punktów końcowych typu ExternalEndpoints lub NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="43d09-123">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="43d09-124">Ten parametr należy określić podczas korzystania z metody routingu ruchu wydajności.</span><span class="sxs-lookup"><span data-stu-id="43d09-124">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="43d09-125">Określ nazwę regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43d09-125">Specify an Azure region name.</span></span>
<span data-ttu-id="43d09-126">Aby uzyskać pełną listę regionów platformy Azure, zobacz Regiony platformy Azure http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) (.</span><span class="sxs-lookup"><span data-stu-id="43d09-126">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="43d09-127">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="43d09-127">-EndpointStatus</span></span>
<span data-ttu-id="43d09-128">Określa stan punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="43d09-128">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="43d09-129">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="43d09-129">Valid values are:</span></span> 

- <span data-ttu-id="43d09-130">Włączone</span><span class="sxs-lookup"><span data-stu-id="43d09-130">Enabled</span></span> 
- <span data-ttu-id="43d09-131">Wyłączone</span><span class="sxs-lookup"><span data-stu-id="43d09-131">Disabled</span></span> 

<span data-ttu-id="43d09-132">Jeśli stan jest włączony, punkt końcowy jest prawdopodobny dla kondycji punktu końcowego i jest uwzględniany w metodzie routingu ruchu.</span><span class="sxs-lookup"><span data-stu-id="43d09-132">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="43d09-133">— GeoMapping</span><span class="sxs-lookup"><span data-stu-id="43d09-133">-GeoMapping</span></span>
<span data-ttu-id="43d09-134">Lista regionów zamapowanych na ten punkt końcowy podczas korzystania z metody routingu ruchu geograficznego.</span><span class="sxs-lookup"><span data-stu-id="43d09-134">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="43d09-135">Aby uzyskać pełną listę zaakceptowanych wartości, zapoznaj się z dokumentacją menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="43d09-135">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>

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

### <span data-ttu-id="43d09-136">- MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="43d09-136">-MinChildEndpoints</span></span>
<span data-ttu-id="43d09-137">Określ nazwę regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43d09-137">Specify an Azure region name.</span></span>
<span data-ttu-id="43d09-138">Aby uzyskać pełną listę regionów platformy Azure, zobacz Regiony platformy Azure http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) (.</span><span class="sxs-lookup"><span data-stu-id="43d09-138">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="43d09-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="43d09-139">-Name</span></span>
<span data-ttu-id="43d09-140">Określa nazwę punktu końcowego Menedżera ruchu, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43d09-140">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="43d09-141">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="43d09-141">-Priority</span></span>
<span data-ttu-id="43d09-142">Określa priorytet przypisywany przez Menedżera ruchu do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="43d09-142">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="43d09-143">Ten parametr jest używany tylko wtedy, gdy profil menedżera ruchu jest skonfigurowany przy użyciu metody routingu ruchu o priorytecie.</span><span class="sxs-lookup"><span data-stu-id="43d09-143">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="43d09-144">Prawidłowe wartości to liczby całkowite z od 1 do 1000.</span><span class="sxs-lookup"><span data-stu-id="43d09-144">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="43d09-145">Niższe wartości mają wyższy priorytet.</span><span class="sxs-lookup"><span data-stu-id="43d09-145">Lower values represent higher priority.</span></span>

<span data-ttu-id="43d09-146">Jeśli określisz priorytet, musisz określić priorytety dla wszystkich punktów końcowych w profilu, a dwa punkty końcowe nie mogą mieć tej samej wartości priorytetu.</span><span class="sxs-lookup"><span data-stu-id="43d09-146">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="43d09-147">Jeśli nie określisz priorytetów, menedżer ruchu przypisze domyślne wartości priorytetów do punktów końcowych, zaczynając od jednego (1) w kolejności, w których profil zawiera listę punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="43d09-147">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="43d09-148">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="43d09-148">-ProfileName</span></span>
<span data-ttu-id="43d09-149">Określa nazwę profilu menedżera ruchu, do którego to polecenie cmdlet dodaje punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="43d09-149">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="43d09-150">Aby uzyskać profil, użyj New-AzTrafficManagerProfile lub Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43d09-150">To obtain a profile, use the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="43d09-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43d09-151">-ResourceGroupName</span></span>
<span data-ttu-id="43d09-152">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="43d09-152">Specifies the name of a resource group.</span></span>
<span data-ttu-id="43d09-153">To polecenie cmdlet tworzy punkt końcowy Menedżera ruchu w grupie, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="43d09-153">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="43d09-154">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="43d09-154">-SubnetMapping</span></span>
<span data-ttu-id="43d09-155">Lista zakresów adresów lub podsieci zamapowanych na ten punkt końcowy podczas korzystania z metody routingu ruchu "Podsieci".</span><span class="sxs-lookup"><span data-stu-id="43d09-155">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="43d09-156">— element docelowy</span><span class="sxs-lookup"><span data-stu-id="43d09-156">-Target</span></span>
<span data-ttu-id="43d09-157">Określa w pełni kwalifikowaną nazwę DNS punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="43d09-157">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="43d09-158">Menedżer ruchu zwraca tę wartość w odpowiedziach DNS, gdy kieruje ruch do tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="43d09-158">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="43d09-159">Określ ten parametr tylko dla typu punktu końcowego ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="43d09-159">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="43d09-160">W przypadku innych typów punktów końcowych określ zamiast *tego parametr TargetResourceId.*</span><span class="sxs-lookup"><span data-stu-id="43d09-160">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="43d09-161">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="43d09-161">-TargetResourceId</span></span>
<span data-ttu-id="43d09-162">Określa identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="43d09-162">Specifies resource ID of the target.</span></span>
<span data-ttu-id="43d09-163">Określ ten parametr tylko dla typów punktów końcowych AzureEndpoints i NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="43d09-163">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="43d09-164">W przypadku typu punktu końcowego ExternalEndpoints określ zamiast tego *parametr Target.*</span><span class="sxs-lookup"><span data-stu-id="43d09-164">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="43d09-165">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="43d09-165">-Type</span></span>
<span data-ttu-id="43d09-166">Określa typ punktu końcowego, który to polecenie cmdlet dodaje do profilu Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="43d09-166">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="43d09-167">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="43d09-167">Valid values are:</span></span> 

- <span data-ttu-id="43d09-168">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="43d09-168">AzureEndpoints</span></span>
- <span data-ttu-id="43d09-169">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="43d09-169">ExternalEndpoints</span></span>
- <span data-ttu-id="43d09-170">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="43d09-170">NestedEndpoints</span></span>

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

### <span data-ttu-id="43d09-171">— Waga</span><span class="sxs-lookup"><span data-stu-id="43d09-171">-Weight</span></span>
<span data-ttu-id="43d09-172">Określa wagę przypisywaną przez Menedżera ruchu do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="43d09-172">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="43d09-173">Prawidłowe wartości to liczby całkowite z od 1 do 1000.</span><span class="sxs-lookup"><span data-stu-id="43d09-173">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="43d09-174">Wartość domyślna to jeden (1).</span><span class="sxs-lookup"><span data-stu-id="43d09-174">The default value is one (1).</span></span>
<span data-ttu-id="43d09-175">Ten parametr jest używany tylko wtedy, gdy profil menedżera ruchu jest skonfigurowany przy użyciu metody routingu ruchu ważonego.</span><span class="sxs-lookup"><span data-stu-id="43d09-175">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="43d09-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d09-176">CommonParameters</span></span>
<span data-ttu-id="43d09-177">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43d09-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d09-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43d09-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d09-179">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43d09-179">INPUTS</span></span>

### <span data-ttu-id="43d09-180">Brak</span><span class="sxs-lookup"><span data-stu-id="43d09-180">None</span></span>

## <span data-ttu-id="43d09-181">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43d09-181">OUTPUTS</span></span>

### <span data-ttu-id="43d09-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="43d09-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="43d09-183">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="43d09-183">NOTES</span></span>

## <span data-ttu-id="43d09-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43d09-184">RELATED LINKS</span></span>

[<span data-ttu-id="43d09-185">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="43d09-185">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="43d09-186">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="43d09-186">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="43d09-187">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="43d09-187">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="43d09-188">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="43d09-188">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="43d09-189">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="43d09-189">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="43d09-190">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="43d09-190">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="43d09-191">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="43d09-191">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


