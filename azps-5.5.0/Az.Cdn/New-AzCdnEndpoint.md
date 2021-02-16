---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9e0b8ee74ff89f4a5903df1c73dc7b289b0371c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200826"
---
# <span data-ttu-id="25901-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="25901-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="25901-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25901-102">SYNOPSIS</span></span>
<span data-ttu-id="25901-103">Tworzy punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="25901-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="25901-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="25901-104">SYNTAX</span></span>

### <span data-ttu-id="25901-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="25901-105">ByFieldsParameterSet (Default)</span></span>
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

### <span data-ttu-id="25901-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25901-106">ByObjectParameterSet</span></span>
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

## <span data-ttu-id="25901-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="25901-107">DESCRIPTION</span></span>
<span data-ttu-id="25901-108">Polecenie **cmdlet New-AzCdnEndpoint** tworzy punkt końcowy usługi Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="25901-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="25901-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="25901-109">EXAMPLES</span></span>

## <span data-ttu-id="25901-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25901-110">PARAMETERS</span></span>

### <span data-ttu-id="25901-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="25901-111">-CdnProfile</span></span>
<span data-ttu-id="25901-112">Określa obiekt profilu sieci CDN, do którego został dodany punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="25901-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="25901-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="25901-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="25901-114">Określa tablicę typów zawartości do skompresowania z węzła brzegowego do klienta.</span><span class="sxs-lookup"><span data-stu-id="25901-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="25901-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="25901-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="25901-116">Domyślna grupa pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="25901-116">The default origin group.</span></span>

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

### <span data-ttu-id="25901-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25901-117">-DefaultProfile</span></span>
<span data-ttu-id="25901-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="25901-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25901-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="25901-119">-DeliveryPolicy</span></span>
<span data-ttu-id="25901-120">Zasady dostarczania dla tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="25901-120">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="25901-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="25901-121">-EndpointName</span></span>
<span data-ttu-id="25901-122">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="25901-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="25901-123">— Filtry geograficzne</span><span class="sxs-lookup"><span data-stu-id="25901-123">-GeoFilters</span></span>
<span data-ttu-id="25901-124">Lista filtrów geograficznych, które dotyczą tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="25901-124">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="25901-125">- HttpPort</span><span class="sxs-lookup"><span data-stu-id="25901-125">-HttpPort</span></span>
<span data-ttu-id="25901-126">Określa numer portu HTTP na serwerze pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="25901-126">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="25901-127">—HttpsPort</span><span class="sxs-lookup"><span data-stu-id="25901-127">-HttpsPort</span></span>
<span data-ttu-id="25901-128">Określa numer portu HTTPS na serwerze pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="25901-128">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="25901-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="25901-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="25901-130">Wskazuje, czy dla punktu końcowego włączono kompresję.</span><span class="sxs-lookup"><span data-stu-id="25901-130">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="25901-131">—IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="25901-131">-IsHttpAllowed</span></span>
<span data-ttu-id="25901-132">Wskazuje, czy punkt końcowy umożliwia ruch HTTP.</span><span class="sxs-lookup"><span data-stu-id="25901-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="25901-133">—IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="25901-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="25901-134">Wskazuje, czy punkt końcowy umożliwia ruch HTTPS.</span><span class="sxs-lookup"><span data-stu-id="25901-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="25901-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="25901-135">-Location</span></span>
<span data-ttu-id="25901-136">Określa lokalizację zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="25901-136">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="25901-137">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="25901-137">-OptimizationType</span></span>
<span data-ttu-id="25901-138">Określa dowolną optymalizację dla tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="25901-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="25901-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="25901-139">-OriginGroupName</span></span>
<span data-ttu-id="25901-140">Nazwa grupy pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="25901-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="25901-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="25901-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="25901-142">Liczba sekund między stanem zdrowia.</span><span class="sxs-lookup"><span data-stu-id="25901-142">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="25901-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="25901-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="25901-144">Ścieżka względna względem pochodzenia używanego do określenia kondycji pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="25901-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="25901-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="25901-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="25901-146">Protokół do użycia na użytek kondycji zdrowotnej.</span><span class="sxs-lookup"><span data-stu-id="25901-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="25901-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="25901-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="25901-148">Typ żądania kondycji.</span><span class="sxs-lookup"><span data-stu-id="25901-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="25901-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="25901-149">-OriginHostHeader</span></span>
<span data-ttu-id="25901-150">Określa początek hosta pochodzenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="25901-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="25901-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="25901-151">-OriginHostName</span></span>
<span data-ttu-id="25901-152">Określa nazwę hosta serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="25901-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="25901-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="25901-153">-OriginId</span></span>
<span data-ttu-id="25901-154">Identyfikatory grup pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="25901-154">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="25901-155">-OriginName</span><span class="sxs-lookup"><span data-stu-id="25901-155">-OriginName</span></span>
<span data-ttu-id="25901-156">Określa nazwę zasobu serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="25901-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="25901-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="25901-157">-OriginPath</span></span>
<span data-ttu-id="25901-158">Określa ścieżkę serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="25901-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="25901-159">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="25901-159">-Priority</span></span>
<span data-ttu-id="25901-160">Priorytet pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="25901-160">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="25901-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="25901-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="25901-162">Wiadomość niestandardowa dołączona do żądania zatwierdzenia w celu nawiązania połączenia z linkiem prywatnym.</span><span class="sxs-lookup"><span data-stu-id="25901-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="25901-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="25901-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="25901-164">Lokalizacja prywatnego linku pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="25901-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="25901-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="25901-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="25901-166">Identyfikator zasobu prywatnego pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="25901-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="25901-167">-Path</span><span class="sxs-lookup"><span data-stu-id="25901-167">-ProbePath</span></span>
<span data-ttu-id="25901-168">Określa ścieżkę ścieżki ścieżki dynamicznego przyspieszenia witryny.</span><span class="sxs-lookup"><span data-stu-id="25901-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="25901-169">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="25901-169">-ProfileName</span></span>
<span data-ttu-id="25901-170">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="25901-170">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="25901-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="25901-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="25901-172">Określa zachowanie punktu końcowego sieci CDN, gdy ciąg zapytania znajduje się w adresie URL żądania.</span><span class="sxs-lookup"><span data-stu-id="25901-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="25901-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25901-173">-ResourceGroupName</span></span>
<span data-ttu-id="25901-174">Określa nazwę grupy zasobów, do której należy ten punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="25901-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="25901-175">— Tag</span><span class="sxs-lookup"><span data-stu-id="25901-175">-Tag</span></span>
<span data-ttu-id="25901-176">Tagi do skojarzenia z punktem końcowym sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="25901-176">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="25901-177">— Waga</span><span class="sxs-lookup"><span data-stu-id="25901-177">-Weight</span></span>
<span data-ttu-id="25901-178">Waga pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="25901-178">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="25901-179">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25901-179">-Confirm</span></span>
<span data-ttu-id="25901-180">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="25901-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25901-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25901-181">-WhatIf</span></span>
<span data-ttu-id="25901-182">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25901-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25901-183">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="25901-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25901-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25901-184">CommonParameters</span></span>
<span data-ttu-id="25901-185">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25901-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25901-186">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25901-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25901-187">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25901-187">INPUTS</span></span>

### <span data-ttu-id="25901-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="25901-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="25901-189">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="25901-189">OUTPUTS</span></span>

### <span data-ttu-id="25901-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="25901-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="25901-191">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="25901-191">NOTES</span></span>

## <span data-ttu-id="25901-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25901-192">RELATED LINKS</span></span>

[<span data-ttu-id="25901-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="25901-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="25901-194">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="25901-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="25901-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="25901-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="25901-196">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="25901-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="25901-197">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="25901-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


