---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9e0b8ee74ff89f4a5903df1c73dc7b289b0371c4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504196"
---
# <span data-ttu-id="35ca5-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="35ca5-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="35ca5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="35ca5-103">Tworzy punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="35ca5-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="35ca5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35ca5-104">SYNTAX</span></span>

### <span data-ttu-id="35ca5-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="35ca5-105">ByFieldsParameterSet (Default)</span></span>
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

### <span data-ttu-id="35ca5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35ca5-106">ByObjectParameterSet</span></span>
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

## <span data-ttu-id="35ca5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="35ca5-107">DESCRIPTION</span></span>
<span data-ttu-id="35ca5-108">Polecenie cmdlet **New-AzCdnEndpoint** umożliwia utworzenie punktu końcowego sieci dostarczania zawartości Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="35ca5-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="35ca5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35ca5-109">EXAMPLES</span></span>

## <span data-ttu-id="35ca5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35ca5-110">PARAMETERS</span></span>

### <span data-ttu-id="35ca5-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="35ca5-111">-CdnProfile</span></span>
<span data-ttu-id="35ca5-112">Określa obiekt profilu sieci CDN, do którego jest dodawany punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="35ca5-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="35ca5-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="35ca5-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="35ca5-114">Określa tablicę typów zawartości, które mają być kompresowane z węzła Edge do klienta.</span><span class="sxs-lookup"><span data-stu-id="35ca5-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="35ca5-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="35ca5-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="35ca5-116">Domyślna grupa pochodzenie.</span><span class="sxs-lookup"><span data-stu-id="35ca5-116">The default origin group.</span></span>

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

### <span data-ttu-id="35ca5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ca5-117">-DefaultProfile</span></span>
<span data-ttu-id="35ca5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="35ca5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35ca5-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="35ca5-119">-DeliveryPolicy</span></span>
<span data-ttu-id="35ca5-120">Zasady dostarczania dla tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="35ca5-120">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="35ca5-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="35ca5-121">-EndpointName</span></span>
<span data-ttu-id="35ca5-122">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="35ca5-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="35ca5-123">-Filtry</span><span class="sxs-lookup"><span data-stu-id="35ca5-123">-GeoFilters</span></span>
<span data-ttu-id="35ca5-124">Lista filtrów Geo, które dotyczą tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="35ca5-124">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="35ca5-125">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="35ca5-125">-HttpPort</span></span>
<span data-ttu-id="35ca5-126">Określa numer portu HTTP na serwerze źródłowym.</span><span class="sxs-lookup"><span data-stu-id="35ca5-126">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="35ca5-127">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="35ca5-127">-HttpsPort</span></span>
<span data-ttu-id="35ca5-128">Określa numer portu HTTPS na serwerze źródłowym.</span><span class="sxs-lookup"><span data-stu-id="35ca5-128">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="35ca5-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="35ca5-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="35ca5-130">Wskazuje, czy kompresja jest włączona dla punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="35ca5-130">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="35ca5-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="35ca5-131">-IsHttpAllowed</span></span>
<span data-ttu-id="35ca5-132">Wskazuje, czy punkt końcowy włącza ruch HTTP.</span><span class="sxs-lookup"><span data-stu-id="35ca5-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="35ca5-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="35ca5-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="35ca5-134">Wskazuje, czy punkt końcowy włącza ruch HTTPS.</span><span class="sxs-lookup"><span data-stu-id="35ca5-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="35ca5-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="35ca5-135">-Location</span></span>
<span data-ttu-id="35ca5-136">Określa lokalizację zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="35ca5-136">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="35ca5-137">-Optymalizacja typu</span><span class="sxs-lookup"><span data-stu-id="35ca5-137">-OptimizationType</span></span>
<span data-ttu-id="35ca5-138">Określa dowolną optymalizację tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="35ca5-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="35ca5-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="35ca5-139">-OriginGroupName</span></span>
<span data-ttu-id="35ca5-140">Nazwa grupy źródłowej.</span><span class="sxs-lookup"><span data-stu-id="35ca5-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="35ca5-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="35ca5-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="35ca5-142">Liczba sekund między badaniami kondycji.</span><span class="sxs-lookup"><span data-stu-id="35ca5-142">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="35ca5-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="35ca5-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="35ca5-144">Ścieżka odnosząca się do pochodzenia, która jest używana do określania kondycji pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="35ca5-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="35ca5-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="35ca5-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="35ca5-146">Protokół używany do badania kondycji.</span><span class="sxs-lookup"><span data-stu-id="35ca5-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="35ca5-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="35ca5-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="35ca5-148">Typ żądania badania kondycji, które zostało wykonane.</span><span class="sxs-lookup"><span data-stu-id="35ca5-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="35ca5-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="35ca5-149">-OriginHostHeader</span></span>
<span data-ttu-id="35ca5-150">Określa początkową pozycję hosta punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="35ca5-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="35ca5-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="35ca5-151">-OriginHostName</span></span>
<span data-ttu-id="35ca5-152">Określa nazwę hosta serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="35ca5-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="35ca5-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="35ca5-153">-OriginId</span></span>
<span data-ttu-id="35ca5-154">Identyfikatory grup pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="35ca5-154">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="35ca5-155">-Originname</span><span class="sxs-lookup"><span data-stu-id="35ca5-155">-OriginName</span></span>
<span data-ttu-id="35ca5-156">Określa nazwę zasobu serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="35ca5-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="35ca5-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="35ca5-157">-OriginPath</span></span>
<span data-ttu-id="35ca5-158">Określa ścieżkę serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="35ca5-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="35ca5-159">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="35ca5-159">-Priority</span></span>
<span data-ttu-id="35ca5-160">Priorytet pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="35ca5-160">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="35ca5-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="35ca5-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="35ca5-162">Niestandardowa wiadomość, która ma być uwzględniona w żądaniu zatwierdzenia w celu nawiązania połączenia z prywatnym linkiem.</span><span class="sxs-lookup"><span data-stu-id="35ca5-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="35ca5-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="35ca5-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="35ca5-164">Lokalizacja prywatnego łącza pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="35ca5-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="35ca5-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="35ca5-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="35ca5-166">Identyfikator zasobu prywatnego łącza pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="35ca5-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="35ca5-167">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="35ca5-167">-ProbePath</span></span>
<span data-ttu-id="35ca5-168">Określa ścieżkę sondy dla przyspieszania dynamicznego witryny</span><span class="sxs-lookup"><span data-stu-id="35ca5-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="35ca5-169">-Refilename</span><span class="sxs-lookup"><span data-stu-id="35ca5-169">-ProfileName</span></span>
<span data-ttu-id="35ca5-170">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="35ca5-170">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="35ca5-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="35ca5-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="35ca5-172">Określa zachowanie punktu końcowego sieci CDN, gdy ciąg zapytania znajduje się w adresie URL żądania.</span><span class="sxs-lookup"><span data-stu-id="35ca5-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="35ca5-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35ca5-173">-ResourceGroupName</span></span>
<span data-ttu-id="35ca5-174">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="35ca5-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="35ca5-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="35ca5-175">-Tag</span></span>
<span data-ttu-id="35ca5-176">Znaczniki, które mają zostać skojarzone z punktem końcowym usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="35ca5-176">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="35ca5-177">-Waga</span><span class="sxs-lookup"><span data-stu-id="35ca5-177">-Weight</span></span>
<span data-ttu-id="35ca5-178">Waga pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="35ca5-178">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="35ca5-179">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35ca5-179">-Confirm</span></span>
<span data-ttu-id="35ca5-180">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35ca5-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35ca5-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35ca5-181">-WhatIf</span></span>
<span data-ttu-id="35ca5-182">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35ca5-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35ca5-183">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="35ca5-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35ca5-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ca5-184">CommonParameters</span></span>
<span data-ttu-id="35ca5-185">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35ca5-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ca5-186">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35ca5-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ca5-187">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35ca5-187">INPUTS</span></span>

### <span data-ttu-id="35ca5-188">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="35ca5-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="35ca5-189">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35ca5-189">OUTPUTS</span></span>

### <span data-ttu-id="35ca5-190">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="35ca5-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="35ca5-191">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35ca5-191">NOTES</span></span>

## <span data-ttu-id="35ca5-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35ca5-192">RELATED LINKS</span></span>

[<span data-ttu-id="35ca5-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="35ca5-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="35ca5-194">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="35ca5-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="35ca5-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="35ca5-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="35ca5-196">Start — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="35ca5-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="35ca5-197">Zatrzymaj — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="35ca5-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


