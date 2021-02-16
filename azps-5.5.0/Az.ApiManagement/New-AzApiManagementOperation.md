---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
ms.openlocfilehash: 3cba96c2b68a3045448aa6f6f6ccd011964c6e16
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195379"
---
# <span data-ttu-id="bed87-101">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bed87-101">New-AzApiManagementOperation</span></span>

## <span data-ttu-id="bed87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bed87-102">SYNOPSIS</span></span>
<span data-ttu-id="bed87-103">Tworzy operację zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="bed87-103">Creates an API management operation.</span></span>

## <span data-ttu-id="bed87-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bed87-104">SYNTAX</span></span>

```
New-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bed87-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bed87-105">DESCRIPTION</span></span>
<span data-ttu-id="bed87-106">Polecenie **cmdlet New-AzApiManagementOperation** umożliwia utworzenie operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="bed87-106">The **New-AzApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="bed87-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bed87-107">EXAMPLES</span></span>

### <span data-ttu-id="bed87-108">Przykład 1. Tworzenie operacji zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="bed87-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="bed87-109">To polecenie tworzy operację zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="bed87-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="bed87-110">Przykład 2. Tworzenie operacji zarządzania interfejsem API ze szczegółami żądania i odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="bed87-110">Example 2: Create an API management operation with request and response details</span></span>
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

<span data-ttu-id="bed87-111">W tym przykładzie jest zapytanie o operację zarządzania interfejsem API ze szczegółami żądania i odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="bed87-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="bed87-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bed87-112">PARAMETERS</span></span>

### <span data-ttu-id="bed87-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bed87-113">-ApiId</span></span>
<span data-ttu-id="bed87-114">Określa identyfikator operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="bed87-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="bed87-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="bed87-115">-ApiRevision</span></span>
<span data-ttu-id="bed87-116">Identyfikator poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="bed87-116">Identifier of API Revision.</span></span> <span data-ttu-id="bed87-117">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="bed87-117">This parameter is optional.</span></span> <span data-ttu-id="bed87-118">Jeśli nie zostanie określona, operacja zostanie dołączona do aktualnie aktywnej poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="bed87-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="bed87-119">— kontekst</span><span class="sxs-lookup"><span data-stu-id="bed87-119">-Context</span></span>
<span data-ttu-id="bed87-120">Określa wystąpienie obiektu **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="bed87-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bed87-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bed87-121">-DefaultProfile</span></span>
<span data-ttu-id="bed87-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bed87-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bed87-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="bed87-123">-Description</span></span>
<span data-ttu-id="bed87-124">Określa opis nowej operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="bed87-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="bed87-125">— Metoda</span><span class="sxs-lookup"><span data-stu-id="bed87-125">-Method</span></span>
<span data-ttu-id="bed87-126">Określa metodę HTTP nowej operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="bed87-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="bed87-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bed87-127">-Name</span></span>
<span data-ttu-id="bed87-128">Określa nazwę wyświetlaną nowej operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="bed87-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="bed87-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="bed87-129">-OperationId</span></span>
<span data-ttu-id="bed87-130">Określa identyfikator operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="bed87-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="bed87-131">— Zażądaj</span><span class="sxs-lookup"><span data-stu-id="bed87-131">-Request</span></span>
<span data-ttu-id="bed87-132">Określa szczegóły operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="bed87-132">Specifies the details of the API management operation.</span></span>

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

### <span data-ttu-id="bed87-133">— Odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="bed87-133">-Responses</span></span>
<span data-ttu-id="bed87-134">Określa tablicę możliwych odpowiedzi na operację zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="bed87-134">Specifies an array of possible API management operation responses.</span></span>

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

### <span data-ttu-id="bed87-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="bed87-135">-TemplateParameters</span></span>
<span data-ttu-id="bed87-136">Określa tablicę parametrów zdefiniowaną w parametrze *UrlTemplate.*</span><span class="sxs-lookup"><span data-stu-id="bed87-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="bed87-137">Jeśli nie określisz tego parametru, na podstawie parametru *UrlTemplate* zostanie wygenerowana wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="bed87-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

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

### <span data-ttu-id="bed87-138">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="bed87-138">-UrlTemplate</span></span>
<span data-ttu-id="bed87-139">Określa szablon adresu URL.</span><span class="sxs-lookup"><span data-stu-id="bed87-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="bed87-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bed87-140">CommonParameters</span></span>
<span data-ttu-id="bed87-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bed87-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bed87-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bed87-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bed87-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bed87-143">INPUTS</span></span>

### <span data-ttu-id="bed87-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bed87-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bed87-145">System.String</span><span class="sxs-lookup"><span data-stu-id="bed87-145">System.String</span></span>

### <span data-ttu-id="bed87-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span><span class="sxs-lookup"><span data-stu-id="bed87-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="bed87-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="bed87-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="bed87-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span><span class="sxs-lookup"><span data-stu-id="bed87-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="bed87-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bed87-149">OUTPUTS</span></span>

### <span data-ttu-id="bed87-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bed87-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="bed87-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bed87-151">NOTES</span></span>

## <span data-ttu-id="bed87-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bed87-152">RELATED LINKS</span></span>

[<span data-ttu-id="bed87-153">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bed87-153">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="bed87-154">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bed87-154">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="bed87-155">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bed87-155">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


