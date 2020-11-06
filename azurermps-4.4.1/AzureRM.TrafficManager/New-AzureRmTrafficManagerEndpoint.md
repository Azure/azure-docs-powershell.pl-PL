---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 7eaadd8c80fff6491983a3e1d9c750227eba43cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525470"
---
# <span data-ttu-id="40788-101">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="40788-101">New-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="40788-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40788-102">SYNOPSIS</span></span>
<span data-ttu-id="40788-103">Tworzy punkt końcowy w profilu w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="40788-103">Creates an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40788-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40788-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40788-105">Opis</span><span class="sxs-lookup"><span data-stu-id="40788-105">DESCRIPTION</span></span>
<span data-ttu-id="40788-106">Polecenie cmdlet **New-AzureRmTrafficManagerEndpoint** tworzy punkt końcowy w profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="40788-106">The **New-AzureRmTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="40788-107">To polecenie cmdlet umożliwia przekazanie każdego nowego punktu końcowego do usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="40788-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="40788-108">Aby dodać wiele punktów końcowych do obiektu profilu lokalnego Menedżera ruchu i przekazać zmiany w ramach jednej operacji, użyj polecenia cmdlet Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="40788-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="40788-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40788-109">EXAMPLES</span></span>

### <span data-ttu-id="40788-110">Przykład 1. Tworzenie zewnętrznego punktu końcowego dla profilu</span><span class="sxs-lookup"><span data-stu-id="40788-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="40788-111">To polecenie powoduje utworzenie zewnętrznego punktu końcowego o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="40788-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="40788-112">Przykład 2: Tworzenie punktu końcowego Azure dla profilu</span><span class="sxs-lookup"><span data-stu-id="40788-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="40788-113">To polecenie tworzy punkt końcowy Azure o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasób ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="40788-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="40788-114">Punkt końcowy platformy Azure wskazuje aplikację Azure Web App, której identyfikator Menedżera zasobów Azure jest określony przez ścieżkę URI w *TargetResourceId*.</span><span class="sxs-lookup"><span data-stu-id="40788-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="40788-115">Polecenie nie określa parametru *EndpointLocation* , ponieważ zasób aplikacji sieci Web udostępnia lokalizację.</span><span class="sxs-lookup"><span data-stu-id="40788-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="40788-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40788-116">PARAMETERS</span></span>

### <span data-ttu-id="40788-117">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="40788-117">-EndpointLocation</span></span>
<span data-ttu-id="40788-118">Określa lokalizację punktu końcowego, który ma być używany w metodzie routingu ruch wydajności.</span><span class="sxs-lookup"><span data-stu-id="40788-118">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="40788-119">Ten parametr dotyczy tylko punktów końcowych typu ExternalEndpoints lub NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="40788-119">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="40788-120">Ten parametr należy określić, gdy używana jest metoda routingu ruchowego wydajności.</span><span class="sxs-lookup"><span data-stu-id="40788-120">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="40788-121">Określ nazwę regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="40788-121">Specify an Azure region name.</span></span>
<span data-ttu-id="40788-122">Aby uzyskać pełną listę regionów platformy Azure, zobacz regiony platformy Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="40788-122">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="40788-123">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="40788-123">-EndpointStatus</span></span>
<span data-ttu-id="40788-124">Określa stan punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="40788-124">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="40788-125">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="40788-125">Valid values are:</span></span> 

- <span data-ttu-id="40788-126">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="40788-126">Enabled</span></span> 
- <span data-ttu-id="40788-127">Łącza</span><span class="sxs-lookup"><span data-stu-id="40788-127">Disabled</span></span> 

<span data-ttu-id="40788-128">Jeśli stan jest włączony, punkt końcowy jest sondowany pod kątem kondycji punktu końcowego i jest włączony do metody routingu ruchu.</span><span class="sxs-lookup"><span data-stu-id="40788-128">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="40788-129">-Geomapowanie</span><span class="sxs-lookup"><span data-stu-id="40788-129">-GeoMapping</span></span>
<span data-ttu-id="40788-130">Lista regionów zamapowanych do tego punktu końcowego, gdy używana jest metoda routingu ruchu "geograficzny".</span><span class="sxs-lookup"><span data-stu-id="40788-130">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="40788-131">Aby uzyskać pełną listę zaakceptowanych wartości, zapoznaj się z dokumentacją w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="40788-131">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>
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

### <span data-ttu-id="40788-132">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="40788-132">-MinChildEndpoints</span></span>
<span data-ttu-id="40788-133">Określ nazwę regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="40788-133">Specify an Azure region name.</span></span>
<span data-ttu-id="40788-134">Aby uzyskać pełną listę regionów platformy Azure, zobacz regiony platformy Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="40788-134">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="40788-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="40788-135">-Name</span></span>
<span data-ttu-id="40788-136">Określa nazwę punktu końcowego usługi Traffic Managera, który jest tworzony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40788-136">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="40788-137">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="40788-137">-Priority</span></span>
<span data-ttu-id="40788-138">Określa priorytet, który Menedżer ruchu przypisuje do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="40788-138">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="40788-139">Ten parametr jest wykorzystywany tylko w przypadku, gdy profil usługi Traffic Manager jest skonfigurowany za pomocą metody routingu ruchu w celu uzyskania priorytetu.</span><span class="sxs-lookup"><span data-stu-id="40788-139">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="40788-140">Prawidłowe wartości to liczby całkowite z zakresu od 1 do 1000.</span><span class="sxs-lookup"><span data-stu-id="40788-140">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="40788-141">Niższe wartości reprezentują wyższy priorytet.</span><span class="sxs-lookup"><span data-stu-id="40788-141">Lower values represent higher priority.</span></span>

<span data-ttu-id="40788-142">Jeśli określisz priorytet, musisz określić priorytety dla wszystkich punktów końcowych w profilu, a żadne dwa punkty końcowe nie mogą mieć tej samej wartości priorytetu.</span><span class="sxs-lookup"><span data-stu-id="40788-142">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="40788-143">Jeśli nie określono priorytetów, Menedżer ruchu przypisuje domyślne wartości priorytetu do punktów końcowych, rozpoczynając od jednej (1), w kolejności, w jakiej profil wyświetla punkty końcowe.</span><span class="sxs-lookup"><span data-stu-id="40788-143">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="40788-144">-Refilename</span><span class="sxs-lookup"><span data-stu-id="40788-144">-ProfileName</span></span>
<span data-ttu-id="40788-145">Określa nazwę profilu usługi Traffic Manager, do którego to polecenie cmdlet dodaje punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="40788-145">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="40788-146">Aby uzyskać profil, Użyj poleceń cmdlet New-AzureRmTrafficManagerProfile lub Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="40788-146">To obtain a profile, use the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="40788-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40788-147">-ResourceGroupName</span></span>
<span data-ttu-id="40788-148">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="40788-148">Specifies the name of a resource group.</span></span>
<span data-ttu-id="40788-149">To polecenie cmdlet powoduje utworzenie punktu końcowego zarządzania ruchem w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="40788-149">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="40788-150">-Target</span><span class="sxs-lookup"><span data-stu-id="40788-150">-Target</span></span>
<span data-ttu-id="40788-151">Określa w pełni kwalifikowaną nazwę DNS punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="40788-151">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="40788-152">Usługa Traffic Manager zwraca tę wartość w odpowiedziach DNS, gdy kieruje ruch do tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="40788-152">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="40788-153">Ten parametr można określić tylko dla typu punktu końcowego ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="40788-153">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="40788-154">W przypadku innych typów punktów końcowych zamiast tego określ parametr *TargetResourceId* .</span><span class="sxs-lookup"><span data-stu-id="40788-154">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="40788-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="40788-155">-TargetResourceId</span></span>
<span data-ttu-id="40788-156">Określa identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="40788-156">Specifies resource ID of the target.</span></span>
<span data-ttu-id="40788-157">Ten parametr można określić tylko dla typów punktów końcowych AzureEndpoints i NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="40788-157">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="40788-158">W polu Typ punktu końcowego ExternalEndpoints określ parametr *Target* .</span><span class="sxs-lookup"><span data-stu-id="40788-158">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="40788-159">-Type</span><span class="sxs-lookup"><span data-stu-id="40788-159">-Type</span></span>
<span data-ttu-id="40788-160">Określa typ punktu końcowego, który jest dodawany przez to polecenie cmdlet do profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="40788-160">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="40788-161">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="40788-161">Valid values are:</span></span> 

- <span data-ttu-id="40788-162">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="40788-162">AzureEndpoints</span></span>
- <span data-ttu-id="40788-163">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="40788-163">ExternalEndpoints</span></span>
- <span data-ttu-id="40788-164">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="40788-164">NestedEndpoints</span></span>

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

### <span data-ttu-id="40788-165">-Waga</span><span class="sxs-lookup"><span data-stu-id="40788-165">-Weight</span></span>
<span data-ttu-id="40788-166">Określa wagę, jaką Menedżer ruchu przypisuje do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="40788-166">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="40788-167">Prawidłowe wartości to liczby całkowite z zakresu od 1 do 1000.</span><span class="sxs-lookup"><span data-stu-id="40788-167">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="40788-168">Wartość domyślna to jeden (1).</span><span class="sxs-lookup"><span data-stu-id="40788-168">The default value is one (1).</span></span>
<span data-ttu-id="40788-169">Ten parametr jest wykorzystywany tylko wtedy, gdy profil usługi Traffic Manager jest skonfigurowany przy użyciu ważonej metody routingu ruchu.</span><span class="sxs-lookup"><span data-stu-id="40788-169">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="40788-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40788-170">-DefaultProfile</span></span>
<span data-ttu-id="40788-171">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40788-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40788-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40788-172">CommonParameters</span></span>
<span data-ttu-id="40788-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40788-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40788-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40788-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40788-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40788-175">INPUTS</span></span>

## <span data-ttu-id="40788-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40788-176">OUTPUTS</span></span>

### <span data-ttu-id="40788-177">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="40788-177">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="40788-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40788-178">NOTES</span></span>

## <span data-ttu-id="40788-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40788-179">RELATED LINKS</span></span>

[<span data-ttu-id="40788-180">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="40788-180">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="40788-181">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="40788-181">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="40788-182">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="40788-182">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="40788-183">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="40788-183">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="40788-184">Nowe — AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="40788-184">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="40788-185">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="40788-185">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="40788-186">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="40788-186">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


