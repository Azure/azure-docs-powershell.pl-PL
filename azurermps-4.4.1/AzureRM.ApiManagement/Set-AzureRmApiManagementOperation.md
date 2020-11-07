---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: 28bbc9158639faf066fa9a623f5dfacd6566d236
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718746"
---
# <span data-ttu-id="8f4ac-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8f4ac-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="8f4ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8f4ac-102">SYNOPSIS</span></span>
<span data-ttu-id="8f4ac-103">Ustawia szczegóły operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f4ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8f4ac-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f4ac-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8f4ac-105">DESCRIPTION</span></span>
<span data-ttu-id="8f4ac-106">Polecenie cmdlet **Set-AzureRmApiManagementOperation** ustawia szczegóły operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="8f4ac-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8f4ac-107">EXAMPLES</span></span>

### <span data-ttu-id="8f4ac-108">Przykład 1. Ustawianie szczegółów operacji</span><span class="sxs-lookup"><span data-stu-id="8f4ac-108">Example 1: Set the operation details</span></span>
```
PS C:\>New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="8f4ac-109">To polecenie ustawia szczegóły operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="8f4ac-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8f4ac-110">PARAMETERS</span></span>

### <span data-ttu-id="8f4ac-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8f4ac-111">-ApiId</span></span>
<span data-ttu-id="8f4ac-112">Określa identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="8f4ac-113">-Context</span><span class="sxs-lookup"><span data-stu-id="8f4ac-113">-Context</span></span>
<span data-ttu-id="8f4ac-114">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="8f4ac-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="8f4ac-115">-Description</span></span>
<span data-ttu-id="8f4ac-116">Określa opis nowej operacji.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-116">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="8f4ac-117">-Method</span><span class="sxs-lookup"><span data-stu-id="8f4ac-117">-Method</span></span>
<span data-ttu-id="8f4ac-118">Określa metodę HTTP nowej operacji.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-118">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="8f4ac-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8f4ac-119">-Name</span></span>
<span data-ttu-id="8f4ac-120">Określa nazwę wyświetlaną nowej operacji.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-120">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="8f4ac-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="8f4ac-121">-OperationId</span></span>
<span data-ttu-id="8f4ac-122">Określa identyfikator istniejącej operacji.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-122">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="8f4ac-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f4ac-123">-PassThru</span></span>
<span data-ttu-id="8f4ac-124">passthru</span><span class="sxs-lookup"><span data-stu-id="8f4ac-124">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f4ac-125">-Request</span><span class="sxs-lookup"><span data-stu-id="8f4ac-125">-Request</span></span>
<span data-ttu-id="8f4ac-126">Określa szczegóły żądania operacji.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-126">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="8f4ac-127">-Odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="8f4ac-127">-Responses</span></span>
<span data-ttu-id="8f4ac-128">Określa tablicę możliwych odpowiedzi na operacje.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-128">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="8f4ac-129">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="8f4ac-129">-TemplateParameters</span></span>
<span data-ttu-id="8f4ac-130">Określa tablicę lub parametry zdefiniowane w parametrach *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-130">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="8f4ac-131">Jeśli wartość nie zostanie określona, zostanie wygenerowana wartość domyślna na podstawie UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-131">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="8f4ac-132">Za pomocą tego parametru można uzyskać więcej informacji na temat parametrów, takich jak opis, typ i inne możliwe wartości.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-132">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="8f4ac-133">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="8f4ac-133">-UrlTemplate</span></span>
<span data-ttu-id="8f4ac-134">Określa szablon adresu URL.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-134">Specifies the URL template.</span></span>
<span data-ttu-id="8f4ac-135">Na przykład: Customers/{CID}/Orders/{OID}/? Date = {Date}.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-135">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="8f4ac-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f4ac-136">-DefaultProfile</span></span>
<span data-ttu-id="8f4ac-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f4ac-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f4ac-138">CommonParameters</span></span>
<span data-ttu-id="8f4ac-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f4ac-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f4ac-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f4ac-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f4ac-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f4ac-141">INPUTS</span></span>

## <span data-ttu-id="8f4ac-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8f4ac-142">OUTPUTS</span></span>

### <span data-ttu-id="8f4ac-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8f4ac-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="8f4ac-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8f4ac-144">NOTES</span></span>

## <span data-ttu-id="8f4ac-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f4ac-145">RELATED LINKS</span></span>

[<span data-ttu-id="8f4ac-146">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8f4ac-146">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="8f4ac-147">Nowe — AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8f4ac-147">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="8f4ac-148">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8f4ac-148">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


