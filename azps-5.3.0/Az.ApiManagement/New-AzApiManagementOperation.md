---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
ms.openlocfilehash: 3cba96c2b68a3045448aa6f6f6ccd011964c6e16
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382459"
---
# <span data-ttu-id="836dd-101">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="836dd-101">New-AzApiManagementOperation</span></span>

## <span data-ttu-id="836dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="836dd-102">SYNOPSIS</span></span>
<span data-ttu-id="836dd-103">Tworzy operację zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="836dd-103">Creates an API management operation.</span></span>

## <span data-ttu-id="836dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="836dd-104">SYNTAX</span></span>

```
New-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="836dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="836dd-105">DESCRIPTION</span></span>
<span data-ttu-id="836dd-106">Polecenie cmdlet **New-AzApiManagementOperation** tworzy operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="836dd-106">The **New-AzApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="836dd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="836dd-107">EXAMPLES</span></span>

### <span data-ttu-id="836dd-108">Przykład 1. Tworzenie operacji zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="836dd-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="836dd-109">To polecenie tworzy operację zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="836dd-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="836dd-110">Przykład 2: Tworzenie operacji zarządzania interfejsem API przy użyciu szczegółów żądania i odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="836dd-110">Example 2: Create an API management operation with request and response details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
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
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="836dd-111">W tym przykładzie przedstawiono tworzenie operacji zarządzania interfejsem API przy użyciu szczegółów żądania i odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="836dd-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="836dd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="836dd-112">PARAMETERS</span></span>

### <span data-ttu-id="836dd-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="836dd-113">-ApiId</span></span>
<span data-ttu-id="836dd-114">Określa identyfikator operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="836dd-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="836dd-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="836dd-115">-ApiRevision</span></span>
<span data-ttu-id="836dd-116">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="836dd-116">Identifier of API Revision.</span></span> <span data-ttu-id="836dd-117">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="836dd-117">This parameter is optional.</span></span> <span data-ttu-id="836dd-118">Jeśli nie określono tej funkcji, operacja zostanie dołączona do poprawki obecnie aktywnej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="836dd-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="836dd-119">-Context</span><span class="sxs-lookup"><span data-stu-id="836dd-119">-Context</span></span>
<span data-ttu-id="836dd-120">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="836dd-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="836dd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="836dd-121">-DefaultProfile</span></span>
<span data-ttu-id="836dd-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="836dd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="836dd-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="836dd-123">-Description</span></span>
<span data-ttu-id="836dd-124">Umożliwia określenie opisu nowej operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="836dd-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="836dd-125">-Method</span><span class="sxs-lookup"><span data-stu-id="836dd-125">-Method</span></span>
<span data-ttu-id="836dd-126">Określa metodę HTTP dla nowej operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="836dd-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="836dd-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="836dd-127">-Name</span></span>
<span data-ttu-id="836dd-128">Określa nazwę wyświetlaną nowej operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="836dd-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="836dd-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="836dd-129">-OperationId</span></span>
<span data-ttu-id="836dd-130">Określa identyfikator operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="836dd-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="836dd-131">-Request</span><span class="sxs-lookup"><span data-stu-id="836dd-131">-Request</span></span>
<span data-ttu-id="836dd-132">Określa szczegóły operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="836dd-132">Specifies the details of the API management operation.</span></span>

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

### <span data-ttu-id="836dd-133">-Odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="836dd-133">-Responses</span></span>
<span data-ttu-id="836dd-134">Określa tablicę możliwych odpowiedzi operacji zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="836dd-134">Specifies an array of possible API management operation responses.</span></span>

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

### <span data-ttu-id="836dd-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="836dd-135">-TemplateParameters</span></span>
<span data-ttu-id="836dd-136">Określa tablicę parametrów zdefiniowanych w parametrach *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="836dd-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="836dd-137">Jeśli nie określisz tego parametru, zostanie wygenerowana wartość domyślna na podstawie *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="836dd-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

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

### <span data-ttu-id="836dd-138">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="836dd-138">-UrlTemplate</span></span>
<span data-ttu-id="836dd-139">Określa szablon adresu URL.</span><span class="sxs-lookup"><span data-stu-id="836dd-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="836dd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="836dd-140">CommonParameters</span></span>
<span data-ttu-id="836dd-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="836dd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="836dd-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="836dd-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="836dd-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="836dd-143">INPUTS</span></span>

### <span data-ttu-id="836dd-144">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="836dd-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="836dd-145">System. String</span><span class="sxs-lookup"><span data-stu-id="836dd-145">System.String</span></span>

### <span data-ttu-id="836dd-146">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="836dd-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="836dd-147">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="836dd-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="836dd-148">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="836dd-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="836dd-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="836dd-149">OUTPUTS</span></span>

### <span data-ttu-id="836dd-150">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="836dd-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="836dd-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="836dd-151">NOTES</span></span>

## <span data-ttu-id="836dd-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="836dd-152">RELATED LINKS</span></span>

[<span data-ttu-id="836dd-153">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="836dd-153">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="836dd-154">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="836dd-154">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="836dd-155">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="836dd-155">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


