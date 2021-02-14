---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 77bb21030c24d9fed159160262c23e1e821e0fe1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241586"
---
# <span data-ttu-id="b8bca-101">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b8bca-101">Add-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="b8bca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8bca-102">SYNOPSIS</span></span>
<span data-ttu-id="b8bca-103">Dodaje punkt końcowy do obiektu profilu lokalnego menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="b8bca-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="b8bca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b8bca-104">SYNTAX</span></span>

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8bca-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b8bca-105">DESCRIPTION</span></span>
<span data-ttu-id="b8bca-106">Polecenie **cmdlet Add-AzTrafficManagerEndpointConfig** dodaje punkt końcowy do lokalnego obiektu profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="b8bca-106">The **Add-AzTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="b8bca-107">Profil można uzyskać za pomocą New-AzTrafficManagerProfile lub Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8bca-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="b8bca-108">To polecenie cmdlet działa na lokalnym obiekcie profilu.</span><span class="sxs-lookup"><span data-stu-id="b8bca-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="b8bca-109">Zatwierdzanie zmian w profilu menedżera ruchu za pomocą Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8bca-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="b8bca-110">Aby utworzyć punkt końcowy i zatwierdzić zmianę w ramach jednej operacji, użyj New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8bca-110">To create an endpoint and commit the change in a single operation, use the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="b8bca-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b8bca-111">EXAMPLES</span></span>

### <span data-ttu-id="b8bca-112">Przykład 1. Dodawanie punktu końcowego do profilu</span><span class="sxs-lookup"><span data-stu-id="b8bca-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="b8bca-113">Pierwsze polecenie otrzymuje profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="b8bca-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="b8bca-114">Polecenie przechowuje profil lokalny w $TrafficManagerProfile zmienną.</span><span class="sxs-lookup"><span data-stu-id="b8bca-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="b8bca-115">Drugie polecenie powoduje dodanie punktu końcowego o nazwie contoso do profilu przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b8bca-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="b8bca-116">To polecenie zawiera dane konfiguracji dla punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="b8bca-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="b8bca-117">To polecenie zmienia tylko obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="b8bca-117">This command changes only the local object.</span></span>

<span data-ttu-id="b8bca-118">Ostatnie polecenie aktualizuje profil usługi Traffic Manager na platformie Azure w celu dopasowania wartości lokalnej do $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b8bca-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="b8bca-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8bca-119">PARAMETERS</span></span>

### <span data-ttu-id="b8bca-120">- CustomHeader</span><span class="sxs-lookup"><span data-stu-id="b8bca-120">-CustomHeader</span></span>
<span data-ttu-id="b8bca-121">Lista niestandardowych par nazw nagłówków i wartości dla żądań zakupu.</span><span class="sxs-lookup"><span data-stu-id="b8bca-121">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="b8bca-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8bca-122">-DefaultProfile</span></span>
<span data-ttu-id="b8bca-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8bca-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8bca-124">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="b8bca-124">-EndpointLocation</span></span>
<span data-ttu-id="b8bca-125">Określa lokalizację punktu końcowego do użycia w metodzie routingu ruchu wydajności.</span><span class="sxs-lookup"><span data-stu-id="b8bca-125">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="b8bca-126">Ten parametr ma zastosowanie tylko do punktów końcowych typu ExternalEndpoints lub NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="b8bca-126">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="b8bca-127">Ten parametr należy określić podczas korzystania z metody routingu ruchu wydajności.</span><span class="sxs-lookup"><span data-stu-id="b8bca-127">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="b8bca-128">Określ nazwę regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b8bca-128">Specify an Azure region name.</span></span>
<span data-ttu-id="b8bca-129">Aby uzyskać pełną listę regionów platformy Azure, zobacz Regiony platformy Azure http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) (.</span><span class="sxs-lookup"><span data-stu-id="b8bca-129">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="b8bca-130">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b8bca-130">-EndpointName</span></span>
<span data-ttu-id="b8bca-131">Określa nazwę punktu końcowego Menedżera ruchu, który dodaje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8bca-131">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="b8bca-132">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="b8bca-132">-EndpointStatus</span></span>
<span data-ttu-id="b8bca-133">Określa stan punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="b8bca-133">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="b8bca-134">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="b8bca-134">Valid values are:</span></span> 

- <span data-ttu-id="b8bca-135">Włączone</span><span class="sxs-lookup"><span data-stu-id="b8bca-135">Enabled</span></span> 
- <span data-ttu-id="b8bca-136">Wyłączone</span><span class="sxs-lookup"><span data-stu-id="b8bca-136">Disabled</span></span> 

<span data-ttu-id="b8bca-137">Jeśli stan jest włączony, punkt końcowy jest prawdopodobny dla kondycji punktu końcowego i jest uwzględniany w metodzie routingu ruchu.</span><span class="sxs-lookup"><span data-stu-id="b8bca-137">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="b8bca-138">— GeoMapping</span><span class="sxs-lookup"><span data-stu-id="b8bca-138">-GeoMapping</span></span>
<span data-ttu-id="b8bca-139">Lista regionów zamapowanych na ten punkt końcowy podczas korzystania z metody routingu ruchu geograficznego.</span><span class="sxs-lookup"><span data-stu-id="b8bca-139">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="b8bca-140">Aby uzyskać pełną listę zaakceptowanych wartości, zapoznaj się z [dokumentacją menedżera ruchu.](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)</span><span class="sxs-lookup"><span data-stu-id="b8bca-140">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>

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

### <span data-ttu-id="b8bca-141">- MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="b8bca-141">-MinChildEndpoints</span></span>
<span data-ttu-id="b8bca-142">Minimalna liczba punktów końcowych, które muszą być dostępne w profilu podrzędnym, aby zagnieżdżony punkt końcowy w profilu nadrzędnym był uznawany za dostępny.</span><span class="sxs-lookup"><span data-stu-id="b8bca-142">The minimum number of endpoints that must be available in the child profile in order for the Nested Endpoint in the parent profile to be considered available.</span></span>
<span data-ttu-id="b8bca-143">Dotyczy tylko punktu końcowego typu "NestedEndpoints".</span><span class="sxs-lookup"><span data-stu-id="b8bca-143">Only applicable to endpoint of type 'NestedEndpoints'.</span></span>

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

### <span data-ttu-id="b8bca-144">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="b8bca-144">-Priority</span></span>
<span data-ttu-id="b8bca-145">Określa priorytet przypisywany przez Menedżera ruchu do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="b8bca-145">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="b8bca-146">Ten parametr jest używany tylko wtedy, gdy profil menedżera ruchu jest skonfigurowany przy użyciu metody routingu ruchu o priorytecie.</span><span class="sxs-lookup"><span data-stu-id="b8bca-146">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="b8bca-147">Prawidłowe wartości to liczby całkowite z od 1 do 1000.</span><span class="sxs-lookup"><span data-stu-id="b8bca-147">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="b8bca-148">Niższe wartości mają wyższy priorytet.</span><span class="sxs-lookup"><span data-stu-id="b8bca-148">Lower values represent higher priority.</span></span>

<span data-ttu-id="b8bca-149">Jeśli określisz priorytet, musisz określić priorytety dla wszystkich punktów końcowych w profilu, a dwa punkty końcowe nie mogą mieć tej samej wartości priorytetu.</span><span class="sxs-lookup"><span data-stu-id="b8bca-149">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="b8bca-150">Jeśli nie określisz priorytetów, menedżer ruchu przypisze domyślne wartości priorytetów do punktów końcowych, zaczynając od jednego (1) w kolejności, w których profil zawiera listę punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="b8bca-150">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="b8bca-151">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="b8bca-151">-SubnetMapping</span></span>
<span data-ttu-id="b8bca-152">Lista zakresów adresów lub podsieci zamapowanych na ten punkt końcowy podczas korzystania z metody routingu ruchu "Podsieci".</span><span class="sxs-lookup"><span data-stu-id="b8bca-152">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="b8bca-153">— element docelowy</span><span class="sxs-lookup"><span data-stu-id="b8bca-153">-Target</span></span>
<span data-ttu-id="b8bca-154">Określa w pełni kwalifikowaną nazwę DNS punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="b8bca-154">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="b8bca-155">Menedżer ruchu zwraca tę wartość w odpowiedziach DNS, gdy kieruje ruch do tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="b8bca-155">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="b8bca-156">Określ ten parametr tylko dla typu punktu końcowego ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="b8bca-156">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="b8bca-157">W przypadku innych typów punktów końcowych określ zamiast *tego parametr TargetResourceId.*</span><span class="sxs-lookup"><span data-stu-id="b8bca-157">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="b8bca-158">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b8bca-158">-TargetResourceId</span></span>
<span data-ttu-id="b8bca-159">Określa identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="b8bca-159">Specifies resource ID of the target.</span></span>
<span data-ttu-id="b8bca-160">Określ ten parametr tylko dla typów punktów końcowych AzureEndpoints i NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="b8bca-160">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="b8bca-161">W przypadku typu punktu końcowego ExternalEndpoints określ zamiast tego *parametr Target.*</span><span class="sxs-lookup"><span data-stu-id="b8bca-161">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="b8bca-162">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b8bca-162">-TrafficManagerProfile</span></span>
<span data-ttu-id="b8bca-163">Określa lokalny obiekt **TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="b8bca-163">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="b8bca-164">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="b8bca-164">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="b8bca-165">Aby uzyskać obiekt **TrafficManagerProfile,** użyj Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8bca-165">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8bca-166">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="b8bca-166">-Type</span></span>
<span data-ttu-id="b8bca-167">Określa typ punktu końcowego, który to polecenie cmdlet dodaje do profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="b8bca-167">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="b8bca-168">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="b8bca-168">Valid values are:</span></span> 

- <span data-ttu-id="b8bca-169">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="b8bca-169">AzureEndpoints</span></span>
- <span data-ttu-id="b8bca-170">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="b8bca-170">ExternalEndpoints</span></span>
- <span data-ttu-id="b8bca-171">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="b8bca-171">NestedEndpoints</span></span>

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

### <span data-ttu-id="b8bca-172">— Waga</span><span class="sxs-lookup"><span data-stu-id="b8bca-172">-Weight</span></span>
<span data-ttu-id="b8bca-173">Określa wagę przypisywaną przez Menedżera ruchu do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="b8bca-173">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="b8bca-174">Prawidłowe wartości to liczby całkowite z od 1 do 1000.</span><span class="sxs-lookup"><span data-stu-id="b8bca-174">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="b8bca-175">Wartość domyślna to jeden (1).</span><span class="sxs-lookup"><span data-stu-id="b8bca-175">The default value is one (1).</span></span>
<span data-ttu-id="b8bca-176">Ten parametr jest używany tylko wtedy, gdy profil menedżera ruchu jest skonfigurowany przy użyciu metody routingu ruchu ważonego.</span><span class="sxs-lookup"><span data-stu-id="b8bca-176">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="b8bca-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8bca-177">CommonParameters</span></span>
<span data-ttu-id="b8bca-178">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8bca-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8bca-179">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8bca-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8bca-180">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8bca-180">INPUTS</span></span>

### <span data-ttu-id="b8bca-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b8bca-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="b8bca-182">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8bca-182">OUTPUTS</span></span>

### <span data-ttu-id="b8bca-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b8bca-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="b8bca-184">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b8bca-184">NOTES</span></span>

## <span data-ttu-id="b8bca-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8bca-185">RELATED LINKS</span></span>

[<span data-ttu-id="b8bca-186">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b8bca-186">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="b8bca-187">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8bca-187">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="b8bca-188">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b8bca-188">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="b8bca-189">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b8bca-189">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


