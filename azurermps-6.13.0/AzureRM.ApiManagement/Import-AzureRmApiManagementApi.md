---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
ms.openlocfilehash: 7eb2e25f137abb303e1c9fa5b4ebe8b932346871
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543988"
---
# <span data-ttu-id="f567f-101">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f567f-101">Import-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="f567f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f567f-102">SYNOPSIS</span></span>
<span data-ttu-id="f567f-103">Importuje interfejs API z pliku lub adresu URL.</span><span class="sxs-lookup"><span data-stu-id="f567f-103">Imports an API from a file or a URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f567f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f567f-104">SYNTAX</span></span>

### <span data-ttu-id="f567f-105">ImportFromLocalFile (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f567f-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f567f-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="f567f-106">ImportFromUrl</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f567f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f567f-107">DESCRIPTION</span></span>
<span data-ttu-id="f567f-108">Polecenie cmdlet **Import-AzureRmApiManagementApi** IMPORTUJE interfejs API zarządzania interfejsem Azure API z pliku lub adresu URL w programie sieci Web Application Description Language (WADL), Web Services Description Language (WSDL) lub w formacie Swagger.</span><span class="sxs-lookup"><span data-stu-id="f567f-108">The **Import-AzureRmApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="f567f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f567f-109">EXAMPLES</span></span>

### <span data-ttu-id="f567f-110">Przykład 1 Importowanie interfejsu API z pliku WADL</span><span class="sxs-lookup"><span data-stu-id="f567f-110">Example 1 Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="f567f-111">To polecenie importuje interfejs API z określonego pliku WADL.</span><span class="sxs-lookup"><span data-stu-id="f567f-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="f567f-112">Przykład 2 Importowanie interfejsu API z pliku struktury Swagger</span><span class="sxs-lookup"><span data-stu-id="f567f-112">Example 2 Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="f567f-113">To polecenie importuje interfejs API z określonego pliku struktury Swagger.</span><span class="sxs-lookup"><span data-stu-id="f567f-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="f567f-114">Przykład 3: Importowanie interfejsu API z linku WADL</span><span class="sxs-lookup"><span data-stu-id="f567f-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="f567f-115">To polecenie importuje interfejs API z określonego linku WADL.</span><span class="sxs-lookup"><span data-stu-id="f567f-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="f567f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f567f-116">PARAMETERS</span></span>

### <span data-ttu-id="f567f-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f567f-117">-ApiId</span></span>
<span data-ttu-id="f567f-118">Określa identyfikator interfejsu API do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="f567f-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="f567f-119">Jeśli nie określisz tego parametru, zostanie wygenerowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="f567f-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="f567f-120">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f567f-120">-ApiRevision</span></span>
<span data-ttu-id="f567f-121">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f567f-121">Identifier of API Revision.</span></span> <span data-ttu-id="f567f-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f567f-122">This parameter is optional.</span></span> <span data-ttu-id="f567f-123">Jeśli nie określono tej funkcji, importowanie zostanie przeprowadzone na obecnie aktywnej wersji lub w nowym interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="f567f-123">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="f567f-124">-ApiType</span><span class="sxs-lookup"><span data-stu-id="f567f-124">-ApiType</span></span>
<span data-ttu-id="f567f-125">Ten parametr jest opcjonalny z wartością domyślną protokołu HTTP.</span><span class="sxs-lookup"><span data-stu-id="f567f-125">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="f567f-126">Opcja SOAP jest stosowana tylko podczas importowania elementu WSDL i tworzenia interfejsu API przekazywania protokołu SOAP.</span><span class="sxs-lookup"><span data-stu-id="f567f-126">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="f567f-127">-Context</span><span class="sxs-lookup"><span data-stu-id="f567f-127">-Context</span></span>
<span data-ttu-id="f567f-128">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f567f-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f567f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f567f-129">-DefaultProfile</span></span>
<span data-ttu-id="f567f-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f567f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f567f-131">-Path</span><span class="sxs-lookup"><span data-stu-id="f567f-131">-Path</span></span>
<span data-ttu-id="f567f-132">Określa ścieżkę internetowego interfejsu API jako ostatnią część publicznego adresu URL interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f567f-132">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="f567f-133">Ten adres URL jest wykorzystywany przez użytkowników korzystających z interfejsu API w celu wysyłania żądań do usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f567f-133">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="f567f-134">Musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="f567f-134">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="f567f-135">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="f567f-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="f567f-136">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="f567f-136">-SpecificationFormat</span></span>
<span data-ttu-id="f567f-137">Określa format specyfikacji.</span><span class="sxs-lookup"><span data-stu-id="f567f-137">Specifies the specification format.</span></span>
<span data-ttu-id="f567f-138">psdx_paramvalues WADL, WSDL i Swagger.</span><span class="sxs-lookup"><span data-stu-id="f567f-138">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

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

### <span data-ttu-id="f567f-139">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="f567f-139">-SpecificationPath</span></span>
<span data-ttu-id="f567f-140">Określa ścieżkę pliku specyfikacji.</span><span class="sxs-lookup"><span data-stu-id="f567f-140">Specifies the specification file path.</span></span>

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

### <span data-ttu-id="f567f-141">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="f567f-141">-SpecificationUrl</span></span>
<span data-ttu-id="f567f-142">Określa adres URL specyfikacji.</span><span class="sxs-lookup"><span data-stu-id="f567f-142">Specifies the specification URL.</span></span>

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

### <span data-ttu-id="f567f-143">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="f567f-143">-WsdlEndpointName</span></span>
<span data-ttu-id="f567f-144">Nazwa lokalna punktu końcowego WSDL (port) do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="f567f-144">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="f567f-145">Musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="f567f-145">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="f567f-146">Ten parametr jest opcjonalny i jest wymagany tylko do importowania elementu WSDL.</span><span class="sxs-lookup"><span data-stu-id="f567f-146">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="f567f-147">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="f567f-147">Default value is $null.</span></span>

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

### <span data-ttu-id="f567f-148">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="f567f-148">-WsdlServiceName</span></span>
<span data-ttu-id="f567f-149">Nazwa lokalna usługi WSDL do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="f567f-149">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="f567f-150">Musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="f567f-150">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="f567f-151">Ten parametr jest opcjonalny i jest wymagany tylko do importowania elementu WSDL.</span><span class="sxs-lookup"><span data-stu-id="f567f-151">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="f567f-152">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="f567f-152">Default value is $null.</span></span>

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

### <span data-ttu-id="f567f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f567f-153">CommonParameters</span></span>
<span data-ttu-id="f567f-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f567f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f567f-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f567f-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f567f-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f567f-156">INPUTS</span></span>

### <span data-ttu-id="f567f-157">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f567f-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f567f-158">System. String</span><span class="sxs-lookup"><span data-stu-id="f567f-158">System.String</span></span>

### <span data-ttu-id="f567f-159">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="f567f-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="f567f-160">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementApiType, Microsoft. Azure. Commands. ApiManagement. servicemanagement, Version = 6.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f567f-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f567f-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f567f-161">OUTPUTS</span></span>

### <span data-ttu-id="f567f-162">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f567f-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="f567f-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f567f-163">NOTES</span></span>

## <span data-ttu-id="f567f-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f567f-164">RELATED LINKS</span></span>

[<span data-ttu-id="f567f-165">Eksportowanie — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f567f-165">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="f567f-166">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f567f-166">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="f567f-167">Nowe — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f567f-167">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="f567f-168">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f567f-168">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="f567f-169">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f567f-169">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


