---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 5fd06ad41e6fafe629ba50166650dd3d8766d29c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707045"
---
# <span data-ttu-id="df6c0-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="df6c0-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="df6c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df6c0-102">SYNOPSIS</span></span>
<span data-ttu-id="df6c0-103">Importuje interfejs API z pliku lub adresu URL.</span><span class="sxs-lookup"><span data-stu-id="df6c0-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="df6c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df6c0-104">SYNTAX</span></span>

### <span data-ttu-id="df6c0-105">ImportFromLocalFile (domyślny)</span><span class="sxs-lookup"><span data-stu-id="df6c0-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df6c0-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="df6c0-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df6c0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="df6c0-107">DESCRIPTION</span></span>
<span data-ttu-id="df6c0-108">Polecenie cmdlet **Import-AzApiManagementApi** IMPORTUJE interfejs API zarządzania interfejsem Azure API z pliku lub adresu URL w programie sieci Web Application Description Language (WADL), Web Services Description Language (WSDL) lub w formacie Swagger.</span><span class="sxs-lookup"><span data-stu-id="df6c0-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="df6c0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df6c0-109">EXAMPLES</span></span>

### <span data-ttu-id="df6c0-110">Przykład 1 Importowanie interfejsu API z pliku WADL</span><span class="sxs-lookup"><span data-stu-id="df6c0-110">Example 1 Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="df6c0-111">To polecenie importuje interfejs API z określonego pliku WADL.</span><span class="sxs-lookup"><span data-stu-id="df6c0-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="df6c0-112">Przykład 2 Importowanie interfejsu API z pliku struktury Swagger</span><span class="sxs-lookup"><span data-stu-id="df6c0-112">Example 2 Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="df6c0-113">To polecenie importuje interfejs API z określonego pliku struktury Swagger.</span><span class="sxs-lookup"><span data-stu-id="df6c0-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="df6c0-114">Przykład 3: Importowanie interfejsu API z linku WADL</span><span class="sxs-lookup"><span data-stu-id="df6c0-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="df6c0-115">To polecenie importuje interfejs API z określonego linku WADL.</span><span class="sxs-lookup"><span data-stu-id="df6c0-115">This command imports an API from the specified WADL link.</span></span>

### <span data-ttu-id="df6c0-116">Przykład 4: Importowanie interfejsu API z łącza Open API</span><span class="sxs-lookup"><span data-stu-id="df6c0-116">Example 4: Import an API from a Open Api Link</span></span>
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

<span data-ttu-id="df6c0-117">To polecenie importuje interfejs API z określonego linku specyfikacji Open 3,0.</span><span class="sxs-lookup"><span data-stu-id="df6c0-117">This command imports an API from the specified Open 3.0 specification link.</span></span>

### <span data-ttu-id="df6c0-118">Przykład 5: Importowanie interfejsu API z łącza Open API do zestawu ApiVersion</span><span class="sxs-lookup"><span data-stu-id="df6c0-118">Example 5:  Import an API from a Open Api Link into a ApiVersion Set</span></span>

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

<span data-ttu-id="df6c0-119">To polecenie importuje interfejs API z określonego dokumentu specyfikacji Open 3,0 i tworzy nowy ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="df6c0-119">This command imports an API from the specified Open 3.0 specification document and create a new ApiVersion.</span></span>

## <span data-ttu-id="df6c0-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df6c0-120">PARAMETERS</span></span>

### <span data-ttu-id="df6c0-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="df6c0-121">-ApiId</span></span>
<span data-ttu-id="df6c0-122">Określa identyfikator interfejsu API do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="df6c0-122">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="df6c0-123">Jeśli nie określisz tego parametru, zostanie wygenerowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="df6c0-123">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="df6c0-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="df6c0-124">-ApiRevision</span></span>
<span data-ttu-id="df6c0-125">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="df6c0-125">Identifier of API Revision.</span></span> <span data-ttu-id="df6c0-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="df6c0-126">This parameter is optional.</span></span> <span data-ttu-id="df6c0-127">Jeśli nie określono tej funkcji, importowanie zostanie przeprowadzone na obecnie aktywnej wersji lub w nowym interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="df6c0-127">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="df6c0-128">-ApiType</span><span class="sxs-lookup"><span data-stu-id="df6c0-128">-ApiType</span></span>
<span data-ttu-id="df6c0-129">Ten parametr jest opcjonalny z wartością domyślną protokołu HTTP.</span><span class="sxs-lookup"><span data-stu-id="df6c0-129">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="df6c0-130">Opcja SOAP jest stosowana tylko podczas importowania elementu WSDL i tworzenia interfejsu API przekazywania protokołu SOAP.</span><span class="sxs-lookup"><span data-stu-id="df6c0-130">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="df6c0-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="df6c0-131">-ApiVersion</span></span>
<span data-ttu-id="df6c0-132">Wersja API interfejsu API do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="df6c0-132">Api Version of the Api to create.</span></span> <span data-ttu-id="df6c0-133">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="df6c0-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="df6c0-134">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="df6c0-134">-ApiVersionSetId</span></span>
<span data-ttu-id="df6c0-135">Identyfikator zasobu powiązanego zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="df6c0-135">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="df6c0-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="df6c0-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="df6c0-137">-Context</span><span class="sxs-lookup"><span data-stu-id="df6c0-137">-Context</span></span>
<span data-ttu-id="df6c0-138">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="df6c0-138">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="df6c0-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df6c0-139">-DefaultProfile</span></span>
<span data-ttu-id="df6c0-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df6c0-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df6c0-141">-Path</span><span class="sxs-lookup"><span data-stu-id="df6c0-141">-Path</span></span>
<span data-ttu-id="df6c0-142">Określa ścieżkę internetowego interfejsu API jako ostatnią część publicznego adresu URL interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="df6c0-142">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="df6c0-143">Ten adres URL jest wykorzystywany przez użytkowników korzystających z interfejsu API w celu wysyłania żądań do usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="df6c0-143">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="df6c0-144">Musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="df6c0-144">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="df6c0-145">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="df6c0-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="df6c0-146">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="df6c0-146">-Protocol</span></span>
<span data-ttu-id="df6c0-147">Protokoły API sieci Web (http, https).</span><span class="sxs-lookup"><span data-stu-id="df6c0-147">Web API protocols (http, https).</span></span> <span data-ttu-id="df6c0-148">Protokoły, w których udostępniono interfejs API.</span><span class="sxs-lookup"><span data-stu-id="df6c0-148">Protocols over which API is made available.</span></span> <span data-ttu-id="df6c0-149">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="df6c0-149">This parameter is optional.</span></span> <span data-ttu-id="df6c0-150">Jeśli przewidziano, zastąpi protokoły określone w dokumencie specyfikacje.</span><span class="sxs-lookup"><span data-stu-id="df6c0-150">If provided it will override the protocols specified in the specifications document.</span></span>

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

### <span data-ttu-id="df6c0-151">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="df6c0-151">-ServiceUrl</span></span>
<span data-ttu-id="df6c0-152">Adres URL usługi sieci Web, która uwidacznia interfejs API.</span><span class="sxs-lookup"><span data-stu-id="df6c0-152">A URL of the web service exposing the API.</span></span> <span data-ttu-id="df6c0-153">Ten adres URL będzie wykorzystany tylko przez funkcję zarządzania interfejsem Azure API i nie zostanie udostępniony publicznie.</span><span class="sxs-lookup"><span data-stu-id="df6c0-153">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="df6c0-154">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="df6c0-154">This parameter is optional.</span></span> <span data-ttu-id="df6c0-155">Jeśli to pole zastąpi ServiceUrl określone w dokumencie specyfikacji.</span><span class="sxs-lookup"><span data-stu-id="df6c0-155">If provided it will override the ServiceUrl specified in the Specifications document.</span></span>

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

### <span data-ttu-id="df6c0-156">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="df6c0-156">-SpecificationFormat</span></span>
<span data-ttu-id="df6c0-157">Określa format specyfikacji.</span><span class="sxs-lookup"><span data-stu-id="df6c0-157">Specifies the specification format.</span></span>
<span data-ttu-id="df6c0-158">psdx_paramvalues WADL, WSDL i Swagger.</span><span class="sxs-lookup"><span data-stu-id="df6c0-158">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6c0-159">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="df6c0-159">-SpecificationPath</span></span>
<span data-ttu-id="df6c0-160">Określa ścieżkę pliku specyfikacji.</span><span class="sxs-lookup"><span data-stu-id="df6c0-160">Specifies the specification file path.</span></span>

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

### <span data-ttu-id="df6c0-161">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="df6c0-161">-SpecificationUrl</span></span>
<span data-ttu-id="df6c0-162">Określa adres URL specyfikacji.</span><span class="sxs-lookup"><span data-stu-id="df6c0-162">Specifies the specification URL.</span></span>

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

### <span data-ttu-id="df6c0-163">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="df6c0-163">-WsdlEndpointName</span></span>
<span data-ttu-id="df6c0-164">Nazwa lokalna punktu końcowego WSDL (port) do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="df6c0-164">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="df6c0-165">Musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="df6c0-165">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="df6c0-166">Ten parametr jest opcjonalny i jest wymagany tylko do importowania elementu WSDL.</span><span class="sxs-lookup"><span data-stu-id="df6c0-166">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="df6c0-167">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="df6c0-167">Default value is $null.</span></span>

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

### <span data-ttu-id="df6c0-168">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="df6c0-168">-WsdlServiceName</span></span>
<span data-ttu-id="df6c0-169">Nazwa lokalna usługi WSDL do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="df6c0-169">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="df6c0-170">Musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="df6c0-170">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="df6c0-171">Ten parametr jest opcjonalny i jest wymagany tylko do importowania elementu WSDL.</span><span class="sxs-lookup"><span data-stu-id="df6c0-171">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="df6c0-172">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="df6c0-172">Default value is $null.</span></span>

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

### <span data-ttu-id="df6c0-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df6c0-173">CommonParameters</span></span>
<span data-ttu-id="df6c0-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df6c0-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df6c0-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df6c0-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df6c0-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df6c0-176">INPUTS</span></span>

### <span data-ttu-id="df6c0-177">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="df6c0-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="df6c0-178">System. String</span><span class="sxs-lookup"><span data-stu-id="df6c0-178">System.String</span></span>

### <span data-ttu-id="df6c0-179">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="df6c0-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="df6c0-180">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementApiType, Microsoft. Azure. PowerShell. cmdlet. ApiManagement. servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="df6c0-180">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="df6c0-181">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df6c0-181">OUTPUTS</span></span>

### <span data-ttu-id="df6c0-182">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="df6c0-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="df6c0-183">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df6c0-183">NOTES</span></span>

## <span data-ttu-id="df6c0-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df6c0-184">RELATED LINKS</span></span>

[<span data-ttu-id="df6c0-185">Eksportowanie — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="df6c0-185">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="df6c0-186">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="df6c0-186">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="df6c0-187">Nowe — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="df6c0-187">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="df6c0-188">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="df6c0-188">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="df6c0-189">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="df6c0-189">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


