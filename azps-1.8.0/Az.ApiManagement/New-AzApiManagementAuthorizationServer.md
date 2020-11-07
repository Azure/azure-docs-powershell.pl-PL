---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: b09ea243dac2952cc4ec630755537a0e3cc5a745
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704611"
---
# <span data-ttu-id="5817c-101">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="5817c-101">New-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="5817c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5817c-102">SYNOPSIS</span></span>
<span data-ttu-id="5817c-103">Tworzy serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="5817c-103">Creates an authorization server.</span></span>

## <span data-ttu-id="5817c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5817c-104">SYNTAX</span></span>

```
New-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>] -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5817c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5817c-105">DESCRIPTION</span></span>
<span data-ttu-id="5817c-106">Polecenie cmdlet **New-AzApiManagementAuthorizationServer** tworzy serwer autoryzacji zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="5817c-106">The **New-AzApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="5817c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5817c-107">EXAMPLES</span></span>

### <span data-ttu-id="5817c-108">Przykład 1. Tworzenie serwera autoryzacji</span><span class="sxs-lookup"><span data-stu-id="5817c-108">Example 1: Create an authorization server</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementAuthrizarionServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="5817c-109">To polecenie tworzy serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="5817c-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="5817c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5817c-110">PARAMETERS</span></span>

### <span data-ttu-id="5817c-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="5817c-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="5817c-112">Określa tablicę metod wysyłania tokena dostępu.</span><span class="sxs-lookup"><span data-stu-id="5817c-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="5817c-113">psdx_paramvalues AuthorizationHeader i Query.</span><span class="sxs-lookup"><span data-stu-id="5817c-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="5817c-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="5817c-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="5817c-115">Określa punkt końcowy autoryzacji w celu uwierzytelnienia właścicieli zasobów i uzyskania dotacji na autoryzację.</span><span class="sxs-lookup"><span data-stu-id="5817c-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="5817c-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="5817c-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="5817c-117">Określa tablicę metod żądań autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="5817c-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="5817c-118">Prawidłowe wartości: GET, POST.</span><span class="sxs-lookup"><span data-stu-id="5817c-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="5817c-119">Wartość domyślna to GET.</span><span class="sxs-lookup"><span data-stu-id="5817c-119">The default value is GET.</span></span>

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

### <span data-ttu-id="5817c-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="5817c-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="5817c-121">Określa tablicę metod uwierzytelniania klienta.</span><span class="sxs-lookup"><span data-stu-id="5817c-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="5817c-122">psdx_paramvalues podstawowy i podstawowy.</span><span class="sxs-lookup"><span data-stu-id="5817c-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="5817c-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="5817c-123">-ClientId</span></span>
<span data-ttu-id="5817c-124">Określa identyfikator klienta konsoli dewelopera, która jest aplikacją kliencką.</span><span class="sxs-lookup"><span data-stu-id="5817c-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="5817c-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="5817c-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="5817c-126">Umożliwia określenie punktu końcowego rejestracji klienta w celu zarejestrowania klientów na serwerze autoryzacji i uzyskania poświadczeń klienta.</span><span class="sxs-lookup"><span data-stu-id="5817c-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="5817c-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="5817c-127">-ClientSecret</span></span>
<span data-ttu-id="5817c-128">Określa klucz tajny klienta konsoli dewelopera, która jest aplikacją kliencką.</span><span class="sxs-lookup"><span data-stu-id="5817c-128">Specifies the client secret of developer console that is the client application.</span></span>

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

### <span data-ttu-id="5817c-129">-Context</span><span class="sxs-lookup"><span data-stu-id="5817c-129">-Context</span></span>
<span data-ttu-id="5817c-130">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5817c-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5817c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5817c-131">-DefaultProfile</span></span>
<span data-ttu-id="5817c-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5817c-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5817c-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="5817c-133">-DefaultScope</span></span>
<span data-ttu-id="5817c-134">Określa zakres domyślny dla serwera autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="5817c-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="5817c-135">— Opis</span><span class="sxs-lookup"><span data-stu-id="5817c-135">-Description</span></span>
<span data-ttu-id="5817c-136">Określa opis serwera autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="5817c-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="5817c-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="5817c-137">-GrantTypes</span></span>
<span data-ttu-id="5817c-138">Określa tablicę typów dotacji.</span><span class="sxs-lookup"><span data-stu-id="5817c-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="5817c-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="5817c-139">psdx_paramvalues</span></span>
- <span data-ttu-id="5817c-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="5817c-140">AuthorizationCode</span></span>
- <span data-ttu-id="5817c-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="5817c-141">ClientCredentials</span></span> 
- <span data-ttu-id="5817c-142">Ukrytych</span><span class="sxs-lookup"><span data-stu-id="5817c-142">Implicit</span></span> 
- <span data-ttu-id="5817c-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="5817c-143">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="5817c-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5817c-144">-Name</span></span>
<span data-ttu-id="5817c-145">Określa nazwę serwera autoryzacji, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="5817c-145">Specifies the name of the authorization server to create.</span></span>

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

### <span data-ttu-id="5817c-146">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="5817c-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="5817c-147">Określa hasło właściciela zasobu.</span><span class="sxs-lookup"><span data-stu-id="5817c-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="5817c-148">Ten parametr należy określić jako wymagany, jeśli ResourceOwnerPassword jest określony przez parametr *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="5817c-148">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="5817c-149">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="5817c-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="5817c-150">Określa nazwę użytkownika właściciela zasobu.</span><span class="sxs-lookup"><span data-stu-id="5817c-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="5817c-151">Ten parametr należy określić, jeśli ResourceOwnerPassword jest określony za pomocą parametru *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="5817c-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="5817c-152">-ServerId</span><span class="sxs-lookup"><span data-stu-id="5817c-152">-ServerId</span></span>
<span data-ttu-id="5817c-153">Określa identyfikator serwera autoryzacji, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="5817c-153">Specifies the ID of the authorization server to create.</span></span>

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

### <span data-ttu-id="5817c-154">-SupportState</span><span class="sxs-lookup"><span data-stu-id="5817c-154">-SupportState</span></span>
<span data-ttu-id="5817c-155">Wskazuje, czy ma być obsługiwany parametr *State* .</span><span class="sxs-lookup"><span data-stu-id="5817c-155">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="5817c-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="5817c-156">-TokenBodyParameters</span></span>
<span data-ttu-id="5817c-157">Określa dodatkowe parametry treści przy użyciu formatu **Application/x-www-form-urlencoded** .</span><span class="sxs-lookup"><span data-stu-id="5817c-157">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

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

### <span data-ttu-id="5817c-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="5817c-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="5817c-159">Określa adres URL punktu końcowego tokenu, który jest wykorzystywany przez klientów do uzyskiwania tokenów dostępu w programie Exchange w celu prezentowania uprawnień do autoryzacji lub odświeżania tokenów.</span><span class="sxs-lookup"><span data-stu-id="5817c-159">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="5817c-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5817c-160">CommonParameters</span></span>
<span data-ttu-id="5817c-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5817c-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5817c-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5817c-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5817c-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5817c-163">INPUTS</span></span>

### <span data-ttu-id="5817c-164">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5817c-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5817c-165">System. String</span><span class="sxs-lookup"><span data-stu-id="5817c-165">System.String</span></span>

### <span data-ttu-id="5817c-166">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="5817c-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="5817c-167">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="5817c-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="5817c-168">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="5817c-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="5817c-169">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5817c-169">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5817c-170">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5817c-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5817c-171">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="5817c-171">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

## <span data-ttu-id="5817c-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5817c-172">OUTPUTS</span></span>

### <span data-ttu-id="5817c-173">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="5817c-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="5817c-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5817c-174">NOTES</span></span>

## <span data-ttu-id="5817c-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5817c-175">RELATED LINKS</span></span>
