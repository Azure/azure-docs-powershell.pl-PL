---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: c9c0ab0ed8b932892f2bea27ff811197b808b86b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053966"
---
# <span data-ttu-id="cfa54-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cfa54-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="cfa54-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cfa54-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa54-103">Tworzy interfejs API.</span><span class="sxs-lookup"><span data-stu-id="cfa54-103">Creates an API.</span></span>

## <span data-ttu-id="cfa54-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cfa54-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfa54-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cfa54-105">DESCRIPTION</span></span>
<span data-ttu-id="cfa54-106">Polecenie cmdlet **New-AzApiManagementApi** tworzy interfejs API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="cfa54-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="cfa54-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cfa54-107">EXAMPLES</span></span>

### <span data-ttu-id="cfa54-108">Przykład 1. Tworzenie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="cfa54-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="cfa54-109">To polecenie tworzy interfejs API o nazwie EchoApi z określonym adresem URL.</span><span class="sxs-lookup"><span data-stu-id="cfa54-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="cfa54-110">Przykład 1. Utwórz interfejs API, kopiując wszystkie operacje, Tagi, produkty i zasady z funkcji echo-API i w ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cfa54-110">Example 1: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
```powershell
PS D:\github\azure-powershell>$context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso
PS D:\github\azure-powershell>$versionSet = Get-AzApiManagementApiVersionSet -Context $context -ApiVersionSetId "xmsVersionSet"
PS D:\github\azure-powershell> New-AzApiManagementApi -Context $context -Name "echoapiv4" -Description "Create Echo Api V4" -SubscriptionRequired -ServiceUrl "https://echoapi.cloudapp.net/v4" -Path "echov3" -Protocols @("http", "https") -ApiVersionSetId $versionSet.ApiVersionSetId -SourceApiId "echo-api" -ApiVersion "v4"


ApiId                         : 691b7d410125414a929c108541c60e06
Name                          : echoapiv4
Description                   : Create Echo Api V4
ServiceUrl                    : https://echoapi.cloudapp.net/v4 
Path                          : echov3
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v4
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/xmsVersionSet
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/691b7d410125414a929c108541c60e06    
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="cfa54-111">To polecenie tworzy interfejs API `echoapiv3` w ApiVersionSet `xmsVersionSet` i kopiuje wszystkie operacje, Tagi i zasady ze źródłowego interfejsu API `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="cfa54-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="cfa54-112">Zastępuje ona SubscriptionRequired, ServiceUrl, ścieżkę, protokoły</span><span class="sxs-lookup"><span data-stu-id="cfa54-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

## <span data-ttu-id="cfa54-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cfa54-113">PARAMETERS</span></span>

### <span data-ttu-id="cfa54-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cfa54-114">-ApiId</span></span>
<span data-ttu-id="cfa54-115">Określa identyfikator interfejsu API, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="cfa54-115">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="cfa54-116">Jeśli nie określisz tego parametru, to polecenie cmdlet wygeneruje identyfikator.</span><span class="sxs-lookup"><span data-stu-id="cfa54-116">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="cfa54-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cfa54-117">-ApiVersion</span></span>
<span data-ttu-id="cfa54-118">Wersja API interfejsu API do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="cfa54-118">Api Version of the Api to create.</span></span> <span data-ttu-id="cfa54-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="cfa54-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="cfa54-120">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="cfa54-120">-ApiVersionDescription</span></span>
<span data-ttu-id="cfa54-121">Opis wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="cfa54-121">Api Version Description.</span></span> <span data-ttu-id="cfa54-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="cfa54-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="cfa54-123">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="cfa54-123">-ApiVersionSetId</span></span>
<span data-ttu-id="cfa54-124">Identyfikator zasobu powiązanego zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="cfa54-124">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="cfa54-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="cfa54-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="cfa54-126">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="cfa54-126">-AuthorizationScope</span></span>
<span data-ttu-id="cfa54-127">Określa zakres operacji uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="cfa54-127">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="cfa54-128">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="cfa54-128">The default value is $Null.</span></span>

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

### <span data-ttu-id="cfa54-129">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="cfa54-129">-AuthorizationServerId</span></span>
<span data-ttu-id="cfa54-130">Określa identyfikator serwera autoryzacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="cfa54-130">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="cfa54-131">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="cfa54-131">The default value is $Null.</span></span>
<span data-ttu-id="cfa54-132">Ten parametr należy określić, jeśli *AuthorizationScope* jest określony.</span><span class="sxs-lookup"><span data-stu-id="cfa54-132">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="cfa54-133">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="cfa54-133">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="cfa54-134">OpenId mechanizm serwera autoryzacji, w którym token dostępu jest przekazywany do interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="cfa54-134">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="cfa54-135">Zobacz http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="cfa54-135">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="cfa54-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="cfa54-136">This parameter is optional.</span></span> <span data-ttu-id="cfa54-137">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="cfa54-137">Default value is $null.</span></span>

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

### <span data-ttu-id="cfa54-138">-Context</span><span class="sxs-lookup"><span data-stu-id="cfa54-138">-Context</span></span>
<span data-ttu-id="cfa54-139">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="cfa54-139">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa54-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfa54-140">-DefaultProfile</span></span>
<span data-ttu-id="cfa54-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa54-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfa54-142">— Opis</span><span class="sxs-lookup"><span data-stu-id="cfa54-142">-Description</span></span>
<span data-ttu-id="cfa54-143">Określa opis interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="cfa54-143">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="cfa54-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cfa54-144">-Name</span></span>
<span data-ttu-id="cfa54-145">Określa nazwę internetowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="cfa54-145">Specifies the name of the web API.</span></span>
<span data-ttu-id="cfa54-146">Jest to publiczna nazwa interfejsu API, która jest wyświetlana w portalach dewelopera i administratora.</span><span class="sxs-lookup"><span data-stu-id="cfa54-146">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="cfa54-147">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="cfa54-147">-OpenIdProviderId</span></span>
<span data-ttu-id="cfa54-148">Identyfikator serwera autoryzacji OpenId.</span><span class="sxs-lookup"><span data-stu-id="cfa54-148">OpenId authorization server identifier.</span></span> <span data-ttu-id="cfa54-149">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="cfa54-149">This parameter is optional.</span></span> <span data-ttu-id="cfa54-150">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="cfa54-150">Default value is $null.</span></span> <span data-ttu-id="cfa54-151">Należy określić, czy BearerTokenSendingMethods jest określony.</span><span class="sxs-lookup"><span data-stu-id="cfa54-151">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="cfa54-152">-Path</span><span class="sxs-lookup"><span data-stu-id="cfa54-152">-Path</span></span>
<span data-ttu-id="cfa54-153">Określa ścieżkę internetowego interfejsu API, która jest ostatnią częścią publicznego adresu URL interfejsu API i odpowiada polu sufiksu adresu URL interfejsu API sieci Web w portalu administracyjnym.</span><span class="sxs-lookup"><span data-stu-id="cfa54-153">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="cfa54-154">Ten adres URL jest wykorzystywany przez użytkowników korzystających z interfejsu API do wysyłania żądań do usługi sieci Web i musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="cfa54-154">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="cfa54-155">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="cfa54-155">The default value is $Null.</span></span>

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

### <span data-ttu-id="cfa54-156">-ProductId</span><span class="sxs-lookup"><span data-stu-id="cfa54-156">-ProductIds</span></span>
<span data-ttu-id="cfa54-157">Określa tablicę identyfikatorów produktów, do których ma zostać dodany nowy interfejs API.</span><span class="sxs-lookup"><span data-stu-id="cfa54-157">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="cfa54-158">-Protokoły</span><span class="sxs-lookup"><span data-stu-id="cfa54-158">-Protocols</span></span>
<span data-ttu-id="cfa54-159">Określa tablicę protokołów API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="cfa54-159">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="cfa54-160">Prawidłowe wartości to http, https.</span><span class="sxs-lookup"><span data-stu-id="cfa54-160">Valid values are http, https.</span></span>
<span data-ttu-id="cfa54-161">To są protokoły sieci Web, w których udostępniono interfejs API.</span><span class="sxs-lookup"><span data-stu-id="cfa54-161">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="cfa54-162">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="cfa54-162">The default value is $Null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa54-163">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="cfa54-163">-ServiceUrl</span></span>
<span data-ttu-id="cfa54-164">Określa adres URL usługi sieci Web, która udostępnia interfejs API.</span><span class="sxs-lookup"><span data-stu-id="cfa54-164">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="cfa54-165">Ten adres URL jest wykorzystywany tylko przez usługę Azure API Management i nie został podany jako publiczny.</span><span class="sxs-lookup"><span data-stu-id="cfa54-165">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="cfa54-166">Adres URL musi zawierać od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="cfa54-166">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="cfa54-167">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="cfa54-167">-SourceApiId</span></span>
<span data-ttu-id="cfa54-168">Identyfikator API źródłowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="cfa54-168">Api identifier of the source API.</span></span> <span data-ttu-id="cfa54-169">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="cfa54-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="cfa54-170">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="cfa54-170">-SourceApiRevision</span></span>
<span data-ttu-id="cfa54-171">Wersja API źródłowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="cfa54-171">Api Revision of the source API.</span></span> <span data-ttu-id="cfa54-172">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="cfa54-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="cfa54-173">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="cfa54-173">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="cfa54-174">Określa nazwę nagłówka klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cfa54-174">Specifies the subscription key header name.</span></span>
<span data-ttu-id="cfa54-175">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="cfa54-175">The default value is $Null.</span></span>

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

### <span data-ttu-id="cfa54-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="cfa54-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="cfa54-177">Określa nazwę parametru ciągu kwerendy klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cfa54-177">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="cfa54-178">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="cfa54-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="cfa54-179">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="cfa54-179">-SubscriptionRequired</span></span>
<span data-ttu-id="cfa54-180">Flaga wymuszania SubscriptionRequired dla żądań w interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="cfa54-180">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="cfa54-181">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="cfa54-181">This parameter is optional.</span></span>

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

### <span data-ttu-id="cfa54-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa54-182">CommonParameters</span></span>
<span data-ttu-id="cfa54-183">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfa54-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfa54-184">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfa54-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa54-185">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cfa54-185">INPUTS</span></span>

### <span data-ttu-id="cfa54-186">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cfa54-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cfa54-187">System. String</span><span class="sxs-lookup"><span data-stu-id="cfa54-187">System.String</span></span>

### <span data-ttu-id="cfa54-188">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="cfa54-188">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="cfa54-189">System. String []</span><span class="sxs-lookup"><span data-stu-id="cfa54-189">System.String[]</span></span>

## <span data-ttu-id="cfa54-190">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cfa54-190">OUTPUTS</span></span>

### <span data-ttu-id="cfa54-191">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cfa54-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="cfa54-192">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cfa54-192">NOTES</span></span>

## <span data-ttu-id="cfa54-193">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cfa54-193">RELATED LINKS</span></span>

[<span data-ttu-id="cfa54-194">Eksportowanie — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cfa54-194">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="cfa54-195">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cfa54-195">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="cfa54-196">Import — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cfa54-196">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="cfa54-197">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cfa54-197">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="cfa54-198">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cfa54-198">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


