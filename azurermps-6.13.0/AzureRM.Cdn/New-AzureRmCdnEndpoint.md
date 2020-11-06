---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 62a4859b5a64003956a4975411f809176f2917e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548867"
---
# <span data-ttu-id="cd0e1-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd0e1-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="cd0e1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd0e1-102">SYNOPSIS</span></span>
<span data-ttu-id="cd0e1-103">Tworzy punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd0e1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd0e1-104">SYNTAX</span></span>

### <span data-ttu-id="cd0e1-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd0e1-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd0e1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd0e1-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd0e1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cd0e1-107">DESCRIPTION</span></span>
<span data-ttu-id="cd0e1-108">Polecenie cmdlet **New-AzureRmCdnEndpoint** umożliwia utworzenie punktu końcowego sieci dostarczania zawartości Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="cd0e1-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="cd0e1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd0e1-109">EXAMPLES</span></span>

## <span data-ttu-id="cd0e1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd0e1-110">PARAMETERS</span></span>

### <span data-ttu-id="cd0e1-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="cd0e1-111">-CdnProfile</span></span>
<span data-ttu-id="cd0e1-112">Określa obiekt profilu sieci CDN, do którego jest dodawany punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="cd0e1-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="cd0e1-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="cd0e1-114">Określa tablicę typów zawartości, które mają być kompresowane z węzła Edge do klienta.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="cd0e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd0e1-115">-DefaultProfile</span></span>
<span data-ttu-id="cd0e1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cd0e1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd0e1-117">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="cd0e1-117">-DeliveryPolicy</span></span>
<span data-ttu-id="cd0e1-118">Zasady dostarczania dla tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-118">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="cd0e1-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cd0e1-119">-EndpointName</span></span>
<span data-ttu-id="cd0e1-120">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-120">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="cd0e1-121">-Filtry</span><span class="sxs-lookup"><span data-stu-id="cd0e1-121">-GeoFilters</span></span>
<span data-ttu-id="cd0e1-122">Lista filtrów Geo, które dotyczą tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-122">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="cd0e1-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="cd0e1-123">-HttpPort</span></span>
<span data-ttu-id="cd0e1-124">Określa numer portu HTTP na serwerze źródłowym.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-124">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="cd0e1-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="cd0e1-125">-HttpsPort</span></span>
<span data-ttu-id="cd0e1-126">Określa numer portu HTTPS na serwerze źródłowym.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-126">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="cd0e1-127">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="cd0e1-127">-IsCompressionEnabled</span></span>
<span data-ttu-id="cd0e1-128">Wskazuje, czy kompresja jest włączona dla punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-128">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="cd0e1-129">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="cd0e1-129">-IsHttpAllowed</span></span>
<span data-ttu-id="cd0e1-130">Wskazuje, czy punkt końcowy włącza ruch HTTP.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-130">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="cd0e1-131">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="cd0e1-131">-IsHttpsAllowed</span></span>
<span data-ttu-id="cd0e1-132">Wskazuje, czy punkt końcowy włącza ruch HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-132">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="cd0e1-133">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cd0e1-133">-Location</span></span>
<span data-ttu-id="cd0e1-134">Określa lokalizację zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-134">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="cd0e1-135">-Optymalizacja typu</span><span class="sxs-lookup"><span data-stu-id="cd0e1-135">-OptimizationType</span></span>
<span data-ttu-id="cd0e1-136">Określa dowolną optymalizację tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-136">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="cd0e1-137">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="cd0e1-137">-OriginHostHeader</span></span>
<span data-ttu-id="cd0e1-138">Określa początkową pozycję hosta punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-138">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="cd0e1-139">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="cd0e1-139">-OriginHostName</span></span>
<span data-ttu-id="cd0e1-140">Określa nazwę hosta serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-140">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="cd0e1-141">-Originname</span><span class="sxs-lookup"><span data-stu-id="cd0e1-141">-OriginName</span></span>
<span data-ttu-id="cd0e1-142">Określa nazwę zasobu serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-142">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="cd0e1-143">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="cd0e1-143">-OriginPath</span></span>
<span data-ttu-id="cd0e1-144">Określa ścieżkę serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-144">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="cd0e1-145">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="cd0e1-145">-ProbePath</span></span>
<span data-ttu-id="cd0e1-146">Określa ścieżkę sondy dla przyspieszania dynamicznego witryny</span><span class="sxs-lookup"><span data-stu-id="cd0e1-146">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="cd0e1-147">-Refilename</span><span class="sxs-lookup"><span data-stu-id="cd0e1-147">-ProfileName</span></span>
<span data-ttu-id="cd0e1-148">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-148">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="cd0e1-149">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="cd0e1-149">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="cd0e1-150">Określa zachowanie punktu końcowego sieci CDN, gdy ciąg zapytania znajduje się w adresie URL żądania.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-150">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="cd0e1-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd0e1-151">-ResourceGroupName</span></span>
<span data-ttu-id="cd0e1-152">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-152">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="cd0e1-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="cd0e1-153">-Tag</span></span>
<span data-ttu-id="cd0e1-154">Znaczniki, które mają zostać skojarzone z punktem końcowym usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-154">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="cd0e1-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd0e1-155">-Confirm</span></span>
<span data-ttu-id="cd0e1-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd0e1-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd0e1-157">-WhatIf</span></span>
<span data-ttu-id="cd0e1-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd0e1-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd0e1-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd0e1-160">CommonParameters</span></span>
<span data-ttu-id="cd0e1-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd0e1-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd0e1-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd0e1-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd0e1-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd0e1-163">INPUTS</span></span>

### <span data-ttu-id="cd0e1-164">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="cd0e1-164">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="cd0e1-165">Parametry: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cd0e1-165">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="cd0e1-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd0e1-166">OUTPUTS</span></span>

### <span data-ttu-id="cd0e1-167">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd0e1-167">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="cd0e1-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd0e1-168">NOTES</span></span>

## <span data-ttu-id="cd0e1-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd0e1-169">RELATED LINKS</span></span>

[<span data-ttu-id="cd0e1-170">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd0e1-170">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="cd0e1-171">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd0e1-171">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="cd0e1-172">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd0e1-172">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="cd0e1-173">Start — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd0e1-173">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="cd0e1-174">Zatrzymaj — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd0e1-174">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


