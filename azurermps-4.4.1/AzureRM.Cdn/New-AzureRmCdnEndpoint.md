---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 5d2bfdf2bf5f87ccb0213c006de8612b5eaf0730
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550068"
---
# <span data-ttu-id="9ef0e-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9ef0e-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="9ef0e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ef0e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef0e-103">Tworzy punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ef0e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ef0e-104">SYNTAX</span></span>

### <span data-ttu-id="9ef0e-105">Parametr ustawiony dla parametrów pól (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9ef0e-105">Parameter Set for fields parameters (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ef0e-106">Zestaw parametrów dla parametrów obiektu</span><span class="sxs-lookup"><span data-stu-id="9ef0e-106">Parameter Set for object parameters</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ef0e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9ef0e-107">DESCRIPTION</span></span>
<span data-ttu-id="9ef0e-108">Polecenie cmdlet **New-AzureRmCdnEndpoint** umożliwia utworzenie punktu końcowego sieci dostarczania zawartości Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="9ef0e-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="9ef0e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ef0e-109">EXAMPLES</span></span>

## <span data-ttu-id="9ef0e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ef0e-110">PARAMETERS</span></span>

### <span data-ttu-id="9ef0e-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="9ef0e-111">-CdnProfile</span></span>
<span data-ttu-id="9ef0e-112">Określa obiekt profilu sieci CDN, do którego jest dodawany punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ef0e-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="9ef0e-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="9ef0e-114">Określa tablicę typów zawartości, które mają być kompresowane z węzła Edge do klienta.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="9ef0e-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9ef0e-115">-EndpointName</span></span>
<span data-ttu-id="9ef0e-116">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="9ef0e-117">-Filtry</span><span class="sxs-lookup"><span data-stu-id="9ef0e-117">-GeoFilters</span></span>
<span data-ttu-id="9ef0e-118">Lista filtrów Geo, które dotyczą tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-118">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="9ef0e-119">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="9ef0e-119">-HttpPort</span></span>
<span data-ttu-id="9ef0e-120">Określa numer portu HTTP na serwerze źródłowym.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-120">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="9ef0e-121">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="9ef0e-121">-HttpsPort</span></span>
<span data-ttu-id="9ef0e-122">Określa numer portu HTTPS na serwerze źródłowym.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-122">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="9ef0e-123">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="9ef0e-123">-IsCompressionEnabled</span></span>
<span data-ttu-id="9ef0e-124">Wskazuje, czy kompresja jest włączona dla punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-124">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="9ef0e-125">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="9ef0e-125">-IsHttpAllowed</span></span>
<span data-ttu-id="9ef0e-126">Wskazuje, czy punkt końcowy włącza ruch HTTP.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-126">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="9ef0e-127">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="9ef0e-127">-IsHttpsAllowed</span></span>
<span data-ttu-id="9ef0e-128">Wskazuje, czy punkt końcowy włącza ruch HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-128">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="9ef0e-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9ef0e-129">-Location</span></span>
<span data-ttu-id="9ef0e-130">Określa lokalizację zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-130">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef0e-131">-Optymalizacja typu</span><span class="sxs-lookup"><span data-stu-id="9ef0e-131">-OptimizationType</span></span>
<span data-ttu-id="9ef0e-132">Określa dowolną optymalizację tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-132">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="9ef0e-133">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="9ef0e-133">-OriginHostHeader</span></span>
<span data-ttu-id="9ef0e-134">Określa początkową pozycję hosta punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-134">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="9ef0e-135">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="9ef0e-135">-OriginHostName</span></span>
<span data-ttu-id="9ef0e-136">Określa nazwę hosta serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-136">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="9ef0e-137">-Originname</span><span class="sxs-lookup"><span data-stu-id="9ef0e-137">-OriginName</span></span>
<span data-ttu-id="9ef0e-138">Określa nazwę zasobu serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-138">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="9ef0e-139">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="9ef0e-139">-OriginPath</span></span>
<span data-ttu-id="9ef0e-140">Określa ścieżkę serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-140">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="9ef0e-141">-Refilename</span><span class="sxs-lookup"><span data-stu-id="9ef0e-141">-ProfileName</span></span>
<span data-ttu-id="9ef0e-142">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-142">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef0e-143">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="9ef0e-143">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="9ef0e-144">Określa zachowanie punktu końcowego sieci CDN, gdy ciąg zapytania znajduje się w adresie URL żądania.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-144">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="9ef0e-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef0e-145">-ResourceGroupName</span></span>
<span data-ttu-id="9ef0e-146">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-146">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef0e-147">-Tagi</span><span class="sxs-lookup"><span data-stu-id="9ef0e-147">-Tags</span></span>
<span data-ttu-id="9ef0e-148">Określa tabelę skrótów tagów skojarzonych z tym zasobem.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-148">Specifies a hash table of the tags that associated with this resource.</span></span>

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

### <span data-ttu-id="9ef0e-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9ef0e-149">-Confirm</span></span>
<span data-ttu-id="9ef0e-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ef0e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ef0e-151">-WhatIf</span></span>
<span data-ttu-id="9ef0e-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ef0e-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ef0e-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef0e-154">-DefaultProfile</span></span>
<span data-ttu-id="9ef0e-155">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ef0e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef0e-156">CommonParameters</span></span>
<span data-ttu-id="9ef0e-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ef0e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef0e-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ef0e-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef0e-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ef0e-159">INPUTS</span></span>

### <span data-ttu-id="9ef0e-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="9ef0e-160">PSProfile</span></span>
<span data-ttu-id="9ef0e-161">Parametr "CdnProfile" akceptuje wartość typu "PSProfile" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="9ef0e-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="9ef0e-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ef0e-162">OUTPUTS</span></span>

### <span data-ttu-id="9ef0e-163">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="9ef0e-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="9ef0e-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ef0e-164">NOTES</span></span>

## <span data-ttu-id="9ef0e-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ef0e-165">RELATED LINKS</span></span>

[<span data-ttu-id="9ef0e-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9ef0e-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9ef0e-167">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9ef0e-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9ef0e-168">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9ef0e-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9ef0e-169">Start — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9ef0e-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9ef0e-170">Zatrzymaj — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9ef0e-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


