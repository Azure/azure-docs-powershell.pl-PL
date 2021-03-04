---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
ms.openlocfilehash: 44eb7ef52782f6a00a81385f7b1a87b0292bec33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959857"
---
# <span data-ttu-id="d6ab2-101">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d6ab2-101">New-AzApiManagementOperation</span></span>

## <span data-ttu-id="d6ab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ab2-103">Tworzy operację zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-103">Creates an API management operation.</span></span>

## <span data-ttu-id="d6ab2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6ab2-104">SYNTAX</span></span>

```
New-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6ab2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6ab2-105">DESCRIPTION</span></span>
<span data-ttu-id="d6ab2-106">Polecenie **cmdlet New-AzApiManagementOperation** umożliwia utworzenie operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-106">The **New-AzApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="d6ab2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6ab2-107">EXAMPLES</span></span>

### <span data-ttu-id="d6ab2-108">Przykład 1. Tworzenie operacji zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="d6ab2-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="d6ab2-109">To polecenie tworzy operację zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="d6ab2-110">Przykład 2. Tworzenie operacji zarządzania interfejsem API ze szczegółami żądania i odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="d6ab2-110">Example 2: Create an API management operation with request and response details</span></span>
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

<span data-ttu-id="d6ab2-111">W tym przykładzie jest zapytanie o operację zarządzania interfejsem API ze szczegółami żądania i odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="d6ab2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6ab2-112">PARAMETERS</span></span>

### <span data-ttu-id="d6ab2-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d6ab2-113">-ApiId</span></span>
<span data-ttu-id="d6ab2-114">Określa identyfikator operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="d6ab2-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d6ab2-115">-ApiRevision</span></span>
<span data-ttu-id="d6ab2-116">Identyfikator poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-116">Identifier of API Revision.</span></span> <span data-ttu-id="d6ab2-117">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-117">This parameter is optional.</span></span> <span data-ttu-id="d6ab2-118">Jeśli nie zostanie określona, operacja zostanie dołączona do aktualnie aktywnej poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="d6ab2-119">— kontekst</span><span class="sxs-lookup"><span data-stu-id="d6ab2-119">-Context</span></span>
<span data-ttu-id="d6ab2-120">Określa wystąpienie obiektu **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="d6ab2-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d6ab2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ab2-121">-DefaultProfile</span></span>
<span data-ttu-id="d6ab2-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6ab2-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="d6ab2-123">-Description</span></span>
<span data-ttu-id="d6ab2-124">Określa opis nowej operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="d6ab2-125">— Metoda</span><span class="sxs-lookup"><span data-stu-id="d6ab2-125">-Method</span></span>
<span data-ttu-id="d6ab2-126">Określa metodę HTTP nowej operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="d6ab2-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d6ab2-127">-Name</span></span>
<span data-ttu-id="d6ab2-128">Określa nazwę wyświetlaną nowej operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="d6ab2-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d6ab2-129">-OperationId</span></span>
<span data-ttu-id="d6ab2-130">Określa identyfikator operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="d6ab2-131">— Zażądaj</span><span class="sxs-lookup"><span data-stu-id="d6ab2-131">-Request</span></span>
<span data-ttu-id="d6ab2-132">Określa szczegóły operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-132">Specifies the details of the API management operation.</span></span>

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

### <span data-ttu-id="d6ab2-133">— Odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="d6ab2-133">-Responses</span></span>
<span data-ttu-id="d6ab2-134">Określa tablicę możliwych odpowiedzi na operację zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-134">Specifies an array of possible API management operation responses.</span></span>

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

### <span data-ttu-id="d6ab2-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="d6ab2-135">-TemplateParameters</span></span>
<span data-ttu-id="d6ab2-136">Określa tablicę parametrów zdefiniowaną w parametrze *UrlTemplate.*</span><span class="sxs-lookup"><span data-stu-id="d6ab2-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="d6ab2-137">Jeśli nie określisz tego parametru, na podstawie parametru *UrlTemplate* zostanie wygenerowana wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

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

### <span data-ttu-id="d6ab2-138">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="d6ab2-138">-UrlTemplate</span></span>
<span data-ttu-id="d6ab2-139">Określa szablon adresu URL.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="d6ab2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ab2-140">CommonParameters</span></span>
<span data-ttu-id="d6ab2-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6ab2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ab2-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6ab2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ab2-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6ab2-143">INPUTS</span></span>

### <span data-ttu-id="d6ab2-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d6ab2-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d6ab2-145">System.String</span><span class="sxs-lookup"><span data-stu-id="d6ab2-145">System.String</span></span>

### <span data-ttu-id="d6ab2-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span><span class="sxs-lookup"><span data-stu-id="d6ab2-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="d6ab2-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="d6ab2-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="d6ab2-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span><span class="sxs-lookup"><span data-stu-id="d6ab2-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="d6ab2-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6ab2-149">OUTPUTS</span></span>

### <span data-ttu-id="d6ab2-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d6ab2-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="d6ab2-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6ab2-151">NOTES</span></span>

## <span data-ttu-id="d6ab2-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6ab2-152">RELATED LINKS</span></span>

[<span data-ttu-id="d6ab2-153">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d6ab2-153">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="d6ab2-154">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d6ab2-154">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="d6ab2-155">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d6ab2-155">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


