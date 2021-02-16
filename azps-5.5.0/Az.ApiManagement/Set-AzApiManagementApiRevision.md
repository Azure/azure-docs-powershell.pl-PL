---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: fcae55c69b1874e06ce9110631baaf3b679fe99a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244379"
---
# <span data-ttu-id="a683e-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="a683e-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="a683e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a683e-102">SYNOPSIS</span></span>
<span data-ttu-id="a683e-103">Modyfikuje poprawkę interfejsu API</span><span class="sxs-lookup"><span data-stu-id="a683e-103">Modifies an API Revision</span></span>

## <span data-ttu-id="a683e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a683e-104">SYNTAX</span></span>

### <span data-ttu-id="a683e-105">ExpandedParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a683e-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a683e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a683e-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a683e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a683e-107">DESCRIPTION</span></span>
<span data-ttu-id="a683e-108">Polecenie **cmdlet Set-AzApiManagementApiRevision** modyfikuje poprawkę interfejsu API zarządzania interfejsem API usługi Azure API.</span><span class="sxs-lookup"><span data-stu-id="a683e-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="a683e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a683e-109">EXAMPLES</span></span>

### <span data-ttu-id="a683e-110">Przykład 1. Modyfikowanie poprawki interfejsu API</span><span class="sxs-lookup"><span data-stu-id="a683e-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="a683e-111">Polecenie cmdlet aktualizuje `2` poprawkę interfejsu API `echo-api` o nowy opis, protokół i ścieżkę.</span><span class="sxs-lookup"><span data-stu-id="a683e-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="a683e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a683e-112">PARAMETERS</span></span>

### <span data-ttu-id="a683e-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a683e-113">-ApiId</span></span>
<span data-ttu-id="a683e-114">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a683e-114">Identifier of existing API.</span></span>
<span data-ttu-id="a683e-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a683e-115">This parameter is required.</span></span>

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

### <span data-ttu-id="a683e-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="a683e-116">-ApiRevision</span></span>
<span data-ttu-id="a683e-117">Identyfikator istniejącej poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a683e-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="a683e-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a683e-118">This parameter is required.</span></span>

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

### <span data-ttu-id="a683e-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="a683e-119">-AuthorizationScope</span></span>
<span data-ttu-id="a683e-120">Zakres operacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="a683e-120">OAuth operations scope.</span></span>
<span data-ttu-id="a683e-121">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a683e-121">This parameter is optional.</span></span>
<span data-ttu-id="a683e-122">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="a683e-122">Default value is $null.</span></span>

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

### <span data-ttu-id="a683e-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="a683e-123">-AuthorizationServerId</span></span>
<span data-ttu-id="a683e-124">Identyfikator serwera autoryzacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="a683e-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="a683e-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a683e-125">This parameter is optional.</span></span>
<span data-ttu-id="a683e-126">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="a683e-126">Default value is $null.</span></span>
<span data-ttu-id="a683e-127">Musi zostać określony, jeśli jest określony authorizationscope.</span><span class="sxs-lookup"><span data-stu-id="a683e-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="a683e-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="a683e-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="a683e-129">Mechanizm serwera autoryzacji OpenId, za pomocą którego token dostępu jest przekazywany do interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a683e-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="a683e-130">Zobacz http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="a683e-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="a683e-131">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a683e-131">This parameter is optional.</span></span> <span data-ttu-id="a683e-132">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="a683e-132">Default value is $null.</span></span>

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

### <span data-ttu-id="a683e-133">— kontekst</span><span class="sxs-lookup"><span data-stu-id="a683e-133">-Context</span></span>
<span data-ttu-id="a683e-134">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a683e-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a683e-135">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a683e-135">This parameter is required.</span></span>

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

### <span data-ttu-id="a683e-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a683e-136">-DefaultProfile</span></span>
<span data-ttu-id="a683e-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a683e-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a683e-138">— Opis</span><span class="sxs-lookup"><span data-stu-id="a683e-138">-Description</span></span>
<span data-ttu-id="a683e-139">Opis interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a683e-139">Web API description.</span></span>
<span data-ttu-id="a683e-140">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a683e-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="a683e-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a683e-141">-InputObject</span></span>
<span data-ttu-id="a683e-142">Wystąpienie obiektu PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="a683e-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="a683e-143">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a683e-143">This parameter is required.</span></span>

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

### <span data-ttu-id="a683e-144">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a683e-144">-Name</span></span>
<span data-ttu-id="a683e-145">Nazwa interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a683e-145">Web API name.</span></span>
<span data-ttu-id="a683e-146">Nazwa publiczna interfejsu API, która będzie wyświetlana w portalach dewelopera i administratora.</span><span class="sxs-lookup"><span data-stu-id="a683e-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="a683e-147">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a683e-147">This parameter is required.</span></span>

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

### <span data-ttu-id="a683e-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="a683e-148">-OpenIdProviderId</span></span>
<span data-ttu-id="a683e-149">Identyfikator serwera autoryzacji OpenId.</span><span class="sxs-lookup"><span data-stu-id="a683e-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="a683e-150">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a683e-150">This parameter is optional.</span></span> <span data-ttu-id="a683e-151">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="a683e-151">Default value is $null.</span></span> <span data-ttu-id="a683e-152">Należy określić, jeśli określono wartości BearerTokenSendingMethods.</span><span class="sxs-lookup"><span data-stu-id="a683e-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="a683e-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a683e-153">-PassThru</span></span>
<span data-ttu-id="a683e-154">Jeśli określono, wówczas wystąpienie microsoft.azure.commands.apiManagement.ServiceManagement.Models.PsApiManagementApi typ reprezentujący zestaw interfejs API.</span><span class="sxs-lookup"><span data-stu-id="a683e-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="a683e-155">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="a683e-155">-Path</span></span>
<span data-ttu-id="a683e-156">Ścieżka interfejsu WEB API.</span><span class="sxs-lookup"><span data-stu-id="a683e-156">Web API Path.</span></span>
<span data-ttu-id="a683e-157">Ostatnia część publicznego adresu URL interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a683e-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="a683e-158">Ten adres URL będzie używany przez klientów interfejsu API do wysyłania żądań do usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a683e-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="a683e-159">Musi to być od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="a683e-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="a683e-160">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a683e-160">This parameter is optional.</span></span>
<span data-ttu-id="a683e-161">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="a683e-161">Default value is $null.</span></span>

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

### <span data-ttu-id="a683e-162">- Protokoły</span><span class="sxs-lookup"><span data-stu-id="a683e-162">-Protocols</span></span>
<span data-ttu-id="a683e-163">Protokoły WEB API (http, https).</span><span class="sxs-lookup"><span data-stu-id="a683e-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="a683e-164">Protokoły, dla których jest dostępny interfejs API.</span><span class="sxs-lookup"><span data-stu-id="a683e-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="a683e-165">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a683e-165">This parameter is required.</span></span>
<span data-ttu-id="a683e-166">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="a683e-166">Default value is $null.</span></span>

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

### <span data-ttu-id="a683e-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="a683e-167">-ServiceUrl</span></span>
<span data-ttu-id="a683e-168">Adres URL usługi sieci Web eksponujące interfejs API.</span><span class="sxs-lookup"><span data-stu-id="a683e-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="a683e-169">Ten adres URL będzie używany tylko w usłudze Azure API Management i nie będzie publiczny.</span><span class="sxs-lookup"><span data-stu-id="a683e-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="a683e-170">Musi to być od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="a683e-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="a683e-171">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a683e-171">This parameter is required.</span></span>

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

### <span data-ttu-id="a683e-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="a683e-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="a683e-173">Nazwa nagłówka klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a683e-173">Subscription key header name.</span></span>
<span data-ttu-id="a683e-174">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a683e-174">This parameter is optional.</span></span>
<span data-ttu-id="a683e-175">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="a683e-175">Default value is $null.</span></span>

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

### <span data-ttu-id="a683e-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="a683e-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="a683e-177">Nazwa parametru ciągu zapytania klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a683e-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="a683e-178">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a683e-178">This parameter is optional.</span></span>
<span data-ttu-id="a683e-179">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="a683e-179">Default value is $null.</span></span>

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

### <span data-ttu-id="a683e-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="a683e-180">-SubscriptionRequired</span></span>
<span data-ttu-id="a683e-181">Oflaguj, aby wymusić zapytanie SubscriptionRequired dla żądań interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a683e-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="a683e-182">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a683e-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="a683e-183">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a683e-183">-Confirm</span></span>
<span data-ttu-id="a683e-184">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a683e-184">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a683e-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a683e-185">-WhatIf</span></span>
<span data-ttu-id="a683e-186">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a683e-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a683e-187">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a683e-187">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a683e-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a683e-188">CommonParameters</span></span>
<span data-ttu-id="a683e-189">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a683e-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a683e-190">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a683e-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a683e-191">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a683e-191">INPUTS</span></span>

### <span data-ttu-id="a683e-192">System.String</span><span class="sxs-lookup"><span data-stu-id="a683e-192">System.String</span></span>

### <span data-ttu-id="a683e-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a683e-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a683e-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a683e-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="a683e-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="a683e-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="a683e-196">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="a683e-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a683e-197">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a683e-197">OUTPUTS</span></span>

### <span data-ttu-id="a683e-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a683e-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="a683e-199">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a683e-199">NOTES</span></span>

## <span data-ttu-id="a683e-200">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a683e-200">RELATED LINKS</span></span>

[<span data-ttu-id="a683e-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="a683e-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="a683e-202">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="a683e-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="a683e-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="a683e-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)