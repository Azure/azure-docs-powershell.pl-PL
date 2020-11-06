---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: cfba050b3ec6e464465d72e5f8d236f3b253fd0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547235"
---
# <span data-ttu-id="1f01c-101">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1f01c-101">New-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="1f01c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f01c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f01c-103">Tworzy serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="1f01c-103">Creates an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f01c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f01c-104">SYNTAX</span></span>

```
New-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 -Name <String> [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f01c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1f01c-105">DESCRIPTION</span></span>
<span data-ttu-id="1f01c-106">Polecenie cmdlet **New-AzureRmApiManagementAuthorizationServer** tworzy serwer autoryzacji zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="1f01c-106">The **New-AzureRmApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="1f01c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f01c-107">EXAMPLES</span></span>

### <span data-ttu-id="1f01c-108">Przykład 1. Tworzenie serwera autoryzacji</span><span class="sxs-lookup"><span data-stu-id="1f01c-108">Example 1: Create an authorization server</span></span>
```
PS C:\>New-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="1f01c-109">To polecenie tworzy serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="1f01c-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="1f01c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f01c-110">PARAMETERS</span></span>

### <span data-ttu-id="1f01c-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="1f01c-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="1f01c-112">Określa tablicę metod wysyłania tokena dostępu.</span><span class="sxs-lookup"><span data-stu-id="1f01c-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="1f01c-113">psdx_paramvalues AuthorizationHeader i Query.</span><span class="sxs-lookup"><span data-stu-id="1f01c-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="1f01c-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="1f01c-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="1f01c-115">Określa punkt końcowy autoryzacji w celu uwierzytelnienia właścicieli zasobów i uzyskania dotacji na autoryzację.</span><span class="sxs-lookup"><span data-stu-id="1f01c-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="1f01c-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="1f01c-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="1f01c-117">Określa tablicę metod żądań autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="1f01c-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="1f01c-118">Prawidłowe wartości: GET, POST.</span><span class="sxs-lookup"><span data-stu-id="1f01c-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="1f01c-119">Wartość domyślna to GET.</span><span class="sxs-lookup"><span data-stu-id="1f01c-119">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Get, Post

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f01c-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="1f01c-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="1f01c-121">Określa tablicę metod uwierzytelniania klienta.</span><span class="sxs-lookup"><span data-stu-id="1f01c-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="1f01c-122">psdx_paramvalues podstawowy i podstawowy.</span><span class="sxs-lookup"><span data-stu-id="1f01c-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="1f01c-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="1f01c-123">-ClientId</span></span>
<span data-ttu-id="1f01c-124">Określa identyfikator klienta konsoli dewelopera, która jest aplikacją kliencką.</span><span class="sxs-lookup"><span data-stu-id="1f01c-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="1f01c-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="1f01c-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="1f01c-126">Umożliwia określenie punktu końcowego rejestracji klienta w celu zarejestrowania klientów na serwerze autoryzacji i uzyskania poświadczeń klienta.</span><span class="sxs-lookup"><span data-stu-id="1f01c-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="1f01c-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="1f01c-127">-ClientSecret</span></span>
<span data-ttu-id="1f01c-128">Określa klucz tajny klienta konsoli dewelopera, która jest aplikacją kliencką.</span><span class="sxs-lookup"><span data-stu-id="1f01c-128">Specifies the client secret of developer console that is the client application.</span></span>

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

### <span data-ttu-id="1f01c-129">-Context</span><span class="sxs-lookup"><span data-stu-id="1f01c-129">-Context</span></span>
<span data-ttu-id="1f01c-130">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1f01c-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1f01c-131">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="1f01c-131">-DefaultScope</span></span>
<span data-ttu-id="1f01c-132">Określa zakres domyślny dla serwera autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="1f01c-132">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="1f01c-133">— Opis</span><span class="sxs-lookup"><span data-stu-id="1f01c-133">-Description</span></span>
<span data-ttu-id="1f01c-134">Określa opis serwera autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="1f01c-134">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="1f01c-135">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="1f01c-135">-GrantTypes</span></span>
<span data-ttu-id="1f01c-136">Określa tablicę typów dotacji.</span><span class="sxs-lookup"><span data-stu-id="1f01c-136">Specifies an array of grant types.</span></span>
<span data-ttu-id="1f01c-137">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="1f01c-137">psdx_paramvalues</span></span>

- <span data-ttu-id="1f01c-138">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="1f01c-138">AuthorizationCode</span></span>
- <span data-ttu-id="1f01c-139">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="1f01c-139">ClientCredentials</span></span> 
- <span data-ttu-id="1f01c-140">Ukrytych</span><span class="sxs-lookup"><span data-stu-id="1f01c-140">Implicit</span></span> 
- <span data-ttu-id="1f01c-141">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="1f01c-141">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="1f01c-142">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f01c-142">-Name</span></span>
<span data-ttu-id="1f01c-143">Określa nazwę serwera autoryzacji, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="1f01c-143">Specifies the name of the authorization server to create.</span></span>

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

### <span data-ttu-id="1f01c-144">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="1f01c-144">-ResourceOwnerPassword</span></span>
<span data-ttu-id="1f01c-145">Określa hasło właściciela zasobu.</span><span class="sxs-lookup"><span data-stu-id="1f01c-145">Specifies the resource owner password.</span></span>
<span data-ttu-id="1f01c-146">Ten parametr należy określić jako wymagany, jeśli ResourceOwnerPassword jest określony przez parametr *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="1f01c-146">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="1f01c-147">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="1f01c-147">-ResourceOwnerUsername</span></span>
<span data-ttu-id="1f01c-148">Określa nazwę użytkownika właściciela zasobu.</span><span class="sxs-lookup"><span data-stu-id="1f01c-148">Specifies the resource owner user name.</span></span>
<span data-ttu-id="1f01c-149">Ten parametr należy określić, jeśli ResourceOwnerPassword jest określony za pomocą parametru *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="1f01c-149">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="1f01c-150">-ServerId</span><span class="sxs-lookup"><span data-stu-id="1f01c-150">-ServerId</span></span>
<span data-ttu-id="1f01c-151">Określa identyfikator serwera autoryzacji, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="1f01c-151">Specifies the ID of the authorization server to create.</span></span>

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

### <span data-ttu-id="1f01c-152">-SupportState</span><span class="sxs-lookup"><span data-stu-id="1f01c-152">-SupportState</span></span>
<span data-ttu-id="1f01c-153">Wskazuje, czy ma być obsługiwany parametr *State* .</span><span class="sxs-lookup"><span data-stu-id="1f01c-153">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="1f01c-154">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="1f01c-154">-TokenBodyParameters</span></span>
<span data-ttu-id="1f01c-155">Określa dodatkowe parametry treści przy użyciu formatu **Application/x-www-form-urlencoded** .</span><span class="sxs-lookup"><span data-stu-id="1f01c-155">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

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

### <span data-ttu-id="1f01c-156">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="1f01c-156">-TokenEndpointUrl</span></span>
<span data-ttu-id="1f01c-157">Określa adres URL punktu końcowego tokenu, który jest wykorzystywany przez klientów do uzyskiwania tokenów dostępu w programie Exchange w celu prezentowania uprawnień do autoryzacji lub odświeżania tokenów.</span><span class="sxs-lookup"><span data-stu-id="1f01c-157">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="1f01c-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f01c-158">-DefaultProfile</span></span>
<span data-ttu-id="1f01c-159">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f01c-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f01c-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f01c-160">CommonParameters</span></span>
<span data-ttu-id="1f01c-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f01c-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f01c-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f01c-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f01c-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f01c-163">INPUTS</span></span>

## <span data-ttu-id="1f01c-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f01c-164">OUTPUTS</span></span>

### <span data-ttu-id="1f01c-165">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="1f01c-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="1f01c-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f01c-166">NOTES</span></span>

## <span data-ttu-id="1f01c-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f01c-167">RELATED LINKS</span></span>

