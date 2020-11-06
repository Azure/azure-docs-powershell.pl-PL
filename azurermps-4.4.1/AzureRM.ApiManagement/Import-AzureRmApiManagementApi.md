---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
ms.openlocfilehash: a95aa5cf5d78d2540fe2816cfa4b044502c69b0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547244"
---
# <span data-ttu-id="a1645-101">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a1645-101">Import-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="a1645-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1645-102">SYNOPSIS</span></span>
<span data-ttu-id="a1645-103">Importuje interfejs API z pliku lub adresu URL.</span><span class="sxs-lookup"><span data-stu-id="a1645-103">Imports an API from a file or a URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1645-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1645-104">SYNTAX</span></span>

### <span data-ttu-id="a1645-105">Z pliku lokalnego (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a1645-105">From Local File (Default)</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1645-106">Adres URL od</span><span class="sxs-lookup"><span data-stu-id="a1645-106">From URL</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1645-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a1645-107">DESCRIPTION</span></span>
<span data-ttu-id="a1645-108">Polecenie cmdlet **Import-AzureRmApiManagementApi** IMPORTUJE interfejs API zarządzania interfejsem Azure API z pliku lub adresu URL w programie sieci Web Application Description Language (WADL), Web Services Description Language (WSDL) lub w formacie Swagger.</span><span class="sxs-lookup"><span data-stu-id="a1645-108">The **Import-AzureRmApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="a1645-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1645-109">EXAMPLES</span></span>

### <span data-ttu-id="a1645-110">Przykład 1 Importowanie interfejsu API z pliku WADL</span><span class="sxs-lookup"><span data-stu-id="a1645-110">Example 1 Import an API from a WADL file</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="a1645-111">To polecenie importuje interfejs API z określonego pliku WADL.</span><span class="sxs-lookup"><span data-stu-id="a1645-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="a1645-112">Przykład 2 Importowanie interfejsu API z pliku struktury Swagger</span><span class="sxs-lookup"><span data-stu-id="a1645-112">Example 2 Import an API from a Swagger file</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="a1645-113">To polecenie importuje interfejs API z określonego pliku struktury Swagger.</span><span class="sxs-lookup"><span data-stu-id="a1645-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="a1645-114">Przykład 3: Importowanie interfejsu API z linku WADL</span><span class="sxs-lookup"><span data-stu-id="a1645-114">Example 3: Import an API from a WADL link</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="a1645-115">To polecenie importuje interfejs API z określonego linku WADL.</span><span class="sxs-lookup"><span data-stu-id="a1645-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="a1645-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1645-116">PARAMETERS</span></span>

### <span data-ttu-id="a1645-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a1645-117">-ApiId</span></span>
<span data-ttu-id="a1645-118">Określa identyfikator interfejsu API do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="a1645-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="a1645-119">Jeśli nie określisz tego parametru, zostanie wygenerowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="a1645-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="a1645-120">-ApiType</span><span class="sxs-lookup"><span data-stu-id="a1645-120">-ApiType</span></span>
<span data-ttu-id="a1645-121">Ten parametr jest opcjonalny z wartością domyślną protokołu HTTP.</span><span class="sxs-lookup"><span data-stu-id="a1645-121">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="a1645-122">Opcja SOAP jest stosowana tylko podczas importowania elementu WSDL i tworzenia interfejsu API przekazywania protokołu SOAP.</span><span class="sxs-lookup"><span data-stu-id="a1645-122">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="a1645-123">-Context</span><span class="sxs-lookup"><span data-stu-id="a1645-123">-Context</span></span>
<span data-ttu-id="a1645-124">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a1645-124">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a1645-125">-Path</span><span class="sxs-lookup"><span data-stu-id="a1645-125">-Path</span></span>
<span data-ttu-id="a1645-126">Określa ścieżkę internetowego interfejsu API jako ostatnią część publicznego adresu URL interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a1645-126">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="a1645-127">Ten adres URL jest wykorzystywany przez użytkowników korzystających z interfejsu API w celu wysyłania żądań do usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a1645-127">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="a1645-128">Musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="a1645-128">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="a1645-129">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="a1645-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="a1645-130">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="a1645-130">-SpecificationFormat</span></span>
<span data-ttu-id="a1645-131">Określa format specyfikacji.</span><span class="sxs-lookup"><span data-stu-id="a1645-131">Specifies the specification format.</span></span>
<span data-ttu-id="a1645-132">psdx_paramvalues WADL, WSDL i Swagger.</span><span class="sxs-lookup"><span data-stu-id="a1645-132">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

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

### <span data-ttu-id="a1645-133">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="a1645-133">-SpecificationPath</span></span>
<span data-ttu-id="a1645-134">Określa ścieżkę pliku specyfikacji.</span><span class="sxs-lookup"><span data-stu-id="a1645-134">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: From Local File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1645-135">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="a1645-135">-SpecificationUrl</span></span>
<span data-ttu-id="a1645-136">Określa adres URL specyfikacji.</span><span class="sxs-lookup"><span data-stu-id="a1645-136">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: From URL
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1645-137">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="a1645-137">-WsdlEndpointName</span></span>
<span data-ttu-id="a1645-138">Nazwa lokalna punktu końcowego WSDL (port) do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="a1645-138">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="a1645-139">Musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="a1645-139">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="a1645-140">Ten parametr jest opcjonalny i jest wymagany tylko do importowania elementu WSDL.</span><span class="sxs-lookup"><span data-stu-id="a1645-140">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="a1645-141">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="a1645-141">Default value is $null.</span></span>

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

### <span data-ttu-id="a1645-142">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="a1645-142">-WsdlServiceName</span></span>
<span data-ttu-id="a1645-143">Nazwa lokalna usługi WSDL do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="a1645-143">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="a1645-144">Musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="a1645-144">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="a1645-145">Ten parametr jest opcjonalny i jest wymagany tylko do importowania elementu WSDL.</span><span class="sxs-lookup"><span data-stu-id="a1645-145">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="a1645-146">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="a1645-146">Default value is $null.</span></span>

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

### <span data-ttu-id="a1645-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1645-147">-DefaultProfile</span></span>
<span data-ttu-id="a1645-148">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1645-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1645-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1645-149">CommonParameters</span></span>
<span data-ttu-id="a1645-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1645-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1645-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1645-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1645-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1645-152">INPUTS</span></span>

## <span data-ttu-id="a1645-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1645-153">OUTPUTS</span></span>

### <span data-ttu-id="a1645-154">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a1645-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="a1645-155">To polecenie cmdlet zwraca importowany interfejs API jako obiekt **PsApiManagementApi** .</span><span class="sxs-lookup"><span data-stu-id="a1645-155">This cmdlet returns the imported API as a **PsApiManagementApi** object.</span></span>

## <span data-ttu-id="a1645-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1645-156">NOTES</span></span>

## <span data-ttu-id="a1645-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1645-157">RELATED LINKS</span></span>

[<span data-ttu-id="a1645-158">Eksportowanie — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a1645-158">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="a1645-159">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a1645-159">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="a1645-160">Nowe — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a1645-160">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="a1645-161">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a1645-161">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="a1645-162">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a1645-162">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


