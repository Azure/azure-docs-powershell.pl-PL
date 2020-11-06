---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
ms.openlocfilehash: 545c1f57d269b8cdb36e006a07c754811e0f2b04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547192"
---
# <span data-ttu-id="f112f-101">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f112f-101">New-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="f112f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f112f-102">SYNOPSIS</span></span>
<span data-ttu-id="f112f-103">Tworzy operację zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f112f-103">Creates an API management operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f112f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f112f-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-OperationId <String>]
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f112f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f112f-105">DESCRIPTION</span></span>
<span data-ttu-id="f112f-106">Polecenie cmdlet **New-AzureRmApiManagementOperation** tworzy operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f112f-106">The **New-AzureRmApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="f112f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f112f-107">EXAMPLES</span></span>

### <span data-ttu-id="f112f-108">Przykład 1. Tworzenie operacji zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="f112f-108">Example 1: Create an API management operation</span></span>
```
PS C:\>New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="f112f-109">To polecenie tworzy operację zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f112f-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="f112f-110">Przykład 2: Tworzenie operacji zarządzania interfejsem API przy użyciu szczegółów żądania i odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="f112f-110">Example 2: Create an API management operation with request and response details</span></span>
```
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
New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="f112f-111">W tym przykładzie przedstawiono tworzenie operacji zarządzania interfejsem API przy użyciu szczegółów żądania i odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="f112f-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="f112f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f112f-112">PARAMETERS</span></span>

### <span data-ttu-id="f112f-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f112f-113">-ApiId</span></span>
<span data-ttu-id="f112f-114">Określa identyfikator operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f112f-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="f112f-115">-Context</span><span class="sxs-lookup"><span data-stu-id="f112f-115">-Context</span></span>
<span data-ttu-id="f112f-116">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f112f-116">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f112f-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="f112f-117">-Description</span></span>
<span data-ttu-id="f112f-118">Umożliwia określenie opisu nowej operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f112f-118">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="f112f-119">-Method</span><span class="sxs-lookup"><span data-stu-id="f112f-119">-Method</span></span>
<span data-ttu-id="f112f-120">Określa metodę HTTP dla nowej operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f112f-120">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="f112f-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f112f-121">-Name</span></span>
<span data-ttu-id="f112f-122">Określa nazwę wyświetlaną nowej operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f112f-122">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="f112f-123">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f112f-123">-OperationId</span></span>
<span data-ttu-id="f112f-124">Określa identyfikator operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f112f-124">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="f112f-125">-Request</span><span class="sxs-lookup"><span data-stu-id="f112f-125">-Request</span></span>
<span data-ttu-id="f112f-126">Określa szczegóły operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f112f-126">Specifies the details of the API management operation.</span></span>

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

### <span data-ttu-id="f112f-127">-Odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="f112f-127">-Responses</span></span>
<span data-ttu-id="f112f-128">Określa tablicę możliwych odpowiedzi operacji zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="f112f-128">Specifies an array of possible API management operation responses.</span></span>

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

### <span data-ttu-id="f112f-129">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="f112f-129">-TemplateParameters</span></span>
<span data-ttu-id="f112f-130">Określa tablicę parametrów zdefiniowanych w parametrach *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="f112f-130">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="f112f-131">Jeśli nie określisz tego parametru, zostanie wygenerowana wartość domyślna na podstawie *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="f112f-131">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

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

### <span data-ttu-id="f112f-132">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="f112f-132">-UrlTemplate</span></span>
<span data-ttu-id="f112f-133">Określa szablon adresu URL.</span><span class="sxs-lookup"><span data-stu-id="f112f-133">Specifies the URL template.</span></span>

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

### <span data-ttu-id="f112f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f112f-134">-DefaultProfile</span></span>
<span data-ttu-id="f112f-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f112f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f112f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f112f-136">CommonParameters</span></span>
<span data-ttu-id="f112f-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f112f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f112f-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f112f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f112f-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f112f-139">INPUTS</span></span>

## <span data-ttu-id="f112f-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f112f-140">OUTPUTS</span></span>

### <span data-ttu-id="f112f-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f112f-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="f112f-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f112f-142">NOTES</span></span>

## <span data-ttu-id="f112f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f112f-143">RELATED LINKS</span></span>

[<span data-ttu-id="f112f-144">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f112f-144">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="f112f-145">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f112f-145">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="f112f-146">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f112f-146">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


