---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: f2abe6acd0406f78ba2bb691b562cd0bcbffeb35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525477"
---
# <span data-ttu-id="11512-101">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="11512-101">Add-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="11512-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11512-102">SYNOPSIS</span></span>
<span data-ttu-id="11512-103">Dodaje punkt końcowy do obiektu profilu lokalnego zarządzania ruchem.</span><span class="sxs-lookup"><span data-stu-id="11512-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11512-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11512-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11512-105">Opis</span><span class="sxs-lookup"><span data-stu-id="11512-105">DESCRIPTION</span></span>
<span data-ttu-id="11512-106">Polecenie cmdlet **Add-AzureRmTrafficManagerEndpointConfig** umożliwia dodanie punktu końcowego do obiektu profilu lokalnego usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="11512-106">The **Add-AzureRmTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="11512-107">Możesz uzyskać profil przy użyciu New-AzureRmTrafficManagerProfile lub Get-AzureRmTrafficManagerProfile poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11512-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="11512-108">To polecenie cmdlet działa na obiekcie profilu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="11512-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="11512-109">Zatwierdź zmiany w profilu dla Menedżera ruchu, korzystając z polecenia cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="11512-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="11512-110">Aby utworzyć punkt końcowy i przekazać zmianę w ramach jednej operacji, użyj polecenia cmdlet New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="11512-110">To create an endpoint and commit the change in a single operation, use the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="11512-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11512-111">EXAMPLES</span></span>

### <span data-ttu-id="11512-112">Przykład 1. Dodawanie punktu końcowego do profilu</span><span class="sxs-lookup"><span data-stu-id="11512-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="11512-113">Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="11512-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="11512-114">Polecenie zapisuje profil lokalny w zmiennej $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="11512-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="11512-115">Drugie polecenie dodaje punkt końcowy o nazwie contoso do profilu przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="11512-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="11512-116">Polecenie uwzględnia dane konfiguracji punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="11512-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="11512-117">To polecenie powoduje zmianę tylko obiektu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="11512-117">This command changes only the local object.</span></span>

<span data-ttu-id="11512-118">Ostatnie polecenie aktualizuje profil usługi Traffic managera na platformie Azure, aby odpowiadał wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="11512-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="11512-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11512-119">PARAMETERS</span></span>

### <span data-ttu-id="11512-120">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="11512-120">-EndpointLocation</span></span>
<span data-ttu-id="11512-121">Określa lokalizację punktu końcowego, który ma być używany w metodzie routingu ruch wydajności.</span><span class="sxs-lookup"><span data-stu-id="11512-121">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="11512-122">Ten parametr dotyczy tylko punktów końcowych typu ExternalEndpoints lub NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="11512-122">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="11512-123">Ten parametr należy określić, gdy używana jest metoda routingu ruchowego wydajności.</span><span class="sxs-lookup"><span data-stu-id="11512-123">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="11512-124">Określ nazwę regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11512-124">Specify an Azure region name.</span></span>
<span data-ttu-id="11512-125">Aby uzyskać pełną listę regionów platformy Azure, zobacz regiony platformy Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="11512-125">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="11512-126">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="11512-126">-EndpointName</span></span>
<span data-ttu-id="11512-127">Określa nazwę punktu końcowego usługi Traffic Managera, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11512-127">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="11512-128">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="11512-128">-EndpointStatus</span></span>
<span data-ttu-id="11512-129">Określa stan punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="11512-129">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="11512-130">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="11512-130">Valid values are:</span></span> 

- <span data-ttu-id="11512-131">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="11512-131">Enabled</span></span> 
- <span data-ttu-id="11512-132">Łącza</span><span class="sxs-lookup"><span data-stu-id="11512-132">Disabled</span></span> 

<span data-ttu-id="11512-133">Jeśli stan jest włączony, punkt końcowy jest sondowany pod kątem kondycji punktu końcowego i jest włączony do metody routingu ruchu.</span><span class="sxs-lookup"><span data-stu-id="11512-133">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="11512-134">-Geomapowanie</span><span class="sxs-lookup"><span data-stu-id="11512-134">-GeoMapping</span></span>
<span data-ttu-id="11512-135">Lista regionów zamapowanych do tego punktu końcowego, gdy używana jest metoda routingu ruchu "geograficzny".</span><span class="sxs-lookup"><span data-stu-id="11512-135">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="11512-136">Aby uzyskać [pełną listę zaakceptowanych wartości](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions), zapoznaj się z dokumentacją w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="11512-136">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>
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

### <span data-ttu-id="11512-137">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="11512-137">-MinChildEndpoints</span></span>
<span data-ttu-id="11512-138">Określ nazwę regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11512-138">Specify an Azure region name.</span></span>
<span data-ttu-id="11512-139">Aby uzyskać pełną listę regionów platformy Azure, zobacz regiony platformy Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="11512-139">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="11512-140">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="11512-140">-Priority</span></span>
<span data-ttu-id="11512-141">Określa priorytet, który Menedżer ruchu przypisuje do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="11512-141">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="11512-142">Ten parametr jest wykorzystywany tylko w przypadku, gdy profil usługi Traffic Manager jest skonfigurowany za pomocą metody routingu ruchu w celu uzyskania priorytetu.</span><span class="sxs-lookup"><span data-stu-id="11512-142">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="11512-143">Prawidłowe wartości to liczby całkowite z zakresu od 1 do 1000.</span><span class="sxs-lookup"><span data-stu-id="11512-143">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="11512-144">Niższe wartości reprezentują wyższy priorytet.</span><span class="sxs-lookup"><span data-stu-id="11512-144">Lower values represent higher priority.</span></span>

<span data-ttu-id="11512-145">Jeśli określisz priorytet, musisz określić priorytety dla wszystkich punktów końcowych w profilu, a żadne dwa punkty końcowe nie mogą mieć tej samej wartości priorytetu.</span><span class="sxs-lookup"><span data-stu-id="11512-145">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="11512-146">Jeśli nie określono priorytetów, Menedżer ruchu przypisuje domyślne wartości priorytetu do punktów końcowych, rozpoczynając od jednej (1), w kolejności, w jakiej profil wyświetla punkty końcowe.</span><span class="sxs-lookup"><span data-stu-id="11512-146">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="11512-147">-Target</span><span class="sxs-lookup"><span data-stu-id="11512-147">-Target</span></span>
<span data-ttu-id="11512-148">Określa w pełni kwalifikowaną nazwę DNS punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="11512-148">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="11512-149">Usługa Traffic Manager zwraca tę wartość w odpowiedziach DNS, gdy kieruje ruch do tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="11512-149">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="11512-150">Ten parametr można określić tylko dla typu punktu końcowego ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="11512-150">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="11512-151">W przypadku innych typów punktów końcowych zamiast tego określ parametr *TargetResourceId* .</span><span class="sxs-lookup"><span data-stu-id="11512-151">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="11512-152">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="11512-152">-TargetResourceId</span></span>
<span data-ttu-id="11512-153">Określa identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="11512-153">Specifies resource ID of the target.</span></span>
<span data-ttu-id="11512-154">Ten parametr można określić tylko dla typów punktów końcowych AzureEndpoints i NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="11512-154">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="11512-155">W polu Typ punktu końcowego ExternalEndpoints określ parametr *Target* .</span><span class="sxs-lookup"><span data-stu-id="11512-155">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="11512-156">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11512-156">-TrafficManagerProfile</span></span>
<span data-ttu-id="11512-157">Określa lokalny obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="11512-157">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="11512-158">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="11512-158">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="11512-159">Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="11512-159">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="11512-160">-Type</span><span class="sxs-lookup"><span data-stu-id="11512-160">-Type</span></span>
<span data-ttu-id="11512-161">Określa typ punktu końcowego, który jest dodawany przez to polecenie cmdlet do profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="11512-161">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="11512-162">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="11512-162">Valid values are:</span></span> 

- <span data-ttu-id="11512-163">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="11512-163">AzureEndpoints</span></span>
- <span data-ttu-id="11512-164">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="11512-164">ExternalEndpoints</span></span>
- <span data-ttu-id="11512-165">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="11512-165">NestedEndpoints</span></span>

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

### <span data-ttu-id="11512-166">-Waga</span><span class="sxs-lookup"><span data-stu-id="11512-166">-Weight</span></span>
<span data-ttu-id="11512-167">Określa wagę, jaką Menedżer ruchu przypisuje do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="11512-167">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="11512-168">Prawidłowe wartości to liczby całkowite z zakresu od 1 do 1000.</span><span class="sxs-lookup"><span data-stu-id="11512-168">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="11512-169">Wartość domyślna to jeden (1).</span><span class="sxs-lookup"><span data-stu-id="11512-169">The default value is one (1).</span></span>
<span data-ttu-id="11512-170">Ten parametr jest wykorzystywany tylko wtedy, gdy profil usługi Traffic Manager jest skonfigurowany przy użyciu ważonej metody routingu ruchu.</span><span class="sxs-lookup"><span data-stu-id="11512-170">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="11512-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11512-171">-DefaultProfile</span></span>
<span data-ttu-id="11512-172">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11512-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11512-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11512-173">CommonParameters</span></span>
<span data-ttu-id="11512-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11512-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11512-175">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11512-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11512-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11512-176">INPUTS</span></span>

### <span data-ttu-id="11512-177">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11512-177">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="11512-178">To polecenie cmdlet akceptuje obiekt **TrafficManagerProfile** do tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11512-178">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="11512-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11512-179">OUTPUTS</span></span>

### <span data-ttu-id="11512-180">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11512-180">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="11512-181">To polecenie cmdlet zwraca zmodyfikowany obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="11512-181">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="11512-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11512-182">NOTES</span></span>

## <span data-ttu-id="11512-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11512-183">RELATED LINKS</span></span>

[<span data-ttu-id="11512-184">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11512-184">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="11512-185">Nowe — AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="11512-185">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="11512-186">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="11512-186">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="11512-187">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11512-187">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


