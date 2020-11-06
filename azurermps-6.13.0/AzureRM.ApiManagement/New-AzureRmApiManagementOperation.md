---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
ms.openlocfilehash: d7411b99847b76db5f6e01215b49056842d4e444
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526401"
---
# <span data-ttu-id="18ff5-101">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="18ff5-101">New-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="18ff5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18ff5-102">SYNOPSIS</span></span>
<span data-ttu-id="18ff5-103">Tworzy operację zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="18ff5-103">Creates an API management operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18ff5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18ff5-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18ff5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="18ff5-105">DESCRIPTION</span></span>
<span data-ttu-id="18ff5-106">Polecenie cmdlet **New-AzureRmApiManagementOperation** tworzy operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="18ff5-106">The **New-AzureRmApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="18ff5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18ff5-107">EXAMPLES</span></span>

### <span data-ttu-id="18ff5-108">Przykład 1. Tworzenie operacji zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="18ff5-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="18ff5-109">To polecenie tworzy operację zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="18ff5-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="18ff5-110">Przykład 2: Tworzenie operacji zarządzania interfejsem API przy użyciu szczegółów żądania i odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="18ff5-110">Example 2: Create an API management operation with request and response details</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$RID = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$RID.Name = "RID"
$RID.Description = "Resource identifier"
$RID.Type = "string"
$Query = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Query.Name = "query"
$Query.Description = "Query string"
$Query.Type = 'string'
$Request = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
$Request.Description = "Create/update resource request"
$DummyQp = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$DummyQp.Name = 'dummy'
$DummyQp.Type = 'string'
$DummyQp.Required = $FALSE
$Request.QueryParameters = @($DummyQp)
$Header = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Header.Name = 'x-custom-header'
$Header.Type = 'string'
$Request.Headers = @($Header)
$RequestRepresentation = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRepresentation
$RequestRepresentation.ContentType = 'application/json'
$RequestRepresentation.Sample = '{ "propName": "propValue" }'
$Request.Representations = @($requestRepresentation)
$Response = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse
$Response.StatusCode = 204
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="18ff5-111">W tym przykładzie przedstawiono tworzenie operacji zarządzania interfejsem API przy użyciu szczegółów żądania i odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="18ff5-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="18ff5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18ff5-112">PARAMETERS</span></span>

### <span data-ttu-id="18ff5-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="18ff5-113">-ApiId</span></span>
<span data-ttu-id="18ff5-114">Określa identyfikator operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="18ff5-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="18ff5-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="18ff5-115">-ApiRevision</span></span>
<span data-ttu-id="18ff5-116">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="18ff5-116">Identifier of API Revision.</span></span> <span data-ttu-id="18ff5-117">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="18ff5-117">This parameter is optional.</span></span> <span data-ttu-id="18ff5-118">Jeśli nie określono tej funkcji, operacja zostanie dołączona do poprawki obecnie aktywnej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="18ff5-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="18ff5-119">-Context</span><span class="sxs-lookup"><span data-stu-id="18ff5-119">-Context</span></span>
<span data-ttu-id="18ff5-120">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="18ff5-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="18ff5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18ff5-121">-DefaultProfile</span></span>
<span data-ttu-id="18ff5-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18ff5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18ff5-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="18ff5-123">-Description</span></span>
<span data-ttu-id="18ff5-124">Umożliwia określenie opisu nowej operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="18ff5-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="18ff5-125">-Method</span><span class="sxs-lookup"><span data-stu-id="18ff5-125">-Method</span></span>
<span data-ttu-id="18ff5-126">Określa metodę HTTP dla nowej operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="18ff5-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="18ff5-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="18ff5-127">-Name</span></span>
<span data-ttu-id="18ff5-128">Określa nazwę wyświetlaną nowej operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="18ff5-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="18ff5-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="18ff5-129">-OperationId</span></span>
<span data-ttu-id="18ff5-130">Określa identyfikator operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="18ff5-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="18ff5-131">-Request</span><span class="sxs-lookup"><span data-stu-id="18ff5-131">-Request</span></span>
<span data-ttu-id="18ff5-132">Określa szczegóły operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="18ff5-132">Specifies the details of the API management operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18ff5-133">-Odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="18ff5-133">-Responses</span></span>
<span data-ttu-id="18ff5-134">Określa tablicę możliwych odpowiedzi operacji zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="18ff5-134">Specifies an array of possible API management operation responses.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18ff5-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="18ff5-135">-TemplateParameters</span></span>
<span data-ttu-id="18ff5-136">Określa tablicę parametrów zdefiniowanych w parametrach *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="18ff5-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="18ff5-137">Jeśli nie określisz tego parametru, zostanie wygenerowana wartość domyślna na podstawie *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="18ff5-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18ff5-138">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="18ff5-138">-UrlTemplate</span></span>
<span data-ttu-id="18ff5-139">Określa szablon adresu URL.</span><span class="sxs-lookup"><span data-stu-id="18ff5-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="18ff5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18ff5-140">CommonParameters</span></span>
<span data-ttu-id="18ff5-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18ff5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18ff5-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18ff5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18ff5-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18ff5-143">INPUTS</span></span>

### <span data-ttu-id="18ff5-144">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="18ff5-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="18ff5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="18ff5-145">System.String</span></span>

### <span data-ttu-id="18ff5-146">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="18ff5-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="18ff5-147">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="18ff5-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="18ff5-148">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="18ff5-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="18ff5-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18ff5-149">OUTPUTS</span></span>

### <span data-ttu-id="18ff5-150">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="18ff5-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="18ff5-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18ff5-151">NOTES</span></span>

## <span data-ttu-id="18ff5-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18ff5-152">RELATED LINKS</span></span>

[<span data-ttu-id="18ff5-153">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="18ff5-153">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="18ff5-154">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="18ff5-154">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="18ff5-155">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="18ff5-155">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


