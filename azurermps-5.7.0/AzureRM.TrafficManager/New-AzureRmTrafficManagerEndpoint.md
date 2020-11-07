---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 6117bbae035653762d99096eb8735885c0554d0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717671"
---
# <span data-ttu-id="769d2-101">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="769d2-101">New-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="769d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="769d2-102">SYNOPSIS</span></span>
<span data-ttu-id="769d2-103">Tworzy punkt końcowy w profilu w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="769d2-103">Creates an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="769d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="769d2-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="769d2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="769d2-105">DESCRIPTION</span></span>
<span data-ttu-id="769d2-106">Polecenie cmdlet **New-AzureRmTrafficManagerEndpoint** tworzy punkt końcowy w profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="769d2-106">The **New-AzureRmTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="769d2-107">To polecenie cmdlet umożliwia przekazanie każdego nowego punktu końcowego do usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="769d2-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="769d2-108">Aby dodać wiele punktów końcowych do obiektu profilu lokalnego Menedżera ruchu i przekazać zmiany w ramach jednej operacji, użyj polecenia cmdlet Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="769d2-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="769d2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="769d2-109">EXAMPLES</span></span>

### <span data-ttu-id="769d2-110">Przykład 1. Tworzenie zewnętrznego punktu końcowego dla profilu</span><span class="sxs-lookup"><span data-stu-id="769d2-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="769d2-111">To polecenie powoduje utworzenie zewnętrznego punktu końcowego o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="769d2-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="769d2-112">Przykład 2: Tworzenie punktu końcowego Azure dla profilu</span><span class="sxs-lookup"><span data-stu-id="769d2-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="769d2-113">To polecenie tworzy punkt końcowy Azure o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasób ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="769d2-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="769d2-114">Punkt końcowy platformy Azure wskazuje aplikację Azure Web App, której identyfikator Menedżera zasobów Azure jest określony przez ścieżkę URI w *TargetResourceId*.</span><span class="sxs-lookup"><span data-stu-id="769d2-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="769d2-115">Polecenie nie określa parametru *EndpointLocation* , ponieważ zasób aplikacji sieci Web udostępnia lokalizację.</span><span class="sxs-lookup"><span data-stu-id="769d2-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="769d2-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="769d2-116">PARAMETERS</span></span>

### <span data-ttu-id="769d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="769d2-117">-DefaultProfile</span></span>
<span data-ttu-id="769d2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="769d2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="769d2-119">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="769d2-119">-EndpointLocation</span></span>
<span data-ttu-id="769d2-120">Określa lokalizację punktu końcowego, który ma być używany w metodzie routingu ruch wydajności.</span><span class="sxs-lookup"><span data-stu-id="769d2-120">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="769d2-121">Ten parametr dotyczy tylko punktów końcowych typu ExternalEndpoints lub NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="769d2-121">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="769d2-122">Ten parametr należy określić, gdy używana jest metoda routingu ruchowego wydajności.</span><span class="sxs-lookup"><span data-stu-id="769d2-122">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="769d2-123">Określ nazwę regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="769d2-123">Specify an Azure region name.</span></span>
<span data-ttu-id="769d2-124">Aby uzyskać pełną listę regionów platformy Azure, zobacz regiony platformy Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="769d2-124">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="769d2-125">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="769d2-125">-EndpointStatus</span></span>
<span data-ttu-id="769d2-126">Określa stan punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="769d2-126">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="769d2-127">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="769d2-127">Valid values are:</span></span> 

- <span data-ttu-id="769d2-128">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="769d2-128">Enabled</span></span> 
- <span data-ttu-id="769d2-129">Łącza</span><span class="sxs-lookup"><span data-stu-id="769d2-129">Disabled</span></span> 

<span data-ttu-id="769d2-130">Jeśli stan jest włączony, punkt końcowy jest sondowany pod kątem kondycji punktu końcowego i jest włączony do metody routingu ruchu.</span><span class="sxs-lookup"><span data-stu-id="769d2-130">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="769d2-131">-Geomapowanie</span><span class="sxs-lookup"><span data-stu-id="769d2-131">-GeoMapping</span></span>
<span data-ttu-id="769d2-132">Lista regionów zamapowanych do tego punktu końcowego, gdy używana jest metoda routingu ruchu "geograficzny".</span><span class="sxs-lookup"><span data-stu-id="769d2-132">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="769d2-133">Aby uzyskać pełną listę zaakceptowanych wartości, zapoznaj się z dokumentacją w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="769d2-133">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>
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

### <span data-ttu-id="769d2-134">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="769d2-134">-MinChildEndpoints</span></span>
<span data-ttu-id="769d2-135">Określ nazwę regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="769d2-135">Specify an Azure region name.</span></span>
<span data-ttu-id="769d2-136">Aby uzyskać pełną listę regionów platformy Azure, zobacz regiony platformy Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="769d2-136">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="769d2-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="769d2-137">-Name</span></span>
<span data-ttu-id="769d2-138">Określa nazwę punktu końcowego usługi Traffic Managera, który jest tworzony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="769d2-138">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="769d2-139">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="769d2-139">-Priority</span></span>
<span data-ttu-id="769d2-140">Określa priorytet, który Menedżer ruchu przypisuje do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="769d2-140">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="769d2-141">Ten parametr jest wykorzystywany tylko w przypadku, gdy profil usługi Traffic Manager jest skonfigurowany za pomocą metody routingu ruchu w celu uzyskania priorytetu.</span><span class="sxs-lookup"><span data-stu-id="769d2-141">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="769d2-142">Prawidłowe wartości to liczby całkowite z zakresu od 1 do 1000.</span><span class="sxs-lookup"><span data-stu-id="769d2-142">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="769d2-143">Niższe wartości reprezentują wyższy priorytet.</span><span class="sxs-lookup"><span data-stu-id="769d2-143">Lower values represent higher priority.</span></span>

<span data-ttu-id="769d2-144">Jeśli określisz priorytet, musisz określić priorytety dla wszystkich punktów końcowych w profilu, a żadne dwa punkty końcowe nie mogą mieć tej samej wartości priorytetu.</span><span class="sxs-lookup"><span data-stu-id="769d2-144">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="769d2-145">Jeśli nie określono priorytetów, Menedżer ruchu przypisuje domyślne wartości priorytetu do punktów końcowych, rozpoczynając od jednej (1), w kolejności, w jakiej profil wyświetla punkty końcowe.</span><span class="sxs-lookup"><span data-stu-id="769d2-145">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="769d2-146">-Refilename</span><span class="sxs-lookup"><span data-stu-id="769d2-146">-ProfileName</span></span>
<span data-ttu-id="769d2-147">Określa nazwę profilu usługi Traffic Manager, do którego to polecenie cmdlet dodaje punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="769d2-147">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="769d2-148">Aby uzyskać profil, Użyj poleceń cmdlet New-AzureRmTrafficManagerProfile lub Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="769d2-148">To obtain a profile, use the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="769d2-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="769d2-149">-ResourceGroupName</span></span>
<span data-ttu-id="769d2-150">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="769d2-150">Specifies the name of a resource group.</span></span>
<span data-ttu-id="769d2-151">To polecenie cmdlet powoduje utworzenie punktu końcowego zarządzania ruchem w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="769d2-151">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="769d2-152">-Target</span><span class="sxs-lookup"><span data-stu-id="769d2-152">-Target</span></span>
<span data-ttu-id="769d2-153">Określa w pełni kwalifikowaną nazwę DNS punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="769d2-153">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="769d2-154">Usługa Traffic Manager zwraca tę wartość w odpowiedziach DNS, gdy kieruje ruch do tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="769d2-154">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="769d2-155">Ten parametr można określić tylko dla typu punktu końcowego ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="769d2-155">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="769d2-156">W przypadku innych typów punktów końcowych zamiast tego określ parametr *TargetResourceId* .</span><span class="sxs-lookup"><span data-stu-id="769d2-156">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="769d2-157">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="769d2-157">-TargetResourceId</span></span>
<span data-ttu-id="769d2-158">Określa identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="769d2-158">Specifies resource ID of the target.</span></span>
<span data-ttu-id="769d2-159">Ten parametr można określić tylko dla typów punktów końcowych AzureEndpoints i NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="769d2-159">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="769d2-160">W polu Typ punktu końcowego ExternalEndpoints określ parametr *Target* .</span><span class="sxs-lookup"><span data-stu-id="769d2-160">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="769d2-161">-Type</span><span class="sxs-lookup"><span data-stu-id="769d2-161">-Type</span></span>
<span data-ttu-id="769d2-162">Określa typ punktu końcowego, który jest dodawany przez to polecenie cmdlet do profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="769d2-162">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="769d2-163">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="769d2-163">Valid values are:</span></span> 

- <span data-ttu-id="769d2-164">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="769d2-164">AzureEndpoints</span></span>
- <span data-ttu-id="769d2-165">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="769d2-165">ExternalEndpoints</span></span>
- <span data-ttu-id="769d2-166">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="769d2-166">NestedEndpoints</span></span>

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

### <span data-ttu-id="769d2-167">-Waga</span><span class="sxs-lookup"><span data-stu-id="769d2-167">-Weight</span></span>
<span data-ttu-id="769d2-168">Określa wagę, jaką Menedżer ruchu przypisuje do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="769d2-168">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="769d2-169">Prawidłowe wartości to liczby całkowite z zakresu od 1 do 1000.</span><span class="sxs-lookup"><span data-stu-id="769d2-169">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="769d2-170">Wartość domyślna to jeden (1).</span><span class="sxs-lookup"><span data-stu-id="769d2-170">The default value is one (1).</span></span>
<span data-ttu-id="769d2-171">Ten parametr jest wykorzystywany tylko wtedy, gdy profil usługi Traffic Manager jest skonfigurowany przy użyciu ważonej metody routingu ruchu.</span><span class="sxs-lookup"><span data-stu-id="769d2-171">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="769d2-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="769d2-172">CommonParameters</span></span>
<span data-ttu-id="769d2-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="769d2-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="769d2-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="769d2-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="769d2-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="769d2-175">INPUTS</span></span>

### <span data-ttu-id="769d2-176">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="769d2-176">None</span></span>
<span data-ttu-id="769d2-177">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="769d2-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="769d2-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="769d2-178">OUTPUTS</span></span>

### <span data-ttu-id="769d2-179">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="769d2-179">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="769d2-180">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="769d2-180">NOTES</span></span>

## <span data-ttu-id="769d2-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="769d2-181">RELATED LINKS</span></span>

[<span data-ttu-id="769d2-182">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="769d2-182">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="769d2-183">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="769d2-183">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="769d2-184">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="769d2-184">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="769d2-185">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="769d2-185">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="769d2-186">Nowe — AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="769d2-186">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="769d2-187">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="769d2-187">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="769d2-188">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="769d2-188">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


