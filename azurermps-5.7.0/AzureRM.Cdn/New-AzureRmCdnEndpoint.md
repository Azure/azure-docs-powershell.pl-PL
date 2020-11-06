---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 682c12270608f9c75e86cea742fd411e0eb657a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527017"
---
# <span data-ttu-id="529cc-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="529cc-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="529cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="529cc-102">SYNOPSIS</span></span>
<span data-ttu-id="529cc-103">Tworzy punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="529cc-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="529cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="529cc-104">SYNTAX</span></span>

### <span data-ttu-id="529cc-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="529cc-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="529cc-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="529cc-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="529cc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="529cc-107">DESCRIPTION</span></span>
<span data-ttu-id="529cc-108">Polecenie cmdlet **New-AzureRmCdnEndpoint** umożliwia utworzenie punktu końcowego sieci dostarczania zawartości Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="529cc-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="529cc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="529cc-109">EXAMPLES</span></span>

## <span data-ttu-id="529cc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="529cc-110">PARAMETERS</span></span>

### <span data-ttu-id="529cc-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="529cc-111">-CdnProfile</span></span>
<span data-ttu-id="529cc-112">Określa obiekt profilu sieci CDN, do którego jest dodawany punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="529cc-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="529cc-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="529cc-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="529cc-114">Określa tablicę typów zawartości, które mają być kompresowane z węzła Edge do klienta.</span><span class="sxs-lookup"><span data-stu-id="529cc-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="529cc-115">-DefaultProfile</span></span>
<span data-ttu-id="529cc-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="529cc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="529cc-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="529cc-117">-EndpointName</span></span>
<span data-ttu-id="529cc-118">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="529cc-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="529cc-119">-Filtry</span><span class="sxs-lookup"><span data-stu-id="529cc-119">-GeoFilters</span></span>
<span data-ttu-id="529cc-120">Lista filtrów Geo, które dotyczą tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="529cc-120">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529cc-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="529cc-121">-HttpPort</span></span>
<span data-ttu-id="529cc-122">Określa numer portu HTTP na serwerze źródłowym.</span><span class="sxs-lookup"><span data-stu-id="529cc-122">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529cc-123">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="529cc-123">-HttpsPort</span></span>
<span data-ttu-id="529cc-124">Określa numer portu HTTPS na serwerze źródłowym.</span><span class="sxs-lookup"><span data-stu-id="529cc-124">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529cc-125">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="529cc-125">-IsCompressionEnabled</span></span>
<span data-ttu-id="529cc-126">Wskazuje, czy kompresja jest włączona dla punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="529cc-126">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529cc-127">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="529cc-127">-IsHttpAllowed</span></span>
<span data-ttu-id="529cc-128">Wskazuje, czy punkt końcowy włącza ruch HTTP.</span><span class="sxs-lookup"><span data-stu-id="529cc-128">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529cc-129">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="529cc-129">-IsHttpsAllowed</span></span>
<span data-ttu-id="529cc-130">Wskazuje, czy punkt końcowy włącza ruch HTTPS.</span><span class="sxs-lookup"><span data-stu-id="529cc-130">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529cc-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="529cc-131">-Location</span></span>
<span data-ttu-id="529cc-132">Określa lokalizację zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="529cc-132">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529cc-133">-Optymalizacja typu</span><span class="sxs-lookup"><span data-stu-id="529cc-133">-OptimizationType</span></span>
<span data-ttu-id="529cc-134">Określa dowolną optymalizację tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="529cc-134">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="529cc-135">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="529cc-135">-OriginHostHeader</span></span>
<span data-ttu-id="529cc-136">Określa początkową pozycję hosta punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="529cc-136">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="529cc-137">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="529cc-137">-OriginHostName</span></span>
<span data-ttu-id="529cc-138">Określa nazwę hosta serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="529cc-138">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="529cc-139">-Originname</span><span class="sxs-lookup"><span data-stu-id="529cc-139">-OriginName</span></span>
<span data-ttu-id="529cc-140">Określa nazwę zasobu serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="529cc-140">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="529cc-141">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="529cc-141">-OriginPath</span></span>
<span data-ttu-id="529cc-142">Określa ścieżkę serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="529cc-142">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="529cc-143">-Refilename</span><span class="sxs-lookup"><span data-stu-id="529cc-143">-ProfileName</span></span>
<span data-ttu-id="529cc-144">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="529cc-144">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529cc-145">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="529cc-145">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="529cc-146">Określa zachowanie punktu końcowego sieci CDN, gdy ciąg zapytania znajduje się w adresie URL żądania.</span><span class="sxs-lookup"><span data-stu-id="529cc-146">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: PSQueryStringCachingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529cc-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="529cc-147">-ResourceGroupName</span></span>
<span data-ttu-id="529cc-148">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="529cc-148">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529cc-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="529cc-149">-Tag</span></span>
<span data-ttu-id="529cc-150">Znaczniki, które mają zostać skojarzone z punktem końcowym usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="529cc-150">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529cc-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="529cc-151">-Confirm</span></span>
<span data-ttu-id="529cc-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="529cc-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529cc-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="529cc-153">-WhatIf</span></span>
<span data-ttu-id="529cc-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="529cc-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="529cc-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="529cc-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529cc-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="529cc-156">CommonParameters</span></span>
<span data-ttu-id="529cc-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="529cc-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="529cc-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="529cc-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="529cc-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="529cc-159">INPUTS</span></span>

### <span data-ttu-id="529cc-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="529cc-160">PSProfile</span></span>
<span data-ttu-id="529cc-161">Parametr "CdnProfile" akceptuje wartość typu "PSProfile" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="529cc-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="529cc-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="529cc-162">OUTPUTS</span></span>

### <span data-ttu-id="529cc-163">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="529cc-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="529cc-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="529cc-164">NOTES</span></span>

## <span data-ttu-id="529cc-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="529cc-165">RELATED LINKS</span></span>

[<span data-ttu-id="529cc-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="529cc-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="529cc-167">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="529cc-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="529cc-168">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="529cc-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="529cc-169">Start — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="529cc-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="529cc-170">Zatrzymaj — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="529cc-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


