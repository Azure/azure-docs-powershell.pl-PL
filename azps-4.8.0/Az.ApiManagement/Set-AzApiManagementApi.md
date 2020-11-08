---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 02a7a35f4498724266d4c352744169d733f5eeab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063707"
---
# <span data-ttu-id="92984-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="92984-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="92984-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92984-102">SYNOPSIS</span></span>
<span data-ttu-id="92984-103">Modyfikuje interfejs API.</span><span class="sxs-lookup"><span data-stu-id="92984-103">Modifies an API.</span></span>

## <span data-ttu-id="92984-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92984-104">SYNTAX</span></span>

### <span data-ttu-id="92984-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="92984-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92984-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="92984-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92984-107">Opis</span><span class="sxs-lookup"><span data-stu-id="92984-107">DESCRIPTION</span></span>
<span data-ttu-id="92984-108">Polecenie cmdlet **Set-AzApiManagementApi** modyfikuje interfejs API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="92984-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="92984-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92984-109">EXAMPLES</span></span>

### <span data-ttu-id="92984-110">Przykład 1: modyfikowanie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="92984-110">Example 1: Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="92984-111">Przykład 2: Dodawanie interfejsu API do istniejącego ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="92984-111">Example 2: Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="92984-112">W tym przykładzie dodano interfejs API do istniejącego zestawu wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="92984-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="92984-113">Przykład 3: Zmienianie wewnętrznej bazy danych ServiceUrl, w której wskazuje interfejs API</span><span class="sxs-lookup"><span data-stu-id="92984-113">Example 3: Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="92984-114">W tym przykładzie Zaktualizowano ServiceUrl, `echo-api` do której wskazuje.</span><span class="sxs-lookup"><span data-stu-id="92984-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="92984-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92984-115">PARAMETERS</span></span>

### <span data-ttu-id="92984-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="92984-116">-ApiId</span></span>
<span data-ttu-id="92984-117">Określa identyfikator interfejsu API do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="92984-117">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="92984-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="92984-118">-AuthorizationScope</span></span>
<span data-ttu-id="92984-119">Określa zakres operacji uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="92984-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="92984-120">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="92984-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="92984-121">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="92984-121">-AuthorizationServerId</span></span>
<span data-ttu-id="92984-122">Określa identyfikator serwera autoryzacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="92984-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="92984-123">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="92984-123">The default value is $Null.</span></span>
<span data-ttu-id="92984-124">Ten parametr należy określić, jeśli *AuthorizationScope* jest określony.</span><span class="sxs-lookup"><span data-stu-id="92984-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="92984-125">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="92984-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="92984-126">OpenId mechanizm serwera autoryzacji, w którym token dostępu jest przekazywany do interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="92984-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="92984-127">Zobacz http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="92984-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="92984-128">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="92984-128">This parameter is optional.</span></span> <span data-ttu-id="92984-129">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="92984-129">Default value is $null.</span></span>

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

### <span data-ttu-id="92984-130">-Context</span><span class="sxs-lookup"><span data-stu-id="92984-130">-Context</span></span>
<span data-ttu-id="92984-131">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="92984-131">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="92984-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92984-132">-DefaultProfile</span></span>
<span data-ttu-id="92984-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92984-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92984-134">— Opis</span><span class="sxs-lookup"><span data-stu-id="92984-134">-Description</span></span>
<span data-ttu-id="92984-135">Określa opis interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="92984-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="92984-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="92984-136">-InputObject</span></span>
<span data-ttu-id="92984-137">Wystąpienie PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="92984-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="92984-138">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="92984-138">This parameter is required.</span></span>

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

### <span data-ttu-id="92984-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="92984-139">-Name</span></span>
<span data-ttu-id="92984-140">Określa nazwę internetowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="92984-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="92984-141">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="92984-141">-OpenIdProviderId</span></span>
<span data-ttu-id="92984-142">Identyfikator serwera autoryzacji OpenId.</span><span class="sxs-lookup"><span data-stu-id="92984-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="92984-143">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="92984-143">This parameter is optional.</span></span> <span data-ttu-id="92984-144">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="92984-144">Default value is $null.</span></span> <span data-ttu-id="92984-145">Należy określić, czy BearerTokenSendingMethods jest określony.</span><span class="sxs-lookup"><span data-stu-id="92984-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="92984-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92984-146">-PassThru</span></span>
<span data-ttu-id="92984-147">passthru</span><span class="sxs-lookup"><span data-stu-id="92984-147">passthru</span></span>

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

### <span data-ttu-id="92984-148">-Path</span><span class="sxs-lookup"><span data-stu-id="92984-148">-Path</span></span>
<span data-ttu-id="92984-149">Określa ścieżkę internetowego interfejsu API, która jest ostatnią częścią publicznego adresu URL interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="92984-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="92984-150">Ten adres URL jest wykorzystywany przez użytkowników korzystających z interfejsu API do wysyłania żądań do usługi sieci Web i musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="92984-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="92984-151">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="92984-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="92984-152">-Protokoły</span><span class="sxs-lookup"><span data-stu-id="92984-152">-Protocols</span></span>
<span data-ttu-id="92984-153">Określa tablicę protokołów API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="92984-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="92984-154">psdx_paramvalues http i https.</span><span class="sxs-lookup"><span data-stu-id="92984-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="92984-155">To są protokoły sieci Web, w których udostępniono interfejs API.</span><span class="sxs-lookup"><span data-stu-id="92984-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="92984-156">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="92984-156">The default value is $Null.</span></span>

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

### <span data-ttu-id="92984-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="92984-157">-ServiceUrl</span></span>
<span data-ttu-id="92984-158">Określa adres URL usługi sieci Web, która udostępnia interfejs API.</span><span class="sxs-lookup"><span data-stu-id="92984-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="92984-159">Ten adres URL jest wykorzystywany tylko przez usługę Azure API Management i nie został podany jako publiczny.</span><span class="sxs-lookup"><span data-stu-id="92984-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="92984-160">Adres URL musi zawierać od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="92984-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="92984-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="92984-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="92984-162">Określa nazwę nagłówka klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="92984-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="92984-163">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="92984-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="92984-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="92984-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="92984-165">Określa nazwę parametru ciągu kwerendy klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="92984-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="92984-166">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="92984-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="92984-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="92984-167">-SubscriptionRequired</span></span>
<span data-ttu-id="92984-168">Flaga wymuszania SubscriptionRequired dla żądań w interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="92984-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="92984-169">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="92984-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="92984-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92984-170">CommonParameters</span></span>
<span data-ttu-id="92984-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92984-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92984-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92984-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92984-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92984-173">INPUTS</span></span>

### <span data-ttu-id="92984-174">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="92984-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="92984-175">System. String</span><span class="sxs-lookup"><span data-stu-id="92984-175">System.String</span></span>

### <span data-ttu-id="92984-176">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="92984-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="92984-177">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="92984-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="92984-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="92984-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="92984-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92984-179">OUTPUTS</span></span>

### <span data-ttu-id="92984-180">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="92984-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="92984-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92984-181">NOTES</span></span>

## <span data-ttu-id="92984-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92984-182">RELATED LINKS</span></span>

[<span data-ttu-id="92984-183">Eksportowanie — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="92984-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="92984-184">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="92984-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="92984-185">Import — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="92984-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="92984-186">Nowe — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="92984-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="92984-187">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="92984-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


