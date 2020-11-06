---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: e9e6817d9a290acf1e91067edfd90cdf8081f1f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549504"
---
# <span data-ttu-id="87af1-101">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="87af1-101">Add-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="87af1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87af1-102">SYNOPSIS</span></span>
<span data-ttu-id="87af1-103">Dodaje punkt końcowy do obiektu profilu lokalnego zarządzania ruchem.</span><span class="sxs-lookup"><span data-stu-id="87af1-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87af1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87af1-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87af1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="87af1-105">DESCRIPTION</span></span>
<span data-ttu-id="87af1-106">Polecenie cmdlet **Add-AzureRmTrafficManagerEndpointConfig** umożliwia dodanie punktu końcowego do obiektu profilu lokalnego usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="87af1-106">The **Add-AzureRmTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="87af1-107">Możesz uzyskać profil przy użyciu New-AzureRmTrafficManagerProfile lub Get-AzureRmTrafficManagerProfile poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87af1-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="87af1-108">To polecenie cmdlet działa na obiekcie profilu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="87af1-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="87af1-109">Zatwierdź zmiany w profilu dla Menedżera ruchu, korzystając z polecenia cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="87af1-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="87af1-110">Aby utworzyć punkt końcowy i przekazać zmianę w ramach jednej operacji, użyj polecenia cmdlet New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="87af1-110">To create an endpoint and commit the change in a single operation, use the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="87af1-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87af1-111">EXAMPLES</span></span>

### <span data-ttu-id="87af1-112">Przykład 1. Dodawanie punktu końcowego do profilu</span><span class="sxs-lookup"><span data-stu-id="87af1-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="87af1-113">Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="87af1-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="87af1-114">Polecenie zapisuje profil lokalny w zmiennej $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="87af1-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="87af1-115">Drugie polecenie dodaje punkt końcowy o nazwie contoso do profilu przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="87af1-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="87af1-116">Polecenie uwzględnia dane konfiguracji punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="87af1-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="87af1-117">To polecenie powoduje zmianę tylko obiektu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="87af1-117">This command changes only the local object.</span></span>

<span data-ttu-id="87af1-118">Ostatnie polecenie aktualizuje profil usługi Traffic managera na platformie Azure, aby odpowiadał wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="87af1-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="87af1-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87af1-119">PARAMETERS</span></span>

### <span data-ttu-id="87af1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87af1-120">-DefaultProfile</span></span>
<span data-ttu-id="87af1-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87af1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87af1-122">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="87af1-122">-EndpointLocation</span></span>
<span data-ttu-id="87af1-123">Określa lokalizację punktu końcowego, który ma być używany w metodzie routingu ruch wydajności.</span><span class="sxs-lookup"><span data-stu-id="87af1-123">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="87af1-124">Ten parametr dotyczy tylko punktów końcowych typu ExternalEndpoints lub NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="87af1-124">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="87af1-125">Ten parametr należy określić, gdy używana jest metoda routingu ruchowego wydajności.</span><span class="sxs-lookup"><span data-stu-id="87af1-125">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="87af1-126">Określ nazwę regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="87af1-126">Specify an Azure region name.</span></span>
<span data-ttu-id="87af1-127">Aby uzyskać pełną listę regionów platformy Azure, zobacz regiony platformy Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="87af1-127">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87af1-128">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="87af1-128">-EndpointName</span></span>
<span data-ttu-id="87af1-129">Określa nazwę punktu końcowego usługi Traffic Managera, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87af1-129">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87af1-130">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="87af1-130">-EndpointStatus</span></span>
<span data-ttu-id="87af1-131">Określa stan punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="87af1-131">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="87af1-132">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="87af1-132">Valid values are:</span></span> 

- <span data-ttu-id="87af1-133">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="87af1-133">Enabled</span></span> 
- <span data-ttu-id="87af1-134">Łącza</span><span class="sxs-lookup"><span data-stu-id="87af1-134">Disabled</span></span> 

<span data-ttu-id="87af1-135">Jeśli stan jest włączony, punkt końcowy jest sondowany pod kątem kondycji punktu końcowego i jest włączony do metody routingu ruchu.</span><span class="sxs-lookup"><span data-stu-id="87af1-135">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87af1-136">-Geomapowanie</span><span class="sxs-lookup"><span data-stu-id="87af1-136">-GeoMapping</span></span>
<span data-ttu-id="87af1-137">Lista regionów zamapowanych do tego punktu końcowego, gdy używana jest metoda routingu ruchu "geograficzny".</span><span class="sxs-lookup"><span data-stu-id="87af1-137">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="87af1-138">Aby uzyskać [pełną listę zaakceptowanych wartości](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions), zapoznaj się z dokumentacją w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="87af1-138">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>
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

### <span data-ttu-id="87af1-139">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="87af1-139">-MinChildEndpoints</span></span>
<span data-ttu-id="87af1-140">Określ nazwę regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="87af1-140">Specify an Azure region name.</span></span>
<span data-ttu-id="87af1-141">Aby uzyskać pełną listę regionów platformy Azure, zobacz regiony platformy Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="87af1-141">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87af1-142">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="87af1-142">-Priority</span></span>
<span data-ttu-id="87af1-143">Określa priorytet, który Menedżer ruchu przypisuje do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="87af1-143">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="87af1-144">Ten parametr jest wykorzystywany tylko w przypadku, gdy profil usługi Traffic Manager jest skonfigurowany za pomocą metody routingu ruchu w celu uzyskania priorytetu.</span><span class="sxs-lookup"><span data-stu-id="87af1-144">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="87af1-145">Prawidłowe wartości to liczby całkowite z zakresu od 1 do 1000.</span><span class="sxs-lookup"><span data-stu-id="87af1-145">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="87af1-146">Niższe wartości reprezentują wyższy priorytet.</span><span class="sxs-lookup"><span data-stu-id="87af1-146">Lower values represent higher priority.</span></span>

<span data-ttu-id="87af1-147">Jeśli określisz priorytet, musisz określić priorytety dla wszystkich punktów końcowych w profilu, a żadne dwa punkty końcowe nie mogą mieć tej samej wartości priorytetu.</span><span class="sxs-lookup"><span data-stu-id="87af1-147">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="87af1-148">Jeśli nie określono priorytetów, Menedżer ruchu przypisuje domyślne wartości priorytetu do punktów końcowych, rozpoczynając od jednej (1), w kolejności, w jakiej profil wyświetla punkty końcowe.</span><span class="sxs-lookup"><span data-stu-id="87af1-148">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87af1-149">-Target</span><span class="sxs-lookup"><span data-stu-id="87af1-149">-Target</span></span>
<span data-ttu-id="87af1-150">Określa w pełni kwalifikowaną nazwę DNS punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="87af1-150">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="87af1-151">Usługa Traffic Manager zwraca tę wartość w odpowiedziach DNS, gdy kieruje ruch do tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="87af1-151">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="87af1-152">Ten parametr można określić tylko dla typu punktu końcowego ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="87af1-152">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="87af1-153">W przypadku innych typów punktów końcowych zamiast tego określ parametr *TargetResourceId* .</span><span class="sxs-lookup"><span data-stu-id="87af1-153">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87af1-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="87af1-154">-TargetResourceId</span></span>
<span data-ttu-id="87af1-155">Określa identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="87af1-155">Specifies resource ID of the target.</span></span>
<span data-ttu-id="87af1-156">Ten parametr można określić tylko dla typów punktów końcowych AzureEndpoints i NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="87af1-156">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="87af1-157">W polu Typ punktu końcowego ExternalEndpoints określ parametr *Target* .</span><span class="sxs-lookup"><span data-stu-id="87af1-157">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87af1-158">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="87af1-158">-TrafficManagerProfile</span></span>
<span data-ttu-id="87af1-159">Określa lokalny obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="87af1-159">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="87af1-160">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="87af1-160">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="87af1-161">Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="87af1-161">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87af1-162">-Type</span><span class="sxs-lookup"><span data-stu-id="87af1-162">-Type</span></span>
<span data-ttu-id="87af1-163">Określa typ punktu końcowego, który jest dodawany przez to polecenie cmdlet do profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="87af1-163">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="87af1-164">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="87af1-164">Valid values are:</span></span> 

- <span data-ttu-id="87af1-165">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="87af1-165">AzureEndpoints</span></span>
- <span data-ttu-id="87af1-166">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="87af1-166">ExternalEndpoints</span></span>
- <span data-ttu-id="87af1-167">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="87af1-167">NestedEndpoints</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87af1-168">-Waga</span><span class="sxs-lookup"><span data-stu-id="87af1-168">-Weight</span></span>
<span data-ttu-id="87af1-169">Określa wagę, jaką Menedżer ruchu przypisuje do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="87af1-169">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="87af1-170">Prawidłowe wartości to liczby całkowite z zakresu od 1 do 1000.</span><span class="sxs-lookup"><span data-stu-id="87af1-170">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="87af1-171">Wartość domyślna to jeden (1).</span><span class="sxs-lookup"><span data-stu-id="87af1-171">The default value is one (1).</span></span>
<span data-ttu-id="87af1-172">Ten parametr jest wykorzystywany tylko wtedy, gdy profil usługi Traffic Manager jest skonfigurowany przy użyciu ważonej metody routingu ruchu.</span><span class="sxs-lookup"><span data-stu-id="87af1-172">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87af1-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87af1-173">CommonParameters</span></span>
<span data-ttu-id="87af1-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87af1-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87af1-175">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87af1-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87af1-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87af1-176">INPUTS</span></span>

### <span data-ttu-id="87af1-177">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="87af1-177">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="87af1-178">To polecenie cmdlet akceptuje obiekt **TrafficManagerProfile** do tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87af1-178">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="87af1-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87af1-179">OUTPUTS</span></span>

### <span data-ttu-id="87af1-180">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="87af1-180">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="87af1-181">To polecenie cmdlet zwraca zmodyfikowany obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="87af1-181">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="87af1-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87af1-182">NOTES</span></span>

## <span data-ttu-id="87af1-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87af1-183">RELATED LINKS</span></span>

[<span data-ttu-id="87af1-184">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="87af1-184">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="87af1-185">Nowe — AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="87af1-185">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="87af1-186">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="87af1-186">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="87af1-187">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="87af1-187">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


