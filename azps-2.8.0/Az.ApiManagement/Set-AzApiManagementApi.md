---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 973dc9bac629ee9a82b7624053f689bf7884fd8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706919"
---
# <span data-ttu-id="2b62c-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2b62c-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="2b62c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b62c-102">SYNOPSIS</span></span>
<span data-ttu-id="2b62c-103">Modyfikuje interfejs API.</span><span class="sxs-lookup"><span data-stu-id="2b62c-103">Modifies an API.</span></span>

## <span data-ttu-id="2b62c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b62c-104">SYNTAX</span></span>

### <span data-ttu-id="2b62c-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2b62c-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b62c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2b62c-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b62c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2b62c-107">DESCRIPTION</span></span>
<span data-ttu-id="2b62c-108">Polecenie cmdlet **Set-AzApiManagementApi** modyfikuje interfejs API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="2b62c-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="2b62c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b62c-109">EXAMPLES</span></span>

### <span data-ttu-id="2b62c-110">Przykład 1 modyfikowanie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="2b62c-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="2b62c-111">Przykład 2 Dodawanie interfejsu API do istniejącego ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2b62c-111">Example 2 Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```
<span data-ttu-id="2b62c-112">W tym przykładzie dodano interfejs API do istniejącego zestawu wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="2b62c-112">This example adds an API to an existing API Version Set</span></span>

## <span data-ttu-id="2b62c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b62c-113">PARAMETERS</span></span>

### <span data-ttu-id="2b62c-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2b62c-114">-ApiId</span></span>
<span data-ttu-id="2b62c-115">Określa identyfikator interfejsu API do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="2b62c-115">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="2b62c-116">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="2b62c-116">-AuthorizationScope</span></span>
<span data-ttu-id="2b62c-117">Określa zakres operacji uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="2b62c-117">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="2b62c-118">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="2b62c-118">The default value is $Null.</span></span>

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

### <span data-ttu-id="2b62c-119">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="2b62c-119">-AuthorizationServerId</span></span>
<span data-ttu-id="2b62c-120">Określa identyfikator serwera autoryzacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="2b62c-120">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="2b62c-121">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="2b62c-121">The default value is $Null.</span></span>
<span data-ttu-id="2b62c-122">Ten parametr należy określić, jeśli *AuthorizationScope* jest określony.</span><span class="sxs-lookup"><span data-stu-id="2b62c-122">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="2b62c-123">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="2b62c-123">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="2b62c-124">OpenId mechanizm serwera autoryzacji, w którym token dostępu jest przekazywany do interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="2b62c-124">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="2b62c-125">Zobacz http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="2b62c-125">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="2b62c-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2b62c-126">This parameter is optional.</span></span> <span data-ttu-id="2b62c-127">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="2b62c-127">Default value is $null.</span></span>

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

### <span data-ttu-id="2b62c-128">-Context</span><span class="sxs-lookup"><span data-stu-id="2b62c-128">-Context</span></span>
<span data-ttu-id="2b62c-129">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2b62c-129">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2b62c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b62c-130">-DefaultProfile</span></span>
<span data-ttu-id="2b62c-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b62c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b62c-132">— Opis</span><span class="sxs-lookup"><span data-stu-id="2b62c-132">-Description</span></span>
<span data-ttu-id="2b62c-133">Określa opis interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="2b62c-133">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="2b62c-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2b62c-134">-InputObject</span></span>
<span data-ttu-id="2b62c-135">Wystąpienie PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="2b62c-135">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="2b62c-136">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2b62c-136">This parameter is required.</span></span>

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

### <span data-ttu-id="2b62c-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2b62c-137">-Name</span></span>
<span data-ttu-id="2b62c-138">Określa nazwę internetowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="2b62c-138">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="2b62c-139">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="2b62c-139">-OpenIdProviderId</span></span>
<span data-ttu-id="2b62c-140">Identyfikator serwera autoryzacji OpenId.</span><span class="sxs-lookup"><span data-stu-id="2b62c-140">OpenId authorization server identifier.</span></span> <span data-ttu-id="2b62c-141">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2b62c-141">This parameter is optional.</span></span> <span data-ttu-id="2b62c-142">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="2b62c-142">Default value is $null.</span></span> <span data-ttu-id="2b62c-143">Należy określić, czy BearerTokenSendingMethods jest określony.</span><span class="sxs-lookup"><span data-stu-id="2b62c-143">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="2b62c-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b62c-144">-PassThru</span></span>
<span data-ttu-id="2b62c-145">passthru</span><span class="sxs-lookup"><span data-stu-id="2b62c-145">passthru</span></span>

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

### <span data-ttu-id="2b62c-146">-Path</span><span class="sxs-lookup"><span data-stu-id="2b62c-146">-Path</span></span>
<span data-ttu-id="2b62c-147">Określa ścieżkę internetowego interfejsu API, która jest ostatnią częścią publicznego adresu URL interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="2b62c-147">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="2b62c-148">Ten adres URL jest wykorzystywany przez użytkowników korzystających z interfejsu API do wysyłania żądań do usługi sieci Web i musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="2b62c-148">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="2b62c-149">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="2b62c-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="2b62c-150">-Protokoły</span><span class="sxs-lookup"><span data-stu-id="2b62c-150">-Protocols</span></span>
<span data-ttu-id="2b62c-151">Określa tablicę protokołów API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="2b62c-151">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="2b62c-152">psdx_paramvalues http i https.</span><span class="sxs-lookup"><span data-stu-id="2b62c-152">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="2b62c-153">To są protokoły sieci Web, w których udostępniono interfejs API.</span><span class="sxs-lookup"><span data-stu-id="2b62c-153">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="2b62c-154">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="2b62c-154">The default value is $Null.</span></span>

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

### <span data-ttu-id="2b62c-155">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="2b62c-155">-ServiceUrl</span></span>
<span data-ttu-id="2b62c-156">Określa adres URL usługi sieci Web, która udostępnia interfejs API.</span><span class="sxs-lookup"><span data-stu-id="2b62c-156">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="2b62c-157">Ten adres URL jest wykorzystywany tylko przez usługę Azure API Management i nie został podany jako publiczny.</span><span class="sxs-lookup"><span data-stu-id="2b62c-157">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="2b62c-158">Adres URL musi zawierać od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="2b62c-158">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="2b62c-159">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="2b62c-159">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="2b62c-160">Określa nazwę nagłówka klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2b62c-160">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="2b62c-161">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="2b62c-161">The default value is $Null.</span></span>

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

### <span data-ttu-id="2b62c-162">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="2b62c-162">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="2b62c-163">Określa nazwę parametru ciągu kwerendy klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2b62c-163">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="2b62c-164">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="2b62c-164">The default value is $Null.</span></span>

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

### <span data-ttu-id="2b62c-165">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="2b62c-165">-SubscriptionRequired</span></span>
<span data-ttu-id="2b62c-166">Flaga wymuszania SubscriptionRequired dla żądań w interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="2b62c-166">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="2b62c-167">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2b62c-167">This parameter is optional.</span></span>

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

### <span data-ttu-id="2b62c-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b62c-168">CommonParameters</span></span>
<span data-ttu-id="2b62c-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b62c-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b62c-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b62c-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b62c-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b62c-171">INPUTS</span></span>

### <span data-ttu-id="2b62c-172">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2b62c-172">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2b62c-173">System. String</span><span class="sxs-lookup"><span data-stu-id="2b62c-173">System.String</span></span>

### <span data-ttu-id="2b62c-174">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2b62c-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="2b62c-175">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="2b62c-175">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="2b62c-176">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2b62c-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2b62c-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b62c-177">OUTPUTS</span></span>

### <span data-ttu-id="2b62c-178">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2b62c-178">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="2b62c-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b62c-179">NOTES</span></span>

## <span data-ttu-id="2b62c-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b62c-180">RELATED LINKS</span></span>

[<span data-ttu-id="2b62c-181">Eksportowanie — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2b62c-181">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="2b62c-182">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2b62c-182">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="2b62c-183">Import — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2b62c-183">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="2b62c-184">Nowe — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2b62c-184">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="2b62c-185">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2b62c-185">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


