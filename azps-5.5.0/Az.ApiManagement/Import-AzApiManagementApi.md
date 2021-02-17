---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 5a9141cf0f609eedd35c25f6fd3d7977201e58c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192499"
---
# <span data-ttu-id="53be9-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="53be9-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="53be9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53be9-102">SYNOPSIS</span></span>
<span data-ttu-id="53be9-103">Importuje interfejs API z pliku lub adresu URL.</span><span class="sxs-lookup"><span data-stu-id="53be9-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="53be9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="53be9-104">SYNTAX</span></span>

### <span data-ttu-id="53be9-105">ImportFromLocalFile (domyślne)</span><span class="sxs-lookup"><span data-stu-id="53be9-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53be9-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="53be9-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53be9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="53be9-107">DESCRIPTION</span></span>
<span data-ttu-id="53be9-108">Polecenie cmdlet **Import-AzApiManagementApi** importuje interfejs API zarządzania interfejsem Azure API Management z pliku lub adresu URL w języku WADL (Web Application Description Language), w języku WSDL (Web Services Description Language) lub w formacie Swagger.</span><span class="sxs-lookup"><span data-stu-id="53be9-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="53be9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="53be9-109">EXAMPLES</span></span>

### <span data-ttu-id="53be9-110">Przykład 1. Importowanie interfejsu API z pliku WADL</span><span class="sxs-lookup"><span data-stu-id="53be9-110">Example 1: Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="53be9-111">To polecenie importuje interfejs API z określonego pliku WADL.</span><span class="sxs-lookup"><span data-stu-id="53be9-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="53be9-112">Przykład 2. Importowanie interfejsu API z pliku Swagger</span><span class="sxs-lookup"><span data-stu-id="53be9-112">Example 2: Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="53be9-113">To polecenie importuje interfejs API z określonego pliku swaggera.</span><span class="sxs-lookup"><span data-stu-id="53be9-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="53be9-114">Przykład 3. Importowanie interfejsu API z linku WADL</span><span class="sxs-lookup"><span data-stu-id="53be9-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="53be9-115">To polecenie importuje interfejs API z określonego linku WADL.</span><span class="sxs-lookup"><span data-stu-id="53be9-115">This command imports an API from the specified WADL link.</span></span>

### <span data-ttu-id="53be9-116">Przykład 4. Importowanie interfejsu API z linku Open Api</span><span class="sxs-lookup"><span data-stu-id="53be9-116">Example 4: Import an API from a Open Api Link</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationFormat OpenApi -SpecificationUrl https://raw.githubusercontent.com/OAI/OpenAPI-Specification/master/examples/v3.0/petstore.yaml -Path "petstore30"

ApiId                         : af3f57bab399455aa875d7050654e9d1
Name                          : Swagger Petstore
Description                   :
ServiceUrl                    : http://petstore.swagger.io/v1
Path                          : petstore30
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    :
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/af3f57bab399455aa875d7050654e9d1     
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="53be9-117">To polecenie importuje interfejs API z określonego łącza specyfikacji Open 3.0.</span><span class="sxs-lookup"><span data-stu-id="53be9-117">This command imports an API from the specified Open 3.0 specification link.</span></span>

### <span data-ttu-id="53be9-118">Przykład 5. Importowanie interfejsu API z otwartego linku interfejsu API do zestawu apiVersion</span><span class="sxs-lookup"><span data-stu-id="53be9-118">Example 5:  Import an API from a Open Api Link into a ApiVersion Set</span></span>

```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationPath "C:\contoso\specifications\uspto.yml" -SpecificationFormat OpenApi -Path uspostal -ApiVersionSetId 0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd -ApiVersion v2

ApiId                         : 6c3f20c66e5745b19229d06cd865948f
Name                          : USPTO Data Set API
Description                   : The Data Set API (DSAPI) allows the public users to discover and search USPTO exported data sets. This is a generic API that allows USPTO users to make any CSV based data files
                                searchable through API. With the help of GET call, it returns the list of data fields that are searchable. With the help of POST call, data can be fetched based on the filters on the    
                                field names. Please note that POST call is used to search the actual data. The reason for the POST call is that it allows users to specify any complex search criteria without worry      
                                about the GET size limitations as well as encoding of the input parameters.
ServiceUrl                    : https://developer.uspto.gov/ds-api
Path                          : uspostal
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v2
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd
Id                            : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis/6c3f20c66e5745b19229d06cd865948f    
ResourceGroupName             : Api-Default-East-US
ServiceName                   : contoso
```

<span data-ttu-id="53be9-119">To polecenie importuje interfejs API z określonego dokumentu specyfikacji Open 3.0 i tworzy nowy interfejs ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="53be9-119">This command imports an API from the specified Open 3.0 specification document and create a new ApiVersion.</span></span>

## <span data-ttu-id="53be9-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53be9-120">PARAMETERS</span></span>

### <span data-ttu-id="53be9-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="53be9-121">-ApiId</span></span>
<span data-ttu-id="53be9-122">Określa identyfikator interfejsu API do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="53be9-122">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="53be9-123">Jeśli nie określisz tego parametru, zostanie wygenerowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="53be9-123">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="53be9-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="53be9-124">-ApiRevision</span></span>
<span data-ttu-id="53be9-125">Identyfikator poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="53be9-125">Identifier of API Revision.</span></span> <span data-ttu-id="53be9-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="53be9-126">This parameter is optional.</span></span> <span data-ttu-id="53be9-127">Jeśli nie zostanie określona, importowanie zostanie wykonane na aktualnie aktywnej poprawce lub w nowym interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="53be9-127">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="53be9-128">-ApiType</span><span class="sxs-lookup"><span data-stu-id="53be9-128">-ApiType</span></span>
<span data-ttu-id="53be9-129">Ten parametr jest opcjonalny z domyślną wartością Http.</span><span class="sxs-lookup"><span data-stu-id="53be9-129">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="53be9-130">Opcja mydła ma zastosowanie tylko podczas importowania pliku WSDL i powoduje utworzenie interfejsu API przekazać protokołu SOAP.</span><span class="sxs-lookup"><span data-stu-id="53be9-130">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53be9-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="53be9-131">-ApiVersion</span></span>
<span data-ttu-id="53be9-132">Wersja interfejsu API do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="53be9-132">Api Version of the Api to create.</span></span> <span data-ttu-id="53be9-133">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="53be9-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="53be9-134">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="53be9-134">-ApiVersionSetId</span></span>
<span data-ttu-id="53be9-135">Identyfikator zasobu dla powiązanego zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="53be9-135">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="53be9-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="53be9-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="53be9-137">— kontekst</span><span class="sxs-lookup"><span data-stu-id="53be9-137">-Context</span></span>
<span data-ttu-id="53be9-138">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="53be9-138">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="53be9-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53be9-139">-DefaultProfile</span></span>
<span data-ttu-id="53be9-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="53be9-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53be9-141">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="53be9-141">-Path</span></span>
<span data-ttu-id="53be9-142">Określa ścieżkę interfejsu API sieci Web jako ostatnią część publicznego adresu URL interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="53be9-142">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="53be9-143">Ten adres URL jest używany przez klientów interfejsu API do wysyłania żądań do usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="53be9-143">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="53be9-144">Musi to być od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="53be9-144">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="53be9-145">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="53be9-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="53be9-146">— Protokół</span><span class="sxs-lookup"><span data-stu-id="53be9-146">-Protocol</span></span>
<span data-ttu-id="53be9-147">Protokoły WEB API (http, https).</span><span class="sxs-lookup"><span data-stu-id="53be9-147">Web API protocols (http, https).</span></span> <span data-ttu-id="53be9-148">Protokoły, dla których jest dostępny interfejs API.</span><span class="sxs-lookup"><span data-stu-id="53be9-148">Protocols over which API is made available.</span></span> <span data-ttu-id="53be9-149">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="53be9-149">This parameter is optional.</span></span> <span data-ttu-id="53be9-150">Jeśli zostanie podany, zastąpi on protokoły określone w dokumencie specyfikacji.</span><span class="sxs-lookup"><span data-stu-id="53be9-150">If provided it will override the protocols specified in the specifications document.</span></span>

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

### <span data-ttu-id="53be9-151">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="53be9-151">-ServiceUrl</span></span>
<span data-ttu-id="53be9-152">Adres URL usługi sieci Web eksponujące interfejs API.</span><span class="sxs-lookup"><span data-stu-id="53be9-152">A URL of the web service exposing the API.</span></span> <span data-ttu-id="53be9-153">Ten adres URL będzie używany tylko w usłudze Azure API Management i nie będzie publiczny.</span><span class="sxs-lookup"><span data-stu-id="53be9-153">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="53be9-154">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="53be9-154">This parameter is optional.</span></span> <span data-ttu-id="53be9-155">Jeśli zostanie podany, zastąpi ono adres ServiceUrl określony w dokumencie Specyfikacje.</span><span class="sxs-lookup"><span data-stu-id="53be9-155">If provided it will override the ServiceUrl specified in the Specifications document.</span></span>

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

### <span data-ttu-id="53be9-156">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="53be9-156">-SpecificationFormat</span></span>
<span data-ttu-id="53be9-157">Określa format specyfikacji.</span><span class="sxs-lookup"><span data-stu-id="53be9-157">Specifies the specification format.</span></span>
<span data-ttu-id="53be9-158">psdx_paramvalues Wadl, Wsdl i Swagger.</span><span class="sxs-lookup"><span data-stu-id="53be9-158">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53be9-159">- SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="53be9-159">-SpecificationPath</span></span>
<span data-ttu-id="53be9-160">Określa ścieżkę pliku specyfikacji.</span><span class="sxs-lookup"><span data-stu-id="53be9-160">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromLocalFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53be9-161">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="53be9-161">-SpecificationUrl</span></span>
<span data-ttu-id="53be9-162">Określa adres URL specyfikacji.</span><span class="sxs-lookup"><span data-stu-id="53be9-162">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53be9-163">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="53be9-163">-WsdlEndpointName</span></span>
<span data-ttu-id="53be9-164">Nazwa lokalna punktu końcowego WSDL (portu), który ma zostać zaimportowany.</span><span class="sxs-lookup"><span data-stu-id="53be9-164">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="53be9-165">Musi to być od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="53be9-165">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="53be9-166">Ten parametr jest opcjonalny i wymagany tylko do importowania pliku Wsdl.</span><span class="sxs-lookup"><span data-stu-id="53be9-166">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="53be9-167">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="53be9-167">Default value is $null.</span></span>

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

### <span data-ttu-id="53be9-168">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="53be9-168">-WsdlServiceName</span></span>
<span data-ttu-id="53be9-169">Nazwa lokalna usługi WSDL do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="53be9-169">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="53be9-170">Musi to być od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="53be9-170">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="53be9-171">Ten parametr jest opcjonalny i wymagany tylko do importowania pliku Wsdl.</span><span class="sxs-lookup"><span data-stu-id="53be9-171">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="53be9-172">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="53be9-172">Default value is $null.</span></span>

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

### <span data-ttu-id="53be9-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53be9-173">CommonParameters</span></span>
<span data-ttu-id="53be9-174">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53be9-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53be9-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53be9-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53be9-176">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53be9-176">INPUTS</span></span>

### <span data-ttu-id="53be9-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="53be9-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="53be9-178">System.String</span><span class="sxs-lookup"><span data-stu-id="53be9-178">System.String</span></span>

### <span data-ttu-id="53be9-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="53be9-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="53be9-180">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlet.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="53be9-180">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="53be9-181">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53be9-181">OUTPUTS</span></span>

### <span data-ttu-id="53be9-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="53be9-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="53be9-183">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="53be9-183">NOTES</span></span>

## <span data-ttu-id="53be9-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53be9-184">RELATED LINKS</span></span>

[<span data-ttu-id="53be9-185">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="53be9-185">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="53be9-186">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="53be9-186">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="53be9-187">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="53be9-187">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="53be9-188">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="53be9-188">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="53be9-189">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="53be9-189">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


