---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9e0b8ee74ff89f4a5903df1c73dc7b289b0371c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225232"
---
# <span data-ttu-id="bf233-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf233-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="bf233-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf233-102">SYNOPSIS</span></span>
<span data-ttu-id="bf233-103">Tworzy punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="bf233-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="bf233-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf233-104">SYNTAX</span></span>

### <span data-ttu-id="bf233-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bf233-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf233-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf233-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf233-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bf233-107">DESCRIPTION</span></span>
<span data-ttu-id="bf233-108">Polecenie cmdlet **New-AzCdnEndpoint** umożliwia utworzenie punktu końcowego sieci dostarczania zawartości Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="bf233-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="bf233-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf233-109">EXAMPLES</span></span>

## <span data-ttu-id="bf233-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf233-110">PARAMETERS</span></span>

### <span data-ttu-id="bf233-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="bf233-111">-CdnProfile</span></span>
<span data-ttu-id="bf233-112">Określa obiekt profilu sieci CDN, do którego jest dodawany punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="bf233-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="bf233-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="bf233-114">Określa tablicę typów zawartości, które mają być kompresowane z węzła Edge do klienta.</span><span class="sxs-lookup"><span data-stu-id="bf233-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="bf233-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="bf233-116">Domyślna grupa pochodzenie.</span><span class="sxs-lookup"><span data-stu-id="bf233-116">The default origin group.</span></span>

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

### <span data-ttu-id="bf233-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf233-117">-DefaultProfile</span></span>
<span data-ttu-id="bf233-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bf233-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf233-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="bf233-119">-DeliveryPolicy</span></span>
<span data-ttu-id="bf233-120">Zasady dostarczania dla tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="bf233-120">The delivery policy for this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bf233-121">-EndpointName</span></span>
<span data-ttu-id="bf233-122">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="bf233-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="bf233-123">-Filtry</span><span class="sxs-lookup"><span data-stu-id="bf233-123">-GeoFilters</span></span>
<span data-ttu-id="bf233-124">Lista filtrów Geo, które dotyczą tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="bf233-124">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-125">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="bf233-125">-HttpPort</span></span>
<span data-ttu-id="bf233-126">Określa numer portu HTTP na serwerze źródłowym.</span><span class="sxs-lookup"><span data-stu-id="bf233-126">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-127">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="bf233-127">-HttpsPort</span></span>
<span data-ttu-id="bf233-128">Określa numer portu HTTPS na serwerze źródłowym.</span><span class="sxs-lookup"><span data-stu-id="bf233-128">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="bf233-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="bf233-130">Wskazuje, czy kompresja jest włączona dla punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="bf233-130">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="bf233-131">-IsHttpAllowed</span></span>
<span data-ttu-id="bf233-132">Wskazuje, czy punkt końcowy włącza ruch HTTP.</span><span class="sxs-lookup"><span data-stu-id="bf233-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="bf233-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="bf233-134">Wskazuje, czy punkt końcowy włącza ruch HTTPS.</span><span class="sxs-lookup"><span data-stu-id="bf233-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bf233-135">-Location</span></span>
<span data-ttu-id="bf233-136">Określa lokalizację zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="bf233-136">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-137">-Optymalizacja typu</span><span class="sxs-lookup"><span data-stu-id="bf233-137">-OptimizationType</span></span>
<span data-ttu-id="bf233-138">Określa dowolną optymalizację tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="bf233-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="bf233-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="bf233-139">-OriginGroupName</span></span>
<span data-ttu-id="bf233-140">Nazwa grupy źródłowej.</span><span class="sxs-lookup"><span data-stu-id="bf233-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="bf233-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="bf233-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="bf233-142">Liczba sekund między badaniami kondycji.</span><span class="sxs-lookup"><span data-stu-id="bf233-142">The number of seconds between health probes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="bf233-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="bf233-144">Ścieżka odnosząca się do pochodzenia, która jest używana do określania kondycji pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="bf233-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="bf233-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="bf233-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="bf233-146">Protokół używany do badania kondycji.</span><span class="sxs-lookup"><span data-stu-id="bf233-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="bf233-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="bf233-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="bf233-148">Typ żądania badania kondycji, które zostało wykonane.</span><span class="sxs-lookup"><span data-stu-id="bf233-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="bf233-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="bf233-149">-OriginHostHeader</span></span>
<span data-ttu-id="bf233-150">Określa początkową pozycję hosta punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="bf233-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="bf233-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="bf233-151">-OriginHostName</span></span>
<span data-ttu-id="bf233-152">Określa nazwę hosta serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="bf233-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="bf233-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="bf233-153">-OriginId</span></span>
<span data-ttu-id="bf233-154">Identyfikatory grup pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="bf233-154">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="bf233-155">-Originname</span><span class="sxs-lookup"><span data-stu-id="bf233-155">-OriginName</span></span>
<span data-ttu-id="bf233-156">Określa nazwę zasobu serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="bf233-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="bf233-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="bf233-157">-OriginPath</span></span>
<span data-ttu-id="bf233-158">Określa ścieżkę serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="bf233-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="bf233-159">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="bf233-159">-Priority</span></span>
<span data-ttu-id="bf233-160">Priorytet pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="bf233-160">Azure CDN origin priority.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="bf233-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="bf233-162">Niestandardowa wiadomość, która ma być uwzględniona w żądaniu zatwierdzenia w celu nawiązania połączenia z prywatnym linkiem.</span><span class="sxs-lookup"><span data-stu-id="bf233-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="bf233-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="bf233-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="bf233-164">Lokalizacja prywatnego łącza pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="bf233-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="bf233-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="bf233-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="bf233-166">Identyfikator zasobu prywatnego łącza pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="bf233-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="bf233-167">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="bf233-167">-ProbePath</span></span>
<span data-ttu-id="bf233-168">Określa ścieżkę sondy dla przyspieszania dynamicznego witryny</span><span class="sxs-lookup"><span data-stu-id="bf233-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="bf233-169">-Refilename</span><span class="sxs-lookup"><span data-stu-id="bf233-169">-ProfileName</span></span>
<span data-ttu-id="bf233-170">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="bf233-170">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="bf233-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="bf233-172">Określa zachowanie punktu końcowego sieci CDN, gdy ciąg zapytania znajduje się w adresie URL żądania.</span><span class="sxs-lookup"><span data-stu-id="bf233-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSQueryStringCachingBehavior]
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf233-173">-ResourceGroupName</span></span>
<span data-ttu-id="bf233-174">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="bf233-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="bf233-175">-Tag</span></span>
<span data-ttu-id="bf233-176">Znaczniki, które mają zostać skojarzone z punktem końcowym usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="bf233-176">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="bf233-177">-Waga</span><span class="sxs-lookup"><span data-stu-id="bf233-177">-Weight</span></span>
<span data-ttu-id="bf233-178">Waga pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="bf233-178">Azure CDN origin weight.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-179">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bf233-179">-Confirm</span></span>
<span data-ttu-id="bf233-180">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf233-180">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf233-181">-WhatIf</span></span>
<span data-ttu-id="bf233-182">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf233-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf233-183">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bf233-183">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf233-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf233-184">CommonParameters</span></span>
<span data-ttu-id="bf233-185">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf233-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf233-186">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf233-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf233-187">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf233-187">INPUTS</span></span>

### <span data-ttu-id="bf233-188">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="bf233-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="bf233-189">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf233-189">OUTPUTS</span></span>

### <span data-ttu-id="bf233-190">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf233-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="bf233-191">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf233-191">NOTES</span></span>

## <span data-ttu-id="bf233-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf233-192">RELATED LINKS</span></span>

[<span data-ttu-id="bf233-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf233-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="bf233-194">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf233-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="bf233-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf233-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="bf233-196">Start — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf233-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="bf233-197">Zatrzymaj — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf233-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


