---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: fcae55c69b1874e06ce9110631baaf3b679fe99a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381843"
---
# <span data-ttu-id="302aa-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="302aa-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="302aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="302aa-102">SYNOPSIS</span></span>
<span data-ttu-id="302aa-103">Modyfikuje wersję interfejsu API</span><span class="sxs-lookup"><span data-stu-id="302aa-103">Modifies an API Revision</span></span>

## <span data-ttu-id="302aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="302aa-104">SYNTAX</span></span>

### <span data-ttu-id="302aa-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="302aa-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="302aa-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="302aa-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="302aa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="302aa-107">DESCRIPTION</span></span>
<span data-ttu-id="302aa-108">Polecenie cmdlet **Set-AzApiManagementApiRevision** modyfikuje wersję interfejsu API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="302aa-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="302aa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="302aa-109">EXAMPLES</span></span>

### <span data-ttu-id="302aa-110">Przykład 1: modyfikowanie wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="302aa-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="302aa-111">Polecenie cmdlet umożliwia zaktualizowanie `2` poprawki interfejsu API `echo-api` o nowy opis, protokół i ścieżkę.</span><span class="sxs-lookup"><span data-stu-id="302aa-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="302aa-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="302aa-112">PARAMETERS</span></span>

### <span data-ttu-id="302aa-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="302aa-113">-ApiId</span></span>
<span data-ttu-id="302aa-114">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="302aa-114">Identifier of existing API.</span></span>
<span data-ttu-id="302aa-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="302aa-115">This parameter is required.</span></span>

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

### <span data-ttu-id="302aa-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="302aa-116">-ApiRevision</span></span>
<span data-ttu-id="302aa-117">Identyfikator istniejącej poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="302aa-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="302aa-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="302aa-118">This parameter is required.</span></span>

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

### <span data-ttu-id="302aa-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="302aa-119">-AuthorizationScope</span></span>
<span data-ttu-id="302aa-120">Zakres operacji uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="302aa-120">OAuth operations scope.</span></span>
<span data-ttu-id="302aa-121">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="302aa-121">This parameter is optional.</span></span>
<span data-ttu-id="302aa-122">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="302aa-122">Default value is $null.</span></span>

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

### <span data-ttu-id="302aa-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="302aa-123">-AuthorizationServerId</span></span>
<span data-ttu-id="302aa-124">Identyfikator serwera autoryzacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="302aa-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="302aa-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="302aa-125">This parameter is optional.</span></span>
<span data-ttu-id="302aa-126">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="302aa-126">Default value is $null.</span></span>
<span data-ttu-id="302aa-127">Należy określić, czy AuthorizationScope.</span><span class="sxs-lookup"><span data-stu-id="302aa-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="302aa-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="302aa-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="302aa-129">OpenId mechanizm serwera autoryzacji, w którym token dostępu jest przekazywany do interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="302aa-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="302aa-130">Zobacz http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="302aa-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="302aa-131">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="302aa-131">This parameter is optional.</span></span> <span data-ttu-id="302aa-132">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="302aa-132">Default value is $null.</span></span>

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

### <span data-ttu-id="302aa-133">-Context</span><span class="sxs-lookup"><span data-stu-id="302aa-133">-Context</span></span>
<span data-ttu-id="302aa-134">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="302aa-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="302aa-135">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="302aa-135">This parameter is required.</span></span>

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

### <span data-ttu-id="302aa-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="302aa-136">-DefaultProfile</span></span>
<span data-ttu-id="302aa-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="302aa-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="302aa-138">— Opis</span><span class="sxs-lookup"><span data-stu-id="302aa-138">-Description</span></span>
<span data-ttu-id="302aa-139">Opis interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="302aa-139">Web API description.</span></span>
<span data-ttu-id="302aa-140">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="302aa-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="302aa-141">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="302aa-141">-InputObject</span></span>
<span data-ttu-id="302aa-142">Wystąpienie PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="302aa-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="302aa-143">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="302aa-143">This parameter is required.</span></span>

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

### <span data-ttu-id="302aa-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="302aa-144">-Name</span></span>
<span data-ttu-id="302aa-145">Nazwa API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="302aa-145">Web API name.</span></span>
<span data-ttu-id="302aa-146">Publiczna nazwa interfejsu API, która będzie wyświetlana na portalach dewelopera i administratora.</span><span class="sxs-lookup"><span data-stu-id="302aa-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="302aa-147">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="302aa-147">This parameter is required.</span></span>

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

### <span data-ttu-id="302aa-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="302aa-148">-OpenIdProviderId</span></span>
<span data-ttu-id="302aa-149">Identyfikator serwera autoryzacji OpenId.</span><span class="sxs-lookup"><span data-stu-id="302aa-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="302aa-150">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="302aa-150">This parameter is optional.</span></span> <span data-ttu-id="302aa-151">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="302aa-151">Default value is $null.</span></span> <span data-ttu-id="302aa-152">Należy określić, czy BearerTokenSendingMethods jest określony.</span><span class="sxs-lookup"><span data-stu-id="302aa-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="302aa-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="302aa-153">-PassThru</span></span>
<span data-ttu-id="302aa-154">Jeśli jest określone, wystąpienie systemu Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementApi reprezentujące zestaw interfejsów API.</span><span class="sxs-lookup"><span data-stu-id="302aa-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="302aa-155">-Path</span><span class="sxs-lookup"><span data-stu-id="302aa-155">-Path</span></span>
<span data-ttu-id="302aa-156">Ścieżka internetowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="302aa-156">Web API Path.</span></span>
<span data-ttu-id="302aa-157">Ostatnia część publicznego adresu URL interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="302aa-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="302aa-158">Ten adres URL będzie wykorzystywany przez użytkowników korzystających z interfejsu API w celu wysyłania żądań do usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="302aa-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="302aa-159">Musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="302aa-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="302aa-160">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="302aa-160">This parameter is optional.</span></span>
<span data-ttu-id="302aa-161">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="302aa-161">Default value is $null.</span></span>

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

### <span data-ttu-id="302aa-162">-Protokoły</span><span class="sxs-lookup"><span data-stu-id="302aa-162">-Protocols</span></span>
<span data-ttu-id="302aa-163">Protokoły API sieci Web (http, https).</span><span class="sxs-lookup"><span data-stu-id="302aa-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="302aa-164">Protokoły, w których udostępniono interfejs API.</span><span class="sxs-lookup"><span data-stu-id="302aa-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="302aa-165">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="302aa-165">This parameter is required.</span></span>
<span data-ttu-id="302aa-166">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="302aa-166">Default value is $null.</span></span>

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

### <span data-ttu-id="302aa-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="302aa-167">-ServiceUrl</span></span>
<span data-ttu-id="302aa-168">Adres URL usługi sieci Web, która uwidacznia interfejs API.</span><span class="sxs-lookup"><span data-stu-id="302aa-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="302aa-169">Ten adres URL będzie wykorzystany tylko przez funkcję zarządzania interfejsem Azure API i nie zostanie udostępniony publicznie.</span><span class="sxs-lookup"><span data-stu-id="302aa-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="302aa-170">Musi zawierać od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="302aa-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="302aa-171">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="302aa-171">This parameter is required.</span></span>

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

### <span data-ttu-id="302aa-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="302aa-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="302aa-173">Nazwa nagłówka klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="302aa-173">Subscription key header name.</span></span>
<span data-ttu-id="302aa-174">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="302aa-174">This parameter is optional.</span></span>
<span data-ttu-id="302aa-175">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="302aa-175">Default value is $null.</span></span>

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

### <span data-ttu-id="302aa-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="302aa-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="302aa-177">Nazwa parametru ciągu kwerendy klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="302aa-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="302aa-178">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="302aa-178">This parameter is optional.</span></span>
<span data-ttu-id="302aa-179">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="302aa-179">Default value is $null.</span></span>

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

### <span data-ttu-id="302aa-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="302aa-180">-SubscriptionRequired</span></span>
<span data-ttu-id="302aa-181">Flaga wymuszania SubscriptionRequired dla żądań w interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="302aa-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="302aa-182">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="302aa-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="302aa-183">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="302aa-183">-Confirm</span></span>
<span data-ttu-id="302aa-184">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="302aa-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="302aa-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="302aa-185">-WhatIf</span></span>
<span data-ttu-id="302aa-186">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="302aa-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="302aa-187">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="302aa-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="302aa-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302aa-188">CommonParameters</span></span>
<span data-ttu-id="302aa-189">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="302aa-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="302aa-190">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="302aa-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302aa-191">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="302aa-191">INPUTS</span></span>

### <span data-ttu-id="302aa-192">System. String</span><span class="sxs-lookup"><span data-stu-id="302aa-192">System.String</span></span>

### <span data-ttu-id="302aa-193">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="302aa-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="302aa-194">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="302aa-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="302aa-195">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="302aa-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="302aa-196">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="302aa-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="302aa-197">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="302aa-197">OUTPUTS</span></span>

### <span data-ttu-id="302aa-198">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="302aa-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="302aa-199">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="302aa-199">NOTES</span></span>

## <span data-ttu-id="302aa-200">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="302aa-200">RELATED LINKS</span></span>

[<span data-ttu-id="302aa-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="302aa-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="302aa-202">Nowe — AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="302aa-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="302aa-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="302aa-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)