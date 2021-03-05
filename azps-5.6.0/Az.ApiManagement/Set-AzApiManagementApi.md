---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: cdef3f217cec1401457f2f25daa91edafd4850b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012794"
---
# <span data-ttu-id="d2a94-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d2a94-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="d2a94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2a94-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a94-103">Modyfikuje interfejs API.</span><span class="sxs-lookup"><span data-stu-id="d2a94-103">Modifies an API.</span></span>

## <span data-ttu-id="d2a94-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d2a94-104">SYNTAX</span></span>

### <span data-ttu-id="d2a94-105">ExpandedParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d2a94-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2a94-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d2a94-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2a94-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d2a94-107">DESCRIPTION</span></span>
<span data-ttu-id="d2a94-108">Polecenie **cmdlet Set-AzApiManagementApi** modyfikuje interfejs API usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="d2a94-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="d2a94-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d2a94-109">EXAMPLES</span></span>

### <span data-ttu-id="d2a94-110">Przykład 1. Modyfikowanie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="d2a94-110">Example 1: Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="d2a94-111">Przykład 2. Dodawanie interfejsu API do istniejącego zestawu ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d2a94-111">Example 2: Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="d2a94-112">W tym przykładzie dodano interfejs API do istniejącego zestawu wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="d2a94-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="d2a94-113">Przykład 3. Zmienianie listy ServiceUrl zaplecza, dla której interfejs API</span><span class="sxs-lookup"><span data-stu-id="d2a94-113">Example 3: Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="d2a94-114">W tym przykładzie aktualizacja jest aktualizowana przez usługę ServiceUrl, `echo-api` która jest wskazują.</span><span class="sxs-lookup"><span data-stu-id="d2a94-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="d2a94-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2a94-115">PARAMETERS</span></span>

### <span data-ttu-id="d2a94-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d2a94-116">-ApiId</span></span>
<span data-ttu-id="d2a94-117">Określa identyfikator interfejsu API do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="d2a94-117">Specifies the ID of the API to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a94-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="d2a94-118">-AuthorizationScope</span></span>
<span data-ttu-id="d2a94-119">Określa zakres operacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="d2a94-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="d2a94-120">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="d2a94-120">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a94-121">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="d2a94-121">-AuthorizationServerId</span></span>
<span data-ttu-id="d2a94-122">Określa identyfikator serwera autoryzacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="d2a94-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="d2a94-123">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="d2a94-123">The default value is $Null.</span></span>
<span data-ttu-id="d2a94-124">Ten parametr należy określić, jeśli *parametr AuthorizationScope* jest określony.</span><span class="sxs-lookup"><span data-stu-id="d2a94-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a94-125">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="d2a94-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="d2a94-126">Mechanizm serwera autoryzacji OpenId, za pomocą którego token dostępu jest przekazywany do interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d2a94-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="d2a94-127">Zobacz http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="d2a94-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="d2a94-128">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d2a94-128">This parameter is optional.</span></span> <span data-ttu-id="d2a94-129">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="d2a94-129">Default value is $null.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a94-130">— kontekst</span><span class="sxs-lookup"><span data-stu-id="d2a94-130">-Context</span></span>
<span data-ttu-id="d2a94-131">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="d2a94-131">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a94-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a94-132">-DefaultProfile</span></span>
<span data-ttu-id="d2a94-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2a94-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2a94-134">— Opis</span><span class="sxs-lookup"><span data-stu-id="d2a94-134">-Description</span></span>
<span data-ttu-id="d2a94-135">Określa opis interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d2a94-135">Specifies a description for the web API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a94-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2a94-136">-InputObject</span></span>
<span data-ttu-id="d2a94-137">Wystąpienie obiektu PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="d2a94-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="d2a94-138">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d2a94-138">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a94-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d2a94-139">-Name</span></span>
<span data-ttu-id="d2a94-140">Określa nazwę interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d2a94-140">Specifies the name of the web API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a94-141">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="d2a94-141">-OpenIdProviderId</span></span>
<span data-ttu-id="d2a94-142">Identyfikator serwera autoryzacji OpenId.</span><span class="sxs-lookup"><span data-stu-id="d2a94-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="d2a94-143">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d2a94-143">This parameter is optional.</span></span> <span data-ttu-id="d2a94-144">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="d2a94-144">Default value is $null.</span></span> <span data-ttu-id="d2a94-145">Należy określić, jeśli określono wartości BearerTokenSendingMethods.</span><span class="sxs-lookup"><span data-stu-id="d2a94-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a94-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2a94-146">-PassThru</span></span>
<span data-ttu-id="d2a94-147">passthru</span><span class="sxs-lookup"><span data-stu-id="d2a94-147">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a94-148">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="d2a94-148">-Path</span></span>
<span data-ttu-id="d2a94-149">Określa ścieżkę interfejsu API sieci Web, która jest ostatnią częścią publicznego adresu URL interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d2a94-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="d2a94-150">Ten adres URL jest używany przez klientów interfejsu API do wysyłania żądań do usługi sieci Web i musi mieć od jednego do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="d2a94-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="d2a94-151">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="d2a94-151">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a94-152">- Protokoły</span><span class="sxs-lookup"><span data-stu-id="d2a94-152">-Protocols</span></span>
<span data-ttu-id="d2a94-153">Określa tablicę protokołów WEB API.</span><span class="sxs-lookup"><span data-stu-id="d2a94-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="d2a94-154">psdx_paramvalues http i https.</span><span class="sxs-lookup"><span data-stu-id="d2a94-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="d2a94-155">Są to protokoły sieci Web, za pośrednictwem których interfejs API jest dostępny.</span><span class="sxs-lookup"><span data-stu-id="d2a94-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="d2a94-156">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="d2a94-156">The default value is $Null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a94-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="d2a94-157">-ServiceUrl</span></span>
<span data-ttu-id="d2a94-158">Określa adres URL usługi sieci Web, która udostępnia interfejs API.</span><span class="sxs-lookup"><span data-stu-id="d2a94-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="d2a94-159">Ten adres URL jest używany tylko przez usługę Azure API Management i nie jest publiczny.</span><span class="sxs-lookup"><span data-stu-id="d2a94-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="d2a94-160">Adres URL musi zawierać od jednego do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="d2a94-160">The URL must be one to 2000 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a94-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="d2a94-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="d2a94-162">Określa nazwę nagłówka klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d2a94-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="d2a94-163">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="d2a94-163">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a94-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="d2a94-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="d2a94-165">Określa nazwę parametru ciągu zapytania klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d2a94-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="d2a94-166">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="d2a94-166">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a94-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="d2a94-167">-SubscriptionRequired</span></span>
<span data-ttu-id="d2a94-168">Oflaguj, aby wymusić zapytanie SubscriptionRequired dla żądań interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d2a94-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="d2a94-169">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d2a94-169">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a94-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a94-170">CommonParameters</span></span>
<span data-ttu-id="d2a94-171">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2a94-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a94-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2a94-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a94-173">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2a94-173">INPUTS</span></span>

### <span data-ttu-id="d2a94-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d2a94-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d2a94-175">System.String</span><span class="sxs-lookup"><span data-stu-id="d2a94-175">System.String</span></span>

### <span data-ttu-id="d2a94-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d2a94-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="d2a94-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="d2a94-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="d2a94-178">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="d2a94-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d2a94-179">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2a94-179">OUTPUTS</span></span>

### <span data-ttu-id="d2a94-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d2a94-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="d2a94-181">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d2a94-181">NOTES</span></span>

## <span data-ttu-id="d2a94-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2a94-182">RELATED LINKS</span></span>

[<span data-ttu-id="d2a94-183">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d2a94-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="d2a94-184">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d2a94-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="d2a94-185">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d2a94-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="d2a94-186">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d2a94-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="d2a94-187">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d2a94-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


