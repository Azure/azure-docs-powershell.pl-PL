---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: e7074b799e1c664ceb17499b04b8d4d2ff3acb5d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052830"
---
# <span data-ttu-id="f1d92-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f1d92-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="f1d92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f1d92-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d92-103">Modyfikuje wersję interfejsu API</span><span class="sxs-lookup"><span data-stu-id="f1d92-103">Modifies an API Revision</span></span>

## <span data-ttu-id="f1d92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f1d92-104">SYNTAX</span></span>

### <span data-ttu-id="f1d92-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f1d92-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1d92-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f1d92-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1d92-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f1d92-107">DESCRIPTION</span></span>
<span data-ttu-id="f1d92-108">Polecenie cmdlet **Set-AzApiManagementApiRevision** modyfikuje wersję interfejsu API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="f1d92-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="f1d92-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f1d92-109">EXAMPLES</span></span>

### <span data-ttu-id="f1d92-110">Przykład 1 modyfikowanie poprawki interfejsu API</span><span class="sxs-lookup"><span data-stu-id="f1d92-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="f1d92-111">Polecenie cmdlet umożliwia zaktualizowanie `2` poprawki interfejsu API `echo-api` o nowy opis, protokół i ścieżkę.</span><span class="sxs-lookup"><span data-stu-id="f1d92-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="f1d92-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f1d92-112">PARAMETERS</span></span>

### <span data-ttu-id="f1d92-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f1d92-113">-ApiId</span></span>
<span data-ttu-id="f1d92-114">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f1d92-114">Identifier of existing API.</span></span>
<span data-ttu-id="f1d92-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f1d92-115">This parameter is required.</span></span>

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

### <span data-ttu-id="f1d92-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f1d92-116">-ApiRevision</span></span>
<span data-ttu-id="f1d92-117">Identyfikator istniejącej poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f1d92-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="f1d92-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f1d92-118">This parameter is required.</span></span>

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

### <span data-ttu-id="f1d92-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="f1d92-119">-AuthorizationScope</span></span>
<span data-ttu-id="f1d92-120">Zakres operacji uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="f1d92-120">OAuth operations scope.</span></span>
<span data-ttu-id="f1d92-121">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f1d92-121">This parameter is optional.</span></span>
<span data-ttu-id="f1d92-122">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="f1d92-122">Default value is $null.</span></span>

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

### <span data-ttu-id="f1d92-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="f1d92-123">-AuthorizationServerId</span></span>
<span data-ttu-id="f1d92-124">Identyfikator serwera autoryzacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="f1d92-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="f1d92-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f1d92-125">This parameter is optional.</span></span>
<span data-ttu-id="f1d92-126">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="f1d92-126">Default value is $null.</span></span>
<span data-ttu-id="f1d92-127">Należy określić, czy AuthorizationScope.</span><span class="sxs-lookup"><span data-stu-id="f1d92-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="f1d92-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="f1d92-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="f1d92-129">OpenId mechanizm serwera autoryzacji, w którym token dostępu jest przekazywany do interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f1d92-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="f1d92-130">Zobacz http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="f1d92-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="f1d92-131">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f1d92-131">This parameter is optional.</span></span> <span data-ttu-id="f1d92-132">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="f1d92-132">Default value is $null.</span></span>

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

### <span data-ttu-id="f1d92-133">-Context</span><span class="sxs-lookup"><span data-stu-id="f1d92-133">-Context</span></span>
<span data-ttu-id="f1d92-134">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f1d92-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f1d92-135">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f1d92-135">This parameter is required.</span></span>

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

### <span data-ttu-id="f1d92-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d92-136">-DefaultProfile</span></span>
<span data-ttu-id="f1d92-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1d92-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1d92-138">— Opis</span><span class="sxs-lookup"><span data-stu-id="f1d92-138">-Description</span></span>
<span data-ttu-id="f1d92-139">Opis interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f1d92-139">Web API description.</span></span>
<span data-ttu-id="f1d92-140">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f1d92-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="f1d92-141">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f1d92-141">-InputObject</span></span>
<span data-ttu-id="f1d92-142">Wystąpienie PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="f1d92-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="f1d92-143">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f1d92-143">This parameter is required.</span></span>

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

### <span data-ttu-id="f1d92-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f1d92-144">-Name</span></span>
<span data-ttu-id="f1d92-145">Nazwa API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f1d92-145">Web API name.</span></span>
<span data-ttu-id="f1d92-146">Publiczna nazwa interfejsu API, która będzie wyświetlana na portalach dewelopera i administratora.</span><span class="sxs-lookup"><span data-stu-id="f1d92-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="f1d92-147">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f1d92-147">This parameter is required.</span></span>

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

### <span data-ttu-id="f1d92-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="f1d92-148">-OpenIdProviderId</span></span>
<span data-ttu-id="f1d92-149">Identyfikator serwera autoryzacji OpenId.</span><span class="sxs-lookup"><span data-stu-id="f1d92-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="f1d92-150">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f1d92-150">This parameter is optional.</span></span> <span data-ttu-id="f1d92-151">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="f1d92-151">Default value is $null.</span></span> <span data-ttu-id="f1d92-152">Należy określić, czy BearerTokenSendingMethods jest określony.</span><span class="sxs-lookup"><span data-stu-id="f1d92-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="f1d92-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1d92-153">-PassThru</span></span>
<span data-ttu-id="f1d92-154">Jeśli jest określone, wystąpienie systemu Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementApi reprezentujące zestaw interfejsów API.</span><span class="sxs-lookup"><span data-stu-id="f1d92-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="f1d92-155">-Path</span><span class="sxs-lookup"><span data-stu-id="f1d92-155">-Path</span></span>
<span data-ttu-id="f1d92-156">Ścieżka internetowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f1d92-156">Web API Path.</span></span>
<span data-ttu-id="f1d92-157">Ostatnia część publicznego adresu URL interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f1d92-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="f1d92-158">Ten adres URL będzie wykorzystywany przez użytkowników korzystających z interfejsu API w celu wysyłania żądań do usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f1d92-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="f1d92-159">Musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="f1d92-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="f1d92-160">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f1d92-160">This parameter is optional.</span></span>
<span data-ttu-id="f1d92-161">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="f1d92-161">Default value is $null.</span></span>

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

### <span data-ttu-id="f1d92-162">-Protokoły</span><span class="sxs-lookup"><span data-stu-id="f1d92-162">-Protocols</span></span>
<span data-ttu-id="f1d92-163">Protokoły API sieci Web (http, https).</span><span class="sxs-lookup"><span data-stu-id="f1d92-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="f1d92-164">Protokoły, w których udostępniono interfejs API.</span><span class="sxs-lookup"><span data-stu-id="f1d92-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="f1d92-165">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f1d92-165">This parameter is required.</span></span>
<span data-ttu-id="f1d92-166">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="f1d92-166">Default value is $null.</span></span>

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

### <span data-ttu-id="f1d92-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="f1d92-167">-ServiceUrl</span></span>
<span data-ttu-id="f1d92-168">Adres URL usługi sieci Web, która uwidacznia interfejs API.</span><span class="sxs-lookup"><span data-stu-id="f1d92-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="f1d92-169">Ten adres URL będzie wykorzystany tylko przez funkcję zarządzania interfejsem Azure API i nie zostanie udostępniony publicznie.</span><span class="sxs-lookup"><span data-stu-id="f1d92-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="f1d92-170">Musi zawierać od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="f1d92-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="f1d92-171">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f1d92-171">This parameter is required.</span></span>

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

### <span data-ttu-id="f1d92-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="f1d92-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="f1d92-173">Nazwa nagłówka klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f1d92-173">Subscription key header name.</span></span>
<span data-ttu-id="f1d92-174">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f1d92-174">This parameter is optional.</span></span>
<span data-ttu-id="f1d92-175">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="f1d92-175">Default value is $null.</span></span>

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

### <span data-ttu-id="f1d92-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="f1d92-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="f1d92-177">Nazwa parametru ciągu kwerendy klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f1d92-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="f1d92-178">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f1d92-178">This parameter is optional.</span></span>
<span data-ttu-id="f1d92-179">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="f1d92-179">Default value is $null.</span></span>

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

### <span data-ttu-id="f1d92-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="f1d92-180">-SubscriptionRequired</span></span>
<span data-ttu-id="f1d92-181">Flaga wymuszania SubscriptionRequired dla żądań w interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="f1d92-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="f1d92-182">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f1d92-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="f1d92-183">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f1d92-183">-Confirm</span></span>
<span data-ttu-id="f1d92-184">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1d92-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1d92-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1d92-185">-WhatIf</span></span>
<span data-ttu-id="f1d92-186">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1d92-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1d92-187">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f1d92-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1d92-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d92-188">CommonParameters</span></span>
<span data-ttu-id="f1d92-189">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1d92-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d92-190">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1d92-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d92-191">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1d92-191">INPUTS</span></span>

### <span data-ttu-id="f1d92-192">System. String</span><span class="sxs-lookup"><span data-stu-id="f1d92-192">System.String</span></span>

### <span data-ttu-id="f1d92-193">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f1d92-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f1d92-194">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f1d92-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="f1d92-195">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="f1d92-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="f1d92-196">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f1d92-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f1d92-197">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f1d92-197">OUTPUTS</span></span>

### <span data-ttu-id="f1d92-198">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f1d92-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="f1d92-199">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f1d92-199">NOTES</span></span>

## <span data-ttu-id="f1d92-200">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1d92-200">RELATED LINKS</span></span>

[<span data-ttu-id="f1d92-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f1d92-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="f1d92-202">Nowe — AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f1d92-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="f1d92-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f1d92-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)