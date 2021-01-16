---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 3312c725d63bcb42aab7d82144c5a8f6f8e67641
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364595"
---
# <span data-ttu-id="d5a48-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d5a48-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="d5a48-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5a48-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a48-103">Tworzy interfejs API.</span><span class="sxs-lookup"><span data-stu-id="d5a48-103">Creates an API.</span></span>

## <span data-ttu-id="d5a48-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5a48-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5a48-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d5a48-105">DESCRIPTION</span></span>
<span data-ttu-id="d5a48-106">Polecenie cmdlet **New-AzApiManagementApi** tworzy interfejs API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="d5a48-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="d5a48-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5a48-107">EXAMPLES</span></span>

### <span data-ttu-id="d5a48-108">Przykład 1. Tworzenie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="d5a48-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="d5a48-109">To polecenie tworzy interfejs API o nazwie EchoApi z określonym adresem URL.</span><span class="sxs-lookup"><span data-stu-id="d5a48-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="d5a48-110">Przykład 2: Tworzenie interfejsu API przez skopiowanie wszystkich operacji, tagów, produktów i zasad z funkcji echo-API i w ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d5a48-110">Example 2: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
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

<span data-ttu-id="d5a48-111">To polecenie tworzy interfejs API `echoapiv3` w ApiVersionSet `xmsVersionSet` i kopiuje wszystkie operacje, Tagi i zasady ze źródłowego interfejsu API `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="d5a48-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="d5a48-112">Zastępuje ona SubscriptionRequired, ServiceUrl, ścieżkę, protokoły</span><span class="sxs-lookup"><span data-stu-id="d5a48-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

### <span data-ttu-id="d5a48-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d5a48-113">Example 3</span></span>

<span data-ttu-id="d5a48-114">Tworzy interfejs API.</span><span class="sxs-lookup"><span data-stu-id="d5a48-114">Creates an API.</span></span> <span data-ttu-id="d5a48-115">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="d5a48-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementApi -ApiId '0001' -Context <PsApiManagementContext> -Name 'Echo api' -Path 'echov3' -Protocols Http -ServiceUrl 'https://contoso.com/apis/echo'
```

## <span data-ttu-id="d5a48-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5a48-116">PARAMETERS</span></span>

### <span data-ttu-id="d5a48-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d5a48-117">-ApiId</span></span>
<span data-ttu-id="d5a48-118">Określa identyfikator interfejsu API, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="d5a48-118">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="d5a48-119">Jeśli nie określisz tego parametru, to polecenie cmdlet wygeneruje identyfikator.</span><span class="sxs-lookup"><span data-stu-id="d5a48-119">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="d5a48-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d5a48-120">-ApiVersion</span></span>
<span data-ttu-id="d5a48-121">Wersja API interfejsu API do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="d5a48-121">Api Version of the Api to create.</span></span> <span data-ttu-id="d5a48-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d5a48-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="d5a48-123">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="d5a48-123">-ApiVersionDescription</span></span>
<span data-ttu-id="d5a48-124">Opis wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d5a48-124">Api Version Description.</span></span> <span data-ttu-id="d5a48-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d5a48-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="d5a48-126">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="d5a48-126">-ApiVersionSetId</span></span>
<span data-ttu-id="d5a48-127">Identyfikator zasobu powiązanego zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d5a48-127">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="d5a48-128">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d5a48-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="d5a48-129">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="d5a48-129">-AuthorizationScope</span></span>
<span data-ttu-id="d5a48-130">Określa zakres operacji uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="d5a48-130">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="d5a48-131">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="d5a48-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="d5a48-132">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="d5a48-132">-AuthorizationServerId</span></span>
<span data-ttu-id="d5a48-133">Określa identyfikator serwera autoryzacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="d5a48-133">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="d5a48-134">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="d5a48-134">The default value is $Null.</span></span>
<span data-ttu-id="d5a48-135">Ten parametr należy określić, jeśli *AuthorizationScope* jest określony.</span><span class="sxs-lookup"><span data-stu-id="d5a48-135">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="d5a48-136">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="d5a48-136">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="d5a48-137">OpenId mechanizm serwera autoryzacji, w którym token dostępu jest przekazywany do interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d5a48-137">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="d5a48-138">Zobacz http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="d5a48-138">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="d5a48-139">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d5a48-139">This parameter is optional.</span></span> <span data-ttu-id="d5a48-140">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="d5a48-140">Default value is $null.</span></span>

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

### <span data-ttu-id="d5a48-141">-Context</span><span class="sxs-lookup"><span data-stu-id="d5a48-141">-Context</span></span>
<span data-ttu-id="d5a48-142">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d5a48-142">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d5a48-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a48-143">-DefaultProfile</span></span>
<span data-ttu-id="d5a48-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a48-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5a48-145">— Opis</span><span class="sxs-lookup"><span data-stu-id="d5a48-145">-Description</span></span>
<span data-ttu-id="d5a48-146">Określa opis interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d5a48-146">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="d5a48-147">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d5a48-147">-Name</span></span>
<span data-ttu-id="d5a48-148">Określa nazwę internetowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d5a48-148">Specifies the name of the web API.</span></span>
<span data-ttu-id="d5a48-149">Jest to publiczna nazwa interfejsu API, która jest wyświetlana w portalach dewelopera i administratora.</span><span class="sxs-lookup"><span data-stu-id="d5a48-149">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="d5a48-150">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="d5a48-150">-OpenIdProviderId</span></span>
<span data-ttu-id="d5a48-151">Identyfikator serwera autoryzacji OpenId.</span><span class="sxs-lookup"><span data-stu-id="d5a48-151">OpenId authorization server identifier.</span></span> <span data-ttu-id="d5a48-152">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d5a48-152">This parameter is optional.</span></span> <span data-ttu-id="d5a48-153">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="d5a48-153">Default value is $null.</span></span> <span data-ttu-id="d5a48-154">Należy określić, czy BearerTokenSendingMethods jest określony.</span><span class="sxs-lookup"><span data-stu-id="d5a48-154">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="d5a48-155">-Path</span><span class="sxs-lookup"><span data-stu-id="d5a48-155">-Path</span></span>
<span data-ttu-id="d5a48-156">Określa ścieżkę internetowego interfejsu API, która jest ostatnią częścią publicznego adresu URL interfejsu API i odpowiada polu sufiksu adresu URL interfejsu API sieci Web w portalu administracyjnym.</span><span class="sxs-lookup"><span data-stu-id="d5a48-156">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="d5a48-157">Ten adres URL jest wykorzystywany przez użytkowników korzystających z interfejsu API do wysyłania żądań do usługi sieci Web i musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="d5a48-157">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="d5a48-158">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="d5a48-158">The default value is $Null.</span></span>

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

### <span data-ttu-id="d5a48-159">-ProductId</span><span class="sxs-lookup"><span data-stu-id="d5a48-159">-ProductIds</span></span>
<span data-ttu-id="d5a48-160">Określa tablicę identyfikatorów produktów, do których ma zostać dodany nowy interfejs API.</span><span class="sxs-lookup"><span data-stu-id="d5a48-160">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="d5a48-161">-Protokoły</span><span class="sxs-lookup"><span data-stu-id="d5a48-161">-Protocols</span></span>
<span data-ttu-id="d5a48-162">Określa tablicę protokołów API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d5a48-162">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="d5a48-163">Prawidłowe wartości to http, https.</span><span class="sxs-lookup"><span data-stu-id="d5a48-163">Valid values are http, https.</span></span>
<span data-ttu-id="d5a48-164">To są protokoły sieci Web, w których udostępniono interfejs API.</span><span class="sxs-lookup"><span data-stu-id="d5a48-164">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="d5a48-165">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="d5a48-165">The default value is $Null.</span></span>

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

### <span data-ttu-id="d5a48-166">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="d5a48-166">-ServiceUrl</span></span>
<span data-ttu-id="d5a48-167">Określa adres URL usługi sieci Web, która udostępnia interfejs API.</span><span class="sxs-lookup"><span data-stu-id="d5a48-167">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="d5a48-168">Ten adres URL jest wykorzystywany tylko przez usługę Azure API Management i nie został podany jako publiczny.</span><span class="sxs-lookup"><span data-stu-id="d5a48-168">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="d5a48-169">Adres URL musi zawierać od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="d5a48-169">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="d5a48-170">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="d5a48-170">-SourceApiId</span></span>
<span data-ttu-id="d5a48-171">Identyfikator API źródłowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d5a48-171">Api identifier of the source API.</span></span> <span data-ttu-id="d5a48-172">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d5a48-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="d5a48-173">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="d5a48-173">-SourceApiRevision</span></span>
<span data-ttu-id="d5a48-174">Wersja API źródłowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d5a48-174">Api Revision of the source API.</span></span> <span data-ttu-id="d5a48-175">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d5a48-175">This parameter is optional.</span></span>

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

### <span data-ttu-id="d5a48-176">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="d5a48-176">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="d5a48-177">Określa nazwę nagłówka klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d5a48-177">Specifies the subscription key header name.</span></span>
<span data-ttu-id="d5a48-178">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="d5a48-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="d5a48-179">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="d5a48-179">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="d5a48-180">Określa nazwę parametru ciągu kwerendy klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d5a48-180">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="d5a48-181">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="d5a48-181">The default value is $Null.</span></span>

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

### <span data-ttu-id="d5a48-182">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="d5a48-182">-SubscriptionRequired</span></span>
<span data-ttu-id="d5a48-183">Flaga wymuszania SubscriptionRequired dla żądań w interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="d5a48-183">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="d5a48-184">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d5a48-184">This parameter is optional.</span></span>

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

### <span data-ttu-id="d5a48-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a48-185">CommonParameters</span></span>
<span data-ttu-id="d5a48-186">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a48-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a48-187">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5a48-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a48-188">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5a48-188">INPUTS</span></span>

### <span data-ttu-id="d5a48-189">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d5a48-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d5a48-190">System. String</span><span class="sxs-lookup"><span data-stu-id="d5a48-190">System.String</span></span>

### <span data-ttu-id="d5a48-191">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="d5a48-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="d5a48-192">System. String []</span><span class="sxs-lookup"><span data-stu-id="d5a48-192">System.String[]</span></span>

## <span data-ttu-id="d5a48-193">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5a48-193">OUTPUTS</span></span>

### <span data-ttu-id="d5a48-194">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d5a48-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="d5a48-195">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5a48-195">NOTES</span></span>

## <span data-ttu-id="d5a48-196">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5a48-196">RELATED LINKS</span></span>

[<span data-ttu-id="d5a48-197">Eksportowanie — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d5a48-197">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="d5a48-198">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d5a48-198">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="d5a48-199">Import — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d5a48-199">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="d5a48-200">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d5a48-200">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="d5a48-201">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d5a48-201">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


