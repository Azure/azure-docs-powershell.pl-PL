---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 88e7c1304aae987dbf7315d5ed474969af12ba08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869356"
---
# <span data-ttu-id="3425b-101">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3425b-101">Set-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="3425b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3425b-102">SYNOPSIS</span></span>
<span data-ttu-id="3425b-103">Modyfikuje serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="3425b-103">Modifies an authorization server.</span></span>

## <span data-ttu-id="3425b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3425b-104">SYNTAX</span></span>

```
Set-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3425b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3425b-105">DESCRIPTION</span></span>
<span data-ttu-id="3425b-106">Polecenie cmdlet **Set-AzApiManagementAuthorizationServer** modyfikuje szczegóły serwera autoryzacji zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="3425b-106">The **Set-AzApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="3425b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3425b-107">EXAMPLES</span></span>

### <span data-ttu-id="3425b-108">Przykład 1: modyfikowanie serwera autoryzacji</span><span class="sxs-lookup"><span data-stu-id="3425b-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementAuthrizarionServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="3425b-109">To polecenie modyfikuje określony serwer autoryzacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3425b-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="3425b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3425b-110">PARAMETERS</span></span>

### <span data-ttu-id="3425b-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="3425b-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="3425b-112">Określa tablicę metod wysyłania tokena dostępu.</span><span class="sxs-lookup"><span data-stu-id="3425b-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="3425b-113">psdx_paramvalues AuthorizationHeader i Query.</span><span class="sxs-lookup"><span data-stu-id="3425b-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3425b-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="3425b-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="3425b-115">Określa punkt końcowy autoryzacji w celu uwierzytelnienia właścicieli zasobów i uzyskania dotacji na autoryzację.</span><span class="sxs-lookup"><span data-stu-id="3425b-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3425b-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="3425b-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="3425b-117">Określa tablicę metod żądań autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="3425b-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="3425b-118">psdx_paramvalues GET i POST.</span><span class="sxs-lookup"><span data-stu-id="3425b-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="3425b-119">Wartość domyślna to GET.</span><span class="sxs-lookup"><span data-stu-id="3425b-119">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Get, Post, Head, Options, Trace, Put, Patch, Delete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3425b-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="3425b-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="3425b-121">Określa tablicę metod uwierzytelniania klienta.</span><span class="sxs-lookup"><span data-stu-id="3425b-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="3425b-122">psdx_paramvalues podstawowy i podstawowy.</span><span class="sxs-lookup"><span data-stu-id="3425b-122">psdx_paramvalues Basic and Body.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3425b-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="3425b-123">-ClientId</span></span>
<span data-ttu-id="3425b-124">Określa identyfikator klienta konsoli dewelopera, która jest aplikacją kliencką.</span><span class="sxs-lookup"><span data-stu-id="3425b-124">Specifies the client ID of the developer console that is the client application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3425b-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="3425b-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="3425b-126">Umożliwia określenie punktu końcowego rejestracji klienta w celu zarejestrowania klientów na serwerze autoryzacji i uzyskania poświadczeń klienta.</span><span class="sxs-lookup"><span data-stu-id="3425b-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3425b-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="3425b-127">-ClientSecret</span></span>
<span data-ttu-id="3425b-128">Określa klucz tajny klienta konsoli dewelopera, która jest aplikacją kliencką.</span><span class="sxs-lookup"><span data-stu-id="3425b-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="3425b-129">-Context</span><span class="sxs-lookup"><span data-stu-id="3425b-129">-Context</span></span>
<span data-ttu-id="3425b-130">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3425b-130">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3425b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3425b-131">-DefaultProfile</span></span>
<span data-ttu-id="3425b-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3425b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3425b-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="3425b-133">-DefaultScope</span></span>
<span data-ttu-id="3425b-134">Określa zakres domyślny dla serwera autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="3425b-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="3425b-135">— Opis</span><span class="sxs-lookup"><span data-stu-id="3425b-135">-Description</span></span>
<span data-ttu-id="3425b-136">Określa opis serwera autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="3425b-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="3425b-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="3425b-137">-GrantTypes</span></span>
<span data-ttu-id="3425b-138">Określa tablicę typów dotacji.</span><span class="sxs-lookup"><span data-stu-id="3425b-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="3425b-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="3425b-139">psdx_paramvalues</span></span>
- <span data-ttu-id="3425b-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="3425b-140">AuthorizationCode</span></span>
- <span data-ttu-id="3425b-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="3425b-141">ClientCredentials</span></span> 
- <span data-ttu-id="3425b-142">Ukrytych</span><span class="sxs-lookup"><span data-stu-id="3425b-142">Implicit</span></span> 
- <span data-ttu-id="3425b-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="3425b-143">ResourceOwnerPassword</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3425b-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3425b-144">-Name</span></span>
<span data-ttu-id="3425b-145">Określa nazwę serwera autoryzacji do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="3425b-145">Specifies the name of the authorization server to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3425b-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3425b-146">-PassThru</span></span>
<span data-ttu-id="3425b-147">passthru</span><span class="sxs-lookup"><span data-stu-id="3425b-147">passthru</span></span>

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

### <span data-ttu-id="3425b-148">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="3425b-148">-ResourceOwnerPassword</span></span>
<span data-ttu-id="3425b-149">Określa hasło właściciela zasobu.</span><span class="sxs-lookup"><span data-stu-id="3425b-149">Specifies the resource owner password.</span></span>
<span data-ttu-id="3425b-150">Ten parametr należy określić, jeśli ResourceOwnerPassword jest określony za pomocą parametru *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="3425b-150">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="3425b-151">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="3425b-151">-ResourceOwnerUsername</span></span>
<span data-ttu-id="3425b-152">Określa nazwę użytkownika właściciela zasobu.</span><span class="sxs-lookup"><span data-stu-id="3425b-152">Specifies the resource owner user name.</span></span>
<span data-ttu-id="3425b-153">Ten parametr należy określić, jeśli ResourceOwnerPassword jest określony za pomocą parametru *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="3425b-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="3425b-154">-ServerId</span><span class="sxs-lookup"><span data-stu-id="3425b-154">-ServerId</span></span>
<span data-ttu-id="3425b-155">Określa identyfikator serwera autoryzacji, który należy zmodyfikować.</span><span class="sxs-lookup"><span data-stu-id="3425b-155">Specifies the ID of the authorization server to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3425b-156">-SupportState</span><span class="sxs-lookup"><span data-stu-id="3425b-156">-SupportState</span></span>
<span data-ttu-id="3425b-157">Wskazuje, czy ma być obsługiwany parametr *State* .</span><span class="sxs-lookup"><span data-stu-id="3425b-157">Indicates whether to support the *State* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3425b-158">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="3425b-158">-TokenBodyParameters</span></span>
<span data-ttu-id="3425b-159">Określa dodatkowe parametry treści przy użyciu formatu application/x-www-form-urlencoded.</span><span class="sxs-lookup"><span data-stu-id="3425b-159">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3425b-160">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="3425b-160">-TokenEndpointUrl</span></span>
<span data-ttu-id="3425b-161">Określa końcowy token dla klientów umożliwiający uzyskanie tokenów dostępu w programie Exchange w celu prezentowania uprawnień do autoryzacji lub odświeżania tokenów.</span><span class="sxs-lookup"><span data-stu-id="3425b-161">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3425b-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3425b-162">CommonParameters</span></span>
<span data-ttu-id="3425b-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3425b-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3425b-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3425b-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3425b-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3425b-165">INPUTS</span></span>

### <span data-ttu-id="3425b-166">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3425b-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3425b-167">System. String</span><span class="sxs-lookup"><span data-stu-id="3425b-167">System.String</span></span>

### <span data-ttu-id="3425b-168">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="3425b-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="3425b-169">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="3425b-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="3425b-170">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="3425b-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="3425b-171">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3425b-171">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3425b-172">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3425b-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3425b-173">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="3425b-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

### <span data-ttu-id="3425b-174">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3425b-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3425b-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3425b-175">OUTPUTS</span></span>

### <span data-ttu-id="3425b-176">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="3425b-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="3425b-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3425b-177">NOTES</span></span>

## <span data-ttu-id="3425b-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3425b-178">RELATED LINKS</span></span>

[<span data-ttu-id="3425b-179">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3425b-179">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="3425b-180">Nowe — AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3425b-180">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="3425b-181">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3425b-181">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)


