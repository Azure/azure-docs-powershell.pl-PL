---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: b332ccc8dc9188259c897c53256f1a14fd96280e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707043"
---
# <span data-ttu-id="a93f6-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a93f6-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="a93f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a93f6-102">SYNOPSIS</span></span>
<span data-ttu-id="a93f6-103">Tworzy interfejs API.</span><span class="sxs-lookup"><span data-stu-id="a93f6-103">Creates an API.</span></span>

## <span data-ttu-id="a93f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a93f6-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a93f6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a93f6-105">DESCRIPTION</span></span>
<span data-ttu-id="a93f6-106">Polecenie cmdlet **New-AzApiManagementApi** tworzy interfejs API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="a93f6-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="a93f6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a93f6-107">EXAMPLES</span></span>

### <span data-ttu-id="a93f6-108">Przykład 1. Tworzenie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="a93f6-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="a93f6-109">To polecenie tworzy interfejs API o nazwie EchoApi z określonym adresem URL.</span><span class="sxs-lookup"><span data-stu-id="a93f6-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="a93f6-110">Przykład 1. Utwórz interfejs API, kopiując wszystkie operacje, Tagi, produkty i zasady z funkcji echo-API i w ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a93f6-110">Example 1: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
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

<span data-ttu-id="a93f6-111">To polecenie tworzy interfejs API `echoapiv3` w ApiVersionSet `xmsVersionSet` i kopiuje wszystkie operacje, Tagi i zasady ze źródłowego interfejsu API `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="a93f6-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="a93f6-112">Zastępuje ona SubscriptionRequired, ServiceUrl, ścieżkę, protokoły</span><span class="sxs-lookup"><span data-stu-id="a93f6-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

## <span data-ttu-id="a93f6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a93f6-113">PARAMETERS</span></span>

### <span data-ttu-id="a93f6-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a93f6-114">-ApiId</span></span>
<span data-ttu-id="a93f6-115">Określa identyfikator interfejsu API, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="a93f6-115">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="a93f6-116">Jeśli nie określisz tego parametru, to polecenie cmdlet wygeneruje identyfikator.</span><span class="sxs-lookup"><span data-stu-id="a93f6-116">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="a93f6-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a93f6-117">-ApiVersion</span></span>
<span data-ttu-id="a93f6-118">Wersja API interfejsu API do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="a93f6-118">Api Version of the Api to create.</span></span> <span data-ttu-id="a93f6-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a93f6-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="a93f6-120">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="a93f6-120">-ApiVersionDescription</span></span>
<span data-ttu-id="a93f6-121">Opis wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a93f6-121">Api Version Description.</span></span> <span data-ttu-id="a93f6-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a93f6-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="a93f6-123">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="a93f6-123">-ApiVersionSetId</span></span>
<span data-ttu-id="a93f6-124">Identyfikator zasobu powiązanego zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a93f6-124">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="a93f6-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a93f6-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="a93f6-126">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="a93f6-126">-AuthorizationScope</span></span>
<span data-ttu-id="a93f6-127">Określa zakres operacji uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="a93f6-127">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="a93f6-128">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="a93f6-128">The default value is $Null.</span></span>

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

### <span data-ttu-id="a93f6-129">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="a93f6-129">-AuthorizationServerId</span></span>
<span data-ttu-id="a93f6-130">Określa identyfikator serwera autoryzacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="a93f6-130">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="a93f6-131">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="a93f6-131">The default value is $Null.</span></span>
<span data-ttu-id="a93f6-132">Ten parametr należy określić, jeśli *AuthorizationScope* jest określony.</span><span class="sxs-lookup"><span data-stu-id="a93f6-132">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="a93f6-133">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="a93f6-133">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="a93f6-134">OpenId mechanizm serwera autoryzacji, w którym token dostępu jest przekazywany do interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a93f6-134">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="a93f6-135">Zobacz http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="a93f6-135">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="a93f6-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a93f6-136">This parameter is optional.</span></span> <span data-ttu-id="a93f6-137">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="a93f6-137">Default value is $null.</span></span>

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

### <span data-ttu-id="a93f6-138">-Context</span><span class="sxs-lookup"><span data-stu-id="a93f6-138">-Context</span></span>
<span data-ttu-id="a93f6-139">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a93f6-139">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a93f6-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a93f6-140">-DefaultProfile</span></span>
<span data-ttu-id="a93f6-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a93f6-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a93f6-142">— Opis</span><span class="sxs-lookup"><span data-stu-id="a93f6-142">-Description</span></span>
<span data-ttu-id="a93f6-143">Określa opis interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a93f6-143">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="a93f6-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a93f6-144">-Name</span></span>
<span data-ttu-id="a93f6-145">Określa nazwę internetowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a93f6-145">Specifies the name of the web API.</span></span>
<span data-ttu-id="a93f6-146">Jest to publiczna nazwa interfejsu API, która jest wyświetlana w portalach dewelopera i administratora.</span><span class="sxs-lookup"><span data-stu-id="a93f6-146">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="a93f6-147">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="a93f6-147">-OpenIdProviderId</span></span>
<span data-ttu-id="a93f6-148">Identyfikator serwera autoryzacji OpenId.</span><span class="sxs-lookup"><span data-stu-id="a93f6-148">OpenId authorization server identifier.</span></span> <span data-ttu-id="a93f6-149">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a93f6-149">This parameter is optional.</span></span> <span data-ttu-id="a93f6-150">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="a93f6-150">Default value is $null.</span></span> <span data-ttu-id="a93f6-151">Należy określić, czy BearerTokenSendingMethods jest określony.</span><span class="sxs-lookup"><span data-stu-id="a93f6-151">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="a93f6-152">-Path</span><span class="sxs-lookup"><span data-stu-id="a93f6-152">-Path</span></span>
<span data-ttu-id="a93f6-153">Określa ścieżkę internetowego interfejsu API, która jest ostatnią częścią publicznego adresu URL interfejsu API i odpowiada polu sufiksu adresu URL interfejsu API sieci Web w portalu administracyjnym.</span><span class="sxs-lookup"><span data-stu-id="a93f6-153">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="a93f6-154">Ten adres URL jest wykorzystywany przez użytkowników korzystających z interfejsu API do wysyłania żądań do usługi sieci Web i musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="a93f6-154">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="a93f6-155">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="a93f6-155">The default value is $Null.</span></span>

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

### <span data-ttu-id="a93f6-156">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a93f6-156">-ProductIds</span></span>
<span data-ttu-id="a93f6-157">Określa tablicę identyfikatorów produktów, do których ma zostać dodany nowy interfejs API.</span><span class="sxs-lookup"><span data-stu-id="a93f6-157">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="a93f6-158">-Protokoły</span><span class="sxs-lookup"><span data-stu-id="a93f6-158">-Protocols</span></span>
<span data-ttu-id="a93f6-159">Określa tablicę protokołów API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a93f6-159">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="a93f6-160">Prawidłowe wartości to http, https.</span><span class="sxs-lookup"><span data-stu-id="a93f6-160">Valid values are http, https.</span></span>
<span data-ttu-id="a93f6-161">To są protokoły sieci Web, w których udostępniono interfejs API.</span><span class="sxs-lookup"><span data-stu-id="a93f6-161">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="a93f6-162">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="a93f6-162">The default value is $Null.</span></span>

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

### <span data-ttu-id="a93f6-163">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="a93f6-163">-ServiceUrl</span></span>
<span data-ttu-id="a93f6-164">Określa adres URL usługi sieci Web, która udostępnia interfejs API.</span><span class="sxs-lookup"><span data-stu-id="a93f6-164">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="a93f6-165">Ten adres URL jest wykorzystywany tylko przez usługę Azure API Management i nie został podany jako publiczny.</span><span class="sxs-lookup"><span data-stu-id="a93f6-165">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="a93f6-166">Adres URL musi zawierać od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="a93f6-166">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="a93f6-167">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="a93f6-167">-SourceApiId</span></span>
<span data-ttu-id="a93f6-168">Identyfikator API źródłowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a93f6-168">Api identifier of the source API.</span></span> <span data-ttu-id="a93f6-169">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a93f6-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="a93f6-170">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="a93f6-170">-SourceApiRevision</span></span>
<span data-ttu-id="a93f6-171">Wersja API źródłowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a93f6-171">Api Revision of the source API.</span></span> <span data-ttu-id="a93f6-172">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a93f6-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="a93f6-173">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="a93f6-173">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="a93f6-174">Określa nazwę nagłówka klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a93f6-174">Specifies the subscription key header name.</span></span>
<span data-ttu-id="a93f6-175">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="a93f6-175">The default value is $Null.</span></span>

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

### <span data-ttu-id="a93f6-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="a93f6-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="a93f6-177">Określa nazwę parametru ciągu kwerendy klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a93f6-177">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="a93f6-178">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="a93f6-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="a93f6-179">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="a93f6-179">-SubscriptionRequired</span></span>
<span data-ttu-id="a93f6-180">Flaga wymuszania SubscriptionRequired dla żądań w interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="a93f6-180">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="a93f6-181">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a93f6-181">This parameter is optional.</span></span>

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

### <span data-ttu-id="a93f6-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93f6-182">CommonParameters</span></span>
<span data-ttu-id="a93f6-183">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a93f6-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93f6-184">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a93f6-184">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93f6-185">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a93f6-185">INPUTS</span></span>

### <span data-ttu-id="a93f6-186">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a93f6-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a93f6-187">System. String</span><span class="sxs-lookup"><span data-stu-id="a93f6-187">System.String</span></span>

### <span data-ttu-id="a93f6-188">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="a93f6-188">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="a93f6-189">System. String []</span><span class="sxs-lookup"><span data-stu-id="a93f6-189">System.String[]</span></span>

## <span data-ttu-id="a93f6-190">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a93f6-190">OUTPUTS</span></span>

### <span data-ttu-id="a93f6-191">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a93f6-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="a93f6-192">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a93f6-192">NOTES</span></span>

## <span data-ttu-id="a93f6-193">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a93f6-193">RELATED LINKS</span></span>

[<span data-ttu-id="a93f6-194">Eksportowanie — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a93f6-194">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="a93f6-195">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a93f6-195">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="a93f6-196">Import — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a93f6-196">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="a93f6-197">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a93f6-197">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="a93f6-198">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a93f6-198">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


