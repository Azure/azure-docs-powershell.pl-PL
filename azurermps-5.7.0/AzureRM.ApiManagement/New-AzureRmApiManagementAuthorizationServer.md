---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: f1853c8f9e1e8449d0b607cadede215ec42b8952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717022"
---
# <span data-ttu-id="3b380-101">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3b380-101">New-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="3b380-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b380-102">SYNOPSIS</span></span>
<span data-ttu-id="3b380-103">Tworzy serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="3b380-103">Creates an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b380-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b380-104">SYNTAX</span></span>

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

## <span data-ttu-id="3b380-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3b380-105">DESCRIPTION</span></span>
<span data-ttu-id="3b380-106">Polecenie cmdlet **New-AzureRmApiManagementAuthorizationServer** tworzy serwer autoryzacji zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="3b380-106">The **New-AzureRmApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="3b380-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b380-107">EXAMPLES</span></span>

### <span data-ttu-id="3b380-108">Przykład 1. Tworzenie serwera autoryzacji</span><span class="sxs-lookup"><span data-stu-id="3b380-108">Example 1: Create an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="3b380-109">To polecenie tworzy serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="3b380-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="3b380-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b380-110">PARAMETERS</span></span>

### <span data-ttu-id="3b380-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="3b380-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="3b380-112">Określa tablicę metod wysyłania tokena dostępu.</span><span class="sxs-lookup"><span data-stu-id="3b380-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="3b380-113">psdx_paramvalues AuthorizationHeader i Query.</span><span class="sxs-lookup"><span data-stu-id="3b380-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

```yaml
Type: PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="3b380-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="3b380-115">Określa punkt końcowy autoryzacji w celu uwierzytelnienia właścicieli zasobów i uzyskania dotacji na autoryzację.</span><span class="sxs-lookup"><span data-stu-id="3b380-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="3b380-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="3b380-117">Określa tablicę metod żądań autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="3b380-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="3b380-118">Prawidłowe wartości: GET, POST.</span><span class="sxs-lookup"><span data-stu-id="3b380-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="3b380-119">Wartość domyślna to GET.</span><span class="sxs-lookup"><span data-stu-id="3b380-119">The default value is GET.</span></span>

```yaml
Type: PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Get, Post

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="3b380-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="3b380-121">Określa tablicę metod uwierzytelniania klienta.</span><span class="sxs-lookup"><span data-stu-id="3b380-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="3b380-122">psdx_paramvalues podstawowy i podstawowy.</span><span class="sxs-lookup"><span data-stu-id="3b380-122">psdx_paramvalues Basic and Body.</span></span>

```yaml
Type: PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="3b380-123">-ClientId</span></span>
<span data-ttu-id="3b380-124">Określa identyfikator klienta konsoli dewelopera, która jest aplikacją kliencką.</span><span class="sxs-lookup"><span data-stu-id="3b380-124">Specifies the client ID of the developer console that is the client application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="3b380-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="3b380-126">Umożliwia określenie punktu końcowego rejestracji klienta w celu zarejestrowania klientów na serwerze autoryzacji i uzyskania poświadczeń klienta.</span><span class="sxs-lookup"><span data-stu-id="3b380-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="3b380-127">-ClientSecret</span></span>
<span data-ttu-id="3b380-128">Określa klucz tajny klienta konsoli dewelopera, która jest aplikacją kliencką.</span><span class="sxs-lookup"><span data-stu-id="3b380-128">Specifies the client secret of developer console that is the client application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-129">-Context</span><span class="sxs-lookup"><span data-stu-id="3b380-129">-Context</span></span>
<span data-ttu-id="3b380-130">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3b380-130">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b380-131">-DefaultProfile</span></span>
<span data-ttu-id="3b380-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b380-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="3b380-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="3b380-133">-DefaultScope</span></span>
<span data-ttu-id="3b380-134">Określa zakres domyślny dla serwera autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="3b380-134">Specifies the default scope for the authorization server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-135">— Opis</span><span class="sxs-lookup"><span data-stu-id="3b380-135">-Description</span></span>
<span data-ttu-id="3b380-136">Określa opis serwera autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="3b380-136">Specifies a description for an authorization server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="3b380-137">-GrantTypes</span></span>
<span data-ttu-id="3b380-138">Określa tablicę typów dotacji.</span><span class="sxs-lookup"><span data-stu-id="3b380-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="3b380-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="3b380-139">psdx_paramvalues</span></span>

- <span data-ttu-id="3b380-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="3b380-140">AuthorizationCode</span></span>
- <span data-ttu-id="3b380-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="3b380-141">ClientCredentials</span></span> 
- <span data-ttu-id="3b380-142">Ukrytych</span><span class="sxs-lookup"><span data-stu-id="3b380-142">Implicit</span></span> 
- <span data-ttu-id="3b380-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="3b380-143">ResourceOwnerPassword</span></span>

```yaml
Type: PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases: 
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3b380-144">-Name</span></span>
<span data-ttu-id="3b380-145">Określa nazwę serwera autoryzacji, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="3b380-145">Specifies the name of the authorization server to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-146">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="3b380-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="3b380-147">Określa hasło właściciela zasobu.</span><span class="sxs-lookup"><span data-stu-id="3b380-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="3b380-148">Ten parametr należy określić jako wymagany, jeśli ResourceOwnerPassword jest określony przez parametr *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="3b380-148">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-149">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="3b380-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="3b380-150">Określa nazwę użytkownika właściciela zasobu.</span><span class="sxs-lookup"><span data-stu-id="3b380-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="3b380-151">Ten parametr należy określić, jeśli ResourceOwnerPassword jest określony za pomocą parametru *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="3b380-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-152">-ServerId</span><span class="sxs-lookup"><span data-stu-id="3b380-152">-ServerId</span></span>
<span data-ttu-id="3b380-153">Określa identyfikator serwera autoryzacji, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="3b380-153">Specifies the ID of the authorization server to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-154">-SupportState</span><span class="sxs-lookup"><span data-stu-id="3b380-154">-SupportState</span></span>
<span data-ttu-id="3b380-155">Wskazuje, czy ma być obsługiwany parametr *State* .</span><span class="sxs-lookup"><span data-stu-id="3b380-155">Indicates whether to support the *State* parameter.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="3b380-156">-TokenBodyParameters</span></span>
<span data-ttu-id="3b380-157">Określa dodatkowe parametry treści przy użyciu formatu **Application/x-www-form-urlencoded** .</span><span class="sxs-lookup"><span data-stu-id="3b380-157">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="3b380-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="3b380-159">Określa adres URL punktu końcowego tokenu, który jest wykorzystywany przez klientów do uzyskiwania tokenów dostępu w programie Exchange w celu prezentowania uprawnień do autoryzacji lub odświeżania tokenów.</span><span class="sxs-lookup"><span data-stu-id="3b380-159">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b380-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b380-160">CommonParameters</span></span>
<span data-ttu-id="3b380-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b380-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b380-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b380-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b380-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b380-163">INPUTS</span></span>

### <span data-ttu-id="3b380-164">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3b380-164">None</span></span>
<span data-ttu-id="3b380-165">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3b380-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b380-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b380-166">OUTPUTS</span></span>

### <span data-ttu-id="3b380-167">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="3b380-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="3b380-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b380-168">NOTES</span></span>

## <span data-ttu-id="3b380-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b380-169">RELATED LINKS</span></span>

