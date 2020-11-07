---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9d8704abaeb5fd320a871b7b15720af3bbb0c472
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869220"
---
# <span data-ttu-id="fe102-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe102-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="fe102-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe102-102">SYNOPSIS</span></span>
<span data-ttu-id="fe102-103">Tworzy punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="fe102-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="fe102-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe102-104">SYNTAX</span></span>

### <span data-ttu-id="fe102-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fe102-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe102-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe102-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe102-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fe102-107">DESCRIPTION</span></span>
<span data-ttu-id="fe102-108">Polecenie cmdlet **New-AzCdnEndpoint** umożliwia utworzenie punktu końcowego sieci dostarczania zawartości Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="fe102-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="fe102-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe102-109">EXAMPLES</span></span>

## <span data-ttu-id="fe102-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe102-110">PARAMETERS</span></span>

### <span data-ttu-id="fe102-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="fe102-111">-CdnProfile</span></span>
<span data-ttu-id="fe102-112">Określa obiekt profilu sieci CDN, do którego jest dodawany punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="fe102-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="fe102-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="fe102-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="fe102-114">Określa tablicę typów zawartości, które mają być kompresowane z węzła Edge do klienta.</span><span class="sxs-lookup"><span data-stu-id="fe102-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="fe102-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe102-115">-DefaultProfile</span></span>
<span data-ttu-id="fe102-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fe102-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe102-117">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="fe102-117">-DeliveryPolicy</span></span>
<span data-ttu-id="fe102-118">Zasady dostarczania dla tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="fe102-118">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="fe102-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fe102-119">-EndpointName</span></span>
<span data-ttu-id="fe102-120">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="fe102-120">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="fe102-121">-Filtry</span><span class="sxs-lookup"><span data-stu-id="fe102-121">-GeoFilters</span></span>
<span data-ttu-id="fe102-122">Lista filtrów Geo, które dotyczą tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="fe102-122">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="fe102-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="fe102-123">-HttpPort</span></span>
<span data-ttu-id="fe102-124">Określa numer portu HTTP na serwerze źródłowym.</span><span class="sxs-lookup"><span data-stu-id="fe102-124">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="fe102-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="fe102-125">-HttpsPort</span></span>
<span data-ttu-id="fe102-126">Określa numer portu HTTPS na serwerze źródłowym.</span><span class="sxs-lookup"><span data-stu-id="fe102-126">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="fe102-127">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="fe102-127">-IsCompressionEnabled</span></span>
<span data-ttu-id="fe102-128">Wskazuje, czy kompresja jest włączona dla punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="fe102-128">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="fe102-129">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="fe102-129">-IsHttpAllowed</span></span>
<span data-ttu-id="fe102-130">Wskazuje, czy punkt końcowy włącza ruch HTTP.</span><span class="sxs-lookup"><span data-stu-id="fe102-130">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="fe102-131">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="fe102-131">-IsHttpsAllowed</span></span>
<span data-ttu-id="fe102-132">Wskazuje, czy punkt końcowy włącza ruch HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fe102-132">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="fe102-133">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fe102-133">-Location</span></span>
<span data-ttu-id="fe102-134">Określa lokalizację zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="fe102-134">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="fe102-135">-Optymalizacja typu</span><span class="sxs-lookup"><span data-stu-id="fe102-135">-OptimizationType</span></span>
<span data-ttu-id="fe102-136">Określa dowolną optymalizację tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="fe102-136">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="fe102-137">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="fe102-137">-OriginHostHeader</span></span>
<span data-ttu-id="fe102-138">Określa początkową pozycję hosta punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="fe102-138">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="fe102-139">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="fe102-139">-OriginHostName</span></span>
<span data-ttu-id="fe102-140">Określa nazwę hosta serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="fe102-140">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="fe102-141">-Originname</span><span class="sxs-lookup"><span data-stu-id="fe102-141">-OriginName</span></span>
<span data-ttu-id="fe102-142">Określa nazwę zasobu serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="fe102-142">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="fe102-143">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="fe102-143">-OriginPath</span></span>
<span data-ttu-id="fe102-144">Określa ścieżkę serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="fe102-144">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="fe102-145">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="fe102-145">-ProbePath</span></span>
<span data-ttu-id="fe102-146">Określa ścieżkę sondy dla przyspieszania dynamicznego witryny</span><span class="sxs-lookup"><span data-stu-id="fe102-146">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="fe102-147">-Refilename</span><span class="sxs-lookup"><span data-stu-id="fe102-147">-ProfileName</span></span>
<span data-ttu-id="fe102-148">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="fe102-148">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="fe102-149">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="fe102-149">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="fe102-150">Określa zachowanie punktu końcowego sieci CDN, gdy ciąg zapytania znajduje się w adresie URL żądania.</span><span class="sxs-lookup"><span data-stu-id="fe102-150">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="fe102-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe102-151">-ResourceGroupName</span></span>
<span data-ttu-id="fe102-152">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="fe102-152">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="fe102-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="fe102-153">-Tag</span></span>
<span data-ttu-id="fe102-154">Znaczniki, które mają zostać skojarzone z punktem końcowym usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="fe102-154">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="fe102-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fe102-155">-Confirm</span></span>
<span data-ttu-id="fe102-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe102-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe102-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe102-157">-WhatIf</span></span>
<span data-ttu-id="fe102-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe102-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe102-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fe102-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe102-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe102-160">CommonParameters</span></span>
<span data-ttu-id="fe102-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe102-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe102-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe102-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe102-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe102-163">INPUTS</span></span>

### <span data-ttu-id="fe102-164">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="fe102-164">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="fe102-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe102-165">OUTPUTS</span></span>

### <span data-ttu-id="fe102-166">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe102-166">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="fe102-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe102-167">NOTES</span></span>

## <span data-ttu-id="fe102-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe102-168">RELATED LINKS</span></span>

[<span data-ttu-id="fe102-169">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe102-169">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="fe102-170">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe102-170">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="fe102-171">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe102-171">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="fe102-172">Start — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe102-172">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="fe102-173">Zatrzymaj — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe102-173">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


