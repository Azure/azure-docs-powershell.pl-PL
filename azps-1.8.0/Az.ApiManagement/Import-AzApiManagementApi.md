---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 690ebbfb1bb3cca6de8feb1f199068510e41f1d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704624"
---
# <span data-ttu-id="178f3-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="178f3-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="178f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="178f3-102">SYNOPSIS</span></span>
<span data-ttu-id="178f3-103">Importuje interfejs API z pliku lub adresu URL.</span><span class="sxs-lookup"><span data-stu-id="178f3-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="178f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="178f3-104">SYNTAX</span></span>

### <span data-ttu-id="178f3-105">ImportFromLocalFile (domyślny)</span><span class="sxs-lookup"><span data-stu-id="178f3-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="178f3-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="178f3-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="178f3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="178f3-107">DESCRIPTION</span></span>
<span data-ttu-id="178f3-108">Polecenie cmdlet **Import-AzApiManagementApi** IMPORTUJE interfejs API zarządzania interfejsem Azure API z pliku lub adresu URL w programie sieci Web Application Description Language (WADL), Web Services Description Language (WSDL) lub w formacie Swagger.</span><span class="sxs-lookup"><span data-stu-id="178f3-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="178f3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="178f3-109">EXAMPLES</span></span>

### <span data-ttu-id="178f3-110">Przykład 1 Importowanie interfejsu API z pliku WADL</span><span class="sxs-lookup"><span data-stu-id="178f3-110">Example 1 Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="178f3-111">To polecenie importuje interfejs API z określonego pliku WADL.</span><span class="sxs-lookup"><span data-stu-id="178f3-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="178f3-112">Przykład 2 Importowanie interfejsu API z pliku struktury Swagger</span><span class="sxs-lookup"><span data-stu-id="178f3-112">Example 2 Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="178f3-113">To polecenie importuje interfejs API z określonego pliku struktury Swagger.</span><span class="sxs-lookup"><span data-stu-id="178f3-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="178f3-114">Przykład 3: Importowanie interfejsu API z linku WADL</span><span class="sxs-lookup"><span data-stu-id="178f3-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="178f3-115">To polecenie importuje interfejs API z określonego linku WADL.</span><span class="sxs-lookup"><span data-stu-id="178f3-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="178f3-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="178f3-116">PARAMETERS</span></span>

### <span data-ttu-id="178f3-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="178f3-117">-ApiId</span></span>
<span data-ttu-id="178f3-118">Określa identyfikator interfejsu API do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="178f3-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="178f3-119">Jeśli nie określisz tego parametru, zostanie wygenerowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="178f3-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="178f3-120">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="178f3-120">-ApiRevision</span></span>
<span data-ttu-id="178f3-121">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="178f3-121">Identifier of API Revision.</span></span> <span data-ttu-id="178f3-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="178f3-122">This parameter is optional.</span></span> <span data-ttu-id="178f3-123">Jeśli nie określono tej funkcji, importowanie zostanie przeprowadzone na obecnie aktywnej wersji lub w nowym interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="178f3-123">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="178f3-124">-ApiType</span><span class="sxs-lookup"><span data-stu-id="178f3-124">-ApiType</span></span>
<span data-ttu-id="178f3-125">Ten parametr jest opcjonalny z wartością domyślną protokołu HTTP.</span><span class="sxs-lookup"><span data-stu-id="178f3-125">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="178f3-126">Opcja SOAP jest stosowana tylko podczas importowania elementu WSDL i tworzenia interfejsu API przekazywania protokołu SOAP.</span><span class="sxs-lookup"><span data-stu-id="178f3-126">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="178f3-127">-Context</span><span class="sxs-lookup"><span data-stu-id="178f3-127">-Context</span></span>
<span data-ttu-id="178f3-128">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="178f3-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="178f3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="178f3-129">-DefaultProfile</span></span>
<span data-ttu-id="178f3-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="178f3-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="178f3-131">-Path</span><span class="sxs-lookup"><span data-stu-id="178f3-131">-Path</span></span>
<span data-ttu-id="178f3-132">Określa ścieżkę internetowego interfejsu API jako ostatnią część publicznego adresu URL interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="178f3-132">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="178f3-133">Ten adres URL jest wykorzystywany przez użytkowników korzystających z interfejsu API w celu wysyłania żądań do usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="178f3-133">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="178f3-134">Musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="178f3-134">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="178f3-135">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="178f3-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="178f3-136">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="178f3-136">-SpecificationFormat</span></span>
<span data-ttu-id="178f3-137">Określa format specyfikacji.</span><span class="sxs-lookup"><span data-stu-id="178f3-137">Specifies the specification format.</span></span>
<span data-ttu-id="178f3-138">psdx_paramvalues WADL, WSDL i Swagger.</span><span class="sxs-lookup"><span data-stu-id="178f3-138">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="178f3-139">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="178f3-139">-SpecificationPath</span></span>
<span data-ttu-id="178f3-140">Określa ścieżkę pliku specyfikacji.</span><span class="sxs-lookup"><span data-stu-id="178f3-140">Specifies the specification file path.</span></span>

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

### <span data-ttu-id="178f3-141">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="178f3-141">-SpecificationUrl</span></span>
<span data-ttu-id="178f3-142">Określa adres URL specyfikacji.</span><span class="sxs-lookup"><span data-stu-id="178f3-142">Specifies the specification URL.</span></span>

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

### <span data-ttu-id="178f3-143">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="178f3-143">-WsdlEndpointName</span></span>
<span data-ttu-id="178f3-144">Nazwa lokalna punktu końcowego WSDL (port) do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="178f3-144">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="178f3-145">Musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="178f3-145">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="178f3-146">Ten parametr jest opcjonalny i jest wymagany tylko do importowania elementu WSDL.</span><span class="sxs-lookup"><span data-stu-id="178f3-146">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="178f3-147">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="178f3-147">Default value is $null.</span></span>

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

### <span data-ttu-id="178f3-148">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="178f3-148">-WsdlServiceName</span></span>
<span data-ttu-id="178f3-149">Nazwa lokalna usługi WSDL do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="178f3-149">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="178f3-150">Musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="178f3-150">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="178f3-151">Ten parametr jest opcjonalny i jest wymagany tylko do importowania elementu WSDL.</span><span class="sxs-lookup"><span data-stu-id="178f3-151">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="178f3-152">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="178f3-152">Default value is $null.</span></span>

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

### <span data-ttu-id="178f3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178f3-153">CommonParameters</span></span>
<span data-ttu-id="178f3-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="178f3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178f3-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="178f3-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178f3-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="178f3-156">INPUTS</span></span>

### <span data-ttu-id="178f3-157">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="178f3-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="178f3-158">System. String</span><span class="sxs-lookup"><span data-stu-id="178f3-158">System.String</span></span>

### <span data-ttu-id="178f3-159">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="178f3-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="178f3-160">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementApiType, Microsoft. Azure. PowerShell. cmdlet. ApiManagement. servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="178f3-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="178f3-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="178f3-161">OUTPUTS</span></span>

### <span data-ttu-id="178f3-162">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="178f3-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="178f3-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="178f3-163">NOTES</span></span>

## <span data-ttu-id="178f3-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="178f3-164">RELATED LINKS</span></span>

[<span data-ttu-id="178f3-165">Eksportowanie — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="178f3-165">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="178f3-166">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="178f3-166">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="178f3-167">Nowe — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="178f3-167">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="178f3-168">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="178f3-168">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="178f3-169">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="178f3-169">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


